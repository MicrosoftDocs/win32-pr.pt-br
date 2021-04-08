---
description: A API de registro de certificado usa uma ASN. 1 para definir, codificar e decodificar as solicitações de certificado e os certificados que ele transfere entre computadores cliente e autoridades de certificação.
ms.assetid: 970a246f-a4c3-489b-b6a4-7d3103f388cf
title: Introdução à sintaxe e codificação ASN. 1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4fe15d2fb8fba4af25b9da7c249fec3a92630e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828345"
---
# <a name="introduction-to-asn1-syntax-and-encoding"></a><span data-ttu-id="4be7f-103">Introdução à sintaxe e codificação ASN. 1</span><span class="sxs-lookup"><span data-stu-id="4be7f-103">Introduction to ASN.1 Syntax and Encoding</span></span>

<span data-ttu-id="4be7f-104">A API de registro de certificado usa uma ASN. 1 para definir, codificar e decodificar as solicitações de certificado e os certificados que ele transfere entre computadores cliente e autoridades de certificação.</span><span class="sxs-lookup"><span data-stu-id="4be7f-104">The Certificate Enrollment API uses Abstract Syntax Notation One (ASN.1) to define, encode, and decode the certificate requests and certificates that it transfers between client computers and certification authorities.</span></span> <span data-ttu-id="4be7f-105">O ASN. 1 pode ser dividido conceitualmente em um conjunto de regras de sintaxe e um conjunto de regras de codificação, conforme mostrado nos exemplos a seguir.</span><span class="sxs-lookup"><span data-stu-id="4be7f-105">ASN.1 can be conceptually divided into a set of syntax rules and a set of encoding rules as shown by the following examples.</span></span>

## <a name="asn1-syntax-example"></a><span data-ttu-id="4be7f-106">Exemplo de sintaxe ASN. 1</span><span class="sxs-lookup"><span data-stu-id="4be7f-106">ASN.1 Syntax Example</span></span>

<span data-ttu-id="4be7f-107">Uma solicitação de certificado contém, entre outras coisas, o nome da entidade que está fazendo a solicitação ou para a qual a solicitação está sendo feita.</span><span class="sxs-lookup"><span data-stu-id="4be7f-107">A certificate request contains, among other things, the name of the entity that is making the request or for which the request is being made.</span></span> <span data-ttu-id="4be7f-108">O nome é uma sequência de RDNs (nomes distintos relativos de X. 500).</span><span class="sxs-lookup"><span data-stu-id="4be7f-108">The name is a sequence of X.500 relative distinguished names (RDNs).</span></span> <span data-ttu-id="4be7f-109">Cada RDN na sequência consiste em um OID (identificador de objeto) e um valor.</span><span class="sxs-lookup"><span data-stu-id="4be7f-109">Each RDN in the sequence consists of an object identifier (OID) and a value.</span></span> <span data-ttu-id="4be7f-110">A sintaxe ASN. 1 para um nome de entidade é mostrada no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="4be7f-110">The ASN.1 syntax for a subject name is shown in the following example.</span></span>

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

## <a name="asn1-encoding-example"></a><span data-ttu-id="4be7f-111">Exemplo de codificação ASN. 1</span><span class="sxs-lookup"><span data-stu-id="4be7f-111">ASN.1 Encoding Example</span></span>

<span data-ttu-id="4be7f-112">A API de registro de certificado usa [*Distinguished Encoding Rules*](/windows/desktop/SecGloss/d-gly) (der) para codificar o nome da entidade anterior.</span><span class="sxs-lookup"><span data-stu-id="4be7f-112">The Certificate Enrollment API uses [*Distinguished Encoding Rules*](/windows/desktop/SecGloss/d-gly) (DER) to encode the preceding subject name.</span></span> <span data-ttu-id="4be7f-113">O DER requer que cada item no nome seja representado por um TLV terceto, onde T contém o número de marca do tipo ASN. 1, L contém o comprimento e V contém o valor associado.</span><span class="sxs-lookup"><span data-stu-id="4be7f-113">DER requires that each item in the name be represented by a TLV triplet where T contains the tag number of the ASN.1 type, L contains the length, and V contains the associated value.</span></span> <span data-ttu-id="4be7f-114">O exemplo a seguir mostra como o nome da entidade TestCN. TestOrg é codificado.</span><span class="sxs-lookup"><span data-stu-id="4be7f-114">The following example shows how the subject name TestCN.TestOrg is encoded.</span></span>

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

<span data-ttu-id="4be7f-115">Observe os seguintes pontos:</span><span class="sxs-lookup"><span data-stu-id="4be7f-115">Note the following points:</span></span>

