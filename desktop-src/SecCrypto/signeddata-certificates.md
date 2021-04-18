---
description: Recupera a coleção de certificados que está associada ao objeto SignedData. Depois de serem recuperados, os objetos de certificado individuais na coleção podem ser enumerados.
ms.assetid: 94741fee-2462-4a18-bc14-c52e9cac374b
title: Propriedade SignedData. Certificates
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedData.Certificates
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 55c0fe432794289fabe67b37deeedfac43f7a7d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758907"
---
# <a name="signeddatacertificates-property"></a><span data-ttu-id="216ec-104">Propriedade SignedData. Certificates</span><span class="sxs-lookup"><span data-stu-id="216ec-104">SignedData.Certificates property</span></span>

<span data-ttu-id="216ec-105">\[A propriedade **Certificates** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="216ec-105">\[The **Certificates** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="216ec-106">Em vez disso, use a [**classe SignedCms**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) no namespace [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="216ec-106">Instead, use the [**SignedCms Class**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="216ec-107">A propriedade **Certificates** recupera a coleção de [**certificados**](certificates.md) que está associada ao objeto [**SignedData**](signeddata.md) .</span><span class="sxs-lookup"><span data-stu-id="216ec-107">The **Certificates** property retrieves the [**Certificates**](certificates.md) collection that is associated with the [**SignedData**](signeddata.md) object.</span></span> <span data-ttu-id="216ec-108">Depois de serem recuperados, os objetos de [**certificado**](certificate.md) individuais na coleção podem ser enumerados.</span><span class="sxs-lookup"><span data-stu-id="216ec-108">After being retrieved, the individual [**Certificate**](certificate.md) objects in the collection can be enumerated.</span></span>

## <a name="syntax"></a><span data-ttu-id="216ec-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="216ec-109">Syntax</span></span>


```VB
SignedData.Certificates As Certificates
```



## <a name="property-value"></a><span data-ttu-id="216ec-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="216ec-110">Property value</span></span>

<span data-ttu-id="216ec-111">A coleção de [**certificados**](certificates.md) que está associada ao objeto [**SignedData**](signeddata.md) .</span><span class="sxs-lookup"><span data-stu-id="216ec-111">The [**Certificates**](certificates.md) collection that is associated with the [**SignedData**](signeddata.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="216ec-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="216ec-112">Requirements</span></span>



| <span data-ttu-id="216ec-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="216ec-113">Requirement</span></span> | <span data-ttu-id="216ec-114">Valor</span><span class="sxs-lookup"><span data-stu-id="216ec-114">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="216ec-115">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="216ec-115">Redistributable</span></span><br/> | <span data-ttu-id="216ec-116">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="216ec-116">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="216ec-117">DLL</span><span class="sxs-lookup"><span data-stu-id="216ec-117">DLL</span></span><br/>             | <dl> <span data-ttu-id="216ec-118"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="216ec-118"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="216ec-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="216ec-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="216ec-120">**SignedData**</span><span class="sxs-lookup"><span data-stu-id="216ec-120">**SignedData**</span></span>](signeddata.md)
</dt> </dl>

 

 
