
## Multi-label Classification model for a Hotel booking app
+ This model helped the client in identifying whether the review was positive or negative and also for
which category the review was given.

## Table of contents
* [General info](#general-info)
* [Technologies](#technologies)
* [Code Examples](#codeexamples)
* [Contact](#contact)

## General info
This project is a flight ticket booking system in which users can book or cancel tickets. They can view fligt and airline details and choose from the collection and also they are able to update their account information. The admin will be able to add, delete and update various components of the services. A combination of Text mining and supervised classification algorithm was used in a pipeline method.

## Description: Multi-label Classification model for a Hotel booking app.
### Goal:
To classify the reviews as Positive or Negative and further identifying them as reviews on 4
important categories (Room, Staff and Service, Amenities, Food).

### Synopsis:
+ This model helped the client in identifying whether the review was positive or negative and also for
which category the review was given. For example if it was a positive review, the model would
identify whether it is on food, staff and service, amenities or room.
+ A combination of Text mining and supervised classification algorithm was used in a pipeline
method.
+ NuSVC was the highest performing algorithm after “K-fold” cross validation for binary classification.
+ Conv 1D was the highest performing algorithm for multi label classification.
+ “F1 micro” score, along with “Hamming loss” was considered as the evaluation metrics.


## Technologies
Tools/Technique: Python, Feature Engineering, Text mining, t-SNE,LSTM, Conv 1D


## Code Examples

To update flight
public AddNewFlight updateFlight(AddNewFlight addNewFlight) {
		FlightEntity flight1 = new FlightEntity();
		flight1 = flightDAO.findByFlightName(addNewFlight.getFlightName());
		flight1.setFlightName(addNewFlight.getFlightName());
		flightDAO.save(flight1);
		return addNewFlight;
	} 
	The service implementation for delete flight
	public String delete(String flightName) {
		String message = null;
		FlightEntity flight1 = new FlightEntity();
		flight1 = flightDAO.findByFlightName(flightName);
		if ( flight1.getFlightName().equals(flightName)){
			message = flight1.getFlightName() + " has been deleted successfully";
			flightDAO.delete(flight1);
		}
		return message;
	}
  

## Contact
created by [@justinseby] - feel free to contact me
