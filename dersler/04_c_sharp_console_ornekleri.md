C# (C Sharp) dlininin genel kurallarını öğrenmek için öncelikle C# konsol uygulamaları üzerinde çalışmalar yapılmıştır.

```csharp
static void Main(string[] args)
{
    int a = 5;
    int b = 7;
    int c;
    c = a + b;

    Console.Write("a degiskeninin degeri: ");
    System.Console.Write(a);
    Console.Write("\nb değiskenin degeri: ");
    Console.WriteLine(b);
    Console.WriteLine(c);

    Console.WriteLine("{0}+{1}={2}", a, b, c);

    int d;
    d = b / a;
    Console.WriteLine(d);

    float e;
    e = (float)b / (float)a;
    Console.WriteLine(e);

    double f;
    f = Convert.ToDouble(b) / Convert.ToDouble(a);
    Console.WriteLine(f);

    string g;
    g = f.ToString();

    Console.WriteLine(g);
    Console.WriteLine("sonuc" + a);

    a = Convert.ToInt32(Console.ReadLine());
    b = Convert.ToInt32(Console.ReadLine());
    c = a + b;
    Console.WriteLine(c);
}
```



```csharp
static void Main(string[] args)
{
    string ad, soyad, egitim;
    char cinsiyet;
    int d;
    do
    {
        Console.WriteLine("Adınız: ");
        ad = Console.ReadLine();
        Console.WriteLine("Soyadınız: ");
        soyad = Console.ReadLine();

        while (true)
        {
            Console.WriteLine("Cinsiyet k/e : ");
            cinsiyet = Convert.ToChar(Console.ReadLine());
            if (cinsiyet == 'e' || cinsiyet == 'E' || cinsiyet == 'k' || cinsiyet == 'K')
            {
                Console.WriteLine("Cinsiyetinizi girdiniz.");
                break;
            }
            else
            {
                Console.WriteLine("Cinsiyetinizi yanlis girdiniz.e/k:");
            }
        }

        while (true)
        {
            Console.WriteLine("Eğitim Durumu Li/Ün: ");
            egitim = Console.ReadLine();
            if (egitim == "Li" || egitim == "Ün")
                break;
            Console.WriteLine("Hatalı giriş: Li/Ün");
        }
        Console.WriteLine("Cikis: -1");
        d = Convert.ToInt32(Console.ReadLine());
    } while (d != -1);
}
```

```csharp
static void Main(string[] args)
{
    int boy;
    string tur;
    bool hata;
    Console.WriteLine("Boyunuzu cm olarak giriniz: ");
    boy = Convert.ToInt32(Console.ReadLine());

    do
    {
        Console.WriteLine("Cevirmek isteginiz tur, mm/m/inc");
        tur = Console.ReadLine();
        hata = false;
        switch (tur)
        {
            case "mm": Console.WriteLine("Boyunuz: " + (boy * 10) + "mm'dir");
                break;
            case "m": Console.WriteLine("Boyunuz: " + ((double)boy / 100) + "m'dir");
                break;
            case "inc": Console.WriteLine("Boyunuz: " + ((double)boy / 2.54) + "inc'dir");
                break;
            default:
                Console.WriteLine("Hatalı giriş: mm/m/inc: ");
                hata = true;
                break;
        }
    } while (hata == true);

}
```

```csharp
static void Main(string[] args)
{
    int a, n;
    double y = 0.0;
    Console.WriteLine("baslangic degeri: ");
    a = Convert.ToInt32(Console.ReadLine());
    Console.WriteLine("bitis degeri: ");
    n = Convert.ToInt32(Console.ReadLine());

    for (int x = a; x <= n; x++)
    {
        y += Math.Abs(2 * Math.Sin(x * Math.PI / 180) - Math.Pow(x, 3));
    }
    Console.WriteLine("Sonuç: " + y);

}
```


```csharp
// Dizi ile ilgili örnek eklenecek
```

```csharp
//metodlarla (fonksiyon) ilgili örnek eklenecek. 
```
