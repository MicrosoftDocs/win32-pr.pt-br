---
title: Motivos de inacessibilidade
description: A tabela a seguir lista os valores constantes que indicam por que uma interface está inacessível.
ms.assetid: 55c0519e-02c8-4a04-bed9-9fe94327a4b6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8b99d36ba895394a417130ab3ae45d1a47c7ed6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007898"
---
# <a name="unreachability-reasons"></a><span data-ttu-id="48438-103">Motivos de inacessibilidade</span><span class="sxs-lookup"><span data-stu-id="48438-103">Unreachability Reasons</span></span>

<span data-ttu-id="48438-104">A tabela a seguir lista os valores constantes que indicam por que uma interface está inacessível.</span><span class="sxs-lookup"><span data-stu-id="48438-104">The following table lists constant values that indicate why an interface is unreachable.</span></span>



| <span data-ttu-id="48438-105">Valor</span><span class="sxs-lookup"><span data-stu-id="48438-105">Value</span></span>                                       | <span data-ttu-id="48438-106">Significado</span><span class="sxs-lookup"><span data-stu-id="48438-106">Meaning</span></span>                                                                                        |
|---------------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48438-107">\_administrador da interface MPR \_ \_ desabilitado</span><span class="sxs-lookup"><span data-stu-id="48438-107">MPR\_INTERFACE\_ADMIN\_DISABLED</span></span>             | <span data-ttu-id="48438-108">O administrador desabilitou a interface.</span><span class="sxs-lookup"><span data-stu-id="48438-108">The administrator has disabled the interface.</span></span>                                                  |
| <span data-ttu-id="48438-109">\_ \_ falha na conexão da interface MPR \_</span><span class="sxs-lookup"><span data-stu-id="48438-109">MPR\_INTERFACE\_CONNECTION\_FAILURE</span></span>         | <span data-ttu-id="48438-110">Falha na tentativa de conexão anterior.</span><span class="sxs-lookup"><span data-stu-id="48438-110">The previous connection attempt failed.</span></span> <span data-ttu-id="48438-111">Examine o membro **dwLastError** do código de erro.</span><span class="sxs-lookup"><span data-stu-id="48438-111">Look at the **dwLastError** member for the error code.</span></span> |
| <span data-ttu-id="48438-112">\_restrição de \_ horas de discagem da interface MPR \_ \_</span><span class="sxs-lookup"><span data-stu-id="48438-112">MPR\_INTERFACE\_DIALOUT\_HOURS\_RESTRICTION</span></span> | <span data-ttu-id="48438-113">A conexão discada não é permitida no momento atual.</span><span class="sxs-lookup"><span data-stu-id="48438-113">Dial-out is not allowed at the current time.</span></span>                                                   |
| <span data-ttu-id="48438-114">\_interface \_ de MPR \_ sem \_ recursos</span><span class="sxs-lookup"><span data-stu-id="48438-114">MPR\_INTERFACE\_OUT\_OF\_RESOURCES</span></span>          | <span data-ttu-id="48438-115">Não há portas ou dispositivos disponíveis para uso.</span><span class="sxs-lookup"><span data-stu-id="48438-115">No ports or devices are available for use.</span></span>                                                     |
| <span data-ttu-id="48438-116">serviço de interface de MPR em \_ \_ \_ pausa</span><span class="sxs-lookup"><span data-stu-id="48438-116">MPR\_INTERFACE\_SERVICE\_PAUSED</span></span>             | <span data-ttu-id="48438-117">O serviço está em pausa.</span><span class="sxs-lookup"><span data-stu-id="48438-117">The service is paused.</span></span>                                                                         |
| <span data-ttu-id="48438-118">\_interface MPR \_ sem \_ sensor de mídia \_</span><span class="sxs-lookup"><span data-stu-id="48438-118">MPR\_INTERFACE\_NO\_MEDIA\_SENSE</span></span>            | <span data-ttu-id="48438-119">O cabo de rede está desconectado da placa de rede.</span><span class="sxs-lookup"><span data-stu-id="48438-119">The network cable is disconnected from the network card.</span></span>                                       |
| <span data-ttu-id="48438-120">INTERFACE de MPR \_ \_ sem \_ dispositivo</span><span class="sxs-lookup"><span data-stu-id="48438-120">MPR\_INTERFACE\_NO\_DEVICE</span></span>                  | <span data-ttu-id="48438-121">A placa de rede foi removida do computador.</span><span class="sxs-lookup"><span data-stu-id="48438-121">The network card has been removed from the machine.</span></span>                                            |



 

## <a name="related-topics"></a><span data-ttu-id="48438-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="48438-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="48438-123">**INTERFACE de MPR \_ \_ 0**</span><span class="sxs-lookup"><span data-stu-id="48438-123">**MPR\_INTERFACE\_0**</span></span>](/windows/desktop/api/Mprapi/ns-mprapi-mpr_interface_0)
</dt> <dt>

[<span data-ttu-id="48438-124">**INTERFACE de MPR \_ \_ 1**</span><span class="sxs-lookup"><span data-stu-id="48438-124">**MPR\_INTERFACE\_1**</span></span>](/windows/desktop/api/Mprapi/ns-mprapi-mpr_interface_1)
</dt> <dt>

[<span data-ttu-id="48438-125">**\_IFROW MIB**</span><span class="sxs-lookup"><span data-stu-id="48438-125">**MIB\_IFROW**</span></span>](/windows/desktop/api/ifmib/ns-ifmib-mib_ifrow)
</dt> <dt>

[<span data-ttu-id="48438-126">**\_IFSTATUS MIB**</span><span class="sxs-lookup"><span data-stu-id="48438-126">**MIB\_IFSTATUS**</span></span>](/windows/desktop/api/iprtrmib/ns-iprtrmib-mib_ifstatus)
</dt> </dl>

 

 