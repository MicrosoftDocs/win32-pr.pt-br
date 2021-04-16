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
# <a name="asn1-type-system"></a><span data-ttu-id="20e76-103">Sistema de tipo ASN. 1</span><span class="sxs-lookup"><span data-stu-id="20e76-103">ASN.1 Type System</span></span>

<span data-ttu-id="20e76-104">O conceito de um tipo de dados é fundamental para o padrão ASN de notação de sintaxe abstrata (Authorized. 1).</span><span class="sxs-lookup"><span data-stu-id="20e76-104">The concept of a data type is fundamental to the Abstract Syntax Notation One (ASN.1) standard.</span></span> <span data-ttu-id="20e76-105">Cada campo de uma estrutura de solicitação de certificado é associado a um tipo.</span><span class="sxs-lookup"><span data-stu-id="20e76-105">Every field of a certificate request structure is associated with a type.</span></span> <span data-ttu-id="20e76-106">Considere, por exemplo, a \# sintaxe de certificado PKCS 10 ASN. 1 mostrada no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="20e76-106">Consider, for example, the PKCS \#10 ASN.1 certificate syntax shown in the following example.</span></span>

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

<span data-ttu-id="20e76-107">A estrutura de solicitação de alto nível, **CertificationRequestInfo**, é um tipo que é composto de uma sequência de outros tipos.</span><span class="sxs-lookup"><span data-stu-id="20e76-107">The high-level request structure, **CertificationRequestInfo**, is a type that is made up from a sequence of other types.</span></span> <span data-ttu-id="20e76-108">Quando um tipo é ou contém apenas tipos básicos, tipos de cadeia de caracteres ou **qualquer** um, ele não pode ser dividido ainda mais.</span><span class="sxs-lookup"><span data-stu-id="20e76-108">When a type is or contains only basic types, string types, or **ANY**, it cannot be broken down further.</span></span> <span data-ttu-id="20e76-109">Por exemplo, o campo **versão** é um tipo **CertificationRequestInfoVersion** que, por sua vez, é um tipo **inteiro** , um tipo ASN básico. 1 que não é composto de outros tipos.</span><span class="sxs-lookup"><span data-stu-id="20e76-109">For example, the **version** field is a **CertificationRequestInfoVersion** type which is, in turn, an **INTEGER** type, a basic ASN.1 type that is not composed from other types.</span></span>

<span data-ttu-id="20e76-110">Um sistema de tipos permite que a sintaxe de uma solicitação seja apresentada visualmente de maneira imediatamente compreendida pelos desenvolvedores e permite que a solicitação seja codificada consistentemente para transmissão em uma rede.</span><span class="sxs-lookup"><span data-stu-id="20e76-110">A type system enables the syntax of a request to be presented visually in a manner readily understood by developers, and it enables the request to be consistently encoded for transmission across a network.</span></span> <span data-ttu-id="20e76-111">Para obter mais informações sobre codificação, consulte [Distinguished Encoding Rules](distinguished-encoding-rules.md).</span><span class="sxs-lookup"><span data-stu-id="20e76-111">For more information about encoding, see [Distinguished Encoding Rules](distinguished-encoding-rules.md).</span></span> <span data-ttu-id="20e76-112">Para obter mais informações sobre os tipos ASN. 1, consulte os tópicos a seguir.</span><span class="sxs-lookup"><span data-stu-id="20e76-112">For more information about ASN.1 types, see the following topics.</span></span>

[<span data-ttu-id="20e76-113">Tipos Básicos</span><span class="sxs-lookup"><span data-stu-id="20e76-113">Basic Types</span></span>](about-basic-types.md)

<span data-ttu-id="20e76-114">Discute os seguintes tipos de dados:</span><span class="sxs-lookup"><span data-stu-id="20e76-114">Discusses the following data types:</span></span>

