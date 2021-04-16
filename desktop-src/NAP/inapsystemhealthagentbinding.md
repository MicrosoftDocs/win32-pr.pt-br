---
title: Interface INapSystemHealthAgentBinding (NapSystemHealthAgent. h)
description: Os SHAs usam para se comunicar com o NapAgent. | Interface INapSystemHealthAgentBinding (NapSystemHealthAgent. h)
ms.assetid: 9366f61f-086a-4f44-900e-9ec3165a35ba
keywords:
- INapSystemHealthAgentBinding da interface NAP
- INapSystemHealthAgentBinding interface NAP, descrita
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d38d1331996e34c6879fc2e98ce566ce6802527a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105754326"
---
# <a name="inapsystemhealthagentbinding-interface"></a><span data-ttu-id="5ad4f-106">Interface INapSystemHealthAgentBinding</span><span class="sxs-lookup"><span data-stu-id="5ad4f-106">INapSystemHealthAgentBinding interface</span></span>

> [!Note]  
> <span data-ttu-id="5ad4f-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="5ad4f-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="5ad4f-108">O **INapSystemHealthAgentBinding** fornece métodos que os SHAs usam para se comunicar com o NapAgent.</span><span class="sxs-lookup"><span data-stu-id="5ad4f-108">The **INapSystemHealthAgentBinding** provides methods that the SHAs use to communicate with the NapAgent.</span></span>

> [!Note]  
> <span data-ttu-id="5ad4f-109">[**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) herda todos os métodos dessa interface e deve ser usado em seu lugar.</span><span class="sxs-lookup"><span data-stu-id="5ad4f-109">[**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) inherits all the methods of this interface and should be used instead.</span></span>

 

## <a name="members"></a><span data-ttu-id="5ad4f-110">Membros</span><span class="sxs-lookup"><span data-stu-id="5ad4f-110">Members</span></span>

<span data-ttu-id="5ad4f-111">A interface **INapSystemHealthAgentBinding** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="5ad4f-111">The **INapSystemHealthAgentBinding** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="5ad4f-112">**INapSystemHealthAgentBinding** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="5ad4f-112">**INapSystemHealthAgentBinding** also has these types of members:</span></span>

