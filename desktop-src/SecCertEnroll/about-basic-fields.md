---
description: Um certificado X. 509 versão 1 contém os campos a seguir. Os campos da versão 2 são discutidos nos campos da versão 2. Os campos da versão 3 são discutidos nas extensões da versão 3.
ms.assetid: d614130c-cf1b-4580-8903-064982ed738e
title: Campos básicos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad24afa21787227b3fe47ab187a97c7886c9c9ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828348"
---
# <a name="basic-fields"></a><span data-ttu-id="ab98a-105">Campos básicos</span><span class="sxs-lookup"><span data-stu-id="ab98a-105">Basic Fields</span></span>

<span data-ttu-id="ab98a-106">Um certificado X. 509 versão 1 contém os campos a seguir.</span><span class="sxs-lookup"><span data-stu-id="ab98a-106">An X.509 version 1 certificate contains the following fields.</span></span> <span data-ttu-id="ab98a-107">Os campos da versão 2 são discutidos nos [campos da versão 2](about-version-2-fields.md).</span><span class="sxs-lookup"><span data-stu-id="ab98a-107">Version 2 fields are discussed in [Version 2 Fields](about-version-2-fields.md).</span></span> <span data-ttu-id="ab98a-108">Os campos da versão 3 são discutidos nas [extensões da versão 3](about-version-3-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="ab98a-108">Version 3 fields are discussed in [Version 3 Extensions](about-version-3-extensions.md).</span></span>

## <a name="version"></a><span data-ttu-id="ab98a-109">Versão</span><span class="sxs-lookup"><span data-stu-id="ab98a-109">Version</span></span>

<span data-ttu-id="ab98a-110">Especifica o número de versão do certificado codificado.</span><span class="sxs-lookup"><span data-stu-id="ab98a-110">Specifies the version number of the encoded certificate.</span></span> <span data-ttu-id="ab98a-111">Atualmente, os valores possíveis desse campo são 0, 1 ou 2, mas isso pode ser expandido no futuro.</span><span class="sxs-lookup"><span data-stu-id="ab98a-111">Currently, the possible values of this field are 0, 1, or 2, but this may be expanded in the future.</span></span>

``` syntax
---------------------------------------------------------------------
-- Version number. Currently, this can be 0, 1, or 2.
---------------------------------------------------------------------
CertificateVersion ::= INTEGER {v1(0), v2(1), v3(2)}
```

## <a name="serial-number"></a><span data-ttu-id="ab98a-112">Número de Série</span><span class="sxs-lookup"><span data-stu-id="ab98a-112">Serial Number</span></span>

<span data-ttu-id="ab98a-113">Contém um inteiro positivo único atribuído pela AC (autoridade de certificação) para o certificado.</span><span class="sxs-lookup"><span data-stu-id="ab98a-113">Contains a positive, unique integer assigned by the certification authority (CA) to the certificate.</span></span>

``` syntax
---------------------------------------------------------------------
-- Certificate serial number
---------------------------------------------------------------------
CertificateSerialNumber ::= INTEGER
```

## <a name="signature-algorithm"></a><span data-ttu-id="ab98a-114">Algoritmo de assinatura</span><span class="sxs-lookup"><span data-stu-id="ab98a-114">Signature Algorithm</span></span>

<span data-ttu-id="ab98a-115">Contém um OID ( [*identificador de objeto*](/windows/desktop/SecGloss/o-gly) ) que especifica o algoritmo usado pela autoridade de certificação para assinar o certificado.</span><span class="sxs-lookup"><span data-stu-id="ab98a-115">Contains an [*object identifier*](/windows/desktop/SecGloss/o-gly) (OID) that specifies the algorithm used by the CA to sign the certificate.</span></span> <span data-ttu-id="ab98a-116">Por exemplo, 1.2.840.113549.1.1.5 especifica um algoritmo de hash SHA-1 combinado com o algoritmo de criptografia RSA da RSA Laboratories.</span><span class="sxs-lookup"><span data-stu-id="ab98a-116">For example, 1.2.840.113549.1.1.5 specifies a SHA-1 hashing algorithm combined with the RSA encryption algorithm from RSA Laboratories.</span></span>

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

## <a name="issuer"></a><span data-ttu-id="ab98a-117">Emissor</span><span class="sxs-lookup"><span data-stu-id="ab98a-117">Issuer</span></span>

<span data-ttu-id="ab98a-118">Contém o DN (nome distinto) [*X. 500*](/windows/desktop/SecGloss/x-gly) da autoridade de certificação que criou e assinou o certificado.</span><span class="sxs-lookup"><span data-stu-id="ab98a-118">Contains the [*X.500*](/windows/desktop/SecGloss/x-gly) distinguished name (DN) of the CA that created and signed the certificate.</span></span>

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

## <a name="validity"></a><span data-ttu-id="ab98a-119">Validade</span><span class="sxs-lookup"><span data-stu-id="ab98a-119">Validity</span></span>

<span data-ttu-id="ab98a-120">Especifica o intervalo de tempo durante o qual o certificado é válido.</span><span class="sxs-lookup"><span data-stu-id="ab98a-120">Specifies the time interval during which the certificate is valid.</span></span> <span data-ttu-id="ab98a-121">As datas no final de 2049 usam o formato de tempo universal coordenado (Greenwich Mean Time) (*yymmddhhmmssZ*).</span><span class="sxs-lookup"><span data-stu-id="ab98a-121">Dates through the end of 2049 use the Coordinated Universal Time (Greenwich Mean Time) format (*yymmddhhmmssz*).</span></span> <span data-ttu-id="ab98a-122">As datas que começam com 1º de janeiro de 2050 usam o formato de tempo generalizado (*yyyymmddhhmmssZ*).</span><span class="sxs-lookup"><span data-stu-id="ab98a-122">Dates beginning with January 1st, 2050 use the generalized time format (*yyyymmddhhmmssz*).</span></span>

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

## <a name="subject"></a><span data-ttu-id="ab98a-123">Assunto</span><span class="sxs-lookup"><span data-stu-id="ab98a-123">Subject</span></span>

<span data-ttu-id="ab98a-124">Contém um nome diferenciado X.500 da entidade associada à chave pública contida no certificado.</span><span class="sxs-lookup"><span data-stu-id="ab98a-124">Contains an X.500 distinguished name of the entity associated with the public key contained in the certificate.</span></span>

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

## <a name="public-key"></a><span data-ttu-id="ab98a-125">Chave pública</span><span class="sxs-lookup"><span data-stu-id="ab98a-125">Public Key</span></span>

<span data-ttu-id="ab98a-126">Contém a chave pública e as informações de algoritmo associadas.</span><span class="sxs-lookup"><span data-stu-id="ab98a-126">Contains the public key and associated algorithm information.</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="ab98a-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ab98a-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ab98a-128">Campos da versão 2</span><span class="sxs-lookup"><span data-stu-id="ab98a-128">Version 2 Fields</span></span>](about-version-2-fields.md)
</dt> <dt>

[<span data-ttu-id="ab98a-129">Extensões da versão 3</span><span class="sxs-lookup"><span data-stu-id="ab98a-129">Version 3 Extensions</span></span>](about-version-3-extensions.md)
</dt> <dt>

[<span data-ttu-id="ab98a-130">Certificados de chave pública X. 509</span><span class="sxs-lookup"><span data-stu-id="ab98a-130">X.509 Public Key Certificates</span></span>](about-x-509-public-key-certificates.md)
</dt> </dl>

 

 
