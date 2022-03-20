# C
SNAKE GAME WİTH C;


#include <stdio.h>

    #include <conio.h>
    
    main(){
        int bas,eksilt,say=0,sonuc;
        printf("Baslangic sayisini ve eksilecek sayi miktarini girin!: ");
        scanf("%d %d",&bas,&eksilt); //değerleri aldık
        oyun: //dönüş etiketi
            printf("%d-%d=? \n",bas,eksilt); //sorumuzu sorduk
            bas-=eksilt; //sorunun sonucunu eksilterek bulduk
            scanf("%d",&sonuc); //kullanıcının cevabını aldık
            if(sonuc==bas){ //eğer sonuc doğruysa etikete giderek tekrar azalttık
                goto oyun;
            }else{ //eğer sonuc doğru değilse yanlış sayısını bir artırıp sayiyi tekrar eski haline getirdik
                bas+=eksilt;
                say++;
                printf("%d.yanlisin! \n",say); //yanlış sayısını söyledil
                if(say==3){
                    printf("3 yanlis yaptin oyun bitti!!"); //yanlış 3 se oyunu bitirdik değilse oyun etiketine geri döndük
                }else{
                    goto oyun;
                }
            }
    }


