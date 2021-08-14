---
description: A API de registro de certificado dá suporte aos seguintes tipos ASN básicos. 1.
ms.assetid: ca247945-ebcf-492e-9cc8-a67a9454fa95
title: Tipos Básicos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16e2cc1b8825872789d095616e868fe39e306736583f8ea1784543808b7ec4d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118905041"
---
# <a name="basic-types"></a>Tipos Básicos

A API de registro de certificado dá suporte aos seguintes tipos ASN básicos. 1.

## <a name="bit-string"></a>CADEIA DE BITS

Marca de codificação: 0x03

Nome do Certreq.exe: \_ cadeia de caracteres de bits

Uma cadeia de caracteres de bits ou binária é uma matriz de bits demorada arbitrariamente. Bits específicos podem ser identificados por inteiros entre parênteses e nomes atribuídos como no exemplo a seguir.

``` syntax
Versions ::= BIT STRING{ version-1(0), version-2(1) } 
```

As assinaturas e as chaves de certificado geralmente são representadas como cadeias de bits.

``` syntax
---------------------------------------------------------------------
-- ASN.1 type example: BIT STRING
-- Tag number: 0x03
---------------------------------------------------------------------
SubjectPublicKeyInfo ::= SEQUENCE 
{
  algorithm           AlgorithmIdentifier,
  subjectPublicKey    BIT STRING
} 
```

## <a name="boolean"></a>BOOLEAN

Marca de codificação: 0x01

Nome do Certreq.exe: BOOLIANo

Um tipo booliano pode conter um dos dois valores, **true** ou **false**. O exemplo a seguir mostra a estrutura ASN. 1 para uma extensão de certificado de restrições básicas. O campo **CA** especifica se uma entidade de certificado é uma autoridade de certificação (CA). A criticalidade padrão é **false**.

``` syntax
---------------------------------------------------------------------
-- ASN.1 type example: BOOLEAN
-- Tag number: 0x01
---------------------------------------------------------------------
BasicConstraints ::= SEQUENCE 
{
  cA                  BOOLEAN DEFAULT FALSE,
  pathLenConstraint   INTEGER OPTIONAL
}
```

## <a name="integer"></a>INTEGER

Marca de codificação: 0x02

Nome do Certreq.exe: inteiro

Um inteiro normalmente pode ser qualquer valor integral positivo ou negativo. O exemplo a seguir mostra a estrutura ASN. 1 para uma chave pública RSA. Observe que o campo **publicExponent** é restrito a um inteiro positivo inferior a 4.294.967.296.

``` syntax
---------------------------------------------------------------------
-- ASN.1 type example: INTEGER
-- Tag number: 0x02
---------------------------------------------------------------------
HUGEINTEGER ::= INTEGER

RSAPublicKey ::= SEQUENCE 
{ 
  modulus         HUGEINTEGER,    
  publicExponent  INTEGER (0..4294967295) 
} 
```

## <a name="null"></a>NULO

Marca de codificação: 0x05

Nome do Certreq.exe: **nulo**

Um tipo **nulo** contém um único byte 0x00. Ele pode ser usado em qualquer lugar que a solicitação de certificado deva indicar um valor vazio. Por exemplo, um **AlgorithmIdentifier** é uma sequência que contém um OID (identificador de objeto) e parâmetros opcionais.

``` syntax
---------------------------------------------------------------------
-- ASN.1 type example: NULL
-- Tag number: 0x05
---------------------------------------------------------------------
AlgorithmIdentifier ::= SEQUENCE 
{
  algorithm           OBJECT IDENTIFIER,
  parameters          ANY OPTIONAL    
}
```

Se não houver parâmetros quando a estrutura for codificada, **NULL** será usado para indicar um valor vazio.

``` syntax
30 0d            ; SEQUENCE (d Bytes)
|  |  |  06 09          ; OBJECT_ID (9 Bytes)
|  |  |  |  2a 86 48 86 f7 0d 01 01  01
|  |  |  |     ; 1.2.840.113549.1.1.1 RSA (RSA_SIGN)
|  |  |  05 00          ; NULL (0 Bytes)
```

## <a name="object-identifier"></a>IDENTIFICADOR DE OBJETO

Marca de codificação: 0x06

Nome do Certreq.exe: \_ ID do objeto

A API de registro de certificado usa OIDs (identificadores de objeto) como um tipo de ponteiro universal para identificadores de algoritmo, atributos e outros elementos PKI. Os OIDs normalmente são apresentados em uma cadeia de caracteres decimais pontilhada, como "2.16.840.1.101.3.4.1.42". Os elementos individuais na cadeia de caracteres, separados por pontos, representam os arcos e folhas em uma árvore de autoridade de registro que identifica exclusivamente o objeto e a organização que o registrou. Por exemplo, o OID anterior pode ser expandido para junta-ISO-ITU-t (2) país (16) US (840) Organization (1) gov (101) Csor (3) nistAlgorithms (4) aesAlgs (1) com. 42 acrescentado para identificar exclusivamente o algoritmo do modo CBC (encadeamento de blocos de criptografia) do AES de 256 bits.

``` syntax
---------------------------------------------------------------------
-- ASN.1 type example: OBJECT IDENTIFIER
-- Tag number: 0x06
---------------------------------------------------------------------
AlgorithmIdentifier ::= SEQUENCE 
{
  algorithm           OBJECT IDENTIFIER,
  parameters          ANY OPTIONAL    
}
```

## <a name="octet-string"></a>CADEIA DE CARACTERES DE OCTETO

Marca de codificação: 0x04

Nome do Certreq.exe: \_ cadeia de caracteres de octeto

Uma cadeia de caracteres de octeto é uma matriz de bytes grandes arbitrariamente. Ao contrário do tipo de **cadeia de caracteres bit** , no entanto, bits específicos e bytes na cadeia de caracteres não podem receber nomes. A palavra octeto deve ser uma maneira independente de plataforma de se referir a uma palavra de memória. No contexto da API de registro de certificado, o octeto e o byte são intercambiáveis.

``` syntax
---------------------------------------------------------------------
-- ASN.1 type example: OCTET STRING
-- Tag number: 0x04
---------------------------------------------------------------------
AuthorityKeyId ::= SEQUENCE 
{
  keyIdentifier       [0] IMPLICIT OCTET STRING OPTIONAL,
  certIssuer          [1] EXPLICIT NAME
  certSerialNumber    [2] IMPLICIT INTEGER OPTIONAL
}
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sistema de tipo ASN. 1](about-asn-1-type-system.md)
</dt> <dt>

[Distinguished Encoding Rules](distinguished-encoding-rules.md)
</dt> <dt>

[Codificação DER dos tipos ASN. 1](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 



