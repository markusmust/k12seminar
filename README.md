# k12seminar

Alamklasse kasutatakse oleamsolevate atribuutide ja meetodite taaskasutamiseks.

Alamklass, ehk klass mis kasutab mõne teise klassi atribuute/meetode - subclass e. child

Klass millelt atribuute ja meetode laenatakse - superclass e. parent

// Näite superclass e. parent


	class Vehicle {
		protected String brand = "Ford";
		public void honk(){
			System.out.println("Tuut, tuut!");
		}	
	}


// Näite subclass e. child

	class Car extends Vehicle {
		private String modelName = "Mustang";
		public static void main(String[] args){

		Car myCar = new Car();

		// kasutame parent classi meetodit child klassi objektiga
		myCar.honk();
		// output: "Tuut, tuut"

		//Kuna class car kasutab klassi vehicle, ei ole vaja myCar.brandi siin klassis määrata
		System.out.println(myCar.brand + " " + myCar.modelName);

		// output: "Ford Mustang"
		}
	}


Abstract klassid 

Abstact classi peab extendima.

Ei saa luua sellest objekte.

Aitab keskenduda sellele, mida objekt teeb, mitte kuidas seda tehakse.

