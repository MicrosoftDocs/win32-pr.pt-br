---
title: Serviços de Área de Trabalho Remota tipos de enumeração de API
description: Lista os tipos de enumeração que são usados com a API de Serviços de Área de Trabalho Remota.
ms.assetid: b5ef61e2-07fa-4963-9b9b-977cc04dab10
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9523a7528fddff4e2dbcf6dde16c29084d4811d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292341"
---
# <a name="remote-desktop-services-api-enumeration-types"></a><span data-ttu-id="42b72-103">Serviços de Área de Trabalho Remota tipos de enumeração de API</span><span class="sxs-lookup"><span data-stu-id="42b72-103">Remote Desktop Services API Enumeration Types</span></span>

<span data-ttu-id="42b72-104">Os tipos de enumeração a seguir são usados com a API Serviços de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="42b72-104">The following enumeration types are used with the Remote Desktop Services API.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="42b72-105">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="42b72-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="42b72-106">**\_classe de configuração WTS \_**</span><span class="sxs-lookup"><span data-stu-id="42b72-106">**WTS\_CONFIG\_CLASS**</span></span>](/windows/desktop/api/Wtsapi32/ne-wtsapi32-wts_config_class)
</dt> <dd>

<span data-ttu-id="42b72-107">Contém valores que indicam o tipo de informações de configuração do usuário a serem definidas ou recuperadas em uma chamada para as funções [**WTSQueryUserConfig**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsqueryuserconfiga) e [**WTSSetUserConfig**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtssetuserconfiga) .</span><span class="sxs-lookup"><span data-stu-id="42b72-107">Contains values that indicate the type of user configuration information to set or retrieve in a call to the [**WTSQueryUserConfig**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsqueryuserconfiga) and [**WTSSetUserConfig**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtssetuserconfiga) functions.</span></span>

</dd> <dt>

[<span data-ttu-id="42b72-108">**\_origem de configuração do WTS \_**</span><span class="sxs-lookup"><span data-stu-id="42b72-108">**WTS\_CONFIG\_SOURCE**</span></span>](/windows/desktop/api/Wtsapi32/ne-wtsapi32-wts_config_source)
</dt> <dd>

<span data-ttu-id="42b72-109">Especifica a fonte de informações de configuração retornada pela função [**WTSQueryUserConfig**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsqueryuserconfiga) .</span><span class="sxs-lookup"><span data-stu-id="42b72-109">Specifies the source of configuration information returned by the [**WTSQueryUserConfig**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsqueryuserconfiga) function.</span></span>

</dd> <dt>

[<span data-ttu-id="42b72-110">**\_classe WTS connectstate \_**</span><span class="sxs-lookup"><span data-stu-id="42b72-110">**WTS\_CONNECTSTATE\_CLASS**</span></span>](/windows/desktop/api/Wtsapi32/ne-wtsapi32-wts_connectstate_class)
</dt> <dd>

<span data-ttu-id="42b72-111">Especifica o estado de conexão de uma sessão de Serviços de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="42b72-111">Specifies the connection state of a Remote Desktop Services session.</span></span>

</dd> <dt>

[<span data-ttu-id="42b72-112">**\_classe de informações de WTS \_**</span><span class="sxs-lookup"><span data-stu-id="42b72-112">**WTS\_INFO\_CLASS**</span></span>](/windows/desktop/api/Wtsapi32/ne-wtsapi32-wts_info_class)
</dt> <dd>

<span data-ttu-id="42b72-113">Contém valores que indicam o tipo de informações de sessão a serem recuperadas em uma chamada para a função [**WTSQuerySessionInformation**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsquerysessioninformationa) .</span><span class="sxs-lookup"><span data-stu-id="42b72-113">Contains values that indicate the type of session information to retrieve in a call to the [**WTSQuerySessionInformation**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsquerysessioninformationa) function.</span></span>

</dd> <dt>

[<span data-ttu-id="42b72-114">**\_classe de tipo WTS \_**</span><span class="sxs-lookup"><span data-stu-id="42b72-114">**WTS\_TYPE\_CLASS**</span></span>](/windows/desktop/api/Wtsapi32/ne-wtsapi32-wts_type_class)
</dt> <dd>

<span data-ttu-id="42b72-115">Especifica o tipo de estrutura que uma função de Serviços de Área de Trabalho Remota retornou em um buffer.</span><span class="sxs-lookup"><span data-stu-id="42b72-115">Specifies the type of structure that a Remote Desktop Services function has returned in a buffer.</span></span>

