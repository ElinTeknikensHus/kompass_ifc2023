# kompassIFC2023

## Kompass (med full tutorial) @unplugged
<div style="display: flex; justify-content: space-around;">
  <img src="https://github.com/ElinTeknikensHus/esero_test/blob/master/logotyp%20esero-sweden_svart.png?raw=true" alt="DampVibrations" width="300"/>
  <img src="https://github.com/ElinTeknikensHus/esero_test/blob/master/TH-logo-liggande-svart%403x.png?raw=true" alt="DampVibrations" width="300"/>
</div>

# Räkna grader-variablen
Skapa en variabel, som du kallar `||variables:grader||`. Sätt variabelns värde till `||input:kompassriktning||` och dra in i `||basic:för alltid||` -loopen

```block
let grader = 0
basic.forever(function () {
    grader = input.compassHeading()
})
```

## steg 1
Detta ska vara på svenska
```block
let grader = 0
basic.forever(function () {
    grader = input.compassHeading()
    if (grader < 45) {
        basic.showString("N")
    } else if (grader < 135) {
        basic.showString("O")
    } else if (grader < 225) {
        basic.showString("Hello!")
    } else if (grader < 315) {
        basic.showString("V")
    } else {
        basic.showString("N")
    }
})
```