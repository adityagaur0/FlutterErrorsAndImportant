1. use stack
2.
```
Positioned.fill(
  child: BackdropFilter(
    filter: ImageFilter.blur(sigmaX: 5, sigmaY: 10),
    child: const SizedBox(),
  )
),
```

3.
```
Container(
      margin: EdgeInsets.all(displayWidth * .05),
      height: displayWidth * .155,
      decoration: BoxDecoration(
        color: Colors.white,
        boxShadow: const [
          BoxShadow(
            color: Colors.black,
            blurRadius: 100,
            offset: Offset(0, 30),
          ),
        ],
        borderRadius: BorderRadius.circular(50),
      ),
```
