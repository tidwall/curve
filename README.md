# curve

C library for generating [Hilbert](https://en.wikipedia.org/wiki/Hilbert_curve)
and [Z-order](https://en.wikipedia.org/wiki/Z-order_curve) curves.

```c
#include <stdio.h>
#include <stdint.h>
#include <inttypes.h>

#include "curve.h"

int main(void) {
    double window[] = { -180, -90, 180, 90 };
    uint32_t hilbert = curve_hilbert(-33, -112, window);
    uint32_t zcurve = curve_z(-33, -112, window);
    printf("hilbert: %" PRIu32 "\n", hilbert);
    printf("z-curve: %" PRIu32 "\n", zcurve);
}
```

This code is released into the public domain.
