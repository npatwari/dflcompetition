[**Home**](index.html) | [**Call for Contesters**](call.html) | [**About**](about.html) | [**Logistics**](logistics.html) | [**Committee**](committee.html) 

## Evaluation Criteria

For both categories of teams, the evaluation period will proceed as follows.  At the start of the evaluation period, the deployment area will be empty of people.  At a time unknown to the teams, a single person will enter into the deployment area.  The person will walk through the deployment area while recording his or her ground truth coordinates.  At a later time, the person will exit the deployment area.  

The software the team runs must estimate, for each time:
1. If no person is in the area, or if there is a person in the area; and 
2. If there is a person present, their coordinate. 
This estimated coordinate (or claim that there is no person in the area) is posted to our server, for each time.  The period between estimates is to be determined.

The ground truth localization file will be processed and used to compute the penalized root-mean-squared error (PRMSE) of each team's posted coordinate estimates.  The team with the lowest RMSE in each category will be the winners.  The _penalty_ is a fixed error (in meters) assessed when the team makes a _presence error_, that is, they estimate that no person is present when someone in fact is, or when they estimate that a person is present when in fact no person is.  When a person is not present and the team estimates that there is no person present, the error is zero.  When a person is present, and the team estimates their coordinate, the error is the Euclidean distance between the estimate and true location.  The errors are then squared, the average is taken over all estimates, and then the square root of this is taken. This is the PRMSE.

The team with the lowest PRMSE in each category will be the winner.

Note that past IPSN localization competitions had to have one test for each team separately, in which the person carried their device only through the deployment area.  However, in DFL, since the person is not carrying any wireless device, we do not need to run the test multiple times.

