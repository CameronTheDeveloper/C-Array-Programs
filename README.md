# C-Array-Programs
    //This C++ program uses a string Array to collect a list of 10 names that the user inputs. Once the user has entered 10 names into the list (Array), an        	additional function allows the user to input a name and check how many times that name is in the 10 name list.

    //Created by Cameron Posey

    int main()
    {
    const int AR_SIZE = 10;                             //CALC -- Size of Array

    string namesAr[AR_SIZE];                            //INPUT -- Array for names of 10 people

    string nameGuess;                                   //INPUT -- User enters a name to check how many instances it appears

    int index;                                          //CALC -- Counts the amount of occurances of a name

    int instances;                                      //CALC -- Counts number of instances a name has appeared


     //Prompts the user to input 10 names. Stores in the Array
     for (index=0; index<AR_SIZE; index++)
     {
    	 cout << "Enter name " << index+1 << ": ";
         getline(cin,namesAr[index]);
     }


     //Searches for how many times the name has appeared
     cout << "Whose name do you want to search for? ";
     cin >> nameGuess;

     //Compares the name the user wants to check to the list of names and displays the amount of times it is in list
     while (nameGuess != "done" || nameGuess != "Done")
     {
         instances = 0;
         for (index = 0; index < AR_SIZE; index++)
	 {
    	     if (nameGuess == namesAr[index])
	     {
		instances++;
	     }
         }
         cout << "There are " << instances << " instances of the name " << nameGuess << "!" << endl;
         cout << "Search for another name or type done to exit: ";
         cin >> nameGuess;
         //Ends the Program if the user types "Done"
         if (nameGuess == "Done" || nameGuess == "done")
         {
      	     cout << "Thanks for using this program!" << endl;
    	     return 0;
         }
     }
    }



