# میانگین نتایج GZSDA

همهٔ اعداد درصد هستند.

## خلاصهٔ H-mean

هر دیتاست در یک سطر آمده و ستون‌ها میانگین `H-mean` روش‌ها هستند.

| دیتاست | CCVAE | our_dc | our_tr | our_dc_tr |
|---|---:|---:|---:|---:|
| Xray | 54.19 | 53.89 | 56.63 | 56.23 |
| Office31 | 84.27 | 84.01 | 84.42 | 84.02 |
| OfficeHome | 66.60 | 66.64 | 67.47 | 67.53 |
| ActionStyle v1 | 27.13 | 28.76 | 39.44 | 39.92 |
| ActionStyle v2 | 86.80 | 85.97 | 93.45 | 92.34 |

## نتایج کامل

| دیتاست | تعداد سناریوی انتقال | روش | Acc_s (دیده‌شده) | Acc_u (دیده‌نشده) | H-mean |
|---|---:|---|---:|---:|---:|
| Xray | ۲ | CCVAE | 84.12 | 40.76 | 54.19 |
| Xray | ۲ | our_dc | 83.53 | 40.54 | 53.89 |
| Xray | ۲ | our_tr | 80.77 | 44.24 | 56.63 |
| Xray | ۲ | our_dc_tr | 79.59 | 44.00 | 56.23 |
| Office31 | ۶ | CCVAE | 89.61 | 80.52 | 84.27 |
| Office31 | ۶ | our_dc | 89.54 | 80.09 | 84.01 |
| Office31 | ۶ | our_tr | 87.64 | 82.19 | 84.42 |
| Office31 | ۶ | our_dc_tr | 87.30 | 81.74 | 84.02 |
| OfficeHome | ۱۲ | CCVAE | 76.72 | 59.17 | 66.60 |
| OfficeHome | ۱۲ | our_dc | 76.80 | 59.18 | 66.64 |
| OfficeHome | ۱۲ | our_tr | 74.17 | 62.19 | 67.47 |
| OfficeHome | ۱۲ | our_dc_tr | 74.08 | 62.34 | 67.53 |
| ActionStyle v1 | ۴۲ | CCVAE | 81.56 | 22.47 | 27.13 |
| ActionStyle v1 | ۴۲ | our_dc | 81.33 | 24.13 | 28.76 |
| ActionStyle v1 | ۴۲ | our_tr | 78.11 | 36.29 | 39.44 |
| ActionStyle v1 | ۴۲ | our_dc_tr | 78.11 | 36.80 | 39.92 |
| ActionStyle v2 | ۷ | CCVAE | 98.37 | 79.80 | 86.80 |
| ActionStyle v2 | ۷ | our_dc | 98.57 | 78.51 | 85.97 |
| ActionStyle v2 | ۷ | our_tr | 97.50 | 90.63 | 93.45 |
| ActionStyle v2 | ۷ | our_dc_tr | 97.37 | 89.04 | 92.34 |

## روش محاسبه

برای هر دیتاست و روش، بخش میانگینِ مقدار `mean ± SEM` هر سناریوی انتقال از فایل نتیجه خوانده شده و میانگین حسابی آن‌ها با وزن یکسان محاسبه شده است. `H-mean` هر دو جدول میانگین **H-mean گزارش‌شده برای سناریوها** است؛ این مقدار از میانگین‌های `Acc_s` و `Acc_u` دوباره محاسبه نشده است. اعداد تا دو رقم اعشار گرد شده‌اند. v1 شامل تمام ۴۲ انتقال جهت‌دار بین هفت سبک است؛ v2 شامل هفت سناریوی `all_but_<style> -> <style>` است.

منابع: [Xray](result/json/xray.json)، [Office31](result/json/office31.json)، [OfficeHome](result/json/officeHome.json)، [ActionStyle v1](result/json/actionStyle_v1.json)، [ActionStyle v2](result/json/actionStyle_v2.json).
