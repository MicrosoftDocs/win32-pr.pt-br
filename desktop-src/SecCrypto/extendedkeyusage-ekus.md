---
description: Retorna a coleção EKUs do certificado.
ms.assetid: 64211a00-7d4d-4381-a134-9cd570ed7dbb
title: Propriedade ExtendedKeyUsage. EKUs
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedKeyUsage.EKUs
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 24bcf7b4332e75afad0e21415a7dfe8eb690c32b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753404"
---
# <a name="extendedkeyusageekus-property"></a><span data-ttu-id="4c25a-103">Propriedade ExtendedKeyUsage. EKUs</span><span class="sxs-lookup"><span data-stu-id="4c25a-103">ExtendedKeyUsage.EKUs property</span></span>

<span data-ttu-id="4c25a-104">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="4c25a-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="4c25a-105">Em vez disso, use a [**classe X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="4c25a-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="4c25a-106">A propriedade **EKUs** retorna a coleção [**EKUs**](ekus.md) para o certificado.</span><span class="sxs-lookup"><span data-stu-id="4c25a-106">The **EKUs** property returns the [**EKUs**](ekus.md) collection for the certificate.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c25a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="4c25a-107">Syntax</span></span>


```VB
ExtendedKeyUsage.EKUs As EKUs
```



## <a name="property-value"></a><span data-ttu-id="4c25a-108">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="4c25a-108">Property value</span></span>

<span data-ttu-id="4c25a-109">A coleção [**EKUs**](ekus.md) que contém os objetos [**EKU**](eku.md) para o certificado.</span><span class="sxs-lookup"><span data-stu-id="4c25a-109">The [**EKUs**](ekus.md) collection that contains the [**EKU**](eku.md) objects for the certificate.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c25a-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4c25a-110">Requirements</span></span>



| <span data-ttu-id="4c25a-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c25a-111">Requirement</span></span> | <span data-ttu-id="4c25a-112">Valor</span><span class="sxs-lookup"><span data-stu-id="4c25a-112">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4c25a-113">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="4c25a-113">End of client support</span></span><br/> | <span data-ttu-id="4c25a-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4c25a-114">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="4c25a-115">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="4c25a-115">End of server support</span></span><br/> | <span data-ttu-id="4c25a-116">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4c25a-116">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="4c25a-117">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="4c25a-117">Redistributable</span></span><br/>       | <span data-ttu-id="4c25a-118">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="4c25a-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="4c25a-119">DLL</span><span class="sxs-lookup"><span data-stu-id="4c25a-119">DLL</span></span><br/>                   | <dl> <span data-ttu-id="4c25a-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4c25a-120"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c25a-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="4c25a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c25a-122">**ExtendedKeyUsage**</span><span class="sxs-lookup"><span data-stu-id="4c25a-122">**ExtendedKeyUsage**</span></span>](extendedkeyusage.md)
</dt> </dl>

 

 
