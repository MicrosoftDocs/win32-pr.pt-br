---
title: Interface INapSystemHealthAgentCallback (NapSystemHealthAgent. h)
description: São declaradas pelo sistema e implementadas pelo gravador de SHA para que o NapAgent possa se comunicar com o SHA.
ms.assetid: f299e796-c81d-4a22-b9c8-f80990098044
keywords:
- INapSystemHealthAgentCallback da interface NAP
- INapSystemHealthAgentCallback interface NAP, descrita
topic_type:
- apiref
api_name:
- INapSystemHealthAgentCallback
api_location:
- NapSystemHealthAgent.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11d08dd9cf77d36ca33902c63831135a0cc2fe5d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105754748"
---
# <a name="inapsystemhealthagentcallback-interface"></a><span data-ttu-id="dfcd3-105">Interface INapSystemHealthAgentCallback</span><span class="sxs-lookup"><span data-stu-id="dfcd3-105">INapSystemHealthAgentCallback interface</span></span>

> [!Note]  
> <span data-ttu-id="dfcd3-106">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="dfcd3-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="dfcd3-107">A interface **INapSystemHealthAgentCallback** fornece métodos de retorno de chamada que são declarados pelo sistema e implementados pelo gravador de SHA para que o NapAgent possa se comunicar com o Sha.</span><span class="sxs-lookup"><span data-stu-id="dfcd3-107">The **INapSystemHealthAgentCallback** interface provides callback methods that are declared by the system and implemented by the SHA writer so the NapAgent can communicate with the SHA.</span></span>

## <a name="members"></a><span data-ttu-id="dfcd3-108">Membros</span><span class="sxs-lookup"><span data-stu-id="dfcd3-108">Members</span></span>

<span data-ttu-id="dfcd3-109">A interface **INapSystemHealthAgentCallback** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="dfcd3-109">The **INapSystemHealthAgentCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="dfcd3-110">**INapSystemHealthAgentCallback** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="dfcd3-110">**INapSystemHealthAgentCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="dfcd3-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="dfcd3-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="dfcd3-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="dfcd3-112">Methods</span></span>

<span data-ttu-id="dfcd3-113">A interface **INapSystemHealthAgentCallback** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="dfcd3-113">The **INapSystemHealthAgentCallback** interface has these methods.</span></span>



