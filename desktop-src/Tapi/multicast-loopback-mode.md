---
description: A \_ enumeração do modo de loopback multicast \_ descreve o modo de loopback multicast.
ms.assetid: bf9c3665-71cc-4cde-9ad4-1a8b62eddf9f
title: Enumeração de MULTICAST_LOOPBACK_MODE (Confpriv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a15505efcd1a9e399866b104da0582ccf846689
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761951"
---
# <a name="multicast_loopback_mode-enumeration"></a><span data-ttu-id="92ca7-103">Enumeração do modo de \_ loopback multicast \_</span><span class="sxs-lookup"><span data-stu-id="92ca7-103">MULTICAST\_LOOPBACK\_MODE enumeration</span></span>

<span data-ttu-id="92ca7-104">\[**Multicast \_ O \_ modo de loopback** não está disponível para uso no Windows Vista, no windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="92ca7-104">\[**MULTICAST\_LOOPBACK\_MODE** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="92ca7-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="92ca7-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="92ca7-106">A enumeração do **\_ \_ modo de loopback multicast** descreve o modo de loopback multicast.</span><span class="sxs-lookup"><span data-stu-id="92ca7-106">The **MULTICAST\_LOOPBACK\_MODE** enum describes the multicast loopback mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="92ca7-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="92ca7-107">Syntax</span></span>


```C++
} MULTICAST_LOOPBACK_MODE;
```



## <a name="constants"></a><span data-ttu-id="92ca7-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="92ca7-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="92ca7-109"><span id="MM_NO_LOOPBACK"></span><span id="mm_no_loopback"></span>**MM \_ sem \_ loopback**</span><span class="sxs-lookup"><span data-stu-id="92ca7-109"><span id="MM_NO_LOOPBACK"></span><span id="mm_no_loopback"></span>**MM\_NO\_LOOPBACK**</span></span>
</dt> <dd>

<span data-ttu-id="92ca7-110">O loopback multicast está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="92ca7-110">Multicast loopback is disabled.</span></span> <span data-ttu-id="92ca7-111">Isso significa que dois aplicativos no mesmo computador que ingressam no mesmo grupo de multicast podem obter os pacotes uns dos outros.</span><span class="sxs-lookup"><span data-stu-id="92ca7-111">That means two applications on the same machine joining the same multicast group can get each other's packets.</span></span>

</dd> <dt>

<span data-ttu-id="92ca7-112"><span id="MM_FULL_LOOPBACK"></span><span id="mm_full_loopback"></span>**\_auto-retorno completo \_ mm**</span><span class="sxs-lookup"><span data-stu-id="92ca7-112"><span id="MM_FULL_LOOPBACK"></span><span id="mm_full_loopback"></span>**MM\_FULL\_LOOPBACK**</span></span>
</dt> <dd>

<span data-ttu-id="92ca7-113">Todos os pacotes enviados também são reproduzidos em loop.</span><span class="sxs-lookup"><span data-stu-id="92ca7-113">All the packets sent out are looped back as well.</span></span> <span data-ttu-id="92ca7-114">Esse modo é útil apenas para teste.</span><span class="sxs-lookup"><span data-stu-id="92ca7-114">This mode is useful only for testing.</span></span>

</dd> <dt>

<span data-ttu-id="92ca7-115"><span id="MM_SELECTIVE_LOOPBACK"></span><span id="mm_selective_loopback"></span>**\_loopback seletivo \_ mm**</span><span class="sxs-lookup"><span data-stu-id="92ca7-115"><span id="MM_SELECTIVE_LOOPBACK"></span><span id="mm_selective_loopback"></span>**MM\_SELECTIVE\_LOOPBACK**</span></span>
</dt> <dd>

<span data-ttu-id="92ca7-116">O loopback seletivo está habilitado.</span><span class="sxs-lookup"><span data-stu-id="92ca7-116">Selective loopback is enabled.</span></span> <span data-ttu-id="92ca7-117">Isso significa que vários aplicativos habilitados em um computador podem ingressar no mesmo grupo de multicast sem confusão.</span><span class="sxs-lookup"><span data-stu-id="92ca7-117">That means enabled multiple applications on one machine can join the same multicast group without confusion.</span></span> <span data-ttu-id="92ca7-118">Os pacotes são reproduzidos em loop da pilha e cada sessão RTP é responsável por filtrar pacotes indesejados.</span><span class="sxs-lookup"><span data-stu-id="92ca7-118">The packets are looped back from the stack and each RTP session is responsible for filtering out unwanted packets.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="92ca7-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="92ca7-119">Requirements</span></span>



| <span data-ttu-id="92ca7-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="92ca7-120">Requirement</span></span> | <span data-ttu-id="92ca7-121">Valor</span><span class="sxs-lookup"><span data-stu-id="92ca7-121">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="92ca7-122">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="92ca7-122">TAPI version</span></span><br/> | <span data-ttu-id="92ca7-123">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="92ca7-123">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="92ca7-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="92ca7-124">Header</span></span><br/>       | <dl> <span data-ttu-id="92ca7-125"><dt>Confpriv. h</dt></span><span class="sxs-lookup"><span data-stu-id="92ca7-125"><dt>Confpriv.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92ca7-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="92ca7-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92ca7-127">**IMulticastControl:: obter \_ loopbackmode**</span><span class="sxs-lookup"><span data-stu-id="92ca7-127">**IMulticastControl::get\_LoopbackMode**</span></span>](imulticastcontrol-get-loopbackmode.md)
</dt> <dt>

[<span data-ttu-id="92ca7-128">**IMulticastControl::p UT \_ loopbackmode**</span><span class="sxs-lookup"><span data-stu-id="92ca7-128">**IMulticastControl::put\_LoopbackMode**</span></span>](imulticastcontrol-put-loopbackmode.md)
</dt> </dl>

 

 




