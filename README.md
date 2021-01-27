# PopupMenu
display costum xml, when you click listener

- `MainActivity.java`
```java
button.setOnClickListener(new View.OnClickListener() {
    @Override
    public void onClick(View v) {
        PopupMenu popupMenu = new PopupMenu(MainActivity.this, button);
        popupMenu.getMenuInflater().inflate(R.menu.popup_menu,popupMenu.getMenu());

        popupMenu.setOnMenuItemClickListener(new PopupMenu.OnMenuItemClickListener() {
            @Override
            public boolean onMenuItemClick(MenuItem item) {
                Toast.makeText(MainActivity.this, "" + item.getTitle(), Toast.LENGTH_SHORT).show();
                return true;
            }
        });

        popupMenu.show();
    }
});
```

- `res->menu->popup_menu.xml`
```xml
<?xml version="1.0" encoding="utf-8"?>
<menu xmlns:android="http://schemas.android.com/apk/res/android">
    <item
        android:id="@+id/p1"
        android:title="Pilihan 1" />
    <item
        android:id="@+id/p2"
        android:title="Pilihan 2" />
    <item
        android:id="@+id/p3"
        android:title="Pilihan 3" />
</menu>
```

<p align="center">
  <img src="https://github.com/gzeinnumer/PopupMenu/blob/master/preview/example1.jpg" width="400"/>
</p>

---

```
Copyright 2020 M. Fadli Zein
```