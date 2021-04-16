---
description: Um tipo ASN criado de notação de sintaxe abstrata (Authorized. 1) é composto de tipos básicos, tipos de cadeia de caracteres ou outros tipos construídos. Por exemplo, uma extensão de certificado X. 509 é composta de três tipos ASN básicos. 1, conforme mostrado pelo exemplo a seguir.
ms.assetid: 90c52d71-5d5b-479c-8e29-06c9f0f6da4a
title: Tipos construídos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a515e6e03ebf3c95ff1cabc1bf7f12eb423df27d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105758284"
---
# <a name="constructed-types"></a>Tipos construídos

Um tipo ASN criado de [*notação de sintaxe abstrata*](/windows/desktop/SecGloss/a-gly) (Authorized. 1) é composto de tipos básicos, tipos de cadeia de caracteres ou outros tipos construídos. Por exemplo, uma extensão de certificado X. 509 é composta de três tipos ASN básicos. 1, conforme mostrado pelo exemplo a seguir.

``` syntax
Extension ::= SEQUENCE 
{
   extnId              OBJECT IDENTIFIER,
   critical            BOOLEAN DEFAULT FALSE,
   extnValue           OCTET STRING
}
```

Uma extensão consiste em um OID ( [*identificador de objeto*](/windows/desktop/SecGloss/o-gly) ), um valor booliano que identifica se a extensão é crítica e uma matriz de bytes que contém o valor. A API de registro de certificado dá suporte aos tipos ASN. 1 construídos a seguir.

## <a name="sequence-and-sequence-of"></a>SEQUÊNCIA e sequência de

Marca de codificação: 0x30

Contém uma série ordenada de campos de um ou mais tipos. Os campos podem ser marcados como **opcional** ou **padrão**. Além disso, para evitar ambigüidade ao decodificar, os campos opcionais sucessivos devem diferir uns dos outros por meio de um identificador exclusivo (um inteiro entre colchetes, como \[ 1 \] ) e do campo obrigatório a seguir, conforme mostrado pelo exemplo a seguir.

``` syntax
SomeValue ::= SEQUENCE 
{
   a     INTEGER,
   b     [0] INTEGER OPTIONAL,
   c     [1] INTEGER DEFAULT 1,
   d     INTEGER
}
```

A diferença entre **sequência** e **sequência de** é que os elementos de uma **sequência de** construção devem ser do mesmo tipo. Veja o exemplo a seguir. Ambos os constructos têm o mesmo valor de marca (0x30) quando codificados.

``` syntax
PolicyQualifiers ::=  SEQUENCE OF PolicyQualifierInfo

PolicyQualifierInfo ::= SEQUENCE 
{
   policyQualifierId   OBJECT IDENTIFIER,
   qualifier           ANY OPTIONAL
}
```

Outra maneira de examinar a diferença entre **sequência** e **sequência de** é compará-los com suas contrapartes na linguagem de programação C. Ou seja, **Sequence** é aproximadamente equivalente a uma estrutura e a **sequência de** é aproximadamente equivalente a uma matriz.

## <a name="set-and-set-of"></a>CONJUNTO e conjunto de

Marca de codificação: 0x31

Contém uma série não ordenada de campos de um ou mais tipos. Isso é diferente de uma **sequência** que contém uma lista ordenada. A especificação de uma lista não ordenada permite que um aplicativo forneça os campos de estrutura para o codificador na ordem mais apropriada. Como with **Sequence**, os campos de uma construção **set** podem ser marcados com **optional** ou **Default**, e os identificadores exclusivos devem ser usados para eliminar a ambiguidade do processo de decodificação. A diferença entre **set** e **set de** é que os elementos de um **conjunto de** construção devem ser do mesmo tipo.

``` syntax
Name ::= SEQUENCE OF RelativeDistinguishedName

RelativeDistinguishedName ::= SET OF AttributeTypeValue

AttributeTypeValue ::= SEQUENCE 
{
   type       OBJECT IDENTIFIER,
   value      ANY 
}
```

## <a name="choice"></a>DESEJADA

Marca de codificação: não aplicável

Define uma escolha entre alternativas. Cada alternativa deve ser identificada exclusivamente por um inteiro entre colchetes para evitar ambigüidade ao decodificar. Quando codificada, a construção **Choice** terá o valor da marca de codificação da alternativa escolhida.

``` syntax
AltNames ::= SEQUENCE OF GeneralName

GeneralNames ::= AltNames

GeneralName ::= CHOICE 
{
   otherName               [0] IMPLICIT OtherName,
   rfc822Name              [1] IMPLICIT IA5String,
   dNSName                 [2] IMPLICIT IA5String,
   x400Address             [3] IMPLICIT SeqOfAny,
   directoryName           [4] EXPLICIT Name,
   ediPartyName            [5] IMPLICIT SEQUENCE OF ANY,
   uniformResourceLocator  [6] IMPLICIT IA5String,
   iPAddress               [7] IMPLICIT OCTET STRING,
   registeredID            [8] IMPLICIT OBJECT IDENTIFIER
}
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sistema de tipo ASN. 1](about-asn-1-type-system.md)
</dt> <dt>

[Codificação DER dos tipos ASN. 1](about-der-encoding-of-asn-1-types.md)
</dt> <dt>

[Distinguished Encoding Rules](distinguished-encoding-rules.md)
</dt> </dl>

 

 
