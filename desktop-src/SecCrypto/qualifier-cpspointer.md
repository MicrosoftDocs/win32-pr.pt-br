---
description: Recupera o URI que aponta para uma declaração de prática de certificação (CPS) publicada pela autoridade de certificação (CA).
ms.assetid: fd030c1c-137c-4036-bf13-ae989a9703cc
title: Propriedade Qualifier. CPSPointer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifier.CPSPointer
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: db16e8faa25fc929e884358fcd885943adc17e32
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750092"
---
# <a name="qualifiercpspointer-property"></a><span data-ttu-id="5314a-103">Propriedade Qualifier. CPSPointer</span><span class="sxs-lookup"><span data-stu-id="5314a-103">Qualifier.CPSPointer property</span></span>

<span data-ttu-id="5314a-104">\[A propriedade **CPSPointer** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="5314a-104">\[The **CPSPointer** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="5314a-105">Em vez disso, use a [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) chamando o construtor que usa um OID como parâmetro e, em seguida, use o OID para políticas de certificado para processar qualificadores que fazem parte das informações de política na extensão de políticas de certificado.\]</span><span class="sxs-lookup"><span data-stu-id="5314a-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to process qualifiers that are part of the policy information in the Certificate Policies extension.\]</span></span>

<span data-ttu-id="5314a-106">A propriedade **CPSPointer** recupera o URI que aponta para uma declaração de prática de certificação (CPS) publicada pela autoridade de certificação (CA).</span><span class="sxs-lookup"><span data-stu-id="5314a-106">The **CPSPointer** property retrieves the URI that points to a Certification Practice Statement (CPS) published by the certification authority (CA).</span></span>

## <a name="syntax"></a><span data-ttu-id="5314a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="5314a-107">Syntax</span></span>


```VB
Qualifier.CPSPointer As String
```



## <a name="property-value"></a><span data-ttu-id="5314a-108">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="5314a-108">Property value</span></span>

<span data-ttu-id="5314a-109">O URI que aponta para um CPS publicado pela autoridade de certificação.</span><span class="sxs-lookup"><span data-stu-id="5314a-109">The URI that points to a CPS published by the CA.</span></span>

## <a name="requirements"></a><span data-ttu-id="5314a-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5314a-110">Requirements</span></span>



| <span data-ttu-id="5314a-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="5314a-111">Requirement</span></span> | <span data-ttu-id="5314a-112">Valor</span><span class="sxs-lookup"><span data-stu-id="5314a-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5314a-113">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="5314a-113">Redistributable</span></span><br/> | <span data-ttu-id="5314a-114">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="5314a-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="5314a-115">DLL</span><span class="sxs-lookup"><span data-stu-id="5314a-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="5314a-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5314a-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5314a-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="5314a-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5314a-118">**Qualificador**</span><span class="sxs-lookup"><span data-stu-id="5314a-118">**Qualifier**</span></span>](qualifier.md)
</dt> </dl>

 

 
