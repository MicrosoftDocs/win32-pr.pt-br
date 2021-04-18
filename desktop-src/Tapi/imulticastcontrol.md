---
description: A interface IMulticastControl é implementada pelo IPConf MSP e disponível somente em objetos de chamada multicast.
ms.assetid: 9bdb4ab9-30b3-46fb-b13a-de9c294c8046
title: Interface IMulticastControl (Confpriv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98ad006ea41034d6d4da32359d1ecbcdd250ab6b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761964"
---
# <a name="imulticastcontrol-interface"></a><span data-ttu-id="1c92b-103">Interface IMulticastControl</span><span class="sxs-lookup"><span data-stu-id="1c92b-103">IMulticastControl interface</span></span>

<span data-ttu-id="1c92b-104">\[O **IMulticastControl** não está disponível para uso no Windows Vista, no windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="1c92b-104">\[**IMulticastControl** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="1c92b-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="1c92b-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="1c92b-106">A interface **IMulticastControl** é implementada pelo IPConf msp e disponível somente em objetos de chamada multicast.</span><span class="sxs-lookup"><span data-stu-id="1c92b-106">The **IMulticastControl** interface is implemented by the IPConf MSP and available only on multicast call objects.</span></span> <span data-ttu-id="1c92b-107">Essa interface expõe métodos que permitem a criação e manipulação de terminais que podem se comunicar entre clientes do H323 e do SDP.</span><span class="sxs-lookup"><span data-stu-id="1c92b-107">This interface exposes methods that enable creation and manipulation of terminals that can communicate between H323 and SDP clients.</span></span> <span data-ttu-id="1c92b-108">A interface **IMulticastControl** controla o modo de loopback multicast.</span><span class="sxs-lookup"><span data-stu-id="1c92b-108">The **IMulticastControl** interface controls the multicast loopback mode.</span></span>

<span data-ttu-id="1c92b-109">No modo MM \_ sem \_ loopback, o loopback multicast está desabilitado, o que significa que dois aplicativos no mesmo computador que ingressam no mesmo grupo de multicast receberão os pacotes uns dos outros.</span><span class="sxs-lookup"><span data-stu-id="1c92b-109">In the MM\_NO\_LOOPBACK mode, multicast loopback is disabled, which means two applications on the same machine who join the same multicast group will get each other's packets.</span></span> <span data-ttu-id="1c92b-110">Esse modo tem o melhor desempenho se sempre houver apenas um aplicativo ingressando no grupo de multicast no computador.</span><span class="sxs-lookup"><span data-stu-id="1c92b-110">This mode has the best performance if there is always only one application joining the multicast group on the machine.</span></span> <span data-ttu-id="1c92b-111">MM \_ nenhum \_ modo de loopback é o modo padrão.</span><span class="sxs-lookup"><span data-stu-id="1c92b-111">MM\_NO\_LOOPBACK mode is the default mode.</span></span>

<span data-ttu-id="1c92b-112">O \_ modo de \_ auto-retorno completo mm é bom apenas para teste.</span><span class="sxs-lookup"><span data-stu-id="1c92b-112">The MM\_FULL\_LOOPBACK mode is good only for testing.</span></span> <span data-ttu-id="1c92b-113">Todos os pacotes enviados também são reproduzidos em loop.</span><span class="sxs-lookup"><span data-stu-id="1c92b-113">All the packets sent out are looped back as well.</span></span> <span data-ttu-id="1c92b-114">Isso pode ser usado para testar se os dispositivos estão funcionando.</span><span class="sxs-lookup"><span data-stu-id="1c92b-114">This can be used to test if the devices are working.</span></span>

<span data-ttu-id="1c92b-115">O \_ modo de \_ auto-retorno seletivo mm é usado para permitir que vários aplicativos em um computador ingressem no mesmo grupo de multicast.</span><span class="sxs-lookup"><span data-stu-id="1c92b-115">The MM\_SELECTIVE\_LOOPBACK mode is used to enable multiple applications on one machine to join the same multicast group.</span></span> <span data-ttu-id="1c92b-116">Os pacotes são reproduzidos em loop da pilha e cada sessão RTP é responsável por filtrar pacotes indesejados.</span><span class="sxs-lookup"><span data-stu-id="1c92b-116">The packets are looped back from the stack, and each RTP session is responsible for filtering out unwanted packets.</span></span>

## <a name="members"></a><span data-ttu-id="1c92b-117">Membros</span><span class="sxs-lookup"><span data-stu-id="1c92b-117">Members</span></span>

<span data-ttu-id="1c92b-118">A interface **IMulticastControl** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="1c92b-118">The **IMulticastControl** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="1c92b-119">**IMulticastControl** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="1c92b-119">**IMulticastControl** also has these types of members:</span></span>

-   [<span data-ttu-id="1c92b-120">Métodos</span><span class="sxs-lookup"><span data-stu-id="1c92b-120">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="1c92b-121">Métodos</span><span class="sxs-lookup"><span data-stu-id="1c92b-121">Methods</span></span>

<span data-ttu-id="1c92b-122">A interface **IMulticastControl** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="1c92b-122">The **IMulticastControl** interface has these methods.</span></span>



| <span data-ttu-id="1c92b-123">Método</span><span class="sxs-lookup"><span data-stu-id="1c92b-123">Method</span></span>                                                          | <span data-ttu-id="1c92b-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="1c92b-124">Description</span></span>                                  |
|:----------------------------------------------------------------|:---------------------------------------------|
| [<span data-ttu-id="1c92b-125">**obter \_ loopbackmode**</span><span class="sxs-lookup"><span data-stu-id="1c92b-125">**get\_LoopbackMode**</span></span>](imulticastcontrol-get-loopbackmode.md) | <span data-ttu-id="1c92b-126">Obtém o modo de loopback multicast.</span><span class="sxs-lookup"><span data-stu-id="1c92b-126">Gets the multicast loopback mode.</span></span><br/> |
| [<span data-ttu-id="1c92b-127">**colocar \_ loopbackmode**</span><span class="sxs-lookup"><span data-stu-id="1c92b-127">**put\_LoopbackMode**</span></span>](imulticastcontrol-put-loopbackmode.md) | <span data-ttu-id="1c92b-128">Define o modo de loopback multicast.</span><span class="sxs-lookup"><span data-stu-id="1c92b-128">Sets the multicast loopback mode.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="1c92b-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1c92b-129">Requirements</span></span>



| <span data-ttu-id="1c92b-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c92b-130">Requirement</span></span> | <span data-ttu-id="1c92b-131">Valor</span><span class="sxs-lookup"><span data-stu-id="1c92b-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1c92b-132">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="1c92b-132">TAPI version</span></span><br/> | <span data-ttu-id="1c92b-133">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="1c92b-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="1c92b-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1c92b-134">Header</span></span><br/>       | <dl> <span data-ttu-id="1c92b-135"><dt>Confpriv. h</dt></span><span class="sxs-lookup"><span data-stu-id="1c92b-135"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="1c92b-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1c92b-136">Library</span></span><br/>      | <dl> <span data-ttu-id="1c92b-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1c92b-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="1c92b-138">DLL</span><span class="sxs-lookup"><span data-stu-id="1c92b-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="1c92b-139"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1c92b-139"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="1c92b-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="1c92b-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c92b-141">IPConf MSP</span><span class="sxs-lookup"><span data-stu-id="1c92b-141">IPConf MSP</span></span>](ipconf-msp.md)
</dt> </dl>

 

