---
title: Interface INapSystemHealthAgentRequest (NapSystemHealthAgent. h)
description: Os SHAs usam para comunicar e coordenar o processamento com o sistema NAP.
ms.assetid: 424e0fb7-cce7-4b75-b474-fda0e053284e
keywords:
- INapSystemHealthAgentRequest da interface NAP
- INapSystemHealthAgentRequest interface NAP, descrita
topic_type:
- apiref
api_name:
- INapSystemHealthAgentRequest
api_location:
- qagentrt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a4e79e2a6347ebffec37595d4ca86b100830047
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499350"
---
# <a name="inapsystemhealthagentrequest-interface"></a><span data-ttu-id="4e828-105">Interface INapSystemHealthAgentRequest</span><span class="sxs-lookup"><span data-stu-id="4e828-105">INapSystemHealthAgentRequest interface</span></span>

> [!Note]  
> <span data-ttu-id="4e828-106">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="4e828-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="4e828-107">A interface **INapSystemHealthAgentRequest** fornece métodos que os SHAs usam para comunicar e coordenar o processamento com o sistema NAP.</span><span class="sxs-lookup"><span data-stu-id="4e828-107">The **INapSystemHealthAgentRequest** interface provides methods that SHAs use to communicate and coordinate processing with the NAP system.</span></span>

## <a name="members"></a><span data-ttu-id="4e828-108">Membros</span><span class="sxs-lookup"><span data-stu-id="4e828-108">Members</span></span>

<span data-ttu-id="4e828-109">A interface **INapSystemHealthAgentRequest** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="4e828-109">The **INapSystemHealthAgentRequest** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="4e828-110">**INapSystemHealthAgentRequest** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="4e828-110">**INapSystemHealthAgentRequest** also has these types of members:</span></span>

-   [<span data-ttu-id="4e828-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="4e828-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="4e828-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="4e828-112">Methods</span></span>

<span data-ttu-id="4e828-113">A interface **INapSystemHealthAgentRequest** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="4e828-113">The **INapSystemHealthAgentRequest** interface has these methods.</span></span>



| <span data-ttu-id="4e828-114">Método</span><span class="sxs-lookup"><span data-stu-id="4e828-114">Method</span></span>                                                                                                                     | <span data-ttu-id="4e828-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="4e828-115">Description</span></span>                                                                                      |
|:---------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4e828-116">**INapSystemHealthAgentRequest::GetCacheSoHFlag**</span><span class="sxs-lookup"><span data-stu-id="4e828-116">**INapSystemHealthAgentRequest::GetCacheSoHFlag**</span></span>](inapsystemhealthagentrequest-getcachesohflag-method.md)               | <span data-ttu-id="4e828-117">Usado somente pelo NapAgent.</span><span class="sxs-lookup"><span data-stu-id="4e828-117">Used only by the NapAgent.</span></span><br/>                                                            |
| [<span data-ttu-id="4e828-118">**INapSystemHealthAgentRequest:: CorrelationId**</span><span class="sxs-lookup"><span data-stu-id="4e828-118">**INapSystemHealthAgentRequest::GetCorrelationId**</span></span>](inapsystemhealthagentrequest-getcorrelationid-method.md)             | <span data-ttu-id="4e828-119">Usado pelos agentes de integridade do sistema para correlacionar SoHs e [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh).</span><span class="sxs-lookup"><span data-stu-id="4e828-119">Used by system health agents to correlate SoHs and [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh).</span></span><br/> |
| [<span data-ttu-id="4e828-120">**INapSystemHealthAgentRequest::GetSoHRequest**</span><span class="sxs-lookup"><span data-stu-id="4e828-120">**INapSystemHealthAgentRequest::GetSoHRequest**</span></span>](inapsystemhealthagentrequest-getsohrequest-method.md)                   | <span data-ttu-id="4e828-121">Usado por SHAs para obter SoHs anteriormente armazenados em cache pelo NapAgent.</span><span class="sxs-lookup"><span data-stu-id="4e828-121">Used by SHAs to get SoHs previously cached by the NapAgent.</span></span><br/>                           |
| [<span data-ttu-id="4e828-122">**INapSystemHealthAgentRequest::GetSoHResponse**</span><span class="sxs-lookup"><span data-stu-id="4e828-122">**INapSystemHealthAgentRequest::GetSoHResponse**</span></span>](inapsystemhealthagentrequest-getsohresponse-method.md)                 | <span data-ttu-id="4e828-123">Usado pelo agente de integridade para recuperar seus [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh).</span><span class="sxs-lookup"><span data-stu-id="4e828-123">Used by the health agent to retrieve their [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh).</span></span><br/>         |
| [<span data-ttu-id="4e828-124">**INapSystemHealthAgentRequest::GetStringCorrelationId**</span><span class="sxs-lookup"><span data-stu-id="4e828-124">**INapSystemHealthAgentRequest::GetStringCorrelationId**</span></span>](inapsystemhealthagentrequest-getstringcorrelationid-method.md) | <span data-ttu-id="4e828-125">Usado pelos agentes de integridade do sistema para registrar a ID de correlação.</span><span class="sxs-lookup"><span data-stu-id="4e828-125">Used by system health agents to log the correlation ID.</span></span><br/>                               |
| [<span data-ttu-id="4e828-126">**INapSystemHealthAgentRequest::SetSoHRequest**</span><span class="sxs-lookup"><span data-stu-id="4e828-126">**INapSystemHealthAgentRequest::SetSoHRequest**</span></span>](inapsystemhealthagentrequest-setsohrequest-method.md)                   | <span data-ttu-id="4e828-127">Usado pelos agentes de integridade para gravar sua solicitação SoH.</span><span class="sxs-lookup"><span data-stu-id="4e828-127">Used by health agents to write their SoH request.</span></span><br/>                                     |



 

## <a name="requirements"></a><span data-ttu-id="4e828-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4e828-128">Requirements</span></span>



| <span data-ttu-id="4e828-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e828-129">Requirement</span></span> | <span data-ttu-id="4e828-130">Valor</span><span class="sxs-lookup"><span data-stu-id="4e828-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e828-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4e828-131">Minimum supported client</span></span><br/> | <span data-ttu-id="4e828-132">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4e828-132">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="4e828-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4e828-133">Minimum supported server</span></span><br/> | <span data-ttu-id="4e828-134">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4e828-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="4e828-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4e828-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="4e828-136"><dt>NapSystemHealthAgent. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e828-136"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="4e828-137">INSERI</span><span class="sxs-lookup"><span data-stu-id="4e828-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4e828-138"><dt>NapSystemHealthAgent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4e828-138"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="4e828-139">DLL</span><span class="sxs-lookup"><span data-stu-id="4e828-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4e828-140"><dt>Qagentrt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4e828-140"><dt>Qagentrt.dll</dt></span></span> </dl>             |



## <a name="see-also"></a><span data-ttu-id="4e828-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="4e828-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e828-142">Interfaces NAP</span><span class="sxs-lookup"><span data-stu-id="4e828-142">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="4e828-143">Referência de NAP</span><span class="sxs-lookup"><span data-stu-id="4e828-143">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