</dd> <dt>

[<span data-ttu-id="42b72-116">**\_classe virtual \_ WTS**</span><span class="sxs-lookup"><span data-stu-id="42b72-116">**WTS\_VIRTUAL\_CLASS**</span></span>](/windows/desktop/api/Wtsapi32/ne-wtsapi32-wts_virtual_class)
</dt> <dd>

<span data-ttu-id="42b72-117">Contém valores que indicam o tipo de informações de canal virtual a serem recuperadas.</span><span class="sxs-lookup"><span data-stu-id="42b72-117">Contains values that indicate the type of virtual channel information to retrieve.</span></span>

</dd> <dt>

[<span data-ttu-id="42b72-118">**\_família de endereços WTSSBX \_**</span><span class="sxs-lookup"><span data-stu-id="42b72-118">**WTSSBX\_ADDRESS\_FAMILY**</span></span>](/windows/win32/api/tssbx/ne-tssbx-wtssbx_address_family)
</dt> <dd>

<span data-ttu-id="42b72-119">Contém valores que indicam a família de endereços de um endereço de rede que está sendo usado para redirecionamento.</span><span class="sxs-lookup"><span data-stu-id="42b72-119">Contains values that indicate the address family of a network address that is being used for redirection.</span></span>

</dd> <dt>

[<span data-ttu-id="42b72-120">**\_drenagem de máquina WTSSBX \_**</span><span class="sxs-lookup"><span data-stu-id="42b72-120">**WTSSBX\_MACHINE\_DRAIN**</span></span>](/windows/win32/api/tssbx/ne-tssbx-wtssbx_machine_drain)
</dt> <dd>

<span data-ttu-id="42b72-121">Contém valores que indicam o estado de drenagem de um servidor de Host da Sessão da Área de Trabalho Remota (Host da Sessão RD).</span><span class="sxs-lookup"><span data-stu-id="42b72-121">Contains values that indicate the drain state of a Remote Desktop Session Host (RD Session Host) server.</span></span>

</dd> <dt>

[<span data-ttu-id="42b72-122">**\_modo de \_ sessão do computador WTSSBX \_**</span><span class="sxs-lookup"><span data-stu-id="42b72-122">**WTSSBX\_MACHINE\_SESSION\_MODE**</span></span>](/windows/win32/api/tssbx/ne-tssbx-wtssbx_machine_session_mode)
</dt> <dd>

<span data-ttu-id="42b72-123">Contém valores que indicam o modo de sessão de um servidor de Host da Sessão RD.</span><span class="sxs-lookup"><span data-stu-id="42b72-123">Contains values that indicate the session mode of a RD Session Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="42b72-124">**\_estado da máquina WTSSBX \_**</span><span class="sxs-lookup"><span data-stu-id="42b72-124">**WTSSBX\_MACHINE\_STATE**</span></span>](/windows/win32/api/tssbx/ne-tssbx-wtssbx_machine_state)
</dt> <dd>

<span data-ttu-id="42b72-125">Contém valores que indicam o estado atual de um servidor.</span><span class="sxs-lookup"><span data-stu-id="42b72-125">Contains values that indicate the current state of a server.</span></span>

</dd> <dt>

[<span data-ttu-id="42b72-126">**\_tipo de notificação WTSSBX \_**</span><span class="sxs-lookup"><span data-stu-id="42b72-126">**WTSSBX\_NOTIFICATION\_TYPE**</span></span>](/windows/win32/api/tssbx/ne-tssbx-wtssbx_notification_type)
</dt> <dd>

<span data-ttu-id="42b72-127">Contém valores que indicam o tipo de alteração de status que ocorreu em um servidor de Host da Sessão RD ou uma sessão de usuário.</span><span class="sxs-lookup"><span data-stu-id="42b72-127">Contains values that indicate the type of status change that occurred on a RD Session Host server or a user session.</span></span>

</dd> <dt>

[<span data-ttu-id="42b72-128">**\_estado de sessão WTSSBX \_**</span><span class="sxs-lookup"><span data-stu-id="42b72-128">**WTSSBX\_SESSION\_STATE**</span></span>](/windows/win32/api/tssbx/ne-tssbx-wtssbx_session_state)
</dt> <dd>

<span data-ttu-id="42b72-129">Contém valores que indicam o estado de conexão de uma sessão de usuário.</span><span class="sxs-lookup"><span data-stu-id="42b72-129">Contains values that indicate the connection state of a user session.</span></span>

</dd> </dl>

 

 




