# DarkLightDetector
Header-only Qt based very light Windows Dark/Light color mode detector.

## Usage
```C++
#include <QCoreApplication>
#include <QDebug>

#include "darklightdetector.hpp"

int main(int argc, char *argv[])
{
    QCoreApplication a(argc, argv);
    
    DarkLightDetector detector;
    
    // notify(bool) signal emitted when color mode changes
    QObject::connect(&detector, &DarkLightDetector::notify, [](bool isDark){ qDebug() << "is dark" << isDark; });
    
    return a.exec();
}
```
