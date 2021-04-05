---
title: Método INapEnforcementClientCallback NotifySoHChange (NapEnforcementClient. h)
description: É usado pelo NapAgent para informar o cliente de imposição de alterações SoH.
ms.assetid: da8b9238-6371-4a6a-a9e7-ab791391ffc2
keywords:
- Método NotifySoHChange NAP
- Método NotifySoHChange NAP, interface INapEnforcementClientCallback
- INapEnforcementClientCallback interface NAP, método NotifySoHChange
topic_type:
- apiref
api_name:
- INapEnforcementClientCallback.NotifySoHChange
api_location:
- NapEnforcementClient.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b405bca5ae27a68eea780dfcb922d1f986f475c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086473"
---
# <a name="inapenforcementclientcallbacknotifysohchange-method"></a><span data-ttu-id="37bf3-106">Método INapEnforcementClientCallback:: NotifySoHChange</span><span class="sxs-lookup"><span data-stu-id="37bf3-106">INapEnforcementClientCallback::NotifySoHChange method</span></span>

> [!Note]  
> <span data-ttu-id="37bf3-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="37bf3-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="37bf3-108">O método de retorno de chamada **INapEnforcementClientCallback:: NotifySoHChange** é usado pelo NapAgent para informar o cliente de imposição de alterações soh.</span><span class="sxs-lookup"><span data-stu-id="37bf3-108">The **INapEnforcementClientCallback::NotifySoHChange** callback method is used by the NapAgent to inform the enforcement client of SoH changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="37bf3-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="37bf3-109">Syntax</span></span>


```C++
HRESULT NotifySoHChange();
```



## <a name="parameters"></a><span data-ttu-id="37bf3-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="37bf3-110">Parameters</span></span>

<span data-ttu-id="37bf3-111">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="37bf3-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="37bf3-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="37bf3-112">Return value</span></span>

<span data-ttu-id="37bf3-113">Esse método de retorno de chamada deve retornar um dos seguintes códigos de erro.</span><span class="sxs-lookup"><span data-stu-id="37bf3-113">This callback method must return one the following error codes.</span></span>



| <span data-ttu-id="37bf3-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="37bf3-114">Return code</span></span>                                                                                                | <span data-ttu-id="37bf3-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="37bf3-115">Description</span></span>                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="37bf3-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="37bf3-116"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="37bf3-117">Retorne esse valor se a operação tiver êxito.</span><span class="sxs-lookup"><span data-stu-id="37bf3-117">Return this value if the operation succeeded.</span></span><br/>                                                                                                                                                              |
| <dl> <span data-ttu-id="37bf3-118"><dt>**\_servidor RPC \_ S \_ não disponível**</dt></span><span class="sxs-lookup"><span data-stu-id="37bf3-118"><dt>**RPC\_S\_SERVER\_UNAVAILABLE**</dt></span></span> </dl> | <span data-ttu-id="37bf3-119">Retornar esse valor faz com que o imforcer seja removido da lista Bound-SHA e a entrada de cache NapAgent correspondente seja liberada.</span><span class="sxs-lookup"><span data-stu-id="37bf3-119">Returning this value causes the enforcer to be removed from the bound-SHA list, and the corresponding NapAgent cache entry to be flushed.</span></span> <span data-ttu-id="37bf3-120">O SHA com falha pode inicializar novamente com o NapAgent.</span><span class="sxs-lookup"><span data-stu-id="37bf3-120">The failing SHA can then re-initialize itself with the NapAgent.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="37bf3-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="37bf3-121">Remarks</span></span>

<span data-ttu-id="37bf3-122">A conclusão da correção do sistema é um evento de alteração de integridade do sistema.</span><span class="sxs-lookup"><span data-stu-id="37bf3-122">The completion of system fix-up is a system health change event.</span></span> <span data-ttu-id="37bf3-123">Isso significa que você deve chamar **NotifySoHChange** quando uma notificação [**INapSystemHealthAgentCallback:: GetFixupInfo**](inapsystemhealthagentcallback-getfixupinfo-method.md) indicar que o cliente está corrigido.</span><span class="sxs-lookup"><span data-stu-id="37bf3-123">That means you must call **NotifySoHChange** when a [**INapSystemHealthAgentCallback::GetFixupInfo**](inapsystemhealthagentcallback-getfixupinfo-method.md) notification indicates that the client is fixed.</span></span> <span data-ttu-id="37bf3-124">Quando um cliente é corrigido, o membro de **estado** da estrutura [**FixupInfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) retornada por **GetFixupInfo** tem um valor de **fixupStateSuccess**.</span><span class="sxs-lookup"><span data-stu-id="37bf3-124">When a client is fixed, the **state** member of the [**FixupInfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) structure returned by **GetFixupInfo** has a value of **fixupStateSuccess**.</span></span>

<span data-ttu-id="37bf3-125">Depois de ser chamado pelo NapAgent por meio desse retorno de chamada, o agente de imposição deve chamar [**INapEnforcementClientBinding:: GetSoHRequest**](inapenforcementclientbinding-getsohrequest-method.md) para recuperar a nova solicitação.</span><span class="sxs-lookup"><span data-stu-id="37bf3-125">After being called by the NapAgent via this callback, the enforcement agent must then call [**INapEnforcementClientBinding::GetSoHRequest**](inapenforcementclientbinding-getsohrequest-method.md) to retrieve the new request.</span></span> <span data-ttu-id="37bf3-126">Essa chamada pode ser feita no mesmo thread que **INapEnforcementClientCallback:: NotifySoHChange**.</span><span class="sxs-lookup"><span data-stu-id="37bf3-126">This call can be made on the same thread as **INapEnforcementClientCallback::NotifySoHChange**.</span></span>

## <a name="requirements"></a><span data-ttu-id="37bf3-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="37bf3-127">Requirements</span></span>



| <span data-ttu-id="37bf3-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="37bf3-128">Requirement</span></span> | <span data-ttu-id="37bf3-129">Valor</span><span class="sxs-lookup"><span data-stu-id="37bf3-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37bf3-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="37bf3-130">Minimum supported client</span></span><br/> | <span data-ttu-id="37bf3-131">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="37bf3-131">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="37bf3-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="37bf3-132">Minimum supported server</span></span><br/> | <span data-ttu-id="37bf3-133">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="37bf3-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="37bf3-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="37bf3-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="37bf3-135"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="37bf3-135"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="37bf3-136">INSERI</span><span class="sxs-lookup"><span data-stu-id="37bf3-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="37bf3-137"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="37bf3-137"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37bf3-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="37bf3-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37bf3-139">**INapEnforcementClientCallback**</span><span class="sxs-lookup"><span data-stu-id="37bf3-139">**INapEnforcementClientCallback**</span></span>](inapenforcementclientcallback.md)
</dt> </dl>

 

 





