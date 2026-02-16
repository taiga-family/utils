### Font size watcher

```ts
const iframe = document.createElement('iframe');

tuiFontSizeWatcher(() => {
  return (size: number): void => {
    const current = clamp(size, 17, 28) - 17;

    return document.documentElement.style.setProperty('--font-offset', `${current}px`);
  };
}, iframe);
```
