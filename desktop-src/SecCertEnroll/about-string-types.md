---
description: Um dos usos mais comuns de cadeias de caracteres em uma PKI (infraestrutura de chave pública) é criar um nome diferenciado X. 500.
ms.assetid: 01e8749b-a040-4267-bc12-f58f2c300337
title: Tipos de cadeia de caracteres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1173de3b2c4c5fd64181cd19c69cfbcecb1d584
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169488"
---
# <a name="string-types"></a>Tipos de cadeia de caracteres

Um dos usos mais comuns de cadeias de caracteres em uma PKI (infraestrutura de chave pública) é criar um nome diferenciado X. 500. Por exemplo, o nome da entidade de uma solicitação de certificado é criado pela combinação de uma sequência de nomes distintos relativos, conforme mostrado no exemplo de sintaxe a seguir.

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

A API de registro de certificado dá suporte aos seguintes tipos de cadeia de caracteres ASN. 1.

## <a name="bmpstring"></a>BMPString

Marca de codificação: 0x1E

Nome do Certreq.exe: \_ cadeia de caracteres Unicode

O BMP (plano multilíngüe básico) é uma codificação de caracteres que abrange o primeiro plano do conjunto de caracteres universal (UCS). Há planos dezessete numerados de 0 a 16. O BMP ocupa o plano 0 e inclui 65.536 pontos de código de 0x0000 a 0xFFFF. Esta é a seção do mapa de caracteres Unicode em que a maioria das atribuições de caracteres foram feitas até o momento. Ele inclui latim, Oriente Médio, asiático, africana e outras linguagens.

## <a name="ia5string"></a>IA5String

Marca de codificação: 0x16

Nome do Certreq.exe: \_ cadeia de caracteres IA5

O alfabeto internacional número 5 (IA5) geralmente é equivalente ao alfabeto ASCII, mas versões diferentes podem incluir acentos ou outros caracteres específicos de um idioma regional. O exemplo a seguir mostra o tipo **IA5String** usado na definição de ASN. 1 da extensão de certificado **alternativonames** .

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

## <a name="printablestring"></a>Imenablestring

Marca de codificação: 0x13

Nome do Certreq.exe: cadeia de caracteres IMPRIMÍvel \_

O tipo de dados **imenablestring** foi originalmente destinado a representar os conjuntos de caracteres limitados disponíveis para terminais de entrada de mainframe, mas ele ainda é normalmente usado. Ele contém os seguintes caracteres:

-   A-Z
-   a-z
-   0-9
-   ' ( ) + , - . / : = ? \[space\]

## <a name="teletexstring"></a>TeletexString

Marca de codificação: 0x14

O **TeletexString** e os tipos de dados **T61String** relacionados são codificados em 8 bits (ou 16 bits para caracteres compostos). Ambos têm um número de marca de 0x14. Eles não são amplamente usados.

## <a name="utf8string"></a>UTF8String

Marca de codificação: 0x0C

Nome do Certreq.exe: \_ cadeia de caracteres UTF8

O formato de transformação UCS/Unicode de 8 bits (UTF-8) é uma codificação de caracteres de comprimento variável que pode representar qualquer caractere universal como caractere Unicode, permitindo que os pontos de código iniciais permaneçam consistentes com o ASCII. O UTF-8 usa um a quatro bytes. O número de marca é 0x0C.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sistema de tipo ASN. 1](about-asn-1-type-system.md)
</dt> <dt>

[Distinguished Encoding Rules](distinguished-encoding-rules.md)
</dt> <dt>

[Codificação DER dos tipos ASN. 1](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 



