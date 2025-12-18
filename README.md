#include <iostream.h>
#include <fstream.h>     
#include <conio.h>

void main() {
    clrscr();

    ofstream fout;       
    ifstream fin;        
    char text[100];

   
    fout.open("sample.txt");   

    cout << "Enter text to write into file: ";
    cin.getline(text, 100);

    fout << text;              
    fout.close();              

    cout << "\nData written to file successfully.\n";

  
    fin.open("sample.txt");   

    cout << "\nReading from file:\n";

    while (fin.getline(text, 100)) {
        cout << text << endl;
    }

    fin.close();

    getch();
}
