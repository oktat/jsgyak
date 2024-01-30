# Táblázat renderelése

## Tömb renderelése táblázatba

### A tömb

```javascript

const jarmuvek = [
    {
      az: 1,
      rendszam: "ABC-123",
      marka: "Opel",
      urtartalom: 1400,
      ar: 2300
    },
    {
      az: 2,
      rendszam: "ADC-235",
      marka: "Ford",
      urtartalom: 1600,
      ar: 3420
    }
  ]
```

### Weblap a táblázatnak

index.html:

```html
<!DOCTYPE html>
<html lang="hu">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>

    <table class="table table-striped">
        <thead>
            <tr>
                <th>#</th>
                <th>Rendszám</th>
                <th>Márka</th>
                <th>Űrtartalom</th>
                <th>Ár</th>
            </tr>
        </thead>
        <tbody id="tbody">
            
        </tbody>

    </table>
    

    <script src="app.js"></script>

</body>
</html>
```

app.js:

```javascript
const tbody = document.querySelector("#tbody")

const jarmuvek = [
    {
      az: 1,
      rendszam: "ABC-123",
      marka: "Opel",
      urtartalom: 1400,
      ar: 2300
    },
    {
      az: 2,
      rendszam: "ADC-235",
      marka: "Ford",
      urtartalom: 1600,
      ar: 3420
    }
  ]

jarmuvek.forEach(jarmu => {
    var tr = document.createElement('tr');
    var aztd = document.createElement('td');
    var rendszamtd = document.createElement('td');
    var markatd = document.createElement('td');
    var urtartalomtd = document.createElement('td');
    var artd = document.createElement('td');
    aztd.textContent = jarmu.az
    rendszamtd.textContent = jarmu.rendszam
    markatd.textContent = jarmu.marka
    urtartalomtd.textContent = jarmu.urtartalom
    artd.textContent = jarmu.ar
    tr.appendChild(aztd);
    tr.appendChild(rendszamtd);
    tr.appendChild(markatd);
    tr.appendChild(urtartalomtd);
    tr.appendChild(artd);
    tbody.appendChild(tr)
})
```
