# محاسبه حقوق به زمان
گرفتن ورودی مقدار حقوق ماهیانه و محاسبه آن به روز و ساعت و حتی ثانیه با داشتن قابلیت ویرایش کردن
#برنامه مقدار درآمد ماهانه به روز،ساعت،دقیقه و ثانیه
print("barname mohasebe hooghogh be zaman")
#از کاربر مقدار حقوق ماهانه گرفته میشود
x = int(input('meghdar hooghoghe mahiane at ro bego : '))
print(f'\ndaramd mahiane shoma : {x:,} TOMAN\n') #نمایش درآمد وارد شده به صورت خوانا
if 0 <= x <= 5000000 :
    print('khyli pol kami migiri ... hava set bashe\n HALA bia bebinim baghi rah chie!!!\n')
elif 5000000 < x <= 10000000 :
    print ('daramad mamoli dari ... vali baz biya berim baghi rah brim ;)\n')
elif x > 10000000 :
    print ('Ooo ... dari bad jor poooool paro mikoni kalak\nye chi dasti be ma bede bala\n')

while True:
    try:
        
        print('==================\naz meno zir yek gozine ro bego : ↓ ')
        print('1.daramd be roz\n2.daramd be saat\n3.daramd be daghighe\n4.daramd be sanie\n5.edit daramad\n6.exit\n\n==================\n')
        
        f = int (input ('yek gozine entekhab kon : '))
        
        if f == 6 :
            print('****  barname be PAYAN resid ... byby  ****')
            break
        
        elif f == 1 :
            #تبدیل به حقوق روزانه
            hooghogh_be_roz = x/30
            print(f'to dar roz < {hooghogh_be_roz:,} toman > dar miyari')
         
        elif f == 2 :
            #دیفالت روی 8 ساعت کاری در هر روز است که میشه 240 در ماه
            hooghogh_be_saat = x/240
            print(f'to dar saat < {hooghogh_be_saat:,} toman > dar miyari')
        
        elif f == 3 :
            #تبدیل به دقیقه
            hooghogh_be_min = (x/240)/60
            print(f'to dar daghighe < {hooghogh_be_min:,} toman > dar miyari')

        elif f == 4 :
            #تبدیل به ثانیه
            hooghogh_be_sec = ((x/240)/60)/60
            print(f'to dar sanie < {hooghogh_be_sec:,} toman > dar miyari')
        #تغییر دادن و ادیت درآمد ماهانه
        elif f == 5 :
            x = int(input('meghdar daramad jadid ro bego : '))
            print (f'daramad : {x:,}')



    #اگر هیچ کدام از گزینه ها وارد نشده بود متن زیر نمایش داده میشود
    except ValueError:
        print('\ngozine vared shode dorost nist')
