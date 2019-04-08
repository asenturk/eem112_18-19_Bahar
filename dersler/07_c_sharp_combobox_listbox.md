**C# Form: Radio Buton, CheckBox Uygulaması:**    

Form elemanlarının Name özellikleri şu şekilde ayarlanmıştır:      
aşağıda tasarımda form elemanlarının üzerine/yakınına kırmızı ile yazılmıştır


*Tasarım*   


![](img/uyg5_form.jpg)




```csharp
 private void combSinif_SelectedIndexChanged(object sender, EventArgs e)
        {
            lblSinif.Text = combSinif.SelectedItem.ToString();
        }

        private void combYD_SelectedIndexChanged(object sender, EventArgs e)
        {
            lblYD.Text = Convert.ToString(combYD.SelectedIndex);
        }

        private void btnListeyeEkle_Click(object sender, EventArgs e)
        {
            lbOgrenciler.Items.Add(tbAdSoyad.Text + " " + combSinif.Text + " " + combYD.Text);
            lblEklemeSayisi.Text =  Convert.ToString(lbOgrenciler.Items.Count);
        }

        private void lbOgrenciler_SelectedIndexChanged(object sender, EventArgs e)
        {
            lblSecilenIndis.Text = Convert.ToString(lbOgrenciler.SelectedIndex);
        }

        private void lbOgrenciler_MouseClick(object sender, MouseEventArgs e)
        {
            lbListe2.Items.Add(lbOgrenciler.SelectedItem.ToString());
        }

        private void lbListe2_SelectedIndexChanged(object sender, EventArgs e)
        {
            lbListe2.Items.Remove(lbListe2.SelectedItem);
        }

        private void btnGuncelle_Click(object sender, EventArgs e)
        {
            int satir = lbOgrenciler.SelectedIndex;
            lbOgrenciler.Items.RemoveAt(satir);
            lbOgrenciler.Items.Insert(satir, tbAdSoyad.Text + " " + combSinif.Text + " " + combYD.Text);
        }

        private void btnArama_Click(object sender, EventArgs e)
        {
            int satir;
            satir = lbOgrenciler.FindString(tbArama.Text,-1);
            lblArama.Text = Convert.ToString(satir);
            lbOgrenciler.SelectedIndex = satir;
        }
```


