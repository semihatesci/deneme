# deneme
import java.util.ArrayList;
import java.util.Scanner;
import java.util.Random;
import java.io.*;
public class yılan {
	        public static void main(String args[])throws IOException
	        { ArrayList<String> my_list = new ArrayList<String>();
	        
	        
	        my_list.add("semih");
	        my_list.add("araba");
	        my_list.add("ev");
	        my_list.add("fiyat");
	        my_list.add("bina");
	        my_list.add("çatı");
	        my_list.add("sevgi");
	        my_list.add("inanç");
	        my_list.add("süleyman");
	        my_list.add("serkan");
	        my_list.add("recep");
	        my_list.add("ege");
	        my_list.add("fethiye");
	        my_list.add("isim");
	      
	        
	       
	  
	        
	        
	        
	           // generating the index using Math.random()
	            int kelime = (int)(Math.random() * my_list.size());
	  

	        
	                String kelime1 = my_list.get(kelime);
	                int i,tahmin=0,anahtar=0,dogru=0;
	                String eldevar[] = new String[kelime1.length()];

	                System.out.println("Kelimeyi bulmak için 5 yanlış hakkınız var.");
	                BufferedReader klavye = new BufferedReader(new InputStreamReader(System.in));

	                for (i = 0; i < kelime1.length(); i++)
	                {
	                        eldevar[i] = "_ ";

	                }

	                finish:
	                while(tahmin<6){
	                        System.out.println("Bir harf giriniz (Kalan hakkiniz "+(5 -tahmin) +") : ");
	                        String harf = klavye.readLine();
	                        tahmin++;
	                        for (i = 0; i < kelime1.length(); i++)
	                        {
	                                if (kelime1.charAt(i) == harf.charAt(0))
	                                {
	                                        eldevar[i] = harf+" ";
	                                        anahtar = 1;
	                                        dogru++;
	                                        if (dogru == kelime1.length()) { System.out.println("kelime " +kelime1+"...Tebrikler..."); break finish; }
	                                }
	                        }
	                        if (anahtar == 1) { anahtar = 0; tahmin--; }
	                        for (i = 0; i < kelime1.length(); i++)
	                        {
	                                System.out.print(eldevar[i]);

	                        }
	                        System.out.println();
	                }
	                if (dogru != kelime1.length()) { System.out.println("Uzgunum... Dogru yanit " + kelime1); }

	        }

}

