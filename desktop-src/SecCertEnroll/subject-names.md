---
description: O campo assunto de uma \# solicitação de certificado PKCS 10 contém o nome distinto da entidade que solicita o certificado.
ms.assetid: 6c35ce42-07be-4d47-a14e-ed5a361dbe33
title: Nomes de Entidades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6be70af23c524e71c1a9b22f43e391e4f5c8302fba70f24fba1f8268ebfda6e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101096"
---
# <a name="subject-names"></a>Nomes de Entidades

O campo **assunto** de uma \# solicitação de certificado PKCS 10 contém o nome distinto da entidade que solicita o certificado.

``` syntax
CertificationRequestInfo ::= SEQUENCE 
{
   version                 CertificationRequestInfoVersion,
   subject                 Name,
   subjectPublicKeyInfo    SubjectPublicKeyInfo,
   attributes              [0] IMPLICIT Attributes
}
```

O nome distinto consiste em uma sequência de nomes distintos relativos (RDNs). Cada RDN consiste em um conjunto de atributos, e cada atributo consiste em um identificador de objeto e um valor. O tipo de dados do valor é identificado pela estrutura **directorystring** .

``` syntax
Name ::= SEQUENCE OF RelativeDistinguishedName

RelativeDistinguishedName ::= SET OF AttributeTypeValue

AttributeTypeValue ::= SEQUENCE 
{
   type       EncodedObjectID,
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

Para obter mais informações, consulte estes tópicos:

-   [Criando um nome de entidade](creating-a-subject-name.md)
-   [Codificando um nome de entidade](encoding-a-subject-name.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Solicitações](/windows/desktop/SecCrypto/requests)
</dt> </dl>

 

 
