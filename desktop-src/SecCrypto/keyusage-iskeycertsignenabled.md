---
description: Recupera um valor booliano que indica se o bit keyCertSign está definido.
ms.assetid: c0331293-4a65-40f0-a404-87d8546349c2
title: Propriedade KeyUsage. IsKeyCertSignEnabled
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage.IsKeyCertSignEnabled
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d475565896910f76211e3843526e9a889586efa0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761863"
---
# <a name="keyusageiskeycertsignenabled-property"></a><span data-ttu-id="e1ee1-103">Propriedade KeyUsage. IsKeyCertSignEnabled</span><span class="sxs-lookup"><span data-stu-id="e1ee1-103">KeyUsage.IsKeyCertSignEnabled property</span></span>

<span data-ttu-id="e1ee1-104">\[A propriedade **IsKeyCertSignEnabled** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="e1ee1-104">\[The **IsKeyCertSignEnabled** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="e1ee1-105">Em vez disso, use a [**classe X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="e1ee1-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="e1ee1-106">A propriedade **IsKeyCertSignEnabled** recupera um valor booliano que indica se o bit keyCertSign está definido.</span><span class="sxs-lookup"><span data-stu-id="e1ee1-106">The **IsKeyCertSignEnabled** property retrieves a Boolean value that indicates whether the keyCertSign bit is set.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1ee1-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e1ee1-107">Syntax</span></span>


```VB
KeyUsage.IsKeyCertSignEnabled As Boolean
```



## <a name="property-value"></a><span data-ttu-id="e1ee1-108">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="e1ee1-108">Property value</span></span>

<span data-ttu-id="e1ee1-109">Se for **true**, o bit keyCertSign será definido.</span><span class="sxs-lookup"><span data-stu-id="e1ee1-109">If **true**, the keyCertSign bit is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1ee1-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e1ee1-110">Requirements</span></span>



| <span data-ttu-id="e1ee1-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1ee1-111">Requirement</span></span> | <span data-ttu-id="e1ee1-112">Valor</span><span class="sxs-lookup"><span data-stu-id="e1ee1-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e1ee1-113">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="e1ee1-113">Redistributable</span></span><br/> | <span data-ttu-id="e1ee1-114">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="e1ee1-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="e1ee1-115">DLL</span><span class="sxs-lookup"><span data-stu-id="e1ee1-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="e1ee1-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e1ee1-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1ee1-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="e1ee1-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1ee1-118">**Uso de**</span><span class="sxs-lookup"><span data-stu-id="e1ee1-118">**KeyUsage**</span></span>](keyusage.md)
</dt> </dl>

 

 
