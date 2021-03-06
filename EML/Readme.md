# EML

## Qu'est que EML ou Electronic Mail Format ?
> EML est un format de fichier mail brute. \
> Le fichier est standardisé et peut donc être lu par des webmail, client mail ou des outils écrits pour. (outlook, Mozilla Thunderbird, internet explorer, ...) \
> Le format est relativement simple puisqu'il est en brute, on trouve l'en-tête du mail, le sujet et le corps. \
> Les pièces jointes y sont aussi présentes. \
> Bref le même contenu que lorsque vous regardez le source d'un mail.

## EML et son code :
> Pour comprendre son contenu nous allons enregistrer un mail et l'ouvrir avec Vscode:
```eml
MIME-Version: 1.0
Date: Mon, 13 Dec 2021 09:31:44 +0400
From: gilles boyer <boyer.gilles@live.fr>
Subject: UML
Thread-Topic: UML
Message-ID:
 <PAXPR02MB74856831A3ADB81D6081747A83749@PAXPR02MB7485.eurprd02.prod.outlook.com>
To: gilles boyer <boyer.gilles@live.fr>
Content-Transfer-Encoding: quoted-printable
Content-Type: text/html; charset="utf-8"

<html xmlns:v=3D"urn:schemas-microsoft-com:vml" xmlns:o=3D"urn:schemas-micr=
osoft-com:office:office" xmlns:w=3D"urn:schemas-microsoft-com:office:word" =
xmlns:m=3D"http://schemas.microsoft.com/office/2004/12/omml" xmlns=3D"http:=
//www.w3.org/TR/REC-html40"><head>
<meta http-equiv=3D"Content-Type" content=3D"text/html; charset=3Dutf-8"><m=
eta name=3D"Generator" content=3D"Microsoft Word 15 (filtered medium)"><!--=
[if !mso]><style>v\:* {behavior:url(#default#VML);}
o\:* {behavior:url(#default#VML);}
w\:* {behavior:url(#default#VML);}
.shape {behavior:url(#default#VML);}
</style><![endif]--><style><!--
/* Font Definitions */
@font-face
	{font-family:"Cambria Math";
	panose-1:2 4 5 3 5 4 6 3 2 4;}
@font-face
	{font-family:Calibri;
	panose-1:2 15 5 2 2 2 4 3 2 4;}
/* Style Definitions */
p.MsoNormal, li.MsoNormal, div.MsoNormal
	{margin:0cm;
	font-size:11.0pt;
	font-family:"Calibri",sans-serif;}
a:link, span.MsoHyperlink
	{mso-style-priority:99;
	color:blue;
	text-decoration:underline;}
.MsoChpDefault
	{mso-style-type:export-only;}
@page WordSection1
	{size:612.0pt 792.0pt;
	margin:70.85pt 70.85pt 70.85pt 70.85pt;}
div.WordSection1
	{page:WordSection1;}
--></style></head><body lang=3D"FR-RE" link=3D"blue" vlink=3D"#954F72" styl=
e=3D"word-wrap:break-word"><div class=3D"WordSection1"><p class=3D"MsoNorma=
l">Hello world </p><p class=3D"MsoNormal"><o:p>&nbsp;</o:p></p><p class=3D"=
MsoNormal"><img width=3D"454" height=3D"227" style=3D"width:4.7291in;height=
:2.3645in" id=3D"Image_x0020_2" src=3D"cid:image002.gif@01D7CC24.73193600">=
<o:p></o:p></p><p class=3D"MsoNormal">Envoy=C3=A9 =C3=A0 partir de <a href=
=3D"https://emea01.safelinks.protection.outlook.com/?url=3Dhttps%3A%2F%2Fgo=
.microsoft.com%2Ffwlink%2F%3FLinkId%3D550986&amp;data=3D04%7C01%7C%7Cda65c5=
4128fc4075c00308d9bdf9d8f8%7C84df9e7fe9f640afb435aaaaaaaaaaaa%7C1%7C0%7C637=
749703041003417%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzI=
iLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000&amp;sdata=3DTxgpzPYIyXHNosxIi%2BGai%=
2F%2FT%2FLfHhiDtKdXCe9HTu5k%3D&amp;reserved=3D0" originalsrc=3D"https://go.=
microsoft.com/fwlink/?LinkId=3D550986" shash=3D"cadlQBHlcd+fMCL+zxxqWFRsw8f=
WsB2Pu20cRgv09+shMZe091U4feLL5u/90rFrw1p9eT8zM/HGDSmzb5BGBKaC65d2vX3MetnbbY=
cL2HOu99BSbPaLeLSLaxFmy1PrjZw/pFSBYspXmOomkCbvfcaV+IM2DxvIOZzpiLcjNNM=3D">C=
ourrier</a> pour Windows<o:p></o:p></p><p class=3D"MsoNormal"><o:p>&nbsp;</=
o:p></p></div></body></html>=
```

### De quoi se compose le code des éléments de l'EML

#### MIME-Version: 1.0 
>Multipurpose Internet Mail Extensions ( MIME ) est une norme Internet qui étend le format des messages électroniques pour prendre en charge le texte dans des jeux de caractères autres que ASCII , ainsi que les pièces jointes d'audio, de vidéo, d'images et de programmes d'application. Les corps de message peuvent être constitués de plusieurs parties et les informations d'en-tête peuvent être spécifiées dans des jeux de caractères non ASCII. Les e-mails au format MIME sont généralement transmis avec des protocoles standard, tels que le Simple Mail Transfer Protocol (SMTP), le Post Office Protocol (POP) et l' Internet Message Access Protocol (IMAP).

