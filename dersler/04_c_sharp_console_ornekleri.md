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

---

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
---

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

---

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

---
Diziye klavyeden veri girişi, Dizinin elemanlarının toplamı:

```csharp
static void Main(string[] args)
{
    //double[] sayilar = new double[5]{2,4,6,8,10};
double[] sayilar = new double[5];
int i;
double toplam = 0;
for (i = 0; i < 5; i++)
{
	Console.WriteLine((i + 1) + ". sayıyı giriniz: ");
	sayilar[i] = Convert.ToDouble(Console.ReadLine());
}

for(i=0;i<5;i++)
	toplam+=sayilar[i];

Console.WriteLine("toplam: " + toplam);
}
```

---

C# ile fonksiyon

```csharp
class Program
    {
        static int r1, r2, r3;

        static void direnc_gir()
        {
            Console.WriteLine("1. direnç: ");
            r1 = Convert.ToInt32(Console.ReadLine());
            Console.WriteLine("2. direnç: ");
            r2 = Convert.ToInt32(Console.ReadLine());
            Console.WriteLine("3. direnç: ");
            r3 = Convert.ToInt32(Console.ReadLine());
        }
        static double seri(double d1, double d2, double d3)
        {
            return d1 + d2 + d3;
        }

        static double paralel(double d1, double d2, double d3)
        {
            return 1/(1/d1 + 1/d2 + 1/d3);
        }

        static void menu()
        {
            char tur;
            do
            {
                Console.WriteLine("Bağlantı türünü giriniz (S/P): ");
                tur = Console.ReadKey().KeyChar;
            } while (!(tur == 'S' || tur == 'P'));

            if (tur == 'S')
            {
                Console.WriteLine("Eşdeğer direnç: "+ seri(r1, r2, r3));
            }
            else
            {
                Console.WriteLine("Eşdeğer direnç: " + paralel(r1, r2, r3));
            }
        }

        static void Main(string[] args)
        {
            direnc_gir();
            menu();
        }
    }

```
