---
description: Recupera um valor booliano que indica se o bit CRLSign está definido.
ms.assetid: 76ca86e3-55f7-4720-9fa5-d465db2a7b5a
title: Propriedade KeyUsage. IsCRLSignEnabled
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage.IsCRLSignEnabled
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 39bd8509ebc89719e5d06e5e60a300ec2cd9949a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105770331"
---
# <a name="keyusageiscrlsignenabled-property"></a><span data-ttu-id="bbefd-103">Propriedade KeyUsage. IsCRLSignEnabled</span><span class="sxs-lookup"><span data-stu-id="bbefd-103">KeyUsage.IsCRLSignEnabled property</span></span>

<span data-ttu-id="bbefd-104">\[A propriedade **IsCRLSignEnabled** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="bbefd-104">\[The **IsCRLSignEnabled** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="bbefd-105">Em vez disso, use a [**classe X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="bbefd-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="bbefd-106">A propriedade **IsCRLSignEnabled** recupera um valor booliano que indica se o bit CRLSign está definido.</span><span class="sxs-lookup"><span data-stu-id="bbefd-106">The **IsCRLSignEnabled** property retrieves a Boolean value that indicates whether the CRLSign bit is set.</span></span>

## <a name="syntax"></a><span data-ttu-id="bbefd-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="bbefd-107">Syntax</span></span>


```VB
KeyUsage.IsCRLSignEnabled As Boolean
```



## <a name="property-value"></a><span data-ttu-id="bbefd-108">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="bbefd-108">Property value</span></span>

<span data-ttu-id="bbefd-109">Se for **true**, o bit CRLSign será definido.</span><span class="sxs-lookup"><span data-stu-id="bbefd-109">If **true**, the CRLSign bit is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="bbefd-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bbefd-110">Requirements</span></span>



| <span data-ttu-id="bbefd-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="bbefd-111">Requirement</span></span> | <span data-ttu-id="bbefd-112">Valor</span><span class="sxs-lookup"><span data-stu-id="bbefd-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bbefd-113">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="bbefd-113">Redistributable</span></span><br/> | <span data-ttu-id="bbefd-114">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="bbefd-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="bbefd-115">DLL</span><span class="sxs-lookup"><span data-stu-id="bbefd-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="bbefd-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bbefd-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bbefd-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="bbefd-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbefd-118">**Uso de**</span><span class="sxs-lookup"><span data-stu-id="bbefd-118">**KeyUsage**</span></span>](keyusage.md)
</dt> </dl>

 

 
