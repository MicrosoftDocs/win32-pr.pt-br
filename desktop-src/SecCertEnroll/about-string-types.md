---
description: Um dos usos mais comuns de cadeias de caracteres em uma PKI (infraestrutura de chave pública) é criar um nome diferenciado X. 500.
ms.assetid: 01e8749b-a040-4267-bc12-f58f2c300337
title: Tipos de cadeia de caracteres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1173de3b2c4c5fd64181cd19c69cfbcecb1d584
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169488"
---
# <a name="string-types"></a><span data-ttu-id="0fc6f-103">Tipos de cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="0fc6f-103">String Types</span></span>

<span data-ttu-id="0fc6f-104">Um dos usos mais comuns de cadeias de caracteres em uma PKI (infraestrutura de chave pública) é criar um nome diferenciado X. 500.</span><span class="sxs-lookup"><span data-stu-id="0fc6f-104">One of the most common uses of strings in a public key infrastructure (PKI) is to create an X.500 Distinguished Name.</span></span> <span data-ttu-id="0fc6f-105">Por exemplo, o nome da entidade de uma solicitação de certificado é criado pela combinação de uma sequência de nomes distintos relativos, conforme mostrado no exemplo de sintaxe a seguir.</span><span class="sxs-lookup"><span data-stu-id="0fc6f-105">For example, the subject name of a certificate request is created by combining a sequence of relative distinguished names as shown in the following syntax example.</span></span>

``` syntax
---------------------------------------------------------------------
-- Breakdown of a subject name in a certificate request.
---------------------------------------------------------------------

CertificationRequestInfo ::= SEQUENCE 
{
   version                 CertificationRequestInfoVersion,
   subject                 Name,
   subjectPublicKeyInfo    SubjectPublicKeyInfo,
   attributes              [0] IMPLICIT Attributes
}

Name ::= SEQUENCE OF RelativeDistinguishedName

RelativeDistinguishedName ::= SET OF AttributeTypeValue

AttributeTypeValue ::= SEQUENCE 
{
   type       OBJECT IDENTIFIER,
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

<span data-ttu-id="0fc6f-106">A API de registro de certificado dá suporte aos seguintes tipos de cadeia de caracteres ASN. 1.</span><span class="sxs-lookup"><span data-stu-id="0fc6f-106">The Certificate Enrollment API supports the following ASN.1 string types.</span></span>

## <a name="bmpstring"></a><span data-ttu-id="0fc6f-107">BMPString</span><span class="sxs-lookup"><span data-stu-id="0fc6f-107">BMPString</span></span>

<span data-ttu-id="0fc6f-108">Marca de codificação: 0x1E</span><span class="sxs-lookup"><span data-stu-id="0fc6f-108">Encoding tag: 0x1E</span></span>

<span data-ttu-id="0fc6f-109">Nome do Certreq.exe: \_ cadeia de caracteres Unicode</span><span class="sxs-lookup"><span data-stu-id="0fc6f-109">Certreq.exe name: UNICODE\_STRING</span></span>

<span data-ttu-id="0fc6f-110">O BMP (plano multilíngüe básico) é uma codificação de caracteres que abrange o primeiro plano do conjunto de caracteres universal (UCS).</span><span class="sxs-lookup"><span data-stu-id="0fc6f-110">The Basic Multilingual Plane (BMP) is a character encoding that encompasses the first plane of the Universal Character Set (UCS).</span></span> <span data-ttu-id="0fc6f-111">Há planos dezessete numerados de 0 a 16.</span><span class="sxs-lookup"><span data-stu-id="0fc6f-111">There are seventeen planes numbered 0 to 16.</span></span> <span data-ttu-id="0fc6f-112">O BMP ocupa o plano 0 e inclui 65.536 pontos de código de 0x0000 a 0xFFFF.</span><span class="sxs-lookup"><span data-stu-id="0fc6f-112">BMP occupies plane 0 and includes 65,536 code points from 0x0000 to 0xFFFF.</span></span> <span data-ttu-id="0fc6f-113">Esta é a seção do mapa de caracteres Unicode em que a maioria das atribuições de caracteres foram feitas até o momento.</span><span class="sxs-lookup"><span data-stu-id="0fc6f-113">This is the section of the Unicode character map where most of the characters assignments have so far been made.</span></span> <span data-ttu-id="0fc6f-114">Ele inclui latim, Oriente Médio, asiático, africana e outras linguagens.</span><span class="sxs-lookup"><span data-stu-id="0fc6f-114">It includes Latin, Middle Eastern, Asian, African, and other languages.</span></span>

## <a name="ia5string"></a><span data-ttu-id="0fc6f-115">IA5String</span><span class="sxs-lookup"><span data-stu-id="0fc6f-115">IA5String</span></span>

<span data-ttu-id="0fc6f-116">Marca de codificação: 0x16</span><span class="sxs-lookup"><span data-stu-id="0fc6f-116">Encoding tag: 0x16</span></span>

<span data-ttu-id="0fc6f-117">Nome do Certreq.exe: \_ cadeia de caracteres IA5</span><span class="sxs-lookup"><span data-stu-id="0fc6f-117">Certreq.exe name: IA5\_STRING</span></span>

<span data-ttu-id="0fc6f-118">O alfabeto internacional número 5 (IA5) geralmente é equivalente ao alfabeto ASCII, mas versões diferentes podem incluir acentos ou outros caracteres específicos de um idioma regional.</span><span class="sxs-lookup"><span data-stu-id="0fc6f-118">The International Alphabet number 5 (IA5) is generally equivalent to the ASCII alphabet, but different versions can include accents or other characters specific to a regional language.</span></span> <span data-ttu-id="0fc6f-119">O exemplo a seguir mostra o tipo **IA5String** usado na definição de ASN. 1 da extensão de certificado **alternativonames** .</span><span class="sxs-lookup"><span data-stu-id="0fc6f-119">The following example shows the **IA5String** type used in the ASN.1 definition of the **AlternativeNames** certificate extension.</span></span>

``` syntax
---------------------------------------------------------------------
-- AlternativeNames extension
---------------------------------------------------------------------

