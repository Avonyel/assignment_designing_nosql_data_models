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

users: {
	id555: {
		username: "Billy",
		password: "IHeartDogs"
		email: "billy@billynet.org"
		semesters: [{ semester_id: "FALL2016"
								  courses: [{course_id: "MATH101",
									 tests: {
									 	"unit_test_1": 76,
										"unit_test_2": 94
									},
									{course_id: "LIT203",
									 tests: {
									 	"unit_test_1": 76,
										"unit_test_2": 94
									 },
								{ semester_id: "SPRING2016"
								  courses: [
								  {course_id: "MATH101",
									 tests: {
									 	"unit_test_1": 76,
										"unit_test_2": 94
									},
									{course_id: "LIT203",
									 tests: {
									 	"unit_test_1": 76,
										"unit_test_2": 94
									 }
							    ]
		]
		}
	}

* Exam Object
  * Name of the test
  * Class_Name: String
  * Semester: String
  * Array of test_object
    * test_object
      * student_id: String
      * score: Number

exams: [
	{ name: "unit_test_1"
		class: "MATH101",
		semester_id: "FALL2016",
		scores: {
			id555: 76,
			id789: 99
		}
	},
	{ name: "unit_test_2"
		class: "MATH101",
		semester_id: "FALL2016",
		scores: {
			id555: 97,
			id789: 40
		}
	}
]



-------------------------------------------------------------
                       Advanced 1
-------------------------------------------------------------

// products
products:{
  000090: {
    name: legos
    department: "Toys"
		price: 700
		num_in_stock: 47000
    units_sold_to_date: 2
		earnings_to_date: 1400
    receipts: ["id_1", "id_2"]
	},
  0009383: {
    name: gameboys
		price: 700
		num_in_stock: 47000
    units_sold_to_date: 2
		earnings_to_date: 1400
    receipts: ["id_1", "id_2"]
	}
}

receipts {
  id_1: {
    date_of_purchase: "1998-12-01 :: 00:00:23"
    total_price: 9999,
    customer_id: "45878"
    products: [
      { product_id: "000098", quantity: 5, price: 500 },
      { product_id: "000098", quantity: 5, price: 500 },
      { product_id: "000908", quantity: 2, price: 500 }
  ]
  },
  id_2: {
    total_price: 9999,
    customer_id: "45878"
    products: [
      { product_id: "000098", quantity: 5, price: 500 },
      { product_id: "000098", quantity: 5, price: 500 },
      { product_id: "000908", quantity: 2, price: 500 }
  ]
}

revenue_intervals_product {
  Quarters: [
    {
      name: "Quarter1 2016",
      revenue_by_product: [
        {
            product_id: 000989
            product_revenue: 9
        },
        {
            product_id: 000989
            product_revenue: 9
        }
      ]
    },
    {
      name: "Quarter1 2016",
      revenue_by_product: [
        {
            product_id: 000989
            product_revenue: 9
        },
        {
            product_id: 000989
            product_revenue: 9
        }
      ]
    }
  ]  
}

-------------------------------------------------------------
                       Advanced 2
-------------------------------------------------------------
