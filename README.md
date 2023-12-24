#include <stdio.h>

int main() {
    int enYuksekTeklif = 0;
    int yeniTeklif;

    printf("Açık artırmaya hoş geldiniz!\n");

    while (1) {
        printf("Şu anki en yüksek teklif: %d TL\n", enYuksekTeklif);
        printf("Yeni teklif vermek isterseniz miktarı girin (Çıkmak için -1): ");
        scanf("%d", &yeniTeklif);

        if (yeniTeklif == -1) {
            printf("Açık artırma sonlandırıldı. En yüksek teklif: %d TL\n", enYuksekTeklif);
            break;
        } else if (yeniTeklif <= enYuksekTeklif) {
            printf("Teklif geçersiz. Lütfen daha yüksek bir teklif verin.\n");
        } else {
            enYuksekTeklif = yeniTeklif;
            printf("Yeni en yüksek teklif: %d TL\n", enYuksekTeklif);
        }
    }

    return 0;
}



AÇIKLAMA:
1-) açık artırma için ilk değer girilir.
2-) girilen değer son artırmaysa program sonlanır. değilse devam eder.
3-) son değer girildikten sonra en yüksek verilen artırma fiyatı kaç ise onu veren kullanıcı belirlenir ve satış gerçekleşir.



