---
description: Recupera um valor booliano que indica se o bit dataEncipherment está definido.
ms.assetid: 9b29a76f-1494-4db3-a5d7-69fe631ca1dd
title: Propriedade KeyUsage. IsDataEnciphermentEnabled
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage.IsDataEnciphermentEnabled
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 0aad6cbcd21830ad127b9537749dfb1c05a4c9ac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105813105"
---
# <a name="keyusageisdataenciphermentenabled-property"></a><span data-ttu-id="c5947-103">Propriedade KeyUsage. IsDataEnciphermentEnabled</span><span class="sxs-lookup"><span data-stu-id="c5947-103">KeyUsage.IsDataEnciphermentEnabled property</span></span>

<span data-ttu-id="c5947-104">\[A propriedade **IsDataEnciphermentEnabled** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="c5947-104">\[The **IsDataEnciphermentEnabled** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="c5947-105">Em vez disso, use a [**classe X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="c5947-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="c5947-106">A propriedade **IsDataEnciphermentEnabled** recupera um valor booliano que indica se o bit dataEncipherment está definido.</span><span class="sxs-lookup"><span data-stu-id="c5947-106">The **IsDataEnciphermentEnabled** property retrieves a Boolean value that indicates whether the dataEncipherment bit is set.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5947-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c5947-107">Syntax</span></span>


```VB
KeyUsage.IsDataEnciphermentEnabled As Boolean
```



## <a name="property-value"></a><span data-ttu-id="c5947-108">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="c5947-108">Property value</span></span>

<span data-ttu-id="c5947-109">Se for **true**, o bit dataEncipherment será definido.</span><span class="sxs-lookup"><span data-stu-id="c5947-109">If **true**, the dataEncipherment bit is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5947-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c5947-110">Requirements</span></span>



| <span data-ttu-id="c5947-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5947-111">Requirement</span></span> | <span data-ttu-id="c5947-112">Valor</span><span class="sxs-lookup"><span data-stu-id="c5947-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c5947-113">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="c5947-113">Redistributable</span></span><br/> | <span data-ttu-id="c5947-114">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="c5947-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="c5947-115">DLL</span><span class="sxs-lookup"><span data-stu-id="c5947-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="c5947-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c5947-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5947-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="c5947-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5947-118">**Uso de**</span><span class="sxs-lookup"><span data-stu-id="c5947-118">**KeyUsage**</span></span>](keyusage.md)
</dt> </dl>

 

 
