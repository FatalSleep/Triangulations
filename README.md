# Triangulations
Delauny-Triangulation Stuff (implementations are not my own).

Find the circumcircle of a triangle:
```C++
// DEFINE INPUT TRIANGLE:
input triangle: [x1,y1], [x2,y2], [x3,y3]

// SQUARE OF TRIANGLE:
sqx1 = sqr(x1);
sqy1 = sqr(y1);
sqx2 = sqr(x2);
sqy2 = sqr(y2);
sqx3 = sqr(x3);
sqy3 = sqr(y3);

// DETERMINENT, CIRCUMCIRCLE X,Y and RADIUS:
dt = 1 / ((x1 * (y2 - y3) + x2 * (y3 - y1) + x3 * (y1 - y2)) * 2);
cx = ((sqx1 + sqy1) * (y2 - y3) + (sqx2 + sqy2) * (y3 - y1) + (sqx3 + sqy3) * (y1 - y2)) * dt;
cy = ((sqx1 + sqy1) * (x3 - x2) + (sqx2 + sqy2) * (x1 - x3) + (sqx3 + sqy3) * (x2 - x1)) * dt;
cr = sqrt(sqr(x1 - cx) + sqr(y1 - cy));
```
