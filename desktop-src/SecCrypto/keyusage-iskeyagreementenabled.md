---
description: Recupera um valor booliano que indica se o bit do keyagreement está definido.
ms.assetid: 3dd1f6c7-893d-453e-92dc-ffeffd879519
title: Propriedade KeyUsage. IsKeyAgreementEnabled
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage.IsKeyAgreementEnabled
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 74369996d9e525746e315d1dd2934ef854ffd110
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811055"
---
# <a name="keyusageiskeyagreementenabled-property"></a><span data-ttu-id="c856b-103">Propriedade KeyUsage. IsKeyAgreementEnabled</span><span class="sxs-lookup"><span data-stu-id="c856b-103">KeyUsage.IsKeyAgreementEnabled property</span></span>

<span data-ttu-id="c856b-104">\[A propriedade **IsKeyAgreementEnabled** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="c856b-104">\[The **IsKeyAgreementEnabled** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="c856b-105">Em vez disso, use a [**classe X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="c856b-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="c856b-106">A propriedade **IsKeyAgreementEnabled** recupera um valor booliano que indica se o bit do keyagreement está definido.</span><span class="sxs-lookup"><span data-stu-id="c856b-106">The **IsKeyAgreementEnabled** property retrieves a Boolean value that indicates whether the keyAgreement bit is set.</span></span>

## <a name="syntax"></a><span data-ttu-id="c856b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c856b-107">Syntax</span></span>


```VB
KeyUsage.IsKeyAgreementEnabled As Boolean
```



## <a name="property-value"></a><span data-ttu-id="c856b-108">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="c856b-108">Property value</span></span>

<span data-ttu-id="c856b-109">Se for **true**, o bit keyagreement será definido.</span><span class="sxs-lookup"><span data-stu-id="c856b-109">If **true**, the keyAgreement bit is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="c856b-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c856b-110">Requirements</span></span>



| <span data-ttu-id="c856b-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="c856b-111">Requirement</span></span> | <span data-ttu-id="c856b-112">Valor</span><span class="sxs-lookup"><span data-stu-id="c856b-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c856b-113">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="c856b-113">Redistributable</span></span><br/> | <span data-ttu-id="c856b-114">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="c856b-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="c856b-115">DLL</span><span class="sxs-lookup"><span data-stu-id="c856b-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="c856b-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c856b-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c856b-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="c856b-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c856b-118">**Uso de**</span><span class="sxs-lookup"><span data-stu-id="c856b-118">**KeyUsage**</span></span>](keyusage.md)
</dt> </dl>

 

 
