# UAS Algoritma dan Pemrograman
Pada UAS Algoritma dan Pemrograman kali ini saya membuat project yang bertujuan untuk menghitung suatu kandungan dalam makanan dan gizi dalam makanan.
Disini saya menggunakan bahasa pemrograman c++, tidak lain dan tidak bukan codingan ini hanya menggunakan codingan dasar dan masih perlu di kembangkan lebih lanjut lagi.
Project ini merupakan langkah awal saya dalam menyiapkan project besar yang mungkin akan saya kembangkan dikemudian hari dan berniat untuk bisa menjadikan sebagai uji kelulusan saya di Univeristas kali ini.
git clone [https://github.com/Xion-Enfys/Menghitung-Gizi-Makanan/blob/main/Codingan](https://github.com/Xion-Enfys/Menghitung-Gizi-Makanan/blob/main/Codingan.cpp)
git submodule init
git submodule update

#include <iostream>
#include <string>
using namespace std;

struct Bahan {
    double Energi;
    double Protein;
    double Lemak;
    double Karbohidrat;
    double Serat;
};

int main() {
    Bahan nasi = {180, 3, 0.3, 39.8, 0.2};
    Bahan telur = {174, 10.8, 14, 1.2, 0};
    Bahan ayam = {338, 35.2, 20.6, 0.4, 0};
    Bahan daging = {301, 55, 9, 0, 0};
    Bahan susu = {64, 4.3, 2.3, 6.6, 0};
    Bahan mentega = {742, 0.5, 81.6, 1.4, 0};
    Bahan santan = {122, 2, 10, 7.6, 1.4};
    Bahan minyak = {902, 0, 100, 0, 0};
    Bahan minyak_wijen = {881, 0.2, 99.7, 0, 0};
    Bahan gula_aren = {368, 0, 0, 92, 0};
    Bahan gula = {394, 0, 0, 94, 0};
    Bahan madu = {294, 0.3, 0, 79.5, 0.2};
    Bahan cuka = {21, 0.1, 0.1, 5, 0};
    Bahan kecap = {71, 5.7, 1.3, 9, 0};
    Bahan saos_tomat = {110, 2, 0.4, 24.5, 0.9};
    Bahan terasi = {155, 22.3, 2.9, 9.9, 2.7};
    Bahan bawang_merah = {46, 1.5, 0.3, 9.2, 1.7};
    Bahan bawang_putih = {112, 4.5, 0.2, 23.1, 0.6};
    Bahan cabai = {120, 4.7, 2.4, 19.9, 15.2};
    Bahan daun_salam = {301, 14.2, 10.9, 49, 9.4};
    Bahan jahe = {51, 1.5, 1, 10.1, 12};
    Bahan kemiri = {675, 19, 63, 8, 3};
    Bahan ketumbar = {418, 14.1, 16.1, 54.2, 12.3};
    Bahan kunyit = {69, 2, 2.7, 9.1, 0.6};
    Bahan merica = {365, 11.5, 6.8, 64.4, 1};
    Bahan bebek = {131, 20.2, 4.3, 2.8, 0};
    Bahan tomat = {24, 1.3, 0.5, 4.7, 0};
    Bahan toge = {34, 3.7, 1.2, 4.3, 1.1};
    Bahan terong = {28, 1.1, 0.2, 5.5, 2.1};
    Bahan jamur_tiram = {30, 1.9, 0.1, 5.5, 3.6};
    Bahan jamur_kuping = {21, 3.8, 0.6, 0.9, 5.1};
    Bahan tempe = {150, 14, 7.7, 9.1, 1.4};
    Bahan tahu = {80, 10.9, 4.7, 0.8, 0.1};
    Bahan tepung_terigu = {333, 9, 1, 77.2, 0.3};
    Bahan mie = {88, 0.6, 3.3, 14, 0.1};
    Bahan bihun = {348, 4.7, 0.1, 82.1, 1.2};
    Bahan garam = {0, 0, 0, 0, 0};
    Bahan kaldu_jamur = {20, 0.3, 0.5, 2, 0};
    Bahan saos_tiram = {10, 0, 0, 2, 0};
    
    string makanan;
    double gram [100];
    double Gizi [5];
    double totalGram;
    double sajian;
    string bahan;
    double totalEnergi = 0, totalLemak = 0, totalSerat = 0, totalProtein = 0, totalKarbohidrat = 0;
    
    cout << "=============== MENGHITUNG KANDUNGAN DAN GIZI PADA MAKANAN ===============\n";
    cout << "Masukan makanan : ";
    getline(cin, makanan);
    cout << "Masukan banyak makanan (gram): ";
    cin >> sajian;
    cout << "\nMakanan yang dipilih " << makanan << endl;
    cout << "Masukkan bahan yang digunakan (ketik 'selesai' untuk mengakhiri):\n";
    for(int i = 0; i < 100; i++){
        if (bahan == "selesai" ){
            break;
        }
    while (true) {
        cout << "========================================================================";
        cout << "\nMasukkan bahan: ";
        cin >> bahan;
        if (bahan == "selesai") {
            break;
        }
        cout << "Masukan banyak bahan(gram): ";
        cin >> gram [i];
        totalGram += gram[i];
        
        if (bahan == "nasi") {
            cout << "Nasi: Energi= " << nasi.Energi << " Protein= " << nasi.Protein << " Lemak= " << nasi.Lemak 
                 << " Karbohidrat= " << nasi.Karbohidrat << " Serat= " << nasi.Serat << endl;
            totalEnergi += gram[i]/100*nasi.Energi;
            totalProtein += gram[i]/100*nasi.Protein;
            totalLemak += gram[i]/100*nasi.Lemak;
            totalKarbohidrat += gram[i]/100*nasi.Karbohidrat;
            totalSerat += gram[i]/100*nasi.Serat;
            
        } else if (bahan == "telur") {
            cout << "Telur: Energi= " << telur.Energi << " Protein= " << telur.Protein << " Lemak= " << telur.Lemak 
                 << " Karbohidrat= " << telur.Karbohidrat << " Serat= " << telur.Serat << endl;
            totalEnergi += gram[i]/100*telur.Energi;
            totalProtein += gram[i]/100*telur.Protein;
            totalLemak += telur.Lemak;
            totalKarbohidrat += gram[i]/100*telur.Karbohidrat;
            totalSerat += gram[i]/100*telur.Serat;
            
        } else if (bahan == "ayam") {
            cout << "Ayam: Energi= " << ayam.Energi << " Protein= " << ayam.Protein << " Lemak= " << ayam.Lemak 
                 << " Karbohidrat= " << ayam.Karbohidrat << " Serat= " << ayam.Serat << endl;
            totalEnergi += gram[i]/100*ayam.Energi;
            totalProtein += gram[i]/100*ayam.Protein;
            totalLemak += gram[i]/100*ayam.Lemak;
            totalKarbohidrat += gram[i]/100*ayam.Karbohidrat;
            totalSerat += gram[i]/100*ayam.Serat;
            
        } else if (bahan == "santan") {
            cout << "Santan: Energi= " << santan.Energi << " Protein= " << santan.Protein << " Lemak= " << santan.Lemak 
                 << " Karbohidrat= " << santan.Karbohidrat << " Serat= " << santan.Serat << endl;
            totalEnergi += gram[i]/100*santan.Energi;
            totalProtein += gram[i]/100*santan.Protein;
            totalLemak += gram[i]/100*santan.Lemak;
            totalKarbohidrat += gram[i]/100*santan.Karbohidrat;
            totalSerat += gram[i]/100*santan.Serat;
            
        } else if (bahan == "daging") {
            cout << "Daging: Energi= " << daging.Energi << " Protein= " << daging.Protein << " Lemak= " << daging.Lemak 
                 << " Karbohidrat= " << daging.Karbohidrat << " Serat= " << daging.Serat << endl;
            totalEnergi += gram[i]/100*daging.Energi;
            totalProtein += gram[i]/100*daging.Protein;
            totalLemak += gram[i]/100*daging.Lemak;
            totalKarbohidrat += gram[i]/100*daging.Karbohidrat;
            totalSerat += gram[i]/100*daging.Serat;
            
        } else if (bahan == "susu") {
            cout << "Susu: Energi= " << susu.Energi << " Protein= " << susu.Protein << " Lemak= " << susu.Lemak 
                 << " Karbohidrat= " << susu.Karbohidrat << " Serat= " << susu.Serat << endl;
            totalEnergi += gram[i]/100*susu.Energi;
            totalProtein += gram[i]/100*susu.Protein;
            totalLemak += gram[i]/100*susu.Lemak;
            totalKarbohidrat += gram[i]/100*susu.Karbohidrat;
            totalSerat += gram[i]/100*susu.Serat;
            
        } else if (bahan == "mentega") {
            cout << "Mentega: Energi= " << mentega.Energi << " Protein= " << mentega.Protein << " Lemak= " << mentega.Lemak 
                 << " Karbohidrat= " << mentega.Karbohidrat << " Serat= " << mentega.Serat << endl;
            totalEnergi += gram[i]/100*mentega.Energi;
            totalProtein += gram[i]/100*mentega.Protein;
            totalLemak += gram[i]/100*mentega.Lemak;
            totalKarbohidrat += gram[i]/100*mentega.Karbohidrat;
            totalSerat += gram[i]/100*mentega.Serat;
            
        } else if (bahan == "minyak") {
            cout << "Minyak : Energi= " << minyak.Energi << " Protein= " << minyak.Protein << " Lemak= " << minyak.Lemak 
                 << " Karbohidrat= " << minyak.Karbohidrat << " Serat= " << minyak.Serat << endl;
            totalEnergi += gram[i]/100*minyak.Energi;
            totalProtein += gram[i]/100*minyak.Protein;
            totalLemak += gram[i]/100*minyak.Lemak;
            totalKarbohidrat += gram[i]/100*minyak.Karbohidrat;
            totalSerat += gram[i]/100*minyak.Serat;
            
        } else if (bahan == "minyak_wijen") {
            cout << "Minyak Wijen: Energi= " << minyak_wijen.Energi << " Protein= " << minyak_wijen.Protein << " Lemak= " << minyak_wijen.Lemak 
                 << " Karbohidrat= " << minyak_wijen.Karbohidrat << " Serat= " << minyak_wijen.Serat << endl;
            totalEnergi += gram[i]/100*minyak_wijen.Energi;
            totalProtein += gram[i]/100*minyak_wijen.Protein;
            totalLemak += gram[i]/100*minyak_wijen.Lemak;
            totalKarbohidrat += gram[i]/100*minyak_wijen.Karbohidrat;
            totalSerat += gram[i]/100*minyak_wijen.Serat;
            
        } else if (bahan == "gula_aren") {
            cout << "Gula Aren: Energi= " << gula_aren.Energi << " Protein= " << gula_aren.Protein << " Lemak= " << gula_aren.Lemak 
                 << " Karbohidrat= " << gula_aren.Karbohidrat << " Serat= " << gula_aren.Serat << endl;
            totalEnergi += gram[i]/100*gula_aren.Energi;
            totalProtein += gram[i]/100*gula_aren.Protein;
            totalLemak += gram[i]/100*gula_aren.Lemak;
            totalKarbohidrat += gram[i]/100*gula_aren.Karbohidrat;
            totalSerat += gram[i]/100*gula_aren.Serat;
            
        } else if (bahan == "gula") {
            cout << "Gula: Energi= " << gula.Energi << " Protein= " << gula.Protein << " Lemak= " << gula.Lemak 
                 << " Karbohidrat= " << gula.Karbohidrat << " Serat= " << gula.Serat << endl;
            totalEnergi += gram[i]/100*gula.Energi;
            totalProtein += gram[i]/100*gula.Protein;
            totalLemak += gram[i]/100*gula.Lemak;
            totalKarbohidrat += gram[i]/100*gula.Karbohidrat;
            totalSerat += gram[i]/100*gula.Serat;
            
        } else if (bahan == "madu") {
            cout << "Madu: Energi= " << madu.Energi << " Protein= " << madu.Protein << " Lemak= " << madu.Lemak 
                 << " Karbohidrat= " << madu.Karbohidrat << " Serat= " << madu.Serat << endl;
            totalEnergi += gram[i]/100*madu.Energi;
            totalProtein += gram[i]/100*madu.Protein;
            totalLemak += gram[i]/100*madu.Lemak;
            totalKarbohidrat += gram[i]/100*madu.Karbohidrat;
            totalSerat += gram[i]/100*madu.Serat;
            
        } else if (bahan == "cuka") {
            cout << "Cuka: Energi= " << cuka.Energi << " Protein= " << cuka.Protein << " Lemak= " << cuka.Lemak 
                 << " Karbohidrat= " << cuka.Karbohidrat << " Serat= " << cuka.Serat << endl;
            totalEnergi += gram[i]/100*cuka.Energi;
            totalProtein += gram[i]/100*cuka.Protein;
            totalLemak += gram[i]/100*cuka.Lemak;
            totalKarbohidrat += gram[i]/100*cuka.Karbohidrat;
            totalSerat += gram[i]/100*cuka.Serat;
            
        } else if (bahan == "kecap") {
            cout << "Kecap: Energi= " << kecap.Energi << " Protein= " << kecap.Protein << " Lemak= " << kecap.Lemak 
                 << " Karbohidrat= " << kecap.Karbohidrat << " Serat= " << kecap.Serat << endl;
            totalEnergi += gram[i]/100*kecap.Energi;
            totalProtein += gram[i]/100*kecap.Protein;
            totalLemak += gram[i]/100*kecap.Lemak;
            totalKarbohidrat += gram[i]/100*kecap.Karbohidrat;
            totalSerat += gram[i]/100*kecap.Serat;
            
        } else if (bahan == "saos_tomat") {
            cout << "Saos Tomat: Energi= " << saos_tomat.Energi << " Protein= " << saos_tomat.Protein << " Lemak= " << saos_tomat.Lemak 
                 << " Karbohidrat= " << saos_tomat.Karbohidrat << " Serat= " << saos_tomat.Serat << endl;
            totalEnergi += gram[i]/100*saos_tomat.Energi;
            totalProtein += gram[i]/100*saos_tomat.Protein;
            totalLemak += gram[i]/100*saos_tomat.Lemak;
            totalKarbohidrat += gram[i]/100*saos_tomat.Karbohidrat;
            totalSerat += gram[i]/100*saos_tomat.Serat;
            
        } else if (bahan == "terasi") {
            cout << "Terasi: Energi= " << terasi.Energi << " Protein= " << terasi.Protein << " Lemak= " << terasi.Lemak 
                 << " Karbohidrat= " << terasi.Karbohidrat << " Serat= " << terasi.Serat << endl;
            totalEnergi += gram[i]/100*terasi.Energi;
            totalProtein += gram[i]/100*terasi.Protein;
            totalLemak += gram[i]/100*terasi.Lemak;
            totalKarbohidrat += gram[i]/100*terasi.Karbohidrat;
            totalSerat += gram[i]/100*terasi.Serat;
            
        } else if (bahan == "bawang_merah") {
            cout << "Bawang Merah: Energi= " << bawang_merah.Energi << " Protein= " << bawang_merah.Protein << " Lemak= " << bawang_merah.Lemak 
                 << " Karbohidrat= " << bawang_merah.Karbohidrat << " Serat= " << bawang_merah.Serat << endl;
            totalEnergi += gram[i]/100*bawang_merah.Energi;
            totalProtein += gram[i]/100*bawang_merah.Protein;
            totalLemak += gram[i]/100*bawang_merah.Lemak;
            totalKarbohidrat += gram[i]/100*bawang_merah.Karbohidrat;
            totalSerat += gram[i]/100*bawang_merah.Serat;
            
        } else if (bahan == "bawang_putih") {
            cout << "Bawang Putih: Energi= " << bawang_putih.Energi << " Protein= " << bawang_putih.Protein << " Lemak= " << bawang_putih.Lemak 
                 << " Karbohidrat= " << bawang_putih.Karbohidrat << " Serat= " << bawang_putih.Serat << endl;
            totalEnergi += gram[i]/100*bawang_putih.Energi;
            totalProtein += gram[i]/100*bawang_putih.Protein;
            totalLemak += gram[i]/100*bawang_putih.Lemak;
            totalKarbohidrat += gram[i]/100*bawang_putih.Karbohidrat;
            totalSerat += gram[i]/100*bawang_putih.Serat;
            
        } else if (bahan == "cabai") {
            cout << "Cabai: Energi= " << cabai.Energi << " Protein= " << cabai.Protein << " Lemak= " << cabai.Lemak 
                 << " Karbohidrat= " << cabai.Karbohidrat << " Serat= " << cabai.Serat << endl;
            totalEnergi += gram[i]/100*cabai.Energi;
            totalProtein += gram[i]/100*cabai.Protein;
            totalLemak += gram[i]/100*cabai.Lemak;
            totalKarbohidrat += gram[i]/100*cabai.Karbohidrat;
            totalSerat += gram[i]/100*cabai.Serat;
            
        } else if (bahan == "daun_salam") {
            cout << "Daun Salam: Energi= " << daun_salam.Energi << " Protein= " << daun_salam.Protein << " Lemak= " << daun_salam.Lemak 
                 << " Karbohidrat= " << daun_salam.Karbohidrat << " Serat= " << daun_salam.Serat << endl;
            totalEnergi += gram[i]/100*daun_salam.Energi;
            totalProtein += gram[i]/100*daun_salam.Protein;
            totalLemak += gram[i]/100*daun_salam.Lemak;
            totalKarbohidrat += gram[i]/100*daun_salam.Karbohidrat;
            totalSerat += gram[i]/100*daun_salam.Serat;
            
        } else if (bahan == "jahe") {
            cout << "Jahe: Energi= " << jahe.Energi << " Protein= " << jahe.Protein << " Lemak= " << jahe.Lemak 
                 << " Karbohidrat= " << jahe.Karbohidrat << " Serat= " << jahe.Serat << endl;
            totalEnergi += gram[i]/100*jahe.Energi;
            totalProtein += gram[i]/100*gram[i]/100*jahe.Protein;
            totalLemak += gram[i]/100*jahe.Lemak;
            totalKarbohidrat += gram[i]/100*jahe.Karbohidrat;
            totalSerat += gram[i]/100*jahe.Serat;
            
        } else if (bahan == "kemiri") {
            cout << "Kemiri: Energi= " << kemiri.Energi << " Protein= " << kemiri.Protein << " Lemak= " << kemiri.Lemak 
                 << " Karbohidrat= " << kemiri.Karbohidrat << " Serat= " << kemiri.Serat << endl;
            totalEnergi += gram[i]/100*kemiri.Energi;
            totalProtein += gram[i]/100*kemiri.Protein;
            totalLemak += gram[i]/100*kemiri.Lemak;
            totalKarbohidrat += gram[i]/100*kemiri.Karbohidrat;
            totalSerat += gram[i]/100*kemiri.Serat;
            
        } else if (bahan == "ketumbar") {
            cout << "Ketumbar: Energi= " << gram[i]/100*ketumbar.Energi << " Protein= " << ketumbar.Protein << " Lemak= " << ketumbar.Lemak 
                 << " Karbohidrat= " << gram[i]/100*ketumbar.Karbohidrat << " Serat= " << ketumbar.Serat << endl;
            totalEnergi += gram[i]/100*ketumbar.Energi;
            totalProtein += gram[i]/100*ketumbar.Protein;
            totalLemak += gram[i]/100*gram[i]/100*gram[i]/100*ketumbar.Lemak;
            totalKarbohidrat += gram[i]/100*gram[i]/100*ketumbar.Karbohidrat;
            totalSerat += gram[i]/100*ketumbar.Serat;
            
        } else if (bahan == "kunyit") {
            cout << "Kunyit: Energi= " << kunyit.Energi << " Protein= " << kunyit.Protein << " Lemak= " << kunyit.Lemak 
                 << " Karbohidrat= " << kunyit.Karbohidrat << " Serat= " << kunyit.Serat << endl;
            totalEnergi += gram[i]/100*kunyit.Energi;
            totalProtein += gram[i]/100*kunyit.Protein;
            totalLemak += gram[i]/100*kunyit.Lemak;
            totalKarbohidrat += gram[i]/100*kunyit.Karbohidrat;
            totalSerat += gram[i]/100*kunyit.Serat;
            
        } else if (bahan == "merica") {
            cout << "Merica: Energi= " << merica.Energi << " Protein= " << merica.Protein << " Lemak= " << merica.Lemak 
                 << " Karbohidrat= " << merica.Karbohidrat << " Serat= " << merica.Serat << endl;
            totalEnergi += gram[i]/100*merica.Energi;
            totalProtein += gram[i]/100*merica.Protein;
            totalLemak += gram[i]/100*merica.Lemak;
            totalKarbohidrat += gram[i]/100*merica.Karbohidrat;
            totalSerat += gram[i]/100*merica.Serat;
            
        } else if (bahan == "bebek") {
            cout << "Bebek: Energi= " << bebek.Energi << " Protein= " << bebek.Protein << " Lemak= " << bebek.Lemak 
                 << " Karbohidrat= " << bebek.Karbohidrat << " Serat= " << bebek.Serat << endl;
            totalEnergi += gram[i]/100*bebek.Energi;
            totalProtein += gram[i]/100*bebek.Protein;
            totalLemak += gram[i]/100*bebek.Lemak;
            totalKarbohidrat += gram[i]/100*bebek.Karbohidrat;
            totalSerat += gram[i]/100*bebek.Serat;
            
        } else if (bahan == "tomat") {
            cout << "Tomat: Energi= " << gram[i]/100*tomat.Energi << " Protein= " << tomat.Protein << " Lemak= " << tomat.Lemak 
                 << " Karbohidrat= " << gram[i]/100*tomat.Karbohidrat << " Serat= " << tomat.Serat << endl;
            totalEnergi += gram[i]/100*tomat.Energi;
            totalProtein += gram[i]/100*tomat.Protein;
            totalLemak += gram[i]/100*tomat.Lemak;
            totalKarbohidrat += gram[i]/100*tomat.Karbohidrat;
            totalSerat += gram[i]/100*tomat.Serat;
            
        } else if (bahan == "toge") {
            cout << "Toge: Energi= " << toge.Energi << " Protein= " << toge.Protein << " Lemak= " << toge.Lemak 
                 << " Karbohidrat= " << toge.Karbohidrat << " Serat= " << toge.Serat << endl;
            totalEnergi += gram[i]/100*toge.Energi;
            totalProtein += gram[i]/100*toge.Protein;
            totalLemak += gram[i]/100*gram[i]/100*toge.Lemak;
            totalKarbohidrat += gram[i]/100*toge.Karbohidrat;
            totalSerat += gram[i]/100*toge.Serat;
            
        } else if (bahan == "terong") {
            cout << "Terong: Energi= " << terong.Energi << " Protein= " << terong.Protein << " Lemak= " << terong.Lemak 
                 << " Karbohidrat= " << terong.Karbohidrat << " Serat= " << terong.Serat << endl;
            totalEnergi += gram[i]/100*terong.Energi;
            totalProtein += gram[i]/100*terong.Protein;
            totalLemak += gram[i]/100*terong.Lemak;
            totalKarbohidrat += gram[i]/100*gram[i]/100*terong.Karbohidrat;
            totalSerat += gram[i]/100*terong.Serat;
            
        } else if (bahan == "jamur_tiram") {
            cout << "Jamur Tiram: Energi= " << jamur_tiram.Energi << " Protein= " << jamur_tiram.Protein << " Lemak= " << jamur_tiram.Lemak 
                 << " Karbohidrat= " << jamur_tiram.Karbohidrat << " Serat= " << jamur_tiram.Serat << endl;
            totalEnergi += gram[i]/100*jamur_tiram.Energi;
            totalProtein += gram[i]/100*jamur_tiram.Protein;
            totalLemak += gram[i]/100*jamur_tiram.Lemak;
            totalKarbohidrat += gram[i]/100*jamur_tiram.Karbohidrat;
            totalSerat += gram[i]/100*jamur_tiram.Serat;
            
        } else if (bahan == "jamur_kuping") {
            cout << "Jamur Kuping: Energi= " << jamur_kuping.Energi << " Protein= " << jamur_kuping.Protein << " Lemak= " << jamur_kuping.Lemak 
                 << " Karbohidrat= " << jamur_kuping.Karbohidrat << " Serat= " << jamur_kuping.Serat << endl;
            totalEnergi += gram[i]/100*jamur_kuping.Energi;
            totalProtein += gram[i]/100*jamur_kuping.Protein;
            totalLemak += gram[i]/100*jamur_kuping.Lemak;
            totalKarbohidrat += jamur_kuping.Karbohidrat;
            totalSerat += gram[i]/100*jamur_kuping.Serat;
            
        } else if (bahan == "tempe") {
            cout << "Tempe: Energi= " << tempe.Energi << " Protein= " << tempe.Protein << " Lemak= " << tempe.Lemak 
                 << " Karbohidrat= " << tempe.Karbohidrat << " Serat= " << tempe.Serat << endl;
            totalEnergi += gram[i]/100*tempe.Energi;
            totalProtein += gram[i]/100*tempe.Protein;
            totalLemak += gram[i]/100*tempe.Lemak;
            totalKarbohidrat += gram[i]/100*tempe.Karbohidrat;
            totalSerat += gram[i]/100*tempe.Serat;
            
        } else if (bahan == "tahu") {
            cout << "Tahu: Energi= " << tahu.Energi << " Protein= " << tahu.Protein << " Lemak= " << tahu.Lemak 
                 << " Karbohidrat= " << tahu.Karbohidrat << " Serat= " << tahu.Serat << endl;
            totalEnergi += gram[i]/100*tahu.Energi;
            totalProtein += gram[i]/100*tahu.Protein;
            totalLemak += gram[i]/100*tahu.Lemak;
            totalKarbohidrat += gram[i]/100*tahu.Karbohidrat;
            totalSerat += gram[i]/100*tahu.Serat;
            
        } else if (bahan == "tepung_terigu") {
            cout << "Tepung Terigu: Energi= " << tepung_terigu.Energi << " Protein= " << tepung_terigu.Protein << " Lemak= " << tepung_terigu.Lemak 
                 << " Karbohidrat= " << tepung_terigu.Karbohidrat << " Serat= " << tepung_terigu.Serat << endl;
            totalEnergi += gram[i]/100*tepung_terigu.Energi;
            totalProtein += gram[i]/100*tepung_terigu.Protein;
            totalLemak += gram[i]/100*tepung_terigu.Lemak;
            totalKarbohidrat += gram[i]/100*tepung_terigu.Karbohidrat;
            totalSerat += gram[i]/100*tepung_terigu.Serat;
            
        } else if (bahan == "mie") {
            cout << "Mie: Energi= " << mie.Energi << " Protein= " << mie.Protein << " Lemak= " << mie.Lemak 
                 << " Karbohidrat= " << mie.Karbohidrat << " Serat= " << mie.Serat << endl;
            totalEnergi += gram[i]/100*mie.Energi;
            totalProtein += gram[i]/100*mie.Protein;
            totalLemak += gram[i]/100*mie.Lemak;
            totalKarbohidrat += gram[i]/100*mie.Karbohidrat;
            totalSerat += gram[i]/100*mie.Serat;
            
        } else if (bahan == "bihun") {
            cout << "Bihun: Energi= " << bihun.Energi << " Protein= " << bihun.Protein << " Lemak= " << bihun.Lemak 
                 << " Karbohidrat= " << bihun.Karbohidrat << " Serat= " << bihun.Serat << endl;
            totalEnergi += gram[i]/100*bihun.Energi;
            totalProtein += gram[i]/100*bihun.Protein;
            totalLemak += gram[i]/100*bihun.Lemak;
            totalKarbohidrat += gram[i]/100*bihun.Karbohidrat;
            totalSerat += gram[i]/100*bihun.Serat;
            
        } else if (bahan == "garam") {
            cout << "Garam: Energi= " << garam.Energi << " Protein= " << garam.Protein << " Lemak= " << garam.Lemak 
                 << " Karbohidrat= " << garam.Karbohidrat << " Serat= " << garam.Serat << endl;
            totalEnergi += gram[i]/100*garam.Energi;
            totalProtein += gram[i]/100*garam.Protein;
            totalLemak += gram[i]/100*garam.Lemak;
            totalKarbohidrat += gram[i]/100*garam.Karbohidrat;
            totalSerat += gram[i]/100*garam.Serat;
            
        } else if (bahan == "kaldu_jamur") {
            cout << "Kaldu Jamur: Energi= " << kaldu_jamur.Energi << " Protein= " << kaldu_jamur.Protein << " Lemak= " << kaldu_jamur.Lemak 
                 << " Karbohidrat= " << kaldu_jamur.Karbohidrat << " Serat= " << kaldu_jamur.Serat << endl;
            totalEnergi += gram[i]/100*kaldu_jamur.Energi;
            totalProtein += gram[i]/100*kaldu_jamur.Protein;
            totalLemak += gram[i]/100*kaldu_jamur.Lemak;
            totalKarbohidrat += gram[i]/100*kaldu_jamur.Karbohidrat;
            totalSerat += gram[i]/100*kaldu_jamur.Serat;
            
        } else if (bahan == "saos_tiram") {
            cout << "Saos Tiram: Energi= " << saos_tiram.Energi << " Protein= " << saos_tiram.Protein << " Lemak= " << saos_tiram.Lemak 
                 << " Karbohidrat= " << saos_tiram.Karbohidrat << " Serat= " << saos_tiram.Serat << endl;
            totalEnergi += gram[i]/100*saos_tiram.Energi;
            totalProtein += gram[i]/100*saos_tiram.Protein;
            totalLemak += gram[i]/100*saos_tiram.Lemak;
            totalKarbohidrat += gram[i]/100*saos_tiram.Karbohidrat;
            totalSerat += gram[i]/100*saos_tiram.Serat;
            
        } else {
            cout << "Bahan tidak dikenal.\n";
        }
    }
    }
    
    Gizi[0] = sajian/totalGram*totalEnergi;
    Gizi[1] = sajian/totalGram*totalProtein;
    Gizi[2] = sajian/totalGram*totalLemak;
    Gizi[3] = sajian/totalGram*totalKarbohidrat;
    Gizi[4] = sajian/totalGram*totalSerat;
    
    cout << "\n========== HASIL KANDUNGAN DAN GIZI YANG DI DAPATKAN ==========";
    cout << "\n ";
    cout << "\nMAKANAN      : " << makanan << endl;
    cout << "BANYAK MAKANAN : " << sajian << endl;
    cout << "==============================\n";
    cout << "\nTOTAL KANDUNGAN :\n";
    cout << "==============================\n";
    cout << "Gram        : " << totalGram << " g\n";
    cout << "Energi      : " << totalEnergi << " kkal\n";
    cout << "Protein     : " << totalProtein << " g\n";
    cout << "Lemak       : " << totalLemak << " g\n";
    cout << "Karbohidrat : " << totalKarbohidrat << " g\n";
    cout << "Serat       : " << totalSerat << " g\n";
    
    cout << "\nTOTAL GIZI :\n";
    cout << "==============================\n";
    cout << "Energi      : " << Gizi[0] << " kkal\n";
    cout << "Protein     : " << Gizi[1] << " g\n";
    cout << "Lemak       : " << Gizi[2] << " g\n";
    cout << "Karbohidrat : " << Gizi[3] << " g\n";
    cout << "Serat       : " << Gizi[4] << " g\n";
    return 0;
}
![alt text](https://github.com/Xion-Enfys/Menghitung-Gizi-Makanan/blob/main/Tampilan%20Hasil%20Run%20Code.png?raw=true)
