## Де знайти панель управління DNS корпоративного домену сервера Google

У більшості випадків панель керування DNS **відсутня** всередині Google Admin Console (`admin.google.com`). Сервіси Google Workspace керують поштою, диском та акаунтами, але не є реєстратором зони DNS за замовчуванням.

Де насправді знаходиться панель керування вашим доменом:

* **У вашого реєстратора домену (найчастіший випадок):** Якщо домен купували окремо (наприклад, NIC.UA, Namecheap, GoDaddy), DNS-записи редагуються в особистому кабінеті цього реєстратора.
* **Якщо домен купували через Google Domains:** Сервіс Google Domains перейшов під управління Squarespace. Усі DNS-записи таких доменів зараз редагуються на **`domains.squarespace.com`**.
* **Якщо компанія використовує Google Cloud:** Якщо DNS-зону свідомо перенесли в хмару Google, записи знаходяться в **Google Cloud Console** (`console.cloud.google.com`) у розділі **Network Services** -> **Cloud DNS**.

1. **Перевірте Name Servers (NS):** 1 хв.
Перейдіть на сайт `whois.com` або `who.is` та введіть ім'я вашого корпоративного домену.


2. **Визначте майданчик DNS:** Крок 2.
Знайдіть у звіті рядок **Name Servers**:

* Якщо там вказано `ns1.godaddy.com`, `ns1.nic.ua` тощо — вам потрібен кабінет відповідного реєстратора.
* Якщо вказано `ns1.squarespace.com` — увійдіть на `domains.squarespace.com`.
* Якщо вказано `ns-cloud-x1.googledomains.com` — панель знаходиться у `console.cloud.google.com`.


3. **Перейдіть у панель записів:** Крок 3.
Увійдіть у потрібний сервіс під акаунтом адміністратора та відкрийте розділ **DNS Management**, **DNS Zone Editor** або **Керування зоною DNS**.

```
% Registrant:
% ===========
person:           TOV "Kotris"
organization:     TOV "Kotris"
e-mail:           info@kotris.com.ua
address:          Pecherskiy uzviz 15
address:          KYIV
postal-code:      01011
country:          UA
country-loc:      UA
phone:            +380.444562275
mnt-by:           ua.imena
status:           ok
status:           linked
created:          2014-03-31 17:32:49+03
source:           UAEPP
```