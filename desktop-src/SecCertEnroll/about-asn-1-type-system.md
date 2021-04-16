---
description: O conceito de um tipo de dados é fundamental para o padrão ASN de notação de sintaxe abstrata (Authorized. 1).
ms.assetid: 85e88e0b-057b-42c7-a3c8-017a30195d1e
title: Sistema de tipo ASN. 1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abbf60bf61e32c5fca882f2e40c946c043ef93e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105750764"
---
# <a name="asn1-type-system"></a>Sistema de tipo ASN. 1

O conceito de um tipo de dados é fundamental para o padrão ASN de notação de sintaxe abstrata (Authorized. 1). Cada campo de uma estrutura de solicitação de certificado é associado a um tipo. Considere, por exemplo, a \# sintaxe de certificado PKCS 10 ASN. 1 mostrada no exemplo a seguir.

``` syntax
--------------------------------------------------------------------
-- PKCS #10 Certificate request.
--------------------------------------------------------------------
CertificationRequestInfo ::= SEQUENCE 
{
   version                 CertificationRequestInfoVersion,
   subject                 Name,
   subjectPublicKeyInfo    SubjectPublicKeyInfo,
   attributes              [0] IMPLICIT Attributes
}

--------------------------------------------------------------------
-- Version number.
--------------------------------------------------------------------
CertificationRequestInfoVersion ::= INTEGER

--------------------------------------------------------------------
-- Subject distinguished name (DN).
--------------------------------------------------------------------
Name ::= SEQUENCE OF RelativeDistinguishedName

RelativeDistinguishedName ::= SET OF AttributeTypeValue

AttributeTypeValue ::= SEQUENCE 
{
   type               OBJECT IDENTIFIER,
   value              ANY 
}

--------------------------------------------------------------------
-- Public key information.
--------------------------------------------------------------------
SubjectPublicKeyInfo ::= SEQUENCE 
{
   algorithm           AlgorithmIdentifier,
   subjectPublicKey    BITSTRING
}

AlgorithmIdentifier ::= SEQUENCE 
{
  algorithm           OBJECT IDENTIFIER,
  parameters          ANY OPTIONAL    
} 

--------------------------------------------------------------------
-- Attributes.
--------------------------------------------------------------------
Attributes ::= SET OF Attribute

Attribute ::= SEQUENCE 
{
   type               OBJECT IDENTIFIER,
   values             AttributeSetValue
}

AttributeSetValue ::= SET OF ANY
```

A estrutura de solicitação de alto nível, **CertificationRequestInfo**, é um tipo que é composto de uma sequência de outros tipos. Quando um tipo é ou contém apenas tipos básicos, tipos de cadeia de caracteres ou **qualquer** um, ele não pode ser dividido ainda mais. Por exemplo, o campo **versão** é um tipo **CertificationRequestInfoVersion** que, por sua vez, é um tipo **inteiro** , um tipo ASN básico. 1 que não é composto de outros tipos.

Um sistema de tipos permite que a sintaxe de uma solicitação seja apresentada visualmente de maneira imediatamente compreendida pelos desenvolvedores e permite que a solicitação seja codificada consistentemente para transmissão em uma rede. Para obter mais informações sobre codificação, consulte [Distinguished Encoding Rules](distinguished-encoding-rules.md). Para obter mais informações sobre os tipos ASN. 1, consulte os tópicos a seguir.

[Tipos Básicos](about-basic-types.md)

Discute os seguintes tipos de dados:

* **CADEIA DE BITS**
* **BOOLEAN**
* **INTEGER**
* **NULL**
* **IDENTIFICADOR DE OBJETO**
* **CADEIA DE CARACTERES DE OCTETO**

[Tipos de cadeia de caracteres](about-string-types.md)

Discute os seguintes tipos de cadeia de caracteres:

* **BMPString**
* **IA5String**
* **Imenablestring**
* **TeletexString**
* **UTF8String**

[Tipos construídos](about-constructed-types.md)

Discute os tipos de dados ASN. 1 que podem conter tipos básicos, tipos de cadeia de caracteres ou outros tipos construídos.




 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Codificação de solicitação de certificado](about-certificate-request-encoding.md)
</dt> <dt>

[Codificação DER dos tipos ASN. 1](about-der-encoding-of-asn-1-types.md)
</dt> <dt>

[Distinguished Encoding Rules](distinguished-encoding-rules.md)
</dt> <dt>

[Introdução à sintaxe e codificação ASN. 1](about-introduction-to-asn-1-syntax-and-encoding.md)
</dt> </dl>

 

 



