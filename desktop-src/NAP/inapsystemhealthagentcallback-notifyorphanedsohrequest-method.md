---
title: Método INapSystemHealthAgentCallback NotifyOrphanedSoHRequest (NapSystemHealthAgent. h)
description: É chamado se um SoHRequest foi consultado a partir do SHA, mas a resposta nunca voltou.
ms.assetid: 9e6fac6c-fb23-4725-ae0f-28ef8a6c4ea6
keywords:
- Método NotifyOrphanedSoHRequest NAP
- Método NotifyOrphanedSoHRequest NAP, interface INapSystemHealthAgentCallback
- INapSystemHealthAgentCallback interface NAP, método NotifyOrphanedSoHRequest
topic_type:
- apiref
api_name:
- INapSystemHealthAgentCallback.NotifyOrphanedSoHRequest
api_location:
- NapSystemHealthAgent.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 676b67b61a9375f4fd44ecc41f9e56e92a97b693
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369882"
---
# <a name="inapsystemhealthagentcallbacknotifyorphanedsohrequest-method"></a><span data-ttu-id="55c0b-106">Método INapSystemHealthAgentCallback:: NotifyOrphanedSoHRequest</span><span class="sxs-lookup"><span data-stu-id="55c0b-106">INapSystemHealthAgentCallback::NotifyOrphanedSoHRequest method</span></span>

> [!Note]  
> <span data-ttu-id="55c0b-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="55c0b-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="55c0b-108">O método **INapSystemHealthAgentCallback:: NotifyOrphanedSoHRequest** é chamado se um [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) foi consultado a partir do Sha, mas a resposta nunca voltou.</span><span class="sxs-lookup"><span data-stu-id="55c0b-108">The **INapSystemHealthAgentCallback::NotifyOrphanedSoHRequest** method is called if an [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) was queried from the SHA, but the response never came back.</span></span>

## <a name="syntax"></a><span data-ttu-id="55c0b-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="55c0b-109">Syntax</span></span>


```C++
HRESULT NotifyOrphanedSoHRequest(
  [in] const CorrelationId *correlationId
);
```



## <a name="parameters"></a><span data-ttu-id="55c0b-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="55c0b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55c0b-111">*CorrelationId* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="55c0b-111">*correlationId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55c0b-112">Um ponteiro para a estrutura exclusiva de [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) que identifica o [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh)órfão.</span><span class="sxs-lookup"><span data-stu-id="55c0b-112">A pointer to the unique [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) structure that identifies the orphaned [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55c0b-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="55c0b-113">Return value</span></span>

<span data-ttu-id="55c0b-114">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="55c0b-114">This method can return one of these values.</span></span>



| <span data-ttu-id="55c0b-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="55c0b-115">Return code</span></span>                                                                          | <span data-ttu-id="55c0b-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="55c0b-116">Description</span></span>                   |
|--------------------------------------------------------------------------------------|-------------------------------|
| <dl> <span data-ttu-id="55c0b-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="55c0b-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="55c0b-118">Indica êxito.</span><span class="sxs-lookup"><span data-stu-id="55c0b-118">Indicates success.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="55c0b-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="55c0b-119">Remarks</span></span>

<span data-ttu-id="55c0b-120">Esse método de retorno de chamada é declarado pelo sistema NAP e deve ser implementado pelo gravador SHA.</span><span class="sxs-lookup"><span data-stu-id="55c0b-120">This callback method is declared by the NAP system and is to be implemented by the SHA writer.</span></span>

<span data-ttu-id="55c0b-121">Esse método pode ser chamado pelo sistema nos seguintes casos:</span><span class="sxs-lookup"><span data-stu-id="55c0b-121">This method can be called by the system in the following cases:</span></span>

-   <span data-ttu-id="55c0b-122">Um [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) não pôde ser enviado na conexão.</span><span class="sxs-lookup"><span data-stu-id="55c0b-122">A [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) could not be sent on the wire.</span></span>
-   <span data-ttu-id="55c0b-123">Um [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) foi enviado na conexão, mas nenhum **SoHResponse** voltou, ou seja, o imforçador esgotou o tempo limite ou não havia um SHV correspondente no lado do servidor.</span><span class="sxs-lookup"><span data-stu-id="55c0b-123">A [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) was sent on the wire, but no **SoHResponse** came back, i.e. the enforcer timed out or there was no corresponding SHV on the server-side.</span></span>
-   <span data-ttu-id="55c0b-124">A conexão foi desativada ou um aplicador ficou offline.</span><span class="sxs-lookup"><span data-stu-id="55c0b-124">The connection went down or an enforcer went offline.</span></span>

<span data-ttu-id="55c0b-125">Essa é apenas uma notificação de melhor esforço, portanto, os SHAs não devem confiar nessas informações para limpar o estado.</span><span class="sxs-lookup"><span data-stu-id="55c0b-125">This is only a best effort notification, so SHAs must not rely on this information to clean up state.</span></span> <span data-ttu-id="55c0b-126">Há várias situações em que um SHA não será notificado:</span><span class="sxs-lookup"><span data-stu-id="55c0b-126">There are several situations in which an SHA will not be notified:</span></span>

-   <span data-ttu-id="55c0b-127">Se um imposição se comportar, ou seja, ele não notifica o SHA quando o estado da conexão está inativo.</span><span class="sxs-lookup"><span data-stu-id="55c0b-127">If an enforcer misbehaves, i.e. it does not notify the SHA when the connection state is down.</span></span>
-   <span data-ttu-id="55c0b-128">Se um aplicador falhar.</span><span class="sxs-lookup"><span data-stu-id="55c0b-128">If an enforcer crashes.</span></span>
-   <span data-ttu-id="55c0b-129">Em condições de erro, ou seja, o NapAgent está sem memória.</span><span class="sxs-lookup"><span data-stu-id="55c0b-129">In error conditions, i.e. the NapAgent is out of memory.</span></span>

<span data-ttu-id="55c0b-130">Os SHAs podem receber algumas notificações falsas quando eles se ligam pela primeira vez ao NapAgent, por exemplo, se uma troca de SoH estiver em andamento quando o SHA estiver ligado e expirar.</span><span class="sxs-lookup"><span data-stu-id="55c0b-130">SHAs may get some spurious notifications when they first bind to the NapAgent, for instance, if an SoH exchange is in progress when the SHA bound, and then it times out.</span></span>

## <a name="requirements"></a><span data-ttu-id="55c0b-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="55c0b-131">Requirements</span></span>



| <span data-ttu-id="55c0b-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="55c0b-132">Requirement</span></span> | <span data-ttu-id="55c0b-133">Valor</span><span class="sxs-lookup"><span data-stu-id="55c0b-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55c0b-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="55c0b-134">Minimum supported client</span></span><br/> | <span data-ttu-id="55c0b-135">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="55c0b-135">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="55c0b-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="55c0b-136">Minimum supported server</span></span><br/> | <span data-ttu-id="55c0b-137">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="55c0b-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="55c0b-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="55c0b-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="55c0b-139"><dt>NapSystemHealthAgent. h</dt></span><span class="sxs-lookup"><span data-stu-id="55c0b-139"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="55c0b-140">INSERI</span><span class="sxs-lookup"><span data-stu-id="55c0b-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="55c0b-141"><dt>NapSystemHealthAgent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="55c0b-141"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55c0b-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="55c0b-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55c0b-143">**INapSystemHealthAgentCallback**</span><span class="sxs-lookup"><span data-stu-id="55c0b-143">**INapSystemHealthAgentCallback**</span></span>](inapsystemhealthagentcallback.md)
</dt> </dl>

 

 





