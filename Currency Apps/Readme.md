# Currency Apps
Aplikasi ini memiliki fungsi perhitungan nilai tukar mata uang, dari dollar ke rupiah dengan satu dollarnya setara Rp.14788

## Scope & Functionalities
- User dapat memasukkan angka
- User dapat menyentuh tombol hitung
- User mendapat info "Invalid" jika yang dimasukkan berupa text

### How Does it Works?

Diawali dari method 'MainWindow' pada class MainWindows.xaml.cs kita mendeklarasikan 

```csharp

  public MainWindow()
        {
            InitializeComponent();
            currency = new CurrencyController();
        }

```
logika perhitungan terdapat pada class CurrencyController.cs sebagai berikut
cara kerjanya 

```csharp
class CurrencyController
    {
        public string usdToIdr(string nominal)
        {
            var nominalDouble = Convert.ToDouble(nominal);
            var result = nominalDouble * 14788;
            return Convert.ToString(result);
        }
```



