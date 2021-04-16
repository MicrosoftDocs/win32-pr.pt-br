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
# <a name="constructed-types"></a><span data-ttu-id="5814e-104">Tipos construídos</span><span class="sxs-lookup"><span data-stu-id="5814e-104">Constructed Types</span></span>

<span data-ttu-id="5814e-105">Um tipo ASN criado de [*notação de sintaxe abstrata*](/windows/desktop/SecGloss/a-gly) (Authorized. 1) é composto de tipos básicos, tipos de cadeia de caracteres ou outros tipos construídos.</span><span class="sxs-lookup"><span data-stu-id="5814e-105">A constructed [*Abstract Syntax Notation One*](/windows/desktop/SecGloss/a-gly) (ASN.1) type is made up from basic types, string types, or other constructed types.</span></span> <span data-ttu-id="5814e-106">Por exemplo, uma extensão de certificado X. 509 é composta de três tipos ASN básicos. 1, conforme mostrado pelo exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="5814e-106">For example, an X.509 certificate extension is composed from three basic ASN.1 types as shown by the following example.</span></span>

``` syntax
Extension ::= SEQUENCE 
{
   extnId              OBJECT IDENTIFIER,
   critical            BOOLEAN DEFAULT FALSE,
   extnValue           OCTET STRING
}
```

<span data-ttu-id="5814e-107">Uma extensão consiste em um OID ( [*identificador de objeto*](/windows/desktop/SecGloss/o-gly) ), um valor booliano que identifica se a extensão é crítica e uma matriz de bytes que contém o valor.</span><span class="sxs-lookup"><span data-stu-id="5814e-107">An extension consists of an [*object identifier*](/windows/desktop/SecGloss/o-gly) (OID), a Boolean value that identifies whether the extension is critical, and a byte array that contains the value.</span></span> <span data-ttu-id="5814e-108">A API de registro de certificado dá suporte aos tipos ASN. 1 construídos a seguir.</span><span class="sxs-lookup"><span data-stu-id="5814e-108">The Certificate Enrollment API supports the following constructed ASN.1 types.</span></span>

## <a name="sequence-and-sequence-of"></a><span data-ttu-id="5814e-109">SEQUÊNCIA e sequência de</span><span class="sxs-lookup"><span data-stu-id="5814e-109">SEQUENCE and SEQUENCE OF</span></span>

<span data-ttu-id="5814e-110">Marca de codificação: 0x30</span><span class="sxs-lookup"><span data-stu-id="5814e-110">Encoding tag: 0x30</span></span>

<span data-ttu-id="5814e-111">Contém uma série ordenada de campos de um ou mais tipos.</span><span class="sxs-lookup"><span data-stu-id="5814e-111">Contains an ordered series of fields of one or more types.</span></span> <span data-ttu-id="5814e-112">Os campos podem ser marcados como **opcional** ou **padrão**.</span><span class="sxs-lookup"><span data-stu-id="5814e-112">Fields can be marked **OPTIONAL** or **DEFAULT**.</span></span> <span data-ttu-id="5814e-113">Além disso, para evitar ambigüidade ao decodificar, os campos opcionais sucessivos devem diferir uns dos outros por meio de um identificador exclusivo (um inteiro entre colchetes, como \[ 1 \] ) e do campo obrigatório a seguir, conforme mostrado pelo exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="5814e-113">Also, to avoid ambiguity when decoding, successive optional fields should differ from one another by use of a unique identifier (a bracketed integer such as \[1\]) and from a following required field as shown by the following example.</span></span>

``` syntax
SomeValue ::= SEQUENCE 
{
   a     INTEGER,
   b     [0] INTEGER OPTIONAL,
   c     [1] INTEGER DEFAULT 1,
   d     INTEGER
}
```

<span data-ttu-id="5814e-114">A diferença entre **sequência** e **sequência de** é que os elementos de uma **sequência de** construção devem ser do mesmo tipo.</span><span class="sxs-lookup"><span data-stu-id="5814e-114">The difference between **SEQUENCE** and **SEQUENCE OF** is that the elements of a **SEQUENCE OF** construct must be of the same type.</span></span> <span data-ttu-id="5814e-115">Veja o exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="5814e-115">See the following example.</span></span> <span data-ttu-id="5814e-116">Ambos os constructos têm o mesmo valor de marca (0x30) quando codificados.</span><span class="sxs-lookup"><span data-stu-id="5814e-116">Both constructs have the same tag value (0x30) when encoded.</span></span>

``` syntax
PolicyQualifiers ::=  SEQUENCE OF PolicyQualifierInfo

PolicyQualifierInfo ::= SEQUENCE 
{
   policyQualifierId   OBJECT IDENTIFIER,
   qualifier           ANY OPTIONAL
}
```

