# C-Practice-7

#include <stdio.h>
#include <math.h>

int main() {
    double x1, y1, r1, x2, y2, r2;
    scanf("%lf %lf %lf %lf %lf %lf", &x1, &y1, &r1, &x2, &y2, &r2);
    double dx = x2 - x1;
    double dy = y2 - y1;
    double d = sqrt(dx * dx + dy * dy);
    if (d > r1 + r2) {
        printf("0\n"); // no intersection
    } else if (d < fabs(r1 - r2)) {
        printf("0\n"); // no intersection
    } else if (d == 0 && r1 == r2) {
        printf("-1\n"); // infinite intersection points
    } else {
        printf("2\n"); // two intersection points
    }
    return 0;
}
