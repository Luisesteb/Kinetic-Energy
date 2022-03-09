// Assignment 3 Kinetic Energy.cpp
// Skill Practice Assignment 3 - Kinetic Energy
// Luis Mondolo
// Date 2-26-22
// "Program that returns the amount of kinetic energy an object has from mass and velocity data"
// Kinetic Energy KE = 1/2 (m*v*v) = (m*v*v)/2

#include <iostream>
#include <cmath>

using namespace std;

// function prototypes
double getMass(); // getMass takes nothing, returns the Mass of the object
double getVeloc();  // getVeloc takes nothing, returns the Velocity of the object
double getKinEn(double, double);  // getKinEn returns KinEn, takes mass and velocity square
void displayData(double, double, double); // returns nothing, takes mass, velocity square, and kinetic energy and prints things out


int main()
{
	// variables
	double mass;  // to hold the objetc's mass in m/s
	double veloc;  // to hold the objetc's velocity in Kg
	double kinen;   // to hold the object's kinetic energy in Joules

	//get the object's mass
	mass = getMass();

	// get the object's velocity
	veloc = getVeloc();

	// calculate the kinetic energy
	kinen = getKinEn(mass, veloc);

	// display the object's data
	displayData(mass, veloc, kinen);

	return 0;
}

// getMass function: takes nothing, returns the mass
double getMass()
{
	double mass;

	// get the mass
	cout << "Enter the mass in Kg: ";
	cin >> mass;
	// return the mass
	return mass;
}
// getVeloc: takes nothing, returns the velocity
double getVeloc()
{
	double veloc;

	// get the velocity
	cout << "Enter the velocity in m/s: ";
	cin >> veloc;
	// return the velocity
	return veloc;
}

// getKinEn: takes mass and velocity, returns kinetic energy
double getKinEn(double ma, double vel)
{
	return (ma * pow(vel, 2)) / 2;
}

// displayData takes mass, velocity, and kinetic energy, returns nothing
void displayData(double ma, double vel, double kinen)
{
	cout << "\nKinetic Energy Data\n";
	cout << "-------------------\n";
	cout << "Mass: " << ma << " Kg" << endl;
	cout << "Velocity: " << vel << " m/s" << endl;
	cout << "Kinetic Energy: " << kinen << " Joules" << endl;
}
