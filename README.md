- 👋 Hi, I’m @Man2h
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
Man2h/Man2h is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
#include <iostream>
#include <cstdlib>
#include <ctime>

using namespace std;

// تعريف هيكل لسيارة
struct Car {
    int position;
};

// تحريك السيارة بشكل عشوائي
void moveCar(Car &car) {
    car.position += rand() % 3 + 1; // تحريك بين 1 و 3 خانات
}

// طباعة حالة السيارة
void printCarStatus(const Car &car) {
    cout << "Car position: " << car.position << endl;
}

int main() {
    // ضبط بذرة لتوليد أرقام عشوائية
    srand(time(0));

    // إنشاء سيارة
    Car playerCar;
    playerCar.position = 0;

    // البداية
    cout << "Welcome to the Car Game!" << endl;

    // اللعب حتى تصل السيارة لنهاية المضمار (مثلاً 20)
    while (playerCar.position < 20) {
        // حركة السيارة
        moveCar(playerCar);

        // طباعة حالة السيارة
        printCarStatus(playerCar);

        // انتظار للرؤية الواضحة للنتيجة
        for (int i = 0; i < 100000000; ++i) {}

        // مسافة للتباطؤ
        system("clear");
    }

    // نهاية اللعبة
    cout << "Congratulations! You reached the finish line." << endl;

    return 0;
}
