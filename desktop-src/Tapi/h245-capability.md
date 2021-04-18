---
description: A \_ enumeração de recursos H245 descreve o suporte a formatos de áudio e vídeo.
ms.assetid: 76aeb3a1-3233-4425-b9db-efacbedc309e
title: Enumeração de H245_CAPABILITY (H323priv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae7a6f81f87480f221f87680d9cf086120deb2de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105792629"
---
# <a name="h245_capability-enumeration"></a><span data-ttu-id="56ddb-103">\_Enumeração de recursos H245</span><span class="sxs-lookup"><span data-stu-id="56ddb-103">H245\_CAPABILITY enumeration</span></span>

<span data-ttu-id="56ddb-104">\[**H245 \_ A funcionalidade** não está disponível para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="56ddb-104">\[**H245\_CAPABILITY** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="56ddb-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="56ddb-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="56ddb-106">A enumeração de **\_ recursos H245** descreve o suporte a formatos de áudio e vídeo.</span><span class="sxs-lookup"><span data-stu-id="56ddb-106">The **H245\_CAPABILITY** enum describes audio and video format support.</span></span>

## <a name="syntax"></a><span data-ttu-id="56ddb-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="56ddb-107">Syntax</span></span>


```C++
} H245_CAPABILITY;
```



## <a name="constants"></a><span data-ttu-id="56ddb-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="56ddb-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="56ddb-109"><span id="HC_G711"></span><span id="hc_g711"></span>**\_G711 HC**</span><span class="sxs-lookup"><span data-stu-id="56ddb-109"><span id="HC_G711"></span><span id="hc_g711"></span>**HC\_G711**</span></span>
</dt> <dd>

<span data-ttu-id="56ddb-110">Há suporte para o protocolo de áudio G. 711.</span><span class="sxs-lookup"><span data-stu-id="56ddb-110">The G.711 audio protocol is supported.</span></span>

</dd> <dt>

<span data-ttu-id="56ddb-111"><span id="HC_G723"></span><span id="hc_g723"></span>**\_G723 HC**</span><span class="sxs-lookup"><span data-stu-id="56ddb-111"><span id="HC_G723"></span><span id="hc_g723"></span>**HC\_G723**</span></span>
</dt> <dd>

<span data-ttu-id="56ddb-112">Há suporte para o protocolo de áudio G. 723.</span><span class="sxs-lookup"><span data-stu-id="56ddb-112">The G.723 audio protocol is supported.</span></span>

</dd> <dt>

<span data-ttu-id="56ddb-113"><span id="HC_H263QCIF"></span><span id="hc_h263qcif"></span>**\_H263QCIF HC**</span><span class="sxs-lookup"><span data-stu-id="56ddb-113"><span id="HC_H263QCIF"></span><span id="hc_h263qcif"></span>**HC\_H263QCIF**</span></span>
</dt> <dd>

<span data-ttu-id="56ddb-114">Há suporte para o protocolo de vídeo H. 263.</span><span class="sxs-lookup"><span data-stu-id="56ddb-114">The H.263 video protocol is supported.</span></span>

</dd> <dt>

<span data-ttu-id="56ddb-115"><span id="HC_H261QCIF"></span><span id="hc_h261qcif"></span>**\_H261QCIF HC**</span><span class="sxs-lookup"><span data-stu-id="56ddb-115"><span id="HC_H261QCIF"></span><span id="hc_h261qcif"></span>**HC\_H261QCIF**</span></span>
</dt> <dd>

<span data-ttu-id="56ddb-116">Há suporte para o protocolo de vídeo H. 263.</span><span class="sxs-lookup"><span data-stu-id="56ddb-116">The H.263 video protocol is supported.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="56ddb-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="56ddb-117">Requirements</span></span>



| <span data-ttu-id="56ddb-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="56ddb-118">Requirement</span></span> | <span data-ttu-id="56ddb-119">Valor</span><span class="sxs-lookup"><span data-stu-id="56ddb-119">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="56ddb-120">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="56ddb-120">TAPI version</span></span><br/> | <span data-ttu-id="56ddb-121">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="56ddb-121">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="56ddb-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="56ddb-122">Header</span></span><br/>       | <dl> <span data-ttu-id="56ddb-123"><dt>H323priv. h</dt></span><span class="sxs-lookup"><span data-stu-id="56ddb-123"><dt>H323priv.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56ddb-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="56ddb-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56ddb-125">**IH323LineEx::SetDefaultCapabilityPreferrence**</span><span class="sxs-lookup"><span data-stu-id="56ddb-125">**IH323LineEx::SetDefaultCapabilityPreferrence**</span></span>](ih323lineex-setdefaultcapabilitypreferrence.md)
</dt> </dl>

 

 




