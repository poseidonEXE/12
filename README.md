#include <iostream> 

  

using namespace std; 

  

void minimumCost(int, int); 

  

int main() { 

int numberOfPeople, numberOfTrips; 

  

setlocale(LC_ALL, "ukr"); 

  

cout << "Введіть скільки людей хоче купити квитки: "; 

cin >> numberOfPeople; 

cout << "Введіть кількість поїздок: "; 

cin >> numberOfTrips; 

minimumCost(numberOfPeople, numberOfTrips); 

  

system("pause"); 

  

return 0; 

} 

  

void minimumCost(int people, int trips) { 

int ticketOneTravel = 50, unlimitedTicket = 90, ticketForPeople = 5, ticketForPeopleCost = 400; 

int sum = people * trips; 

  

cout << "Вартість квитків по одній поїздці: " << sum * ticketOneTravel << endl; 

cout << "Вартість квитків на кожну людину по 1 безлімітному квитку: " << sum * unlimitedTicket << endl; 

cout << "Вартість квитків на кожну группу людей за 5 чоловік: " << sum / 5 * ticketForPeopleCost << endl; 

  

if (sum * ticketOneTravel < sum * unlimitedTicket && sum * ticketOneTravel < sum / 5 * ticketForPeopleCost) 

{ 

cout << "Вартість квитків по одній поїздці вартістю " << sum * ticketOneTravel << " найменша\n"; 

} 

else if (sum * unlimitedTicket < sum * ticketOneTravel && sum * unlimitedTicket < sum / 5 * ticketForPeopleCost) { 

cout << "Вартість квитків на кожну людину по 1 безлімітному квитку вартістю " << sum * unlimitedTicket << " найменша\n"; 

} 

else if (sum / 5 * ticketForPeopleCost < sum * ticketOneTravel && sum / 5 * ticketForPeopleCost < sum * unlimitedTicket) { 

cout << "Вартість квитків на кожну группу людей за 5 чоловік вартістю " << sum / 5 * ticketForPeopleCost << " найменша\n"; 

} 

} 