-   <span data-ttu-id="4be7f-116">Linha 1:</span><span class="sxs-lookup"><span data-stu-id="4be7f-116">Line 1:</span></span><dl> <span data-ttu-id="4be7f-117">O nome é uma sequência de nomes distintos relativos.</span><span class="sxs-lookup"><span data-stu-id="4be7f-117">The name is a sequence of relative distinguished names.</span></span>  
    <span data-ttu-id="4be7f-118">O número de marca para o tipo de **sequência** é 0x30.</span><span class="sxs-lookup"><span data-stu-id="4be7f-118">The tag number for the **SEQUENCE** type is 0x30.</span></span>  
    <span data-ttu-id="4be7f-119">O nome da entidade de TestCN. TestOrg requer 35 (0x23) bytes.</span><span class="sxs-lookup"><span data-stu-id="4be7f-119">The subject name of TestCN.TestOrg requires 35 (0x23) bytes.</span></span>  
    </dl>
-   Line 2:<dl> <span data-ttu-id="4be7f-120">O nome comum, TestCN, é um conjunto único de estruturas **attributetypevalue** .</span><span class="sxs-lookup"><span data-stu-id="4be7f-120">The Common Name, TestCN, is a single set of **AttributeTypeValue** structures.</span></span>  
    <span data-ttu-id="4be7f-121">O número de marca de um **conjunto** é 0x31.</span><span class="sxs-lookup"><span data-stu-id="4be7f-121">The tag number for a **SET** is 0x31.</span></span>  
    </dl><span data-ttu-id="4be7f-122">
-   Linha 3:</span><span class="sxs-lookup"><span data-stu-id="4be7f-122">
-   Line 3:</span></span><dl> <span data-ttu-id="4be7f-123">A estrutura **attributetypevalue** é uma sequência.</span><span class="sxs-lookup"><span data-stu-id="4be7f-123">The **AttributeTypeValue** structure is a sequence.</span></span>  
    <span data-ttu-id="4be7f-124">O número de marca para o tipo de **sequência** é 0x30.</span><span class="sxs-lookup"><span data-stu-id="4be7f-124">The tag number for the **SEQUENCE** type is 0x30.</span></span>  
    <span data-ttu-id="4be7f-125">A estrutura requer 13 (0xD) bytes.</span><span class="sxs-lookup"><span data-stu-id="4be7f-125">The structure requires 13 (0xD) bytes.</span></span>  
    </dl><span data-ttu-id="4be7f-126">
-   Linhas 4 a 6:</span><span class="sxs-lookup"><span data-stu-id="4be7f-126">
-   Lines 4 to 6:</span></span><dl> <span data-ttu-id="4be7f-127">O identificador de objeto (OID) para o nome comum é 2.5.4.3.</span><span class="sxs-lookup"><span data-stu-id="4be7f-127">The object identifier (OID) for the Common Name is 2.5.4.3.</span></span>  
    <span data-ttu-id="4be7f-128">O OID é um tipo de **\_ ID de objeto** de três bytes.</span><span class="sxs-lookup"><span data-stu-id="4be7f-128">The OID is a three byte **OBJECT\_ID** type.</span></span>  
    <span data-ttu-id="4be7f-129">O número de marca para o tipo de **\_ ID de objeto** é 0x06.</span><span class="sxs-lookup"><span data-stu-id="4be7f-129">The tag number for the **OBJECT\_ID** type is 0x06.</span></span>  
    </dl><span data-ttu-id="4be7f-130">
-   Linhas 7 a 9:</span><span class="sxs-lookup"><span data-stu-id="4be7f-130">
-   Lines 7 to 9:</span></span><dl> <span data-ttu-id="4be7f-131">O nome comum, TestCN, é um valor de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="4be7f-131">The Common Name, TestCN, is a string value.</span></span>  
    <span data-ttu-id="4be7f-132">A cadeia de caracteres é um tipo de **\_ cadeia de caracteres imprimível** de seis bytes.</span><span class="sxs-lookup"><span data-stu-id="4be7f-132">The string is a six byte **PRINTABLE\_STRING** type.</span></span>  
    <span data-ttu-id="4be7f-133">O número de marca para o tipo de **\_ cadeia de caracteres imprimível** é 0x13.</span><span class="sxs-lookup"><span data-stu-id="4be7f-133">The tag number for the **PRINTABLE\_STRING** type is 0x13.</span></span>  
    </dl>

## <a name="related-topics"></a><span data-ttu-id="4be7f-134">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4be7f-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4be7f-135">Sistema de tipo ASN. 1</span><span class="sxs-lookup"><span data-stu-id="4be7f-135">ASN.1 Type System</span></span>](about-asn-1-type-system.md)
</dt> <dt>

[<span data-ttu-id="4be7f-136">Codificação de solicitação de certificado</span><span class="sxs-lookup"><span data-stu-id="4be7f-136">Certificate Request Encoding</span></span>](about-certificate-request-encoding.md)
</dt> <dt>

[<span data-ttu-id="4be7f-137">Codificação DER dos tipos ASN. 1</span><span class="sxs-lookup"><span data-stu-id="4be7f-137">DER Encoding of ASN.1 Types</span></span>](about-der-encoding-of-asn-1-types.md)
</dt> <dt>

[<span data-ttu-id="4be7f-138">Distinguished Encoding Rules</span><span class="sxs-lookup"><span data-stu-id="4be7f-138">Distinguished Encoding Rules</span></span>](distinguished-encoding-rules.md)
</dt> </dl>

 

 