AltNames ::= SEQUENCE OF GeneralName

GeneralNames ::= AltNames

GeneralName ::= CHOICE 
{
   otherName               [0] IMPLICIT OtherName,
   rfc822Name              [1] IMPLICIT IA5String,
   dNSName                 [2] IMPLICIT IA5String,
   x400Address             [3] IMPLICIT SEQUENCE OF ANY, 
   directoryName           [4] EXPLICIT ANY,    
   ediPartyName            [5] IMPLICIT SEQUENCE OF ANY,
   uniformResourceLocator  [6] IMPLICIT IA5String,
   iPAddress               [7] IMPLICIT OCTET STRING,
   registeredID            [8] IMPLICIT OBJECT IDENTIFIER
}

OtherName ::= SEQUENCE 
{
   type                    OBJECT IDENTIFIER,
   value                   [0] EXPLICIT ANY 
}
```

## <a name="printablestring"></a><span data-ttu-id="0fc6f-120">Imenablestring</span><span class="sxs-lookup"><span data-stu-id="0fc6f-120">PrintableString</span></span>

<span data-ttu-id="0fc6f-121">Marca de codificação: 0x13</span><span class="sxs-lookup"><span data-stu-id="0fc6f-121">Encoding tag: 0x13</span></span>

<span data-ttu-id="0fc6f-122">Nome do Certreq.exe: cadeia de caracteres IMPRIMÍvel \_</span><span class="sxs-lookup"><span data-stu-id="0fc6f-122">Certreq.exe name: PRINTABLE\_STRING</span></span>

<span data-ttu-id="0fc6f-123">O tipo de dados **imenablestring** foi originalmente destinado a representar os conjuntos de caracteres limitados disponíveis para terminais de entrada de mainframe, mas ele ainda é normalmente usado.</span><span class="sxs-lookup"><span data-stu-id="0fc6f-123">The **PrintableString** data type was originally intended to represent the limited character sets available to mainframe input terminals, but it is still commonly used.</span></span> <span data-ttu-id="0fc6f-124">Ele contém os seguintes caracteres:</span><span class="sxs-lookup"><span data-stu-id="0fc6f-124">It contains the following characters:</span></span>

-   <span data-ttu-id="0fc6f-125">A-Z</span><span class="sxs-lookup"><span data-stu-id="0fc6f-125">A-Z</span></span>
-   <span data-ttu-id="0fc6f-126">a-z</span><span class="sxs-lookup"><span data-stu-id="0fc6f-126">a-z</span></span>
-   <span data-ttu-id="0fc6f-127">0-9</span><span class="sxs-lookup"><span data-stu-id="0fc6f-127">0-9</span></span>
-   <span data-ttu-id="0fc6f-128">' ( ) + , - .</span><span class="sxs-lookup"><span data-stu-id="0fc6f-128">' ( ) + , - .</span></span> <span data-ttu-id="0fc6f-129">/ : = ?</span><span class="sxs-lookup"><span data-stu-id="0fc6f-129">/ : = ?</span></span> <span data-ttu-id="0fc6f-130">\[space\]</span><span class="sxs-lookup"><span data-stu-id="0fc6f-130">\[space\]</span></span>

## <a name="teletexstring"></a><span data-ttu-id="0fc6f-131">TeletexString</span><span class="sxs-lookup"><span data-stu-id="0fc6f-131">TeletexString</span></span>

<span data-ttu-id="0fc6f-132">Marca de codificação: 0x14</span><span class="sxs-lookup"><span data-stu-id="0fc6f-132">Encoding tag: 0x14</span></span>

<span data-ttu-id="0fc6f-133">O **TeletexString** e os tipos de dados **T61String** relacionados são codificados em 8 bits (ou 16 bits para caracteres compostos).</span><span class="sxs-lookup"><span data-stu-id="0fc6f-133">The **TeletexString** and the related **T61String** data types are encoded on 8 bits (or 16 bits for composite characters).</span></span> <span data-ttu-id="0fc6f-134">Ambos têm um número de marca de 0x14.</span><span class="sxs-lookup"><span data-stu-id="0fc6f-134">They both have a tag number of 0x14.</span></span> <span data-ttu-id="0fc6f-135">Eles não são amplamente usados.</span><span class="sxs-lookup"><span data-stu-id="0fc6f-135">They are not extensively used.</span></span>

## <a name="utf8string"></a><span data-ttu-id="0fc6f-136">UTF8String</span><span class="sxs-lookup"><span data-stu-id="0fc6f-136">UTF8String</span></span>

<span data-ttu-id="0fc6f-137">Marca de codificação: 0x0C</span><span class="sxs-lookup"><span data-stu-id="0fc6f-137">Encoding tag: 0x0C</span></span>

<span data-ttu-id="0fc6f-138">Nome do Certreq.exe: \_ cadeia de caracteres UTF8</span><span class="sxs-lookup"><span data-stu-id="0fc6f-138">Certreq.exe name: UTF8\_STRING</span></span>

<span data-ttu-id="0fc6f-139">O formato de transformação UCS/Unicode de 8 bits (UTF-8) é uma codificação de caracteres de comprimento variável que pode representar qualquer caractere universal como caractere Unicode, permitindo que os pontos de código iniciais permaneçam consistentes com o ASCII.</span><span class="sxs-lookup"><span data-stu-id="0fc6f-139">The 8-bit UCS/Unicode Transformation Format (UTF-8) is a variable-length character encoding that can represent any universal character as a Unicode character while allowing initial code points to remain consistent with ASCII.</span></span> <span data-ttu-id="0fc6f-140">O UTF-8 usa um a quatro bytes.</span><span class="sxs-lookup"><span data-stu-id="0fc6f-140">UTF-8 uses one to four bytes.</span></span> <span data-ttu-id="0fc6f-141">O número de marca é 0x0C.</span><span class="sxs-lookup"><span data-stu-id="0fc6f-141">The tag number is 0x0C.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0fc6f-142">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0fc6f-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0fc6f-143">Sistema de tipo ASN. 1</span><span class="sxs-lookup"><span data-stu-id="0fc6f-143">ASN.1 Type System</span></span>](about-asn-1-type-system.md)
</dt> <dt>

[<span data-ttu-id="0fc6f-144">Distinguished Encoding Rules</span><span class="sxs-lookup"><span data-stu-id="0fc6f-144">Distinguished Encoding Rules</span></span>](distinguished-encoding-rules.md)
</dt> <dt>

[<span data-ttu-id="0fc6f-145">Codificação DER dos tipos ASN. 1</span><span class="sxs-lookup"><span data-stu-id="0fc6f-145">DER Encoding of ASN.1 Types</span></span>](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 