-   [<span data-ttu-id="5ad4f-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="5ad4f-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="5ad4f-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="5ad4f-114">Methods</span></span>

<span data-ttu-id="5ad4f-115">A interface **INapSystemHealthAgentBinding** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="5ad4f-115">The **INapSystemHealthAgentBinding** interface has these methods.</span></span>



| <span data-ttu-id="5ad4f-116">Método</span><span class="sxs-lookup"><span data-stu-id="5ad4f-116">Method</span></span>                                                                                                                     | <span data-ttu-id="5ad4f-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="5ad4f-117">Description</span></span>                                                                                        |
|:---------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5ad4f-118">**INapSystemHealthAgentBinding::FlushCache**</span><span class="sxs-lookup"><span data-stu-id="5ad4f-118">**INapSystemHealthAgentBinding::FlushCache**</span></span>](inapsystemhealthagentbinding-flushcache-method.md)                         | <span data-ttu-id="5ad4f-119">Chamado por um SHA para liberar seu cache SoH.</span><span class="sxs-lookup"><span data-stu-id="5ad4f-119">Called by an SHA to flush its SoH cache.</span></span><br/>                                                |
| [<span data-ttu-id="5ad4f-120">**INapSystemHealthAgentBinding::GetSystemIsolationInfo**</span><span class="sxs-lookup"><span data-stu-id="5ad4f-120">**INapSystemHealthAgentBinding::GetSystemIsolationInfo**</span></span>](inapsystemhealthagentbinding-getsystemisolationinfo-method.md) | <span data-ttu-id="5ad4f-121">Chamado por SHAs para determinar o estado de isolamento do sistema.</span><span class="sxs-lookup"><span data-stu-id="5ad4f-121">Called by SHAs to determine the system isolation state.</span></span><br/>                                 |
| [<span data-ttu-id="5ad4f-122">**INapSystemHealthAgentBinding:: Initialize**</span><span class="sxs-lookup"><span data-stu-id="5ad4f-122">**INapSystemHealthAgentBinding::Initialize**</span></span>](inapsystemhealthagentbinding-initialize-method.md)                         | <span data-ttu-id="5ad4f-123">Inicializa o SHA e associa o SHA ao serviço NapAgent.</span><span class="sxs-lookup"><span data-stu-id="5ad4f-123">Initializes the SHA and binds the SHA to the NapAgent service.</span></span> <br/>                         |
| [<span data-ttu-id="5ad4f-124">**INapSystemHealthAgentBinding::NotifySoHChange**</span><span class="sxs-lookup"><span data-stu-id="5ad4f-124">**INapSystemHealthAgentBinding::NotifySoHChange**</span></span>](inapsystemhealthagentbinding-notifysohchange-method.md)               | <span data-ttu-id="5ad4f-125">Chamado por SHAs quando seu SoH é alterado.</span><span class="sxs-lookup"><span data-stu-id="5ad4f-125">Called by SHAs when their SoH changes.</span></span><br/>                                                  |
| [<span data-ttu-id="5ad4f-126">**INapSystemHealthAgentBinding:: Uninitialize**</span><span class="sxs-lookup"><span data-stu-id="5ad4f-126">**INapSystemHealthAgentBinding::Uninitialize**</span></span>](inapsystemhealthagentbinding-uninitialize-method.md)                     | <span data-ttu-id="5ad4f-127">Chamado por SHAs para fazer com que o NapAgent libere todas as suas referências aos ponteiros COM do SHA.</span><span class="sxs-lookup"><span data-stu-id="5ad4f-127">Called by SHAs to cause the NapAgent to release all its references to SHA COM pointers.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5ad4f-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="5ad4f-128">Remarks</span></span>

<span data-ttu-id="5ad4f-129">Todas as APIs nesta interface retornarão **RPC \_ E \_ desconectadas** se o NapAgent for interrompido.</span><span class="sxs-lookup"><span data-stu-id="5ad4f-129">All the APIs in this interface will return **RPC\_E\_DISCONNECTED** if the NapAgent is stopped.</span></span> <span data-ttu-id="5ad4f-130">Este objeto será recuperado automaticamente e reassociado ao NapAgent, depois que ele for reiniciado.</span><span class="sxs-lookup"><span data-stu-id="5ad4f-130">This object will recover automatically and rebind to the NapAgent, once it restarts.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ad4f-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5ad4f-131">Requirements</span></span>



| <span data-ttu-id="5ad4f-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ad4f-132">Requirement</span></span> | <span data-ttu-id="5ad4f-133">Valor</span><span class="sxs-lookup"><span data-stu-id="5ad4f-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ad4f-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5ad4f-134">Minimum supported client</span></span><br/> | <span data-ttu-id="5ad4f-135">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5ad4f-135">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="5ad4f-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5ad4f-136">Minimum supported server</span></span><br/> | <span data-ttu-id="5ad4f-137">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5ad4f-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="5ad4f-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5ad4f-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ad4f-139"><dt>NapSystemHealthAgent. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ad4f-139"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="5ad4f-140">INSERI</span><span class="sxs-lookup"><span data-stu-id="5ad4f-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5ad4f-141"><dt>NapSystemHealthAgent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5ad4f-141"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="5ad4f-142">DLL</span><span class="sxs-lookup"><span data-stu-id="5ad4f-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5ad4f-143"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5ad4f-143"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="5ad4f-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="5ad4f-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ad4f-145">Interfaces NAP</span><span class="sxs-lookup"><span data-stu-id="5ad4f-145">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="5ad4f-146">Referência de NAP</span><span class="sxs-lookup"><span data-stu-id="5ad4f-146">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

