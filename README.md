Alex and Stephanie

# assignment_designing_nosql_data_models
I'll have one data model hold the SQL please

## Users

* username: String
    * Must contain only word characters
* password: String
    * Must be at least 8 characters
* email: String
    * Must contain an @ symbol




* username: String |Must contain only word characters|
* password: String |Must be at least 8 characters|
* email: String |Must contain an @ symbol|
* profile: object (document, whatever)
		* birthday: Object
				* value: datetime obj?
				* displayed: boolean
		* gender Object
				* value: String
				* displayed: boolean
		* phone number Object
				* value: Number |must be 10 digits|
				* displayed: boolean
		* location Object
				* city: String
				* state: String |2 characters, can also be null|
				* country: String
				* displayed: Boolean



-------------------------------------------------------------
                       Intermediate 1
-------------------------------------------------------------

* user_object
  * username: String |Must contain only word characters|
  * password: String |Must be at least 8 characters|
  * email: String |Must contain an @ symbol|
  * reservations: Array of reservation objects
    * table: String
    * number_of_guests: Number
    * reservation_time: Number

* reservation times: Object
		* 8:00: [table3, table6, table19]

* tables: object |must contain table object|
  * table_object
    * time_interval_object
      * available: boolean,
      * reservation_under: String,
      * reservation_phone: Number
      * number_of_guest: Number

tables {
	table1: {
		  5:00: {
  			available: boolean,
  			reservation_under: String (ex: "Name of Person"),
  			reservation_phone: Number (555-555-5555)
  			number_of_guest: 6
      }
		6:00: {}
		7:00: {}
		8:00: {}
		9:00: {}
	},

	table2: {
		5:00: {
      available: boolean,
      reservation_under: String (ex: "Name of Person"),
      reservation_phone: Number (555-555-5555)
      number_of_guest: 6
		}
		6:00: {}
		7:00: {}
		8:00: {}
		9:00: {}
	}
}


-------------------------------------------------------------
                       Intermediate 2
-------------------------------------------------------------


* user_object
  * username: String |Must contain only word characters|
  * student_id: String
  * password: String |Must be at least 8 characters|
  * email: String |Must contain an @ symbol|
  * semester: semester_objects
    * semester: class_objects
      * class_object: exam_strings
        * exam: Number

* Exam Object
  * Name of the test
  * Class_Name: String
  * Semester: String
  * Array of test_object
    * test_object
      * student_id: String
      * score: Number
