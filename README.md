# Homework-Project3
Trying to use some vectors in my homework in C++
#include <iostream>
#include <iomanip>
#include <string>
#include <vector>

using namespace std;

class Person
{ 
private:
	std::vector<string> m_VectorOfNames;
public:
	Person()
	{}
	~Person()
	{}
	void AddName(string name)
	{
		m_VectorOfNames.push_back(name);
	}
	std::vector<string>GetCopyOfVector()
	{
		return m_VectorOfNames;
	}
	
};

class Address
{
private:
	std::vector<string> m_VectorOfAddress;
public:
	Address()
	{}
	~Address()
	{}
	void AddAddress(string address)
	{
		m_VectorOfAddress.push_back(address);
	}
	std::vector<string>GetCopyOfVector()
	{
		return m_VectorOfAddress;
	}

};

int main()
{
	//create class for names
	Person person;
	person.AddName("Bilbo Baggins");
	person.AddName("Wizard Gandalf");
	person.AddName("Elf Elrond");
	//create class for address
	Address add;
	add.AddAddress("The Shire");
	add.AddAddress("Falling Down Moria");
	add.AddAddress("Elfing Stuff Up");
	//create an empty vector of Account objects.
	vector<double> Account(3);
	//Create 3 person objects.
	string p1="Bilbo Baggins";
	string p2="Wizard Gandalf";
	string p3="Elf Elrond";
	//Create 3 account objects.
	double acct1=500.00;
	double acct2 = 1000.00;
	double acct3=1200.00;
	double gain = 25.00;
	double loss = 100.00;
	//Put the Account objects into the vector.
	Account[0] = acct1;
	Account[1] = acct2;
	Account[2] = acct3;
	//Use a for loop and add $25.00 to each account
	for (unsigned int i = 0;i<Account.size(); i++)
	{
		Account[i] = Account[i] + gain;
	}
	 //Use another for loop to remove $100.00 from each account
	for (unsigned int i = 0; i < Account.size(); i++)
	{
		Account[i] = Account[i]-loss;
	}
	//create a vector of vectors

	system("PAUSE");
	return 0;
}
