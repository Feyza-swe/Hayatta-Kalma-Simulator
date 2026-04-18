# 🌲 Hayatta Kalma Simülatörü (Survival Simulator)

Bu proje, C dili ile geliştirilmiş, strateji ve kaynak yönetimi odaklı, metin tabanlı (CLI) bir hayatta kalma oyunudur. Oyuncu, sınırlı kaynaklarla vahşi doğada hayatta kalmaya çalışırken riskli kararlar vermeli ve sağlık/enerji dengesini korumalıdır.

## 🕹️ Oyunun Amacı
Amacınız, sağlığınız (HP) veya enerjiniz tükenmeden hayatta kalabildiğiniz kadar kalmaktır. Her eylem belirli bir risk taşır ve kaynaklarınızı (yemek, sığınak) tüketir veya artırır.

## ✨ Temel Mekanikler

Oyunda yönetmeniz gereken 4 ana unsur bulunmaktadır:
- **Sağlık (HP):** %0 olduğunda oyun biter. Tehlikelerden ve açlıktan etkilenir.
- **Enerji:** %0 olduğunda oyun biter. Her eylem enerji tüketir.
- **Yemek:** Avlanarak elde edilir, enerji ve sağlık yönetimi için kritiktir.
- **Sığınak:** Dinlenme sırasında alınan verimi artırır.

## ⌨️ Komutlar ve Aksiyonlar

| Komut | Eylem | Detaylar |
| :--- | :--- | :--- |
| `A` | **Avlanma** | Yemek bulma şansı sunar. Enerji -20, yaralanma riski vardır. |
| `S` | **Sığınak Ara** | Dinlenme verimini artırmak için sığınak bulmaya çalışır. |
| `E` | **Envanter** | Mevcut durumunuzu (Sağlık, Enerji, Yemek) kontrol eder. |
| `R` | **Dinlenme** | Enerji ve sağlık yeniler (Sığınak varsa daha etkilidir). |
| `F` | **Tehlike** | Kaçma mücadelesi. Kurtulmak için şansınızı zorlayın! |
| `P` | **Şifre** | Şifreli kapıyı açarak ekstra yemek (bonus) kazanın. |
| `X` | **Çıkış** | Oyunu sonlandırır. |

## ⚙️ Teknik Gereksinimler ve Derleme

Uygulamanın çalışması için sisteminizde bir C derleyicisi (GCC, Clang vb.) kurulu olmalıdır.

**Derleme:**
```bash
gcc survival_simulator.c -o simulator
```

Çalıştırma:
```Bash
./simulator
```

## 🧠 Strateji İpuçları
**Önce Güvenlik:** Oyunun başında sığınak bulmak, dinlenme sırasında sağlık geri kazanmanızı sağlar. Bu, hayatta kalma sürenizi ciddi oranda artırır.

**Risk Yönetimi:** Enerjiniz %20'nin altına düştüğünde avlanmak yerine dinlenmeyi tercih edin.

**Şifre Bonusu:** Yemek stoğunuz azaldığında P komutu ile şifreyi çözerek (İpucu: G) bonus yemek almaya çalışın.

## 🛠️ Teknik Detaylar
**Dil:** C

**Yapı:** Standart C kütüphaneleri (stdio.h, stdlib.h, time.h) kullanılarak geliştirilmiştir

**Mantık:** Rastgele olay üretimi (Probabilistic events) için rand() fonksiyonu üzerine kurgulanmış bir oyun döngüsü içerir.
