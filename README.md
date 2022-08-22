# Project-_Java_01
Generate the random password 
package com.pratik;
import java.util.Random;
import java.util.Scanner;
public class Functions {
    public static void main(String[] args){
    //Lenth of our password as we have to choose .
    //Here it is to be 8
    int length = 8;
    System.out.println(password_gen(length));
    }
    //This is our Password generating Method
    //we have use static here,so that we not to make any object for it.
    static char[]password_gen(int len){
        System.out.println("Generating password using random() : ");
        System.out.print(" Your new password is : ");
        //A strong password has cap_char ,Lower_char,
        // numeric value and symbol.so we are using all of them to generate our password.
        String Capital_char = " ABCDEFGHIJKLMNOPQRSTUVWXYZ ";
        String Lower_char = "abcdefghijklmnopqrstuvwxyz";
        String numbers = "0123456789";
        String symbols ="!@#$%^&*_/.?<>()";
        String values = Capital_char + Lower_char + numbers + symbols;
        //Using rndm_method
        Random rndm_method= new Random();
        char[] password = new char[len];
        for(int i=0;i<len;i++)
        {
            //Using of CharAT() method: to get character value
            //Using of nextInt() as it is scanning the value as int
            password[i]=
                    values.charAt(rndm_method.nextInt(values.length()));
        }
        return password;
    }
}
