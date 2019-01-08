# Projet-du-Semestre
Rapport 0 mini projet
Zakaria maouedji & Bechiri abdelghani & kouira noufel


## Sommaire : 
#1.introduction

#2.mecanisme de traitement 

#3.Outils utilisé pour le developement et deployment 

# 1.introduction: 
on resume notre travail dans la structure suivante :
![structfinale](https://user-images.githubusercontent.com/44119963/50853574-dc0c9880-1382-11e9-8321-cefcd3d7ec1d.png)

L’utilisateur consulté notre « site » ou l’interface client suivante :

![interface](https://user-images.githubusercontent.com/44119963/50853710-5210ff80-1383-11e9-9ec6-527fcae31371.png)

Le client doit entreé le chemin de Docx et le chemin de reception de fichier converti
Avec un E-mail  Facultative pour  recevoir le fichier traité dans son mail


# 2. mécanismes de traitement : 

1.	La convertion : 

A l’aide d’une web methode d’un web service , qui comporte des bebliothéque de convertion 

org.apache.poi.xwpf.converter.pdf.PdfConverter; 

org.apache.poi.xwpf.converter.pdf.PdfOptions; 

org.apache.poi.xwpf.usermodel.XWPFDocument; 

2.	L’envoi de mail : 

A l’aide d’une web methode de meme web service , qui comporte aussi des bébliotheque de Send Mail 

import java.io.InputStream;

import java.io.OutputStream;

import java.util.Date;

import java.util.logging.Level;

import java.util.logging.Logger;

import javax.mail.internet.InternetAddress;

import javax.mail.internet.MimeBodyPart;

import javax.mail.internet.MimeMessage;

import javax.mail.internet.MimeMultipart;


 

 # 3. Outils utilisé pour le developement et deployment  :
 
 1.	Web service « soap »
2.	Interface Client (implimenter avec HTML code ) 
3.	Netbeans (outils de programation) 
4.	Compte Mail ‘qui utilise un fournisseur de mail 
5.	openShift pour le deployment de l’application sur le Cloud


 
