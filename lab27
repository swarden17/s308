using System;
using System.Collections.Generic;

public class Airport
{
	// Fields+Properties
	string Name;
	string City;
	List<Airplane> Airplane_List = new List<Airplane>();
	
	//Method to add plane to list
	public void Add(Airplane plane)
	{
		Airplane_List.Add(plane);
	}
	
	
	//Constructor
	public Airport(string nombre, string c)
	{
		Name = nombre;
		City = c;
	}
}


public abstract class Airplane
{
	//Fields+Properties
	public string name;
	public string model;
	
	// Method Fly
	public void fly()
	{
		Console.WriteLine("Airplane is flying");
	}
	
	//Abstract load method
	public abstract void load();
}


public class PassengerPlane : Airplane
{
	//Fields+Properties
	
	//Override load method
	public override void load()
	{	
		Console.WriteLine("My passenger plane is loading");
	}
	
	//Constructor
	public PassengerPlane(string nombre, string modelo)
	{
		//Only works for public
		base.name = nombre;
		base.model = modelo;
	}
}

public class CargoPlane : Airplane
{
	//Override load method
	
	public override void load()
	{
		Console.WriteLine("Cargo plane is loading");
	}
}
	

public class Program 
{
	public static void Main()
	{
		PassengerPlane pass = new PassengerPlane("Boeing", "737");
		
		CargoPlane cargo = new CargoPlane();
		
		Airport airport1 = new Airport("O'Hare", "Chicago");
		
		airport1.Add(pass);
		airport1.Add(cargo);
		
	}
}
