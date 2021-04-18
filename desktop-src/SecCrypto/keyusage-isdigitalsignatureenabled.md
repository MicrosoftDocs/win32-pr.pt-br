---
description: Recupera um valor booliano que indica se o bit digitalSignature está definido.
ms.assetid: 561eea86-ff23-4a26-adf2-b43009566eaa
title: Propriedade KeyUsage. IsDigitalSignatureEnabled
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage.IsDigitalSignatureEnabled
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 3b323effebe60597e1d6cf66e75d48c39fcdca4f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760388"
---
# <a name="keyusageisdigitalsignatureenabled-property"></a><span data-ttu-id="d7fd3-103">Propriedade KeyUsage. IsDigitalSignatureEnabled</span><span class="sxs-lookup"><span data-stu-id="d7fd3-103">KeyUsage.IsDigitalSignatureEnabled property</span></span>

<span data-ttu-id="d7fd3-104">\[A propriedade **IsDigitalSignatureEnabled** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-104">\[The **IsDigitalSignatureEnabled** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="d7fd3-105">Em vez disso, use a [**classe X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="d7fd3-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="d7fd3-106">A propriedade **IsDigitalSignatureEnabled** recupera um valor booliano que indica se o bit DigitalSignature está definido.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-106">The **IsDigitalSignatureEnabled** property retrieves a Boolean value that indicates whether the digitalSignature bit is set.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7fd3-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d7fd3-107">Syntax</span></span>


```VB
KeyUsage.IsDigitalSignatureEnabled As Boolean
```



## <a name="property-value"></a><span data-ttu-id="d7fd3-108">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="d7fd3-108">Property value</span></span>

<span data-ttu-id="d7fd3-109">Se for **true**, o bit DigitalSignature será definido.</span><span class="sxs-lookup"><span data-stu-id="d7fd3-109">If **true**, the digitalSignature bit is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7fd3-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d7fd3-110">Requirements</span></span>



| <span data-ttu-id="d7fd3-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7fd3-111">Requirement</span></span> | <span data-ttu-id="d7fd3-112">Valor</span><span class="sxs-lookup"><span data-stu-id="d7fd3-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d7fd3-113">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="d7fd3-113">Redistributable</span></span><br/> | <span data-ttu-id="d7fd3-114">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="d7fd3-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="d7fd3-115">DLL</span><span class="sxs-lookup"><span data-stu-id="d7fd3-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="d7fd3-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d7fd3-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7fd3-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="d7fd3-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7fd3-118">**Uso de**</span><span class="sxs-lookup"><span data-stu-id="d7fd3-118">**KeyUsage**</span></span>](keyusage.md)
</dt> </dl>

 

 
