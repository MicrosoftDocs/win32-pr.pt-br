---
description: Um dos usos mais comuns de cadeias de caracteres em uma PKI (infraestrutura de chave pública) é criar um Nome Diferenciado X.500.
ms.assetid: 01e8749b-a040-4267-bc12-f58f2c300337
title: Tipos de cadeia de caracteres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53b9e190e10bc86bd68a344f5aa279b4812bc04437418578320c36e0e1791dfd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118903685"
---
# <a name="string-types"></a>Tipos de cadeia de caracteres

Um dos usos mais comuns de cadeias de caracteres em uma PKI (infraestrutura de chave pública) é criar um Nome Diferenciado X.500. Por exemplo, o nome da assunto de uma solicitação de certificado é criado combinando uma sequência de nomes distintos relativos, conforme mostrado no exemplo de sintaxe a seguir.

``` syntax
---------------------------------------------------------------------
-- Breakdown of a subject name in a certificate request.
---------------------------------------------------------------------

CertificationRequestInfo ::= SEQUENCE 
{
   version                 CertificationRequestInfoVersion,
   subject                 Name,
   subjectPublicKeyInfo    SubjectPublicKeyInfo,
   attributes              [0] IMPLICIT Attributes
}

Name ::= SEQUENCE OF RelativeDistinguishedName

RelativeDistinguishedName ::= SET OF AttributeTypeValue

AttributeTypeValue ::= SEQUENCE 
{
   type       OBJECT IDENTIFIER,
   value      ANY 
}

DirectoryString ::= CHOICE 
{
   teletexString           TeletexString (SIZE (1..MAX)),
   printableString         PrintableString (SIZE (1..MAX)),
   universalString         UniversalString (SIZE (1..MAX)),
   utf8String              UTF8String (SIZE (1..MAX)),
   bmpString               BMPString (SIZE (1..MAX)) 
}
```

A API de Registro de Certificado dá suporte aos seguintes tipos de cadeia de caracteres ASN.1.

## <a name="bmpstring"></a>BMPString

Marca de codificação: 0x1E

Certreq.exe nome: CADEIA DE CARACTERES \_ UNICODE

O BMP (Plano Multilíngue Básico) é uma codificação de caracteres que abrange o primeiro plano do UCS (Conjunto de Caracteres Universal). Há planos de 0 a 16 numerados de 0 a 16. O BMP ocupa o plano 0 e inclui 65.536 pontos de código de 0x0000 a 0xFFFF. Esta é a seção do mapa de caracteres Unicode em que a maioria das atribuições de caracteres foi feita até o momento. Ele inclui latino, Oriente Médio, Asiático, África e outros idiomas.

## <a name="ia5string"></a>IA5String

Marca de codificação: 0x16

Certreq.exe nome: CADEIA DE CARACTERES IA5 \_

O IA5 (International Alphabet number 5) geralmente é equivalente ao alfabeto ASCII, mas versões diferentes podem incluir acentos ou outros caracteres específicos de um idioma regional. O exemplo a seguir mostra **o tipo IA5String** usado na definição ASN.1 da **extensão de certificado AlternativeNames.**

``` syntax
---------------------------------------------------------------------
-- AlternativeNames extension
---------------------------------------------------------------------

AltNames ::= SEQUENCE OF GeneralName

GeneralNames ::= AltNames

GeneralName ::= CHOICE 
{
   otherName               [0] IMPLICIT OtherName,
   rfc822Name              [1] IMPLICIT IA5String,
   dNSName                 [2] IMPLICIT IA5String,
   x400Address             [3] IMPLICIT SEQUENCE OF ANY, 
   directoryName           [4] EXPLICIT ANY,    
   ediPartyName            [5] IMPLICIT SEQUENCE OF ANY,
   uniformResourceLocator  [6] IMPLICIT IA5String,
   iPAddress               [7] IMPLICIT OCTET STRING,
   registeredID            [8] IMPLICIT OBJECT IDENTIFIER
}

OtherName ::= SEQUENCE 
{
   type                    OBJECT IDENTIFIER,
   value                   [0] EXPLICIT ANY 
}
```

## <a name="printablestring"></a>PrintableString

Marca de codificação: 0x13

Certreq.exe nome: PRINTABLE \_ STRING

O **tipo de dados PrintableString** foi originalmente destinado a representar os conjuntos de caracteres limitados disponíveis para terminais de entrada de mainframe, mas ele ainda é comumente usado. Ele contém os seguintes caracteres:

-   A a Z
-   a a z
-   0-9
-   ' ( ) + , - . / : = ? \[space\]

## <a name="teletexstring"></a>TeletexString

Marca de codificação: 0x14

O **TeletexString** e os tipos de dados **T61String** relacionados são codificados em 8 bits (ou 16 bits para caracteres compostos). Ambos têm um número de marca de 0x14. Eles não são amplamente usados.

## <a name="utf8string"></a>Utf8string

Marca de codificação: 0x0C

Certreq.exe nome: UTF8 \_ STRING

O formato de transformação UCS/Unicode de 8 bits (UTF-8) é uma codificação de caracteres de comprimento variável que pode representar qualquer caractere universal como um caractere Unicode, permitindo que os pontos de código iniciais permaneçam consistentes com ASCII. UTF-8 usa de um a quatro bytes. O número da marca é 0x0C.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sistema de tipos ASN.1](about-asn-1-type-system.md)
</dt> <dt>

[Distinguished Encoding Rules](distinguished-encoding-rules.md)
</dt> <dt>

[Codificação DER de tipos ASN.1](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 



