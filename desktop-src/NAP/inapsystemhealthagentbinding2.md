---
title: Interface INapSystemHealthAgentBinding2 (NapSystemHealthAgent. h)
description: Os SHAs usam para se comunicar com o NapAgent. | Interface INapSystemHealthAgentBinding2 (NapSystemHealthAgent. h)
ms.assetid: 2b087d79-a738-42d6-a8f2-4698ab844446
keywords:
- INapSystemHealthAgentBinding2 da interface NAP
- INapSystemHealthAgentBinding2 interface NAP, descrita
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding2
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9a7491a2e78d66399f9ca246bcee9182e4f95d0
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104298208"
---
# <a name="inapsystemhealthagentbinding2-interface"></a><span data-ttu-id="fe7ef-106">Interface INapSystemHealthAgentBinding2</span><span class="sxs-lookup"><span data-stu-id="fe7ef-106">INapSystemHealthAgentBinding2 interface</span></span>

> [!Note]  
> <span data-ttu-id="fe7ef-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="fe7ef-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="fe7ef-108">O **INapSystemHealthAgentBinding2** fornece métodos que os SHAs usam para se comunicar com o NapAgent.</span><span class="sxs-lookup"><span data-stu-id="fe7ef-108">The **INapSystemHealthAgentBinding2** provides methods that the SHAs use to communicate with the NapAgent.</span></span>

> [!Note]  
> <span data-ttu-id="fe7ef-109">Essa interface herda todos os métodos de [**INapSystemHealthAgentBinding**](inapsystemhealthagentbinding.md) e deve ser usada em seu lugar.</span><span class="sxs-lookup"><span data-stu-id="fe7ef-109">This interface inherits all the methods of [**INapSystemHealthAgentBinding**](inapsystemhealthagentbinding.md) and should be used instead.</span></span>

 

## <a name="members"></a><span data-ttu-id="fe7ef-110">Membros</span><span class="sxs-lookup"><span data-stu-id="fe7ef-110">Members</span></span>

<span data-ttu-id="fe7ef-111">A interface **INapSystemHealthAgentBinding2** herda de [**INapSystemHealthAgentBinding**](inapsystemhealthagentbinding.md).</span><span class="sxs-lookup"><span data-stu-id="fe7ef-111">The **INapSystemHealthAgentBinding2** interface inherits from [**INapSystemHealthAgentBinding**](inapsystemhealthagentbinding.md).</span></span> <span data-ttu-id="fe7ef-112">**INapSystemHealthAgentBinding2** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="fe7ef-112">**INapSystemHealthAgentBinding2** also has these types of members:</span></span>

-   [<span data-ttu-id="fe7ef-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="fe7ef-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="fe7ef-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="fe7ef-114">Methods</span></span>

<span data-ttu-id="fe7ef-115">A interface **INapSystemHealthAgentBinding2** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="fe7ef-115">The **INapSystemHealthAgentBinding2** interface has these methods.</span></span>



| <span data-ttu-id="fe7ef-116">Método</span><span class="sxs-lookup"><span data-stu-id="fe7ef-116">Method</span></span>                                                                                                                    | <span data-ttu-id="fe7ef-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="fe7ef-117">Description</span></span>                                                                                     |
|:--------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fe7ef-118">**INapSystemHealthAgentBinding2::GetSystemIsolationInfoEx**</span><span class="sxs-lookup"><span data-stu-id="fe7ef-118">**INapSystemHealthAgentBinding2::GetSystemIsolationInfoEx**</span></span>](inapsystemhealthagentbinding2-getsystemisolationinfoex.md) | <span data-ttu-id="fe7ef-119">Chamado por SHAs para determinar o estado de isolamento do sistema e o estado de isolamento estendido.</span><span class="sxs-lookup"><span data-stu-id="fe7ef-119">Called by SHAs to determine the system isolation state and extended isolation state.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="fe7ef-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="fe7ef-120">Remarks</span></span>

<span data-ttu-id="fe7ef-121">Todas as APIs nesta interface retornarão **RPC \_ E \_ desconectadas** se o NapAgent for interrompido.</span><span class="sxs-lookup"><span data-stu-id="fe7ef-121">All the APIs in this interface will return **RPC\_E\_DISCONNECTED** if the NapAgent is stopped.</span></span> <span data-ttu-id="fe7ef-122">Este objeto será recuperado automaticamente e reassociado ao NapAgent, depois que ele for reiniciado.</span><span class="sxs-lookup"><span data-stu-id="fe7ef-122">This object will recover automatically and rebind to the NapAgent, once it restarts.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe7ef-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fe7ef-123">Requirements</span></span>



| <span data-ttu-id="fe7ef-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe7ef-124">Requirement</span></span> | <span data-ttu-id="fe7ef-125">Valor</span><span class="sxs-lookup"><span data-stu-id="fe7ef-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe7ef-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fe7ef-126">Minimum supported client</span></span><br/> | <span data-ttu-id="fe7ef-127">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fe7ef-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="fe7ef-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fe7ef-128">Minimum supported server</span></span><br/> | <span data-ttu-id="fe7ef-129">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fe7ef-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="fe7ef-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fe7ef-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe7ef-131"><dt>NapSystemHealthAgent. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe7ef-131"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="fe7ef-132">INSERI</span><span class="sxs-lookup"><span data-stu-id="fe7ef-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fe7ef-133"><dt>NapSystemHealthAgent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="fe7ef-133"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="fe7ef-134">DLL</span><span class="sxs-lookup"><span data-stu-id="fe7ef-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fe7ef-135"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fe7ef-135"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="fe7ef-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="fe7ef-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe7ef-137">**INapSystemHealthAgentBinding**</span><span class="sxs-lookup"><span data-stu-id="fe7ef-137">**INapSystemHealthAgentBinding**</span></span>](inapsystemhealthagentbinding.md)
</dt> <dt>

[<span data-ttu-id="fe7ef-138">Interfaces NAP</span><span class="sxs-lookup"><span data-stu-id="fe7ef-138">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="fe7ef-139">Referência de NAP</span><span class="sxs-lookup"><span data-stu-id="fe7ef-139">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

 