<span data-ttu-id="5814e-117">Outra maneira de examinar a diferença entre **sequência** e **sequência de** é compará-los com suas contrapartes na linguagem de programação C.</span><span class="sxs-lookup"><span data-stu-id="5814e-117">Another way to look at the difference between **SEQUENCE** and **SEQUENCE OF** is to compare them to their counterparts in the C programming language.</span></span> <span data-ttu-id="5814e-118">Ou seja, **Sequence** é aproximadamente equivalente a uma estrutura e a **sequência de** é aproximadamente equivalente a uma matriz.</span><span class="sxs-lookup"><span data-stu-id="5814e-118">That is, **SEQUENCE** is roughly equivalent to a structure and **SEQUENCE OF** is roughly equivalent to an array.</span></span>

## <a name="set-and-set-of"></a><span data-ttu-id="5814e-119">CONJUNTO e conjunto de</span><span class="sxs-lookup"><span data-stu-id="5814e-119">SET and SET OF</span></span>

<span data-ttu-id="5814e-120">Marca de codificação: 0x31</span><span class="sxs-lookup"><span data-stu-id="5814e-120">Encoding tag: 0x31</span></span>

<span data-ttu-id="5814e-121">Contém uma série não ordenada de campos de um ou mais tipos.</span><span class="sxs-lookup"><span data-stu-id="5814e-121">Contains an unordered series of fields of one or more types.</span></span> <span data-ttu-id="5814e-122">Isso é diferente de uma **sequência** que contém uma lista ordenada.</span><span class="sxs-lookup"><span data-stu-id="5814e-122">This differs from a **SEQUENCE** which contains an ordered list.</span></span> <span data-ttu-id="5814e-123">A especificação de uma lista não ordenada permite que um aplicativo forneça os campos de estrutura para o codificador na ordem mais apropriada.</span><span class="sxs-lookup"><span data-stu-id="5814e-123">Specifying an unordered list enables an application to provide the structure fields to the encoder in the most appropriate order.</span></span> <span data-ttu-id="5814e-124">Como with **Sequence**, os campos de uma construção **set** podem ser marcados com **optional** ou **Default**, e os identificadores exclusivos devem ser usados para eliminar a ambiguidade do processo de decodificação.</span><span class="sxs-lookup"><span data-stu-id="5814e-124">As with **SEQUENCE**, the fields of a **SET** construct can be marked with **OPTIONAL** or **DEFAULT**, and unique identifiers must be used to disambiguate the decoding process.</span></span> <span data-ttu-id="5814e-125">A diferença entre **set** e **set de** é que os elementos de um **conjunto de** construção devem ser do mesmo tipo.</span><span class="sxs-lookup"><span data-stu-id="5814e-125">The difference between **SET** and **SET OF** is that the elements of a **SET OF** construct must be of the same type.</span></span>

``` syntax
Name ::= SEQUENCE OF RelativeDistinguishedName

RelativeDistinguishedName ::= SET OF AttributeTypeValue

AttributeTypeValue ::= SEQUENCE 
{
   type       OBJECT IDENTIFIER,
   value      ANY 
}
```

## <a name="choice"></a><span data-ttu-id="5814e-126">DESEJADA</span><span class="sxs-lookup"><span data-stu-id="5814e-126">CHOICE</span></span>

<span data-ttu-id="5814e-127">Marca de codificação: não aplicável</span><span class="sxs-lookup"><span data-stu-id="5814e-127">Encoding tag: not applicable</span></span>

<span data-ttu-id="5814e-128">Define uma escolha entre alternativas.</span><span class="sxs-lookup"><span data-stu-id="5814e-128">Defines a choice between alternatives.</span></span> <span data-ttu-id="5814e-129">Cada alternativa deve ser identificada exclusivamente por um inteiro entre colchetes para evitar ambigüidade ao decodificar.</span><span class="sxs-lookup"><span data-stu-id="5814e-129">Each alternative must be uniquely identified by a bracketed integer to avoid ambiguity when decoding.</span></span> <span data-ttu-id="5814e-130">Quando codificada, a construção **Choice** terá o valor da marca de codificação da alternativa escolhida.</span><span class="sxs-lookup"><span data-stu-id="5814e-130">When encoded, the **CHOICE** construct will have the encoding tag value of the chosen alternative.</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="5814e-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5814e-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5814e-132">Sistema de tipo ASN. 1</span><span class="sxs-lookup"><span data-stu-id="5814e-132">ASN.1 Type System</span></span>](about-asn-1-type-system.md)
</dt> <dt>

[<span data-ttu-id="5814e-133">Codificação DER dos tipos ASN. 1</span><span class="sxs-lookup"><span data-stu-id="5814e-133">DER Encoding of ASN.1 Types</span></span>](about-der-encoding-of-asn-1-types.md)
</dt> <dt>

[<span data-ttu-id="5814e-134">Distinguished Encoding Rules</span><span class="sxs-lookup"><span data-stu-id="5814e-134">Distinguished Encoding Rules</span></span>](distinguished-encoding-rules.md)
</dt> </dl>

 

 
