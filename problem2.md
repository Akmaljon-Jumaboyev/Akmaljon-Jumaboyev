#include <iostream>

using namespace std;


class Timer {
private:
    int hours;
    int minutes;
    int seconds;

public:
    
    Timer(int h, int m, int s) {
        hours = (h >= 0 && h <= 23) ? h : 0;
        minutes = (m >= 0 && m <= 59) ? m : 0;
        seconds = (s >= 0 && s <= 59) ? s : 0;
    }

    
    void printTime() {
        cout << hours << ":" << minutes << ":" << seconds << endl;
    }
};

int main() {
    
    Timer timer(10, 45, 30);
    timer.printTime();
    return 0;
}
