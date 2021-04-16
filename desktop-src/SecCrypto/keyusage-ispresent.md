---
description: Recupera um valor booliano que indica se a extensão KeyUsage está presente.
ms.assetid: d666049a-4b40-42b6-8c2d-c27a1bb4c48a
title: Propriedade keyutilization. IsPresent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage.IsPresent
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: f70754c15a248cda69f93fcab2a0052bd8351261
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750752"
---
# <a name="keyusageispresent-property"></a><span data-ttu-id="e950a-103">Propriedade keyutilization. IsPresent</span><span class="sxs-lookup"><span data-stu-id="e950a-103">KeyUsage.IsPresent property</span></span>

<span data-ttu-id="e950a-104">\[A propriedade **IsPresent** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="e950a-104">\[The **IsPresent** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="e950a-105">Em vez disso, use a [**classe X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="e950a-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="e950a-106">A propriedade **IsPresent** recupera um valor booliano que indica se a extensão [**KeyUsage**](keyusage.md) está presente.</span><span class="sxs-lookup"><span data-stu-id="e950a-106">The **IsPresent** property retrieves a Boolean value that indicates whether the [**KeyUsage**](keyusage.md) extension is present.</span></span>

<span data-ttu-id="e950a-107">Essa propriedade é a propriedade padrão do objeto [**KeyUsage**](keyusage.md) .</span><span class="sxs-lookup"><span data-stu-id="e950a-107">This property is the default property of the [**KeyUsage**](keyusage.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="e950a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="e950a-108">Syntax</span></span>


```VB
KeyUsage.IsPresent As Boolean
```



## <a name="property-value"></a><span data-ttu-id="e950a-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="e950a-109">Property value</span></span>

<span data-ttu-id="e950a-110">Se for **true**, a extensão KeyUsage estará presente.</span><span class="sxs-lookup"><span data-stu-id="e950a-110">If **true**, the KeyUsage extension is present.</span></span>

## <a name="requirements"></a><span data-ttu-id="e950a-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e950a-111">Requirements</span></span>



| <span data-ttu-id="e950a-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="e950a-112">Requirement</span></span> | <span data-ttu-id="e950a-113">Valor</span><span class="sxs-lookup"><span data-stu-id="e950a-113">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e950a-114">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="e950a-114">Redistributable</span></span><br/> | <span data-ttu-id="e950a-115">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="e950a-115">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="e950a-116">DLL</span><span class="sxs-lookup"><span data-stu-id="e950a-116">DLL</span></span><br/>             | <dl> <span data-ttu-id="e950a-117"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e950a-117"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e950a-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="e950a-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e950a-119">**Uso de**</span><span class="sxs-lookup"><span data-stu-id="e950a-119">**KeyUsage**</span></span>](keyusage.md)
</dt> </dl>

 

 
