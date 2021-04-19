---
description: A API de registro de certificado dá suporte aos seguintes tipos ASN básicos. 1.
ms.assetid: ca247945-ebcf-492e-9cc8-a67a9454fa95
title: Tipos Básicos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e9f3ae64c058fce3466ca06e7bf205c4c4165fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105748462"
---
# <a name="basic-types"></a><span data-ttu-id="f1e3d-103">Tipos Básicos</span><span class="sxs-lookup"><span data-stu-id="f1e3d-103">Basic Types</span></span>

<span data-ttu-id="f1e3d-104">A API de registro de certificado dá suporte aos seguintes tipos ASN básicos. 1.</span><span class="sxs-lookup"><span data-stu-id="f1e3d-104">The Certificate Enrollment API supports the following basic ASN.1 types.</span></span>

## <a name="bit-string"></a><span data-ttu-id="f1e3d-105">CADEIA DE BITS</span><span class="sxs-lookup"><span data-stu-id="f1e3d-105">BIT STRING</span></span>

<span data-ttu-id="f1e3d-106">Marca de codificação: 0x03</span><span class="sxs-lookup"><span data-stu-id="f1e3d-106">Encoding tag: 0x03</span></span>

<span data-ttu-id="f1e3d-107">Nome do Certreq.exe: \_ cadeia de caracteres de bits</span><span class="sxs-lookup"><span data-stu-id="f1e3d-107">Certreq.exe name: BIT\_STRING</span></span>

<span data-ttu-id="f1e3d-108">Uma cadeia de caracteres de bits ou binária é uma matriz de bits demorada arbitrariamente.</span><span class="sxs-lookup"><span data-stu-id="f1e3d-108">A bit or binary string is an arbitrarily long array of bits.</span></span> <span data-ttu-id="f1e3d-109">Bits específicos podem ser identificados por inteiros entre parênteses e nomes atribuídos como no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="f1e3d-109">Specific bits can be identified by parenthesized integers and assigned names as in the following example.</span></span>

``` syntax
Versions ::= BIT STRING{ version-1(0), version-2(1) } 
```

<span data-ttu-id="f1e3d-110">As assinaturas e as chaves de certificado geralmente são representadas como cadeias de bits.</span><span class="sxs-lookup"><span data-stu-id="f1e3d-110">Certificate keys and signatures are often represented as bit strings.</span></span>

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

## <a name="boolean"></a><span data-ttu-id="f1e3d-111">BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="f1e3d-111">BOOLEAN</span></span>

<span data-ttu-id="f1e3d-112">Marca de codificação: 0x01</span><span class="sxs-lookup"><span data-stu-id="f1e3d-112">Encoding tag: 0x01</span></span>

<span data-ttu-id="f1e3d-113">Nome do Certreq.exe: BOOLIANo</span><span class="sxs-lookup"><span data-stu-id="f1e3d-113">Certreq.exe name: BOOLEAN</span></span>

<span data-ttu-id="f1e3d-114">Um tipo booliano pode conter um dos dois valores, **true** ou **false**.</span><span class="sxs-lookup"><span data-stu-id="f1e3d-114">A Boolean type can contain one of two values, **TRUE** or **FALSE**.</span></span> <span data-ttu-id="f1e3d-115">O exemplo a seguir mostra a estrutura ASN. 1 para uma extensão de certificado de restrições básicas.</span><span class="sxs-lookup"><span data-stu-id="f1e3d-115">The following example shows the ASN.1 structure for a Basic Constraints certificate extension.</span></span> <span data-ttu-id="f1e3d-116">O campo **CA** especifica se uma entidade de certificado é uma autoridade de certificação (CA).</span><span class="sxs-lookup"><span data-stu-id="f1e3d-116">The **cA** field specifies whether a certificate subject is a certification authority (CA).</span></span> <span data-ttu-id="f1e3d-117">A criticalidade padrão é **false**.</span><span class="sxs-lookup"><span data-stu-id="f1e3d-117">The default criticality is **FALSE**.</span></span>

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

## <a name="integer"></a><span data-ttu-id="f1e3d-118">INTEGER</span><span class="sxs-lookup"><span data-stu-id="f1e3d-118">INTEGER</span></span>

<span data-ttu-id="f1e3d-119">Marca de codificação: 0x02</span><span class="sxs-lookup"><span data-stu-id="f1e3d-119">Encoding tag: 0x02</span></span>

