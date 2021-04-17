---
description: Recupera um valor booliano que indica se o bit keyEncipherment está definido.
ms.assetid: 2bdce181-3de7-4dc1-8059-1e1ca96c0d2d
title: Propriedade KeyUsage. IsKeyEnciphermentEnabled
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage.IsKeyEnciphermentEnabled
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: db34737954b0627953758ebc1c5bf7a64b45b1b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105787454"
---
# <a name="keyusageiskeyenciphermentenabled-property"></a><span data-ttu-id="867a5-103">Propriedade KeyUsage. IsKeyEnciphermentEnabled</span><span class="sxs-lookup"><span data-stu-id="867a5-103">KeyUsage.IsKeyEnciphermentEnabled property</span></span>

<span data-ttu-id="867a5-104">\[A propriedade **IsKeyEnciphermentEnabled** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="867a5-104">\[The **IsKeyEnciphermentEnabled** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="867a5-105">Em vez disso, use a [**classe X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="867a5-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="867a5-106">A propriedade **IsKeyEnciphermentEnabled** recupera um valor booliano que indica se o bit keyEncipherment está definido.</span><span class="sxs-lookup"><span data-stu-id="867a5-106">The **IsKeyEnciphermentEnabled** property retrieves a Boolean value that indicates whether the keyEncipherment bit is set.</span></span>

## <a name="syntax"></a><span data-ttu-id="867a5-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="867a5-107">Syntax</span></span>


```VB
KeyUsage.IsKeyEnciphermentEnabled As Boolean
```



## <a name="property-value"></a><span data-ttu-id="867a5-108">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="867a5-108">Property value</span></span>

<span data-ttu-id="867a5-109">Se for **true**, o bit keyEncipherment será definido.</span><span class="sxs-lookup"><span data-stu-id="867a5-109">If **true**, the keyEncipherment bit is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="867a5-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="867a5-110">Requirements</span></span>



| <span data-ttu-id="867a5-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="867a5-111">Requirement</span></span> | <span data-ttu-id="867a5-112">Valor</span><span class="sxs-lookup"><span data-stu-id="867a5-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="867a5-113">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="867a5-113">Redistributable</span></span><br/> | <span data-ttu-id="867a5-114">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="867a5-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="867a5-115">DLL</span><span class="sxs-lookup"><span data-stu-id="867a5-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="867a5-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="867a5-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="867a5-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="867a5-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="867a5-118">**Uso de**</span><span class="sxs-lookup"><span data-stu-id="867a5-118">**KeyUsage**</span></span>](keyusage.md)
</dt> </dl>

 

 
