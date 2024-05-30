# Avoid screen keep awake (`@ecocode/avoid-keep-awake`)

⚠️ This rule _warns_ in the ✅ `recommended` config.

<!-- end auto-generated rule header -->

## Why is this an issue?

To avoid draining the battery, an Android device that is left idle quickly falls asleep.
Hence, keeping the screen on should be avoided, unless it is absolutely necessary.

```js
export default function KeepAwakeExample() {
  useKeepAwake(); // Non compliant
  return (
    <View style={{ flex: 1, alignItems: 'center', justifyContent: 'center' }}>
      <Text>This screen will never sleep!</Text>
    </View>
  );
}
```

```js
_activate = () => {
    activateKeepAwake(); // Non-compliant
    alert('Activated!');
  };
```

## Resources

### Documentation