<span data-ttu-id="f1e3d-120">Nome do Certreq.exe: inteiro</span><span class="sxs-lookup"><span data-stu-id="f1e3d-120">Certreq.exe name: INTEGER</span></span>

<span data-ttu-id="f1e3d-121">Um inteiro normalmente pode ser qualquer valor integral positivo ou negativo.</span><span class="sxs-lookup"><span data-stu-id="f1e3d-121">An integer can typically be any positive or negative integral value.</span></span> <span data-ttu-id="f1e3d-122">O exemplo a seguir mostra a estrutura ASN. 1 para uma chave pública RSA.</span><span class="sxs-lookup"><span data-stu-id="f1e3d-122">The following example shows the ASN.1 structure for an RSA public key.</span></span> <span data-ttu-id="f1e3d-123">Observe que o campo **publicExponent** é restrito a um inteiro positivo inferior a 4.294.967.296.</span><span class="sxs-lookup"><span data-stu-id="f1e3d-123">Note that the **publicExponent** field is restricted to a positive integer less than 4,294,967,296.</span></span>

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

## <a name="null"></a><span data-ttu-id="f1e3d-124">NULO</span><span class="sxs-lookup"><span data-stu-id="f1e3d-124">NULL</span></span>

<span data-ttu-id="f1e3d-125">Marca de codificação: 0x05</span><span class="sxs-lookup"><span data-stu-id="f1e3d-125">Encoding tag: 0x05</span></span>

<span data-ttu-id="f1e3d-126">Nome do Certreq.exe: **nulo**</span><span class="sxs-lookup"><span data-stu-id="f1e3d-126">Certreq.exe name: **NULL**</span></span>

<span data-ttu-id="f1e3d-127">Um tipo **nulo** contém um único byte 0x00.</span><span class="sxs-lookup"><span data-stu-id="f1e3d-127">A **NULL** type contains a single byte 0x00.</span></span> <span data-ttu-id="f1e3d-128">Ele pode ser usado em qualquer lugar que a solicitação de certificado deva indicar um valor vazio.</span><span class="sxs-lookup"><span data-stu-id="f1e3d-128">It can be used anywhere that the certificate request must indicate an empty value.</span></span> <span data-ttu-id="f1e3d-129">Por exemplo, um **AlgorithmIdentifier** é uma sequência que contém um OID (identificador de objeto) e parâmetros opcionais.</span><span class="sxs-lookup"><span data-stu-id="f1e3d-129">For example, an **AlgorithmIdentifier** is a sequence that contains an object identifier (OID) and optional parameters.</span></span>

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

<span data-ttu-id="f1e3d-130">Se não houver parâmetros quando a estrutura for codificada, **NULL** será usado para indicar um valor vazio.</span><span class="sxs-lookup"><span data-stu-id="f1e3d-130">If there are no parameters when the structure is encoded, **NULL** is used to indicate an empty value.</span></span>

``` syntax
30 0d            ; SEQUENCE (d Bytes)
|  |  |  06 09          ; OBJECT_ID (9 Bytes)
|  |  |  |  2a 86 48 86 f7 0d 01 01  01
|  |  |  |     ; 1.2.840.113549.1.1.1 RSA (RSA_SIGN)
|  |  |  05 00          ; NULL (0 Bytes)
```

## <a name="object-identifier"></a><span data-ttu-id="f1e3d-131">IDENTIFICADOR DE OBJETO</span><span class="sxs-lookup"><span data-stu-id="f1e3d-131">OBJECT IDENTIFIER</span></span>

<span data-ttu-id="f1e3d-132">Marca de codificação: 0x06</span><span class="sxs-lookup"><span data-stu-id="f1e3d-132">Encoding tag: 0x06</span></span>

<span data-ttu-id="f1e3d-133">Nome do Certreq.exe: \_ ID do objeto</span><span class="sxs-lookup"><span data-stu-id="f1e3d-133">Certreq.exe name: OBJECT\_ID</span></span>