#### Date:
> il s'agit de la date de l'envoi du mail.

#### From:
> il s'agit du mail de l'éméteur.

#### Subject:
> il s'agit de l'objet du mail.

#### Message-ID: 
> il s'agit d'un id identification du mail.

#### To:
> il s'agit de l'adresse mail de personne qui reçoit le courriel

#### Content-Transfer-Encoding:
> Encodage du contenu pour le transfert (champ d'en-tête) \
>Indique selon quelle méthode le contenu de l'article est encodé, par exemple : \
- Base64
- Quoted-Printable
- 7bits
- 8bits

### Content-Type:
> Le Content-Type est un header ou en-tête renvoyé par le serveur au navigateur, par exemple, et qui sert à identifier le typ MIME du contenu qui est envoyé du serveur au client. Ainsi certaines applications comme AJAX, voient apparaître parfois des disfonctionnements si le Content-Type n'est pas correctement défini.
> Le Content-Type, peut également être utilisé pour définir le charset

### Le HTML:
> Oui, l'EML contient de l'html , HTML signifie "HyperText Markup Language". C’est un langage qui permet de composer des pages web. On parle de langage de balisage et non de langage de programmation, car le but du HTML est d’encadrer les différents éléments présents dans une page (images, titres, paragraphes ...) par des balises pour leur permettre d’être mis en forme secondairement (via une feuille de style) et pour leur donner du sens.\
> Notre mail contient de l'html qui est interprété par notre navigateur ou outil mailing.
> Exemple de code :
```html
<html xmlns:v=3D"urn:schemas-microsoft-com:vml" xmlns:o=3D"urn:schemas-micr=osoft-com:office:office"
    xmlns:w=3D"urn:schemas-microsoft-com:office:word"=xmlns:m=3D"http://schemas.microsoft.com/office/2004/12/omml"
    xmlns=3D"http:=//www.w3.org/TR/REC-html40">

<head>
    <meta http-equiv=3D"Content-Type" content=3D"text/html; charset=3Dutf-8">
    <m= eta name=3D"Generator" content=3D"Microsoft Word 15 (filtered medium)">
        <!--=
[if !mso]><style>v\:* {behavior:url(#default#VML);}
o\:* {behavior:url(#default#VML);}
w\:* {behavior:url(#default#VML);}
.shape {behavior:url(#default#VML);}
</style><![endif]-->
        <style>
            <!--
            /* Font Definitions */
            @font-face {
                font-family: "Cambria Math";
                panose-1: 2 4 5 3 5 4 6 3 2 4;
            }

            @font-face {
                font-family: Calibri;
                panose-1: 2 15 5 2 2 2 4 3 2 4;
            }

            /* Style Definitions */
            p.MsoNormal,
            li.MsoNormal,
            div.MsoNormal {
                margin: 0cm;
                font-size: 11.0pt;
                font-family: "Calibri", sans-serif;
            }

            a:link,
            span.MsoHyperlink {
                mso-style-priority: 99;
                color: blue;
                text-decoration: underline;
            }

            .MsoChpDefault {
                mso-style-type: export-only;
            }

            @page WordSection1 {
                size: 612.0pt 792.0pt;
                margin: 70.85pt 70.85pt 70.85pt 70.85pt;
            }

            div.WordSection1 {
                page: WordSection1;
            }
            -->
        </style>
</head>

<body lang=3D"FR-RE" link=3D"blue" vlink=3D"#954F72" styl=e=3D"word-wrap:break-word">
    <div class=3D"WordSection1">
        <p class=3D"MsoNorma=l">Hello world </p>
        <p class=3D"MsoNormal">
            <o:p>&nbsp;</o:p>
        </p>
        <p class=3D"=MsoNormal"><img width=3D"454" height=3D"227" style=3D"width:4.7291in;height=:2.3645in"
                id=3D"Image_x0020_2" src=3D"cid:image002.gif@01D7CC24.73193600">=
            <o:p></o:p>
        </p>
        <p class=3D"MsoNormal">Envoy=C3=A9 =C3=A0 partir de <a
                href==3D"https://emea01.safelinks.protection.outlook.com/?url=3Dhttps%3A%2F%2Fgo=.microsoft.com%2Ffwlink%2F%3FLinkId%3D550986&amp;data=3D04%7C01%7C%7Cda65c5=4128fc4075c00308d9bdf9d8f8%7C84df9e7fe9f640afb435aaaaaaaaaaaa%7C1%7C0%7C637=749703041003417%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzI=iLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000&amp;sdata=3DTxgpzPYIyXHNosxIi%2BGai%=2F%2FT%2FLfHhiDtKdXCe9HTu5k%3D&amp;reserved=3D0"
                originalsrc=3D"https://go.=microsoft.com/fwlink/?LinkId=3D550986"
                shash=3D"cadlQBHlcd+fMCL+zxxqWFRsw8f=WsB2Pu20cRgv09+shMZe091U4feLL5u/90rFrw1p9eT8zM/HGDSmzb5BGBKaC65d2vX3MetnbbY=cL2HOu99BSbPaLeLSLaxFmy1PrjZw/pFSBYspXmOomkCbvfcaV+IM2DxvIOZzpiLcjNNM=3D">C=
                ourrier</a> pour Windows<o:p></o:p>
        </p>
        <p class=3D"MsoNormal">
            <o:p>&nbsp;</= o:p>
        </p>
    </div>
</body>
</html>
```




