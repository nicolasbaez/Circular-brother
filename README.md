# Circular-brother
I am burning up inside.

![buh](https://github.com/nicolasbaez/Circular-brother/blob/main/xp085.gif)
```javascript
setup = (_) => createCanvas((w = 500), w);
k = 0;
d = 30;
draw = (_) => {
  h = w / 2;
  background(0);
  noStroke();
  for (i = 0; i <= w; i += w / d) {
    for (j = 0; j <= w; j += w / d) {
      n = noise(i / 99 + k / 99, j / 99 + k / 99, k / 99) * h;
      fill(h, n, 0, n);
      rect(i, j, w / d, w / d);
    }
  }
  if (k == 0) saveGif("xp085.gif", 666, { delay: 0, units: "frames" });
  k++;
};