<span data-ttu-id="f1e3d-134">A API de registro de certificado usa OIDs (identificadores de objeto) como um tipo de ponteiro universal para identificadores de algoritmo, atributos e outros elementos PKI.</span><span class="sxs-lookup"><span data-stu-id="f1e3d-134">The Certificate Enrollment API uses object identifiers (OIDs) as a type of universal pointer to algorithm identifiers, attributes, and other PKI elements.</span></span> <span data-ttu-id="f1e3d-135">Os OIDs normalmente são apresentados em uma cadeia de caracteres decimais pontilhada, como "2.16.840.1.101.3.4.1.42".</span><span class="sxs-lookup"><span data-stu-id="f1e3d-135">OIDs are typically presented in a dotted decimal string such as "2.16.840.1.101.3.4.1.42".</span></span> <span data-ttu-id="f1e3d-136">Os elementos individuais na cadeia de caracteres, separados por pontos, representam os arcos e folhas em uma árvore de autoridade de registro que identifica exclusivamente o objeto e a organização que o registrou.</span><span class="sxs-lookup"><span data-stu-id="f1e3d-136">The individual elements in the string, separated by periods, represent the arcs and leaves in a registration authority tree that uniquely identifies the object and the organization that registered it.</span></span> <span data-ttu-id="f1e3d-137">Por exemplo, o OID anterior pode ser expandido para junta-ISO-ITU-t (2) país (16) US (840) Organization (1) gov (101) Csor (3) nistAlgorithms (4) aesAlgs (1) com. 42 acrescentado para identificar exclusivamente o algoritmo do modo CBC (encadeamento de blocos de criptografia) do AES de 256 bits.</span><span class="sxs-lookup"><span data-stu-id="f1e3d-137">For example, the preceding OID can be expanded to joint-iso-itu-t(2) country(16) us(840) organization(1) gov(101) csor(3) nistAlgorithms(4) aesAlgs(1) with .42 appended to uniquely identify the 256-bit AES cipher block chaining (CBC) mode algorithm.</span></span>

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

## <a name="octet-string"></a><span data-ttu-id="f1e3d-138">CADEIA DE CARACTERES DE OCTETO</span><span class="sxs-lookup"><span data-stu-id="f1e3d-138">OCTET STRING</span></span>

<span data-ttu-id="f1e3d-139">Marca de codificação: 0x04</span><span class="sxs-lookup"><span data-stu-id="f1e3d-139">Encoding tag: 0x04</span></span>

<span data-ttu-id="f1e3d-140">Nome do Certreq.exe: \_ cadeia de caracteres de octeto</span><span class="sxs-lookup"><span data-stu-id="f1e3d-140">Certreq.exe name: OCTET\_STRING</span></span>

<span data-ttu-id="f1e3d-141">Uma cadeia de caracteres de octeto é uma matriz de bytes grandes arbitrariamente.</span><span class="sxs-lookup"><span data-stu-id="f1e3d-141">An octet string is an arbitrarily large byte array.</span></span> <span data-ttu-id="f1e3d-142">Ao contrário do tipo de **cadeia de caracteres bit** , no entanto, bits específicos e bytes na cadeia de caracteres não podem receber nomes.</span><span class="sxs-lookup"><span data-stu-id="f1e3d-142">Unlike the **BIT STRING** type, however, specific bits and bytes in the string cannot be assigned names.</span></span> <span data-ttu-id="f1e3d-143">A palavra octeto deve ser uma maneira independente de plataforma de se referir a uma palavra de memória.</span><span class="sxs-lookup"><span data-stu-id="f1e3d-143">The word octet is meant to be a platform independent way to refer to a memory word.</span></span> <span data-ttu-id="f1e3d-144">No contexto da API de registro de certificado, o octeto e o byte são intercambiáveis.</span><span class="sxs-lookup"><span data-stu-id="f1e3d-144">Within the context of the Certificate Enrollment API, octet and byte are interchangeable.</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="f1e3d-145">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f1e3d-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f1e3d-146">Sistema de tipo ASN. 1</span><span class="sxs-lookup"><span data-stu-id="f1e3d-146">ASN.1 Type System</span></span>](about-asn-1-type-system.md)
</dt> <dt>

[<span data-ttu-id="f1e3d-147">Distinguished Encoding Rules</span><span class="sxs-lookup"><span data-stu-id="f1e3d-147">Distinguished Encoding Rules</span></span>](distinguished-encoding-rules.md)
</dt> <dt>

[<span data-ttu-id="f1e3d-148">Codificação DER dos tipos ASN. 1</span><span class="sxs-lookup"><span data-stu-id="f1e3d-148">DER Encoding of ASN.1 Types</span></span>](about-der-encoding-of-asn-1-types.md)
</dt> </dl>

 

 



