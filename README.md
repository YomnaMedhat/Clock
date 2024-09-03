# Clock
Clock with hours, minutes, and seconds

#include <iostream>
#include <windows.h>
#include <iomanip>
using namespace std;

int main() {
    int hour, min, sec;

    cout << setw(70) << "Enter Current Time: " << endl;

    cout << "Hours is " << endl;
    cin >> hour;

    cout << "Minutes is " << endl;
    cin >> min;

    cout << "Seconds is " << endl;
    cin >> sec;

    if ((hour > 23) || (min > 60) || (sec > 60)) {
        cout << "Wrong Input" << endl;
    }

    else {
        while (true) {
            for (hour; hour < 24; hour++) {
                for (min; min < 60; min++) {
                    for (sec; sec < 60; sec++) {
                        system("cls");

                        cout << setfill('0') << setw(2) << hour << " : "
                                 << setfill('0') << setw(2) << min << " : "
                                 << setfill('0') << setw(2) << sec << endl;

                        Sleep(1000);
                    }
                    sec = 0;
                }
                min = 0;
            }
            hour = 0;
        }
    }



    return 0;
}