| <span data-ttu-id="dfcd3-114">Método</span><span class="sxs-lookup"><span data-stu-id="dfcd3-114">Method</span></span>                                                                                                                                           | <span data-ttu-id="dfcd3-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="dfcd3-115">Description</span></span>                                                                                                          |
|:-------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dfcd3-116">**INapSystemHealthAgentCallback::CompareSoHRequests**</span><span class="sxs-lookup"><span data-stu-id="dfcd3-116">**INapSystemHealthAgentCallback::CompareSoHRequests**</span></span>](inapsystemhealthagentcallback-comparesohrequests-method.md)                             | <span data-ttu-id="dfcd3-117">Usado pelo SHA para comparar o SoHs.</span><span class="sxs-lookup"><span data-stu-id="dfcd3-117">Used by the SHA to compare the SoHs.</span></span><br/>                                                                      |
| [<span data-ttu-id="dfcd3-118">**INapSystemHealthAgentCallback::GetFixupInfo**</span><span class="sxs-lookup"><span data-stu-id="dfcd3-118">**INapSystemHealthAgentCallback::GetFixupInfo**</span></span>](inapsystemhealthagentcallback-getfixupinfo-method.md)                                         | <span data-ttu-id="dfcd3-119">Chamado pelo NapAgent para determinar o estado do SHA.</span><span class="sxs-lookup"><span data-stu-id="dfcd3-119">Called by the NapAgent to determine the state of the SHA.</span></span><br/>                                                 |
| [<span data-ttu-id="dfcd3-120">**INapSystemHealthAgentCallback::GetSoHRequest**</span><span class="sxs-lookup"><span data-stu-id="dfcd3-120">**INapSystemHealthAgentCallback::GetSoHRequest**</span></span>](inapsystemhealthagentcallback-getsohrequest-method.md)                                       | <span data-ttu-id="dfcd3-121">Chamado pelo NapAgent para consultar a solicitação SoH do SHA.</span><span class="sxs-lookup"><span data-stu-id="dfcd3-121">Called by the NapAgent to query the SHA's SoH request.</span></span><br/>                                                    |
| [<span data-ttu-id="dfcd3-122">**INapSystemHealthAgentCallback::NotifyOrphanedSoHRequest**</span><span class="sxs-lookup"><span data-stu-id="dfcd3-122">**INapSystemHealthAgentCallback::NotifyOrphanedSoHRequest**</span></span>](inapsystemhealthagentcallback-notifyorphanedsohrequest-method.md)                 | <span data-ttu-id="dfcd3-123">Chamado se uma solicitação SoH foi consultada a partir do SHA, mas a resposta nunca voltou.</span><span class="sxs-lookup"><span data-stu-id="dfcd3-123">Called if an SoH request was queried from the SHA, but the response never came back.</span></span><br/>                      |
| [<span data-ttu-id="dfcd3-124">**INapSystemHealthAgentCallback::NotifySystemIsolationStateChange**</span><span class="sxs-lookup"><span data-stu-id="dfcd3-124">**INapSystemHealthAgentCallback::NotifySystemIsolationStateChange**</span></span>](inapsystemhealthagentcallback-notifysystemisolationstatechange-method.md) | <span data-ttu-id="dfcd3-125">Chamado pelo NapAgent para indicar que o estado de isolamento do sistema ou o tempo de término da experiência foi alterado.</span><span class="sxs-lookup"><span data-stu-id="dfcd3-125">Called by the NapAgent to indicate that the system isolation state or the probation end-time has changed.</span></span><br/> |
| [<span data-ttu-id="dfcd3-126">**INapSystemHealthAgentCallback::P rocessSoHResponse**</span><span class="sxs-lookup"><span data-stu-id="dfcd3-126">**INapSystemHealthAgentCallback::ProcessSoHResponse**</span></span>](inapsystemhealthagentcallback-processsohresponse-method.md)                             | <span data-ttu-id="dfcd3-127">Chamado quando o NapAgent recebe uma resposta SoH destinada a este agente de integridade.</span><span class="sxs-lookup"><span data-stu-id="dfcd3-127">Called when the NapAgent receives an SoH response destined for this health agent.</span></span><br/>                         |



 

## <a name="requirements"></a><span data-ttu-id="dfcd3-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dfcd3-128">Requirements</span></span>



| <span data-ttu-id="dfcd3-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="dfcd3-129">Requirement</span></span> | <span data-ttu-id="dfcd3-130">Valor</span><span class="sxs-lookup"><span data-stu-id="dfcd3-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dfcd3-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dfcd3-131">Minimum supported client</span></span><br/> | <span data-ttu-id="dfcd3-132">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="dfcd3-132">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="dfcd3-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dfcd3-133">Minimum supported server</span></span><br/> | <span data-ttu-id="dfcd3-134">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="dfcd3-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="dfcd3-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="dfcd3-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="dfcd3-136"><dt>NapSystemHealthAgent. h</dt></span><span class="sxs-lookup"><span data-stu-id="dfcd3-136"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="dfcd3-137">INSERI</span><span class="sxs-lookup"><span data-stu-id="dfcd3-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="dfcd3-138"><dt>NapSystemHealthAgent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="dfcd3-138"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dfcd3-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="dfcd3-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfcd3-140">Interfaces NAP</span><span class="sxs-lookup"><span data-stu-id="dfcd3-140">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="dfcd3-141">Referência de NAP</span><span class="sxs-lookup"><span data-stu-id="dfcd3-141">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

