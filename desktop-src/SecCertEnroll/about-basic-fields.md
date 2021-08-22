---
description: Um certificado X.509 versão 1 contém os campos a seguir. Os campos da versão 2 são discutidos em Campos da Versão 2. Os campos da versão 3 são discutidos em Extensões da Versão 3.
ms.assetid: d614130c-cf1b-4580-8903-064982ed738e
title: Campos básicos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3dae9ceaa3ddd1c4ac8a8ce86425ec32eee45e82ca8b437ed0f0c27f44817ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118905081"
---
# <a name="basic-fields"></a>Campos básicos

Um certificado X.509 versão 1 contém os campos a seguir. Os campos da versão 2 são discutidos em [Campos da Versão 2.](about-version-2-fields.md) Os campos da versão 3 são discutidos em [Extensões da Versão 3.](about-version-3-extensions.md)

## <a name="version"></a>Versão

Especifica o número de versão do certificado codificado. Atualmente, os valores possíveis desse campo são 0, 1 ou 2, mas isso pode ser expandido no futuro.

``` syntax
---------------------------------------------------------------------
-- Version number. Currently, this can be 0, 1, or 2.
---------------------------------------------------------------------
CertificateVersion ::= INTEGER {v1(0), v2(1), v3(2)}
```

## <a name="serial-number"></a>Número de Série

Contém um inteiro positivo único atribuído pela AC (autoridade de certificação) para o certificado.

``` syntax
---------------------------------------------------------------------
-- Certificate serial number
---------------------------------------------------------------------
CertificateSerialNumber ::= INTEGER
```

## <a name="signature-algorithm"></a>Algoritmo de assinatura

Contém um [*OID (identificador de*](/windows/desktop/SecGloss/o-gly) objeto) que especifica o algoritmo usado pela AC para assinar o certificado. Por exemplo, 1.2.840.113549.1.1.5 especifica um algoritmo de hash SHA-1 combinado com o algoritmo de criptografia RSA da RSA Laboratories.

``` syntax
---------------------------------------------------------------------
-- Signature OID
---------------------------------------------------------------------
signature ::= AlgorithmIdentifier

AlgorithmIdentifier ::= SEQUENCE 
{
  algorithm           OBJECT IDENTIFIER,
  parameters          ANY OPTIONAL    
}
```

## <a name="issuer"></a>Emissor

Contém o DN (nome [*diferenciado) X.500*](/windows/desktop/SecGloss/x-gly) da AC que criou e assinou o certificado.

``` syntax
---------------------------------------------------------------------
-- Issuer name 
---------------------------------------------------------------------
Name ::= SEQUENCE OF RelativeDistinguishedName

RelativeDistinguishedName ::= SET OF AttributeTypeValue

AttributeTypeValue ::= SEQUENCE 
{
  type       OBJECT IDENTIFIER,
  value      ANY 
}
```

## <a name="validity"></a>Validade

Especifica o intervalo de tempo durante o qual o certificado é válido. As datas até o final de 2049 usam o formato Tempo Universal Coordenado (Greenwich Mean Time) (*aymmddhhmmssz*). Datas que começam em 1º de janeiro de 2050 usam o formato de hora generalizado (*aaaammddhhmmssz*).

``` syntax
---------------------------------------------------------------------
-- Validity period 
---------------------------------------------------------------------
Validity ::= SEQUENCE 
{
  notBefore           ChoiceOfTime,
  notAfter            ChoiceOfTime
}

ChoiceOfTime ::= CHOICE 
{
  utcTime                 UTCTime,
  generalTime             GeneralizedTime
}
```

## <a name="subject"></a>Assunto

Contém um nome diferenciado X.500 da entidade associada à chave pública contida no certificado.

``` syntax
---------------------------------------------------------------------
-- Subject name 
---------------------------------------------------------------------
Name ::= SEQUENCE OF RelativeDistinguishedName

RelativeDistinguishedName ::= SET OF AttributeTypeValue

AttributeTypeValue ::= SEQUENCE 
{
  type       OBJECT IDENTIFIER,
  value      ANY 
}
```

## <a name="public-key"></a>Chave pública

Contém a chave pública e as informações de algoritmo associadas.

``` syntax
---------------------------------------------------------------------
--  Subject public key information
---------------------------------------------------------------------
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
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Campos da versão 2](about-version-2-fields.md)
</dt> <dt>

[Extensões da versão 3](about-version-3-extensions.md)
</dt> <dt>

[Certificados de chave pública X.509](about-x-509-public-key-certificates.md)
</dt> </dl>

 

 
