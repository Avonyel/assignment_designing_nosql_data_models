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




* reservation times: Object
		* 8:00: [table3, table6, table19]

tables [
	{ id: table1
		5:00: {
			available: false,
			reservation_under: "Name of Person",
			reservation_phone: 555-555-5555
			number_of_guest: 6
		}
		6:00: {

		}
		7:00: {}
		8:00: {}
		9:00: {}
	},
	{ id: table2
		5:00: {
			available: false,
			reservation_under: "Name of Person",
			reservation_phone: 555-555-5555
			number_of_guest: 6
		}
		6:00: {

		}
		7:00: {}
		8:00: {}
		9:00: {}
	}]
