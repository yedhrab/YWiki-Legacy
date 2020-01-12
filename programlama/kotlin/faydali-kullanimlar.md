# 🌟 Faydalı Kullanımlar

## 🐥 Get Set Kullanımı

* 🌌 Get set olmadan direkt olarak kullanabilirsiniz
* ‍🧙‍♂ Kotlin onu sizin için halletmekte

```kotlin
val arrayAdapter = ArrayAdapter<String>(
    wifiDirectActivity,
    R.layout.activity_wifi_direct,
    deviceNameList
)
wifiDirectActivity.lvPeer.adapter = arrayAdapter
```

## 👮‍♂️ Switch - Case

* 🤝 Koşullu değer atama işlemlerini destekler
* 📈 Sıradan switch yapısına göre daha verimlidir

```kotlin
val reasonMsg = when (reason) {
    WifiP2pManager.P2P_UNSUPPORTED -> "P2P desteklenmiyor"
    WifiP2pManager.ERROR -> "hata oluştur"
    WifiP2pManager.BUSY -> "cihaz başka bir bağlantı ile meşgul"
    else -> ""
}
```

## 👨‍💼 Apply

* 👪 Bir değişkenin birden fazla metodunu kullanmayı sağar
* 📈 Tekrar tekrar yazmayı engeller

```kotlin
private val wifiFilter = IntentFilter().apply {
    addAction(WifiP2pManager.WIFI_P2P_STATE_CHANGED_ACTION)
    addAction(WifiP2pManager.WIFI_P2P_PEERS_CHANGED_ACTION)
    addAction(WifiP2pManager.WIFI_P2P_CONNECTION_CHANGED_ACTION)
    addAction(WifiP2pManager.WIFI_P2P_THIS_DEVICE_CHANGED_ACTION)
}
```

## 💁‍♂️ Also

```kotlin
channel?.also { channel ->
    wifiReceiver = WifiDirectBroadcastReceiver(manager, channel, this)
}
```

## 👀 Dokümantasyon Linkleri

* 👇 Metotların üzerine geldiğinizde \(hover\) açıklamasında doküman linki olur
* ⭐ Link üzerinden kullanım örneklerine erişirsiniz

![](../../.gitbook/assets/image%20%28127%29.png)

## 👮‍♂️ İzinlerin Kontrolü

* 📢 İzin tanımlanmadığında hata verir
* 💁‍♂️ `@SupressLint("MissingPermission")` ile bunu engelleyebilirsiniz
* 🤭 "Ne yaptığımın farkındayım, bana bulaşma" demek gibi

![](../../.gitbook/assets/image%20%2825%29.png)

## 🐣 Keyword Argument

* ✨ Değişkenlerin adları ile onlara değer atayabilirsin
* ⭐ Python gibi dillerde olan bir kullanımdır

```kotlin
hasWifiDirectPermission(activity = activity)

fun hasWifiDirectPermission(activity: Activity): Boolean {
    return hasPermission(
        activity,
        Manifest.permission.ACCESS_FINE_LOCATION
    )
}
```
