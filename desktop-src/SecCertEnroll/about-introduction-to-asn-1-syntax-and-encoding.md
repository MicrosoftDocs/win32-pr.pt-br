---
description: A API de registro de certificado usa uma ASN. 1 para definir, codificar e decodificar as solicitações de certificado e os certificados que ele transfere entre computadores cliente e autoridades de certificação.
ms.assetid: 970a246f-a4c3-489b-b6a4-7d3103f388cf
title: Introdução à sintaxe e codificação ASN. 1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 504f6e643d91951351eaef2c51f9cfeac01919c77718a88ce866670f22803146
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118904225"
---
# <a name="introduction-to-asn1-syntax-and-encoding"></a>Introdução à sintaxe e codificação ASN. 1

A API de registro de certificado usa uma ASN. 1 para definir, codificar e decodificar as solicitações de certificado e os certificados que ele transfere entre computadores cliente e autoridades de certificação. O ASN. 1 pode ser dividido conceitualmente em um conjunto de regras de sintaxe e um conjunto de regras de codificação, conforme mostrado nos exemplos a seguir.

## <a name="asn1-syntax-example"></a>Exemplo de sintaxe ASN. 1

Uma solicitação de certificado contém, entre outras coisas, o nome da entidade que está fazendo a solicitação ou para a qual a solicitação está sendo feita. O nome é uma sequência de RDNs (nomes distintos relativos de X. 500). Cada RDN na sequência consiste em um OID (identificador de objeto) e um valor. A sintaxe ASN. 1 para um nome de entidade é mostrada no exemplo a seguir.

``` syntax
---------------------------------------------------------------------
-- Subject name
---------------------------------------------------------------------
Name ::= SEQUENCE OF RelativeDistinguishedName

RelativeDistinguishedName ::= SET OF AttributeTypeValue

AttributeTypeValue ::= SEQUENCE 
{
   type               OBJECT IDENTIFIER,
   value              ANY 
}
```

## <a name="asn1-encoding-example"></a>Exemplo de codificação ASN. 1

a API de registro de certificado usa [*Distinguished Encoding Rules*](/windows/desktop/SecGloss/d-gly) (DER) para codificar o nome da entidade anterior. O DER requer que cada item no nome seja representado por um TLV terceto, onde T contém o número de marca do tipo ASN. 1, L contém o comprimento e V contém o valor associado. O exemplo a seguir mostra como o nome da entidade TestCN. TestOrg é codificado.

``` syntax
1.     30 23            ; SEQUENCE (23 Bytes)
2.     |  |  31 0f            ; SET (f Bytes)
3.     |  |  |  30 0d            ; SEQUENCE (d Bytes)
4.     |  |  |     06 03         ; OBJECT_ID (3 Bytes)
5.     |  |  |     |  55 04 03
6.     |  |  |     |     ; 2.5.4.3 Common Name (CN)
7.     |  |  |     13 06         ; PRINTABLE_STRING (6 Bytes)
8.     |  |  |        54 65 73 74 43 4e                    ; TestCN
9.     |  |  |           ; "TestCN"
10.    |  |  31 10            ; SET (10 Bytes)
11.    |  |     30 0e            ; SEQUENCE (e Bytes)
12.    |  |        06 03         ; OBJECT_ID (3 Bytes)
13.    |  |        |  55 04 0a
14.    |  |        |     ; 2.5.4.10 Organization (O)
15.    |  |        13 07         ; PRINTABLE_STRING (7 Bytes)
16.    |  |           54 65 73 74 4f 72 67                 ; TestOrg
17.    |  |              ; "TestOrg"
```

Observe os seguintes pontos:

-   Linha 1:<dl> O nome é uma sequência de nomes distintos relativos.  
    O número de marca para o tipo de **sequência** é 0x30.  
    O nome da entidade de TestCN. TestOrg requer 35 (0x23) bytes.  
    </dl>
-   Line 2:<dl> O nome comum, TestCN, é um conjunto único de estruturas **attributetypevalue** .  
    O número de marca de um **conjunto** é 0x31.  
    </dl>
-   Linha 3:<dl> A estrutura **attributetypevalue** é uma sequência.  
    O número de marca para o tipo de **sequência** é 0x30.  
    A estrutura requer 13 (0xD) bytes.  
    </dl>
-   Linhas 4 a 6:<dl> O identificador de objeto (OID) para o nome comum é 2.5.4.3.  
    O OID é um tipo de **\_ ID de objeto** de três bytes.  
    O número de marca para o tipo de **\_ ID de objeto** é 0x06.  
    </dl>
-   Linhas 7 a 9:<dl> O nome comum, TestCN, é um valor de cadeia de caracteres.  
    A cadeia de caracteres é um tipo de **\_ cadeia de caracteres imprimível** de seis bytes.  
    O número de marca para o tipo de **\_ cadeia de caracteres imprimível** é 0x13.  
    </dl>

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sistema de tipo ASN. 1](about-asn-1-type-system.md)
</dt> <dt>

[Codificação de solicitação de certificado](about-certificate-request-encoding.md)
</dt> <dt>

[Codificação DER dos tipos ASN. 1](about-der-encoding-of-asn-1-types.md)
</dt> <dt>

[Distinguished Encoding Rules](distinguished-encoding-rules.md)
</dt> </dl>

 

 
