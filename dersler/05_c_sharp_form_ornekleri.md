**C# form**

Buton: butonun name özelliği *benim_butonum* olarak değiştirilmiş.   
label: name özelliği *etiket* olarak değiştirilmiş.
3 tane textbox eklenmiş. Texboxların name özellikleri *birinciSayi*, *ikinciSayi* ve *sonuc* olarak değiştirilmiş.

```csharp
string[] mesajlar= new string[3]{"birinci mesaj", 
                                 "ikinci mesaj", "üçüncü mesaj"};
int i = 0;
private void benim_butonum_Click(object sender, EventArgs e)
{
	// MessageBox.Show("Merhaba!");
    etiket.Text = mesajlar[i%3];
    i++;
    int a, b, c;
    a = Convert.ToInt32(birinciSayi.Text);
    b = Convert.ToInt32(ikinciSayi.Text);
    c = a + b;
    sonuc.Text = c.ToString();
}
```