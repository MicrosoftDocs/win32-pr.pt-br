---
description: Um tipo ASN.1 (Abstract Syntax Notation One) construído é feito de tipos básicos, tipos de cadeia de caracteres ou outros tipos construídos. Por exemplo, uma extensão de certificado X.509 é composta de três tipos BÁSICOSN.1, conforme mostrado no exemplo a seguir.
ms.assetid: 90c52d71-5d5b-479c-8e29-06c9f0f6da4a
title: Tipos construídos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85ed62c4a59bfc0944ad5e31673ab0ea9031c0175014c8fc1c6b6f2cc071b153
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118904485"
---
# <a name="constructed-types"></a>Tipos construídos

Um tipo ASN.1 [*(Abstract Syntax Notation One)*](/windows/desktop/SecGloss/a-gly) construído é feito de tipos básicos, tipos de cadeia de caracteres ou outros tipos construídos. Por exemplo, uma extensão de certificado X.509 é composta de três tipos BÁSICOSN.1, conforme mostrado no exemplo a seguir.

``` syntax
Extension ::= SEQUENCE 
{
   extnId              OBJECT IDENTIFIER,
   critical            BOOLEAN DEFAULT FALSE,
   extnValue           OCTET STRING
}
```

Uma extensão consiste em um OID [*(identificador*](/windows/desktop/SecGloss/o-gly) de objeto), um valor booliana que identifica se a extensão é crítica e uma matriz de byte que contém o valor. A API de Registro de Certificado dá suporte aos seguintes tipos ASN.1 construídos.

## <a name="sequence-and-sequence-of"></a>SEQUENCE e SEQUENCE OF

Marca de codificação: 0x30

Contém uma série ordenada de campos de um ou mais tipos. Os campos podem ser **marcados como OPCIONAL** **ou DEFAULT.** Além disso, para evitar ambiguidade ao decodificar, os campos opcionais sucessivos devem ser diferentes um do outro por meio de um identificador exclusivo (um inteiro entre colchetes como 1 ) e de um campo obrigatório a seguir, conforme mostrado pelo exemplo a \[ \] seguir.

``` syntax
SomeValue ::= SEQUENCE 
{
   a     INTEGER,
   b     [0] INTEGER OPTIONAL,
   c     [1] INTEGER DEFAULT 1,
   d     INTEGER
}
```

A diferença entre **SEQUENCE** e **SEQUENCE OF** é que os elementos de um constructo **SEQUENCE OF** devem ser do mesmo tipo. Veja o exemplo a seguir. Ambos os constructos têm o mesmo valor de marca (0x30) quando codificados.

``` syntax
PolicyQualifiers ::=  SEQUENCE OF PolicyQualifierInfo

PolicyQualifierInfo ::= SEQUENCE 
{
   policyQualifierId   OBJECT IDENTIFIER,
   qualifier           ANY OPTIONAL
}
```

Outra maneira de ver a diferença entre **SEQUENCE** e **SEQUENCE OF** é compará-los com seus equivalentes na linguagem de programação C. Ou seja, **SEQUENCE** é aproximadamente equivalente a uma estrutura e **SEQUENCE OF** é aproximadamente equivalente a uma matriz.

## <a name="set-and-set-of"></a>SET e SET OF

Marca de codificação: 0x31

Contém uma série nãoordenada de campos de um ou mais tipos. Isso é diferente de uma **SEQUENCE** que contém uma lista ordenada. Especificar uma lista não ordem permite que um aplicativo forneça os campos de estrutura para o codificador na ordem mais apropriada. Assim como com **SEQUENCE**, os campos de um constructo **SET** podem ser marcados com **OPTIONAL** ou **DEFAULT** e identificadores exclusivos devem ser usados para desambiguar o processo de decodificação. A diferença entre **SET** e **SET OF** é que os elementos de um constructo **SET OF** devem ser do mesmo tipo.

``` syntax
Name ::= SEQUENCE OF RelativeDistinguishedName

RelativeDistinguishedName ::= SET OF AttributeTypeValue

AttributeTypeValue ::= SEQUENCE 
{
   type       OBJECT IDENTIFIER,
   value      ANY 
}
```

## <a name="choice"></a>Escolha

Marca de codificação: não aplicável

Define uma opção entre alternativas. Cada alternativa deve ser identificada exclusivamente por um inteiro entre colchetes para evitar ambiguidade ao decodificar. Quando codificado, o **constructo CHOICE** terá o valor da marca de codificação da alternativa escolhida.

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

[Sistema de tipos ASN.1](about-asn-1-type-system.md)
</dt> <dt>

[Codificação DER de tipos ASN.1](about-der-encoding-of-asn-1-types.md)
</dt> <dt>

[Distinguished Encoding Rules](distinguished-encoding-rules.md)
</dt> </dl>

 

 
