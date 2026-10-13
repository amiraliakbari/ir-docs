# دستور العمل تولید فایل‌های لیست بیمه سازمان تامین اجتماعی

تاریخ ۱۳۹۲/۰۸/۱۵

چنانچه شما برای ایجاد فایل لیست بیمه خود از نرم‌افزار موجود روی سایت تامین اجتماعی استفاده نمی‌نمایید و تمایل به تهیه خروجی مورد نظر از سیستم‌های موجود در کارگاه خود می‌باشید، فایل مورد نظر طبق فرمت ذیل باید ایجاد گردد.

- نام فایل اطلاعات کارگاه بایستی `DSKKAR00.DBF` یا `DSKKAR00.TXT` باشد. اولویت با فرمت dbf است.
- نام فایل اطلاعات بیمه‌شدگان بایستی `DSKWOR00.DBF` یا `DSKWOR00.TXT` باشد. اولویت با فرمت dbf است.
- تاریخ‌ها به صورت شمسی و بدون در نظر گرفتن `/` می‌باشد. برای مثال ۱۳۹۲۰۷۰۱
- برای فیلد جنسیت ورودی رشته "مرد" یا "زن" باشد.
- در دو طرف هیچ یک از فیلدها کاراکتر space و یا enter درج نشده باشد.
- مقدار فیلد `DSK_KIND` بایستی با ۰ پر شود.
- در فیلدهای نوع Character به هیچ وجه نباید یکی از ۵ کاراکتر `"`, `'`, `>`, `<`, `&` درج شده باشد.
- Encoding فایل‌ها باید Unicode باشد.

ساختار فایل‌ها طبق جدول زیر باید ایجاد شود.

## فرمت فایل DSKKAR00

| شماره ستون در فایل | نام فیلد | نوع | حداکثر طول | توضیحات |
| --- | --- | --- | --- | --- |
| ۱ | DSK_ID | Character | ۱۰ | کد کارگاه |
| ۲ | DSK_NAME | Character | ۱۰۰ | نام کارگاه |
| ۳ | DSK_FARM | Character | ۱۰۰ | نام کارفرما |
| ۴ | DSK_ADRS | Character | ۱۰۰ | آدرس کارگاه |
| ۵ | DSK_KIND | Numeric | ۱ | نوع لیست |
| ۶ | DSK_YY | Numeric | ۲ | سال عملکرد |
| ۷ | DSK_MM | Numeric | ۲ | ماه عملکرد |
| ۸ | DSK_LISTNO | Character | ۱۲ | شماره لیست |
| ۹ | DSK_DISC | Character | ۱۰۰ | شرح لیست |
| ۱۰ | DSK_NUM | Numeric | ۵ | تعداد کارکنان |
| ۱۱ | DSK_TDD | Numeric | ۶ | مجموع روزهای کارکرد |
| ۱۲ | DSK_TROOZ | Numeric | ۱۲ | مجموع دستمزد روزانه |
| ۱۳ | DSK_TMAH | Numeric | ۱۲ | مجموع دستمزد ماهانه |
| ۱۴ | DSK_TMAZ | Numeric | ۱۲ | مجموع مزایای ماهانه مشمول |
| ۱۵ | DSK_TMASH | Numeric | ۱۲ | مجموع دستمزد و مزایای ماهانه مشمول |
| ۱۶ | DSK_TTOTL | Numeric | ۱۲ | مجموع کل دستمزد و مزایای ماهانه (مشمول و غیر مشمول) |
| ۱۷ | DSK_TBIME | Numeric | ۱۲ | مجموع حق بیمه سهم بیمه‌شده |
| ۱۸ | DSK_TKOSO | Numeric | ۱۲ | مجموع حق بیمه سهم کارفرما |
| ۱۹ | DSK_BIC | Numeric | ۱۲ | مجموع حق بیمه بیکاری |
| ۲۰ | DSK_RATE | Numeric | ۵ | نرخ حق بیمه |
| ۲۱ | DSK_PRATE | Numeric | ۲ | نرخ پورسانتاژ |
| ۲۲ | DSK_BIMH | Numeric | ۱۲ | نرخ مشاغل سخت و زیان‌آور |
| ۲۳ | MON_PYM | Character | ۳ | ردیف پیمان |

## فرمت فایل DSKWOR00

| شماره ستون در فایل | نام فیلد | نوع | حداکثر طول | توضیحات |
| --- | --- | --- | --- | --- |
| ۱ | DSW_ID | Character | ۱۰ | کد کارگاه |
| ۲ | DSW_YY | Numeric | ۲ | سال عملکرد |
| ۳ | DSW_MM | Numeric | ۲ | ماه عملکرد |
| ۴ | DSW_LISTNO | Character | ۱۲ | شماره لیست |
| ۵ | DSW_ID1 | Character | ۱۰ | شماره بیمه |
| ۶ | DSW_FNAME | Character | ۱۰۰ | نام |
| ۷ | DSW_LNAME | Character | ۱۰۰ | نام خانوادگی |
| ۸ | DSW_DNAME | Character | ۱۰۰ | نام پدر |
| ۹ | DSW_IDNO | Character | ۱۵ | شماره شناسنامه |
| ۱۰ | DSW_IDPLC | Character | ۱۰۰ | محل صدور |
| ۱۱ | DSW_IDATE | Character | ۸ | تاریخ صدور |
| ۱۲ | DSW_BDATE | Character | ۸ | تاریخ تولد |
| ۱۳ | DSW_SEX | Character | ۳ | جنسیت |
| ۱۴ | DSW_NAT | Character | ۱۰ | ملیت |
| ۱۵ | DSW_OCP | Character | ۱۰۰ | شرح شغل |
| ۱۶ | DSW_SDATE | Character | ۸ | تاریخ شروع به کار |
| ۱۷ | DSW_EDATE | Character | ۸ | تاریخ ترک کار |
| ۱۸ | DSW_DD | Numeric | ۲ | تعداد روزهای کارکرد |
| ۱۹ | DSW_ROOZ | Numeric | ۱۲ | دستمزد روزانه |
| ۲۰ | DSW_MAH | Numeric | ۱۲ | دستمزد ماهانه |
| ۲۱ | DSW_MAZ | Numeric | ۱۲ | مزایای ماهانه |
| ۲۲ | DSW_MASH | Numeric | ۱۲ | جمع دستمزد و مزایای ماهانه مشمول |
| ۲۳ | DSW_TOTL | Numeric | ۱۲ | جمع کل دستمزد و مزایای ماهانه |
| ۲۴ | DSW_BIME | Numeric | ۱۲ | حق بیمه سهم بیمه‌شده |
| ۲۵ | DSW_PRATE | Numeric | ۲ | نرخ پورسانتاژ |
| ۲۶ | DSW_JOB | Character | ۶ | کد شغل |
| ۲۷ | PER_NATCOD | Character | ۱۰ | کد ملی |

# منابع

* https://tamin.ir/file/file/8460
