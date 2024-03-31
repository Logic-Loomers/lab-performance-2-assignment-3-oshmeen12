Assume you oversee a small library and would like to develop a program that looks up books using their ISBNs. A list of books with their corresponding ISBN digits is in front of you. After the librarian inputs an ISBN, your software will look through the list to locate the relevant book.  The book's title and other details will be shown if the book is located. A notice stating that the book is not available in the library will appear if it cannot be located.
#include <iostream>
using namespace std;
class library
{
public:
    string auth,title;
    double ISBN, searchisbn;
    void get(){
    	 cout << "enter ISBN : ";
    cin >> ISBN;
    cout << "enter author : ";
    cin >> auth;
    cout << "enter title : ";
    cin >> title;
    }
    void display(){
    	cout  << ISBN << endl;
    cout  << title << endl;
    cout << auth<< endl;
    }
    bool search(double)
{
    return x == ISBN;
}
};

int main()
{
    int number, size;
    cout<<"oshmeen 2310997193 "<<endl;
    cout << "enter the number of books you want the details: ";
    cin >> size;
    library obj1[size];
    for (int i = 0; i < size; i++)
    {
        obj1[i].getdata();
    }

    cout << "Enter  ISBN of the  book : ";
    cin >> number;
    bool found = false;
    for (int i = 0; i < size; i++)
    {
        if (obj1[i].search(number))
        {
            cout << "Book found";
            obj1[i].displaydata();
            found = true;
            break;
        }
    }
        if(!found)
        cout<<"Book not found";
        
        return 0;
}
