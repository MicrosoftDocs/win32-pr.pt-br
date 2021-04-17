---
description: Retorna um valor booliano que indica se a extensão EKU está marcada como crítica.
ms.assetid: f6d2a2e0-512b-44f2-a7d9-9ad661398aa8
title: Propriedade ExtendedKeyUsage. iscriticable
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedKeyUsage.IsCritical
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5331922567af3b9a34517ab5059fa03ad9904270
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749884"
---
# <a name="extendedkeyusageiscritical-property"></a><span data-ttu-id="16ace-103">Propriedade ExtendedKeyUsage. iscriticable</span><span class="sxs-lookup"><span data-stu-id="16ace-103">ExtendedKeyUsage.IsCritical property</span></span>

<span data-ttu-id="16ace-104">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="16ace-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="16ace-105">Em vez disso, use a [**classe X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="16ace-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="16ace-106">A propriedade **Iscriticad** retorna um valor booliano que indica se a extensão EKU está marcada como crítica.</span><span class="sxs-lookup"><span data-stu-id="16ace-106">The **IsCritical** property returns a Boolean value that indicates whether the EKU extension is marked critical.</span></span>

## <a name="syntax"></a><span data-ttu-id="16ace-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="16ace-107">Syntax</span></span>


```VB
ExtendedKeyUsage.IsCritical As Boolean
```



## <a name="property-value"></a><span data-ttu-id="16ace-108">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="16ace-108">Property value</span></span>

<span data-ttu-id="16ace-109">Se **for true**, a extensão EKU será marcada como crítica.</span><span class="sxs-lookup"><span data-stu-id="16ace-109">If **true**, the EKU extension is marked critical.</span></span>

## <a name="requirements"></a><span data-ttu-id="16ace-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="16ace-110">Requirements</span></span>



| <span data-ttu-id="16ace-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="16ace-111">Requirement</span></span> | <span data-ttu-id="16ace-112">Valor</span><span class="sxs-lookup"><span data-stu-id="16ace-112">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="16ace-113">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="16ace-113">End of client support</span></span><br/> | <span data-ttu-id="16ace-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="16ace-114">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="16ace-115">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="16ace-115">End of server support</span></span><br/> | <span data-ttu-id="16ace-116">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="16ace-116">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="16ace-117">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="16ace-117">Redistributable</span></span><br/>       | <span data-ttu-id="16ace-118">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="16ace-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="16ace-119">DLL</span><span class="sxs-lookup"><span data-stu-id="16ace-119">DLL</span></span><br/>                   | <dl> <span data-ttu-id="16ace-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="16ace-120"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16ace-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="16ace-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16ace-122">**ExtendedKeyUsage**</span><span class="sxs-lookup"><span data-stu-id="16ace-122">**ExtendedKeyUsage**</span></span>](extendedkeyusage.md)
</dt> </dl>

 

 