* <span data-ttu-id="20e76-115">**CADEIA DE BITS**</span><span class="sxs-lookup"><span data-stu-id="20e76-115">**BIT STRING**</span></span>
* <span data-ttu-id="20e76-116">**BOOLEAN**</span><span class="sxs-lookup"><span data-stu-id="20e76-116">**BOOLEAN**</span></span>
* <span data-ttu-id="20e76-117">**INTEGER**</span><span class="sxs-lookup"><span data-stu-id="20e76-117">**INTEGER**</span></span>
* <span data-ttu-id="20e76-118">**NULL**</span><span class="sxs-lookup"><span data-stu-id="20e76-118">**NULL**</span></span>
* <span data-ttu-id="20e76-119">**IDENTIFICADOR DE OBJETO**</span><span class="sxs-lookup"><span data-stu-id="20e76-119">**OBJECT IDENTIFIER**</span></span>
* <span data-ttu-id="20e76-120">**CADEIA DE CARACTERES DE OCTETO**</span><span class="sxs-lookup"><span data-stu-id="20e76-120">**OCTET STRING**</span></span>

[<span data-ttu-id="20e76-121">Tipos de cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="20e76-121">String Types</span></span>](about-string-types.md)

<span data-ttu-id="20e76-122">Discute os seguintes tipos de cadeia de caracteres:</span><span class="sxs-lookup"><span data-stu-id="20e76-122">Discusses the following string types:</span></span>

* <span data-ttu-id="20e76-123">**BMPString**</span><span class="sxs-lookup"><span data-stu-id="20e76-123">**BMPString**</span></span>
* <span data-ttu-id="20e76-124">**IA5String**</span><span class="sxs-lookup"><span data-stu-id="20e76-124">**IA5String**</span></span>
* <span data-ttu-id="20e76-125">**Imenablestring**</span><span class="sxs-lookup"><span data-stu-id="20e76-125">**PrintableString**</span></span>
* <span data-ttu-id="20e76-126">**TeletexString**</span><span class="sxs-lookup"><span data-stu-id="20e76-126">**TeletexString**</span></span>
* <span data-ttu-id="20e76-127">**UTF8String**</span><span class="sxs-lookup"><span data-stu-id="20e76-127">**UTF8String**</span></span>

[<span data-ttu-id="20e76-128">Tipos construídos</span><span class="sxs-lookup"><span data-stu-id="20e76-128">Constructed Types</span></span>](about-constructed-types.md)

<span data-ttu-id="20e76-129">Discute os tipos de dados ASN. 1 que podem conter tipos básicos, tipos de cadeia de caracteres ou outros tipos construídos.</span><span class="sxs-lookup"><span data-stu-id="20e76-129">Discusses ASN.1 data types that can contain basic types, string types, or other constructed types.</span></span>




 

## <a name="related-topics"></a><span data-ttu-id="20e76-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="20e76-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="20e76-131">Codificação de solicitação de certificado</span><span class="sxs-lookup"><span data-stu-id="20e76-131">Certificate Request Encoding</span></span>](about-certificate-request-encoding.md)
</dt> <dt>

[<span data-ttu-id="20e76-132">Codificação DER dos tipos ASN. 1</span><span class="sxs-lookup"><span data-stu-id="20e76-132">DER Encoding of ASN.1 Types</span></span>](about-der-encoding-of-asn-1-types.md)
</dt> <dt>

[<span data-ttu-id="20e76-133">Distinguished Encoding Rules</span><span class="sxs-lookup"><span data-stu-id="20e76-133">Distinguished Encoding Rules</span></span>](distinguished-encoding-rules.md)
</dt> <dt>

[<span data-ttu-id="20e76-134">Introdução à sintaxe e codificação ASN. 1</span><span class="sxs-lookup"><span data-stu-id="20e76-134">Introduction to ASN.1 Syntax and Encoding</span></span>](about-introduction-to-asn-1-syntax-and-encoding.md)
</dt> </dl>

 

 



