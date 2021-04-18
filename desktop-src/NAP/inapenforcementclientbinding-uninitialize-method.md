---
title: Método Uninitialize do INapEnforcementClientBinding (NapEnforcementClient. h)
description: Conclui o serviço NapAgent.
ms.assetid: 792600e5-586f-4858-8439-75761c928745
keywords:
- Método Uninitialize NAP
- Método Uninitialize NAP, interface INapEnforcementClientBinding
- INapEnforcementClientBinding interface NAP, método Uninitialize
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding.Uninitialize
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4132ff1a498a598483758623a588fa26e8b75021
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105787389"
---
# <a name="inapenforcementclientbindinguninitialize-method"></a><span data-ttu-id="27243-106">Método INapEnforcementClientBinding:: Uninitialize</span><span class="sxs-lookup"><span data-stu-id="27243-106">INapEnforcementClientBinding::Uninitialize method</span></span>

> [!Note]  
> <span data-ttu-id="27243-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="27243-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="27243-108">O método **INapEnforcementClientBinding:: Uninitialize** conclui o serviço NapAgent.</span><span class="sxs-lookup"><span data-stu-id="27243-108">The **INapEnforcementClientBinding::Uninitialize** method concludes the NapAgent service.</span></span>

## <a name="syntax"></a><span data-ttu-id="27243-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="27243-109">Syntax</span></span>


```C++
HRESULT Uninitialize();
```



## <a name="parameters"></a><span data-ttu-id="27243-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="27243-110">Parameters</span></span>

<span data-ttu-id="27243-111">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="27243-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="27243-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="27243-112">Return value</span></span>

<span data-ttu-id="27243-113">Outros códigos de erro específicos de COM também podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="27243-113">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="27243-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="27243-114">Return code</span></span>                                                                                     | <span data-ttu-id="27243-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="27243-115">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="27243-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="27243-116"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="27243-117">A operação teve êxito.</span><span class="sxs-lookup"><span data-stu-id="27243-117">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="27243-118"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="27243-118"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="27243-119">Erro de permissões, acesso negado.</span><span class="sxs-lookup"><span data-stu-id="27243-119">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="27243-120"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="27243-120"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="27243-121">O limite de recursos do sistema não pôde executar a operação.</span><span class="sxs-lookup"><span data-stu-id="27243-121">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="27243-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="27243-122">Remarks</span></span>

<span data-ttu-id="27243-123">O NapAgent bloqueia o processamento adicional até que todas as chamadas existentes nas interfaces [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) e [**INapEnforcementClientCallback**](inapenforcementclientcallback.md) sejam concluídas.</span><span class="sxs-lookup"><span data-stu-id="27243-123">The NapAgent blocks further processing until all existing calls on the [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) and [**INapEnforcementClientCallback**](inapenforcementclientcallback.md) interfaces complete.</span></span> <span data-ttu-id="27243-124">No final desta chamada, o NapAgent libera Todas as suas referências em ponteiros COM do cliente de imposição.</span><span class="sxs-lookup"><span data-stu-id="27243-124">At the end of this call, the NapAgent releases all its references on enforcement client COM pointers.</span></span>

<span data-ttu-id="27243-125">Antes que essa função seja chamada, o aplicador deve chamar [**INapEnforcementClientBinding:: NotifyConnectionStateDown**](inapenforcementclientbinding-notifyconnectionstatedown-method.md) em todas as suas conexões ativas, para que os SHAs possam ser notificados se qualquer um dos seus SoH-Requests estavam órfãos.</span><span class="sxs-lookup"><span data-stu-id="27243-125">Before this function is called, the enforcer must call [**INapEnforcementClientBinding::NotifyConnectionStateDown**](inapenforcementclientbinding-notifyconnectionstatedown-method.md) on all its active connections, so the SHAs can be notified if any of their SoH-Requests were orphaned.</span></span>

<span data-ttu-id="27243-126">O cliente de imposição deve chamar o método [**INapEnforcementClientBinding:: Initialize**](inapenforcementclientbinding-initialize-method.md) antes de chamar este ou qualquer outro método da interface [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) .</span><span class="sxs-lookup"><span data-stu-id="27243-126">The enforcement client must call the [**INapEnforcementClientBinding::Initialize**](inapenforcementclientbinding-initialize-method.md) method before calling this or any other method of the [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="27243-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="27243-127">Requirements</span></span>



| <span data-ttu-id="27243-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="27243-128">Requirement</span></span> | <span data-ttu-id="27243-129">Valor</span><span class="sxs-lookup"><span data-stu-id="27243-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27243-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="27243-130">Minimum supported client</span></span><br/> | <span data-ttu-id="27243-131">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="27243-131">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="27243-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="27243-132">Minimum supported server</span></span><br/> | <span data-ttu-id="27243-133">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="27243-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="27243-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="27243-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="27243-135"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="27243-135"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="27243-136">INSERI</span><span class="sxs-lookup"><span data-stu-id="27243-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="27243-137"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="27243-137"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="27243-138">DLL</span><span class="sxs-lookup"><span data-stu-id="27243-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="27243-139"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="27243-139"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="27243-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="27243-140">See also</span></span>

<dl> <span data-ttu-id="27243-141"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="27243-141"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="27243-142">**INapEnforcementClientBinding**</span><span class="sxs-lookup"><span data-stu-id="27243-142">**INapEnforcementClientBinding**</span></span>](inapenforcementclientbinding.md)
</dt> <dt>

[<span data-ttu-id="27243-143">**INapEnforcementClientBinding::NotifyConnectionStateDown**</span><span class="sxs-lookup"><span data-stu-id="27243-143">**INapEnforcementClientBinding::NotifyConnectionStateDown**</span></span>](inapenforcementclientbinding-notifyconnectionstatedown-method.md)
</dt> <dt>

[<span data-ttu-id="27243-144">**INapEnforcementClientCallback**</span><span class="sxs-lookup"><span data-stu-id="27243-144">**INapEnforcementClientCallback**</span></span>](inapenforcementclientcallback.md)
</dt> </dl>

 

 





