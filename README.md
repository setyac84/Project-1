/* adt1.c */
#include <stdio.h>
#include <stdio.h>
#include <string.h>
#include <time.h>

#pragma GCC diagnostic ignored "-Wwrite-strings"  
/*struktur Mahasiswa*/


typedef struct{
	char noreg[11];
	char nama[26];
	int tahun_masuk;
	float IPK;
	
}Mahasiswa;

typedef struct{
	char alamat[20];
	char jenis_kelamin[11];
	char asal_sekolah[26];
	int tahun_lulus;
	
}Data;

typedef struct{
	char nama_ayah[18];
	char nama_ibu[18];
	char pekerjaan_ayah[15];
	char pekerjaan_ibu[15];
	
}Dataortu;

Mahasiswa inisialisasi(char *noreg, char *nama, int th_masuk, float
ipk){
Mahasiswa temp;
	strcpy(temp.noreg, noreg);
	strcpy(temp.nama, nama);
	temp.tahun_masuk =th_masuk;
	temp.IPK = ipk;
return temp;
}

Data inisialisasi(int tahun_lulus, char *alamat, char *jenis_kelamin, char *asal_sekolah){
Data temp;
	strcpy(temp.alamat, alamat);
	strcpy(temp.jenis_kelamin, jenis_kelamin);
	strcpy(temp.asal_sekolah, asal_sekolah);
	temp.tahun_lulus =tahun_lulus;
return temp;
}

Dataortu inisialisasi(char *nama_ayah, char *nama_ibu, char *pekerjaan_ayah, char *pekerjaan_ibu){
Dataortu temp;
	strcpy(temp.nama_ayah, nama_ayah);
	strcpy(temp.nama_ibu, nama_ibu);
	strcpy(temp.pekerjaan_ayah, pekerjaan_ayah);
	strcpy(temp.pekerjaan_ibu, pekerjaan_ibu);
return temp;
}


void cetak(Mahasiswa m){
	printf("Noreg = %s\n",m.noreg);
	printf("Nama = %s\n",m.nama);
	printf("Angkatan = %d\n",m.tahun_masuk);
	printf("IPK = %.2f\n",m.IPK);
}

void cetak (Data m){
	printf("Alamat = %s\n",m.alamat);
	printf("Jenis Kelamin = %s\n",m.jenis_kelamin);
	printf("Asal Sekolah = %.s\n",m.asal_sekolah);
	printf("Tahun Lulus = %d\n",m.tahun_lulus);
}

void cetak (Dataortu m){
	printf("Nama Ayah = %s\n",m.nama_ayah);
	printf("Nama Ibu = %s\n",m.nama_ibu);
	printf("Jenis Pekerjaan Ayah = %s\n",m.pekerjaan_ayah);
	printf("Jenis Pekerjaan Ibu = %.s\n",m.pekerjaan_ibu);
}

void ubahNama(Mahasiswa *m, char *new_nama){
strcpy(m->nama,new_nama);
}


void ubahIPK(Mahasiswa *m, float new_ipk){
m->IPK = new_ipk;
}


int jatahSKS(Mahasiswa m){
if(m.IPK>=3.0){
return 24;
}else if(m.IPK>=2.75){
return 20;
}else if(m.IPK>=2.5){
return 18;
}else{
return 12;
	}
}


void cetakJatahSKS(Mahasiswa m){
printf("Mahasiswa %s mendapat jatah maksimal mengambil SKS sebesar %d sks",m.nama, jatahSKS(m));
}


main(){
Mahasiswa Alfiansyah;
Alfiansyah = inisialisasi("5235150001","Alfiansyah Putra", 2016,3.45);
cetak(Alfiansyah);
printf("\n");
ubahNama(&Alfiansyah,"Alfiansyah PTIK");
cetak(Alfiansyah);
printf("\n");
ubahIPK(&Alfiansyah, 3.67);
cetak(Alfiansyah);
cetakJatahSKS(Alfiansyah);

	strcpy(Alfiansyah.data[0].alamat,"Jalan Superhero XI, Greendland");
	strcpy(Alfiansyah.data[0].jenis_kelamin,"Laki-laki");
	strcpy(Alfiansyah.data[0].asal_sekolah,"SMAN 999 Superhero");
	alfiansyah.data[0].tahun_lulus=2016;


		strcpy(Alfiansyah.dataortu[1].nama_ayah,"James Watt");
		strcpy(Alfiansyah.dataortu[1].nama_ibu,"Sarah Cameron");
		strcpy(Alfiansyah.dataortu[1].pekerjaan_ayah,"Wiraswasta");
		strcpy(Alfiansyah.dataortu[1].pekerjaan_ibu,"Pegawai Negeri");

	

}
