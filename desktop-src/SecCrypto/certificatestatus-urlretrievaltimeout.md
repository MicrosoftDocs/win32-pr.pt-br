---
description: Define ou recupera o período de tempo antes que uma URL seja determinada como inacessível.
ms.assetid: f39dafc4-6017-463c-aeee-948b6173862a
title: Propriedade CertificateStatus. UrlRetrievalTimeout
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.UrlRetrievalTimeout
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: fcaaafa1f2e870195b612eb225696f2c23a80ee1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105788113"
---
# <a name="certificatestatusurlretrievaltimeout-property"></a><span data-ttu-id="a4e85-103">Propriedade CertificateStatus. UrlRetrievalTimeout</span><span class="sxs-lookup"><span data-stu-id="a4e85-103">CertificateStatus.UrlRetrievalTimeout property</span></span>

<span data-ttu-id="a4e85-104">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a4e85-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="a4e85-105">Em vez disso, use a [**estrutura X509ChainStatus**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="a4e85-105">Instead, use the [**X509ChainStatus Structure**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="a4e85-106">A propriedade **UrlRetrievalTimeout** define ou recupera o período de tempo antes que uma URL seja determinada como inacessível.</span><span class="sxs-lookup"><span data-stu-id="a4e85-106">The **UrlRetrievalTimeout** property sets or retrieves the length of time before a URL is determined to be unreachable.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4e85-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a4e85-107">Syntax</span></span>


```VB
CertificateStatus.UrlRetrievalTimeout As Long
```



## <a name="property-value"></a><span data-ttu-id="a4e85-108">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="a4e85-108">Property value</span></span>

<span data-ttu-id="a4e85-109">O número de segundos antes que uma URL seja determinada como inacessível.</span><span class="sxs-lookup"><span data-stu-id="a4e85-109">The number of seconds before a URL is determined to be unreachable.</span></span>

## <a name="remarks"></a><span data-ttu-id="a4e85-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="a4e85-110">Remarks</span></span>

<span data-ttu-id="a4e85-111">Se essa propriedade não for definida, o tempo limite padrão será de 15 segundos.</span><span class="sxs-lookup"><span data-stu-id="a4e85-111">If this property is not set, the default time-out is 15 seconds.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4e85-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a4e85-112">Requirements</span></span>



| <span data-ttu-id="a4e85-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="a4e85-113">Requirement</span></span> | <span data-ttu-id="a4e85-114">Valor</span><span class="sxs-lookup"><span data-stu-id="a4e85-114">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a4e85-115">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="a4e85-115">End of client support</span></span><br/> | <span data-ttu-id="a4e85-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a4e85-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="a4e85-117">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="a4e85-117">End of server support</span></span><br/> | <span data-ttu-id="a4e85-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a4e85-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="a4e85-119">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="a4e85-119">Redistributable</span></span><br/>       | <span data-ttu-id="a4e85-120">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="a4e85-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="a4e85-121">DLL</span><span class="sxs-lookup"><span data-stu-id="a4e85-121">DLL</span></span><br/>                   | <dl> <span data-ttu-id="a4e85-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a4e85-122"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
