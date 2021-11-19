# Html-Helpers
# Html Helper

> For değerlerini model ile kullanıldığı zaman kullanıyoruz DropDownListFor gibi
> 

> [https://www.muratoner.net/aspnet/aspnet-mvc/aspnet-mvc-html-helper-elemanlari](https://www.muratoner.net/aspnet/aspnet-mvc/aspnet-mvc-html-helper-elemanlari) daha fazlası için burdaki makaleyi okuya bilirsiniz
> 

### Form

```csharp
@using (Html.BeginForm("About","Home",FormMethod.Post)){
	<input type="text" name="isim"/>
	<input type="submit" value="Kaydet"/>
}
//Html versiyonu
<form action="/Home/About" method="Post">
	<input type="text" name="isim"/>
	<input type="submit" value="Kaydet"/>
</form>
```

### CheckBox

```csharp
@Html.CheckBox("hobi1",false) 
@Html.CheckBox("hobi2",false)
@Html.CheckBox("hobi3",false)
//Html versiyonu
<input type="checkbox" name="hobi1" value="hobi1"/>
<input type="checkbox" name="hobi2" value="hobi2"/>
<input type="checkbox" name="hobi3" value="hobi3""/>
```

### DropDownList

```csharp
@Html.DropDownList("Ogrenciler","Lütfen bir öğrenci seç")
//Html versiyonu
<label for="Ogrenciler">Lütfen bir öğrenci seç</label>
<select name="Ogrenciler" id="Ogrenciler">
  <option value="ogrenci1">ogrenci1</option>
  <option value="ogrenci2">ogrenci2</option>
  <option value="ogrenci3">ogrenci3</option>
  <option value="ogrenci4">ogrenci4</option>
</select>
```

### TextArea

```csharp
@Html.TextArea("aciklama","",new {@row = 5})
//Html versiyonu
<label>aciklama:</label>
<textarea name="aciklama" rows="4" cols="50">
Bu uzun bir açıklama metnidir
</textarea>
```

### TextBox

```csharp
@Html.TextBox("isim","",new {maxlength = 5})
//Html versiyonu
<input type="text" name="isim">
```
