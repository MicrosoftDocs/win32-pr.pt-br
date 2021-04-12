---
title: Método de inicialização de INapSystemHealthAgentBinding (NapSystemHealthAgent. h)
description: Inicializa o SHA (agente de integridade do sistema) e associa o SHA ao serviço NapAgent.
ms.assetid: abbc942b-0217-4b07-bf43-fab55ca9c411
keywords:
- Inicializar método NAP
- Método Initialize NAP, interface INapSystemHealthAgentBinding
- INapSystemHealthAgentBinding interface NAP, método Initialize
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding.Initialize
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ee4d4f602303ca1943e47c04ba30ab8f6e75e72
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104294762"
---
# <a name="inapsystemhealthagentbindinginitialize-method"></a><span data-ttu-id="2082f-106">Método INapSystemHealthAgentBinding:: Initialize</span><span class="sxs-lookup"><span data-stu-id="2082f-106">INapSystemHealthAgentBinding::Initialize method</span></span>

> [!Note]  
> <span data-ttu-id="2082f-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="2082f-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="2082f-108">O método **INapSystemHealthAgentBinding:: Initialize** INICIALIZA o SHA (agente de integridade do sistema) e associa o Sha ao serviço NapAgent.</span><span class="sxs-lookup"><span data-stu-id="2082f-108">The **INapSystemHealthAgentBinding::Initialize** method initializes the system health agent (SHA) and binds the SHA to the NapAgent service.</span></span> <span data-ttu-id="2082f-109">Esse método deve ser chamado antes de chamar qualquer outro método na interface [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) .</span><span class="sxs-lookup"><span data-stu-id="2082f-109">This method must be called before calling any other method on the [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="2082f-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2082f-110">Syntax</span></span>


```C++
HRESULT Initialize(
  [in] SystemHealthEntityId          id,
  [in] INapSystemHealthAgentCallback *callback
);
```



## <a name="parameters"></a><span data-ttu-id="2082f-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2082f-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2082f-112">*ID* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="2082f-112">*id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2082f-113">Um [SystemHealthEntityId](nap-datatypes.md) exclusivo que contém a ID do Sha que está sendo associado ao serviço NapAgent.</span><span class="sxs-lookup"><span data-stu-id="2082f-113">A unique [SystemHealthEntityId](nap-datatypes.md) that contains the ID of the SHA being bound to the NapAgent service.</span></span>

</dd> <dt>

<span data-ttu-id="2082f-114">*retorno de chamada* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2082f-114">*callback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2082f-115">Um ponteiro COM para uma interface [**INapSystemHealthAgentCallback**](inapsystemhealthagentcallback.md) usada pelo NapAgent para fazer o retorno de chamada do agente de integridade com uma notificação/processo.</span><span class="sxs-lookup"><span data-stu-id="2082f-115">A COM pointer to an [**INapSystemHealthAgentCallback**](inapsystemhealthagentcallback.md) interface used by the NapAgent to callback the health agent with a notify/process.</span></span> <span data-ttu-id="2082f-116">O NapAgent mantém uma referência ao objeto associado a essa interface até que [**Uninitialize**](inapsystemhealthagentbinding-uninitialize-method.md) seja chamado.</span><span class="sxs-lookup"><span data-stu-id="2082f-116">The NapAgent holds a reference to the object associated with this interface until [**Uninitialize**](inapsystemhealthagentbinding-uninitialize-method.md) is called.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2082f-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2082f-117">Return value</span></span>

<span data-ttu-id="2082f-118">Outros códigos de erro específicos de COM também podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="2082f-118">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="2082f-119">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="2082f-119">Return code</span></span>                                                                                                | <span data-ttu-id="2082f-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="2082f-120">Description</span></span>                                                                                                                    |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2082f-121"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="2082f-121"><dt>**S\_OK** </dt></span></span> </dl>                      | <span data-ttu-id="2082f-122">Operação bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="2082f-122">Operation succeeded.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="2082f-123"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="2082f-123"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>            | <span data-ttu-id="2082f-124">Erro de permissões, acesso negado.</span><span class="sxs-lookup"><span data-stu-id="2082f-124">Permissions error, access denied.</span></span><br/>                                                                                   |
| <dl> <span data-ttu-id="2082f-125"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="2082f-125"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>             | <span data-ttu-id="2082f-126">O limite de recursos do sistema não pôde executar a operação.</span><span class="sxs-lookup"><span data-stu-id="2082f-126">System resource limit, could not perform the operation.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="2082f-127"><dt>**ERRO \_ já \_ inicializado**</dt></span><span class="sxs-lookup"><span data-stu-id="2082f-127"><dt>**ERROR\_ALREADY\_INITIALIZED**</dt></span></span> </dl> | <span data-ttu-id="2082f-128">Se o SHA tiver sido inicializado anteriormente, esse erro será retornado.</span><span class="sxs-lookup"><span data-stu-id="2082f-128">If the SHA has initialized previously, this error is returned.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="2082f-129"><dt>**\_E/s NAP \_ não \_ registradas**</dt></span><span class="sxs-lookup"><span data-stu-id="2082f-129"><dt>**NAP\_E\_NOT\_REGISTERED**</dt></span></span> </dl>     | <span data-ttu-id="2082f-130">Se o SHA não tiver sido registrado anteriormente, esse erro será retornado.</span><span class="sxs-lookup"><span data-stu-id="2082f-130">If the SHA has not registered earlier, this error is returned.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="2082f-131"><dt>**RPC \_ E \_ desconectado**</dt></span><span class="sxs-lookup"><span data-stu-id="2082f-131"><dt>**RPC\_E\_DISCONNECTED**</dt></span></span> </dl>        | <span data-ttu-id="2082f-132">O NapAgent foi interrompido.</span><span class="sxs-lookup"><span data-stu-id="2082f-132">The NapAgent has been stopped.</span></span> <span data-ttu-id="2082f-133">Este objeto será recuperado automaticamente e reassociado ao NapAgent, depois que ele for reiniciado.</span><span class="sxs-lookup"><span data-stu-id="2082f-133">This object will recover automatically and rebind to the NapAgent, once it restarts.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2082f-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="2082f-134">Remarks</span></span>

<span data-ttu-id="2082f-135">O NapAgent não dispara uma troca SoH como resultado da inicialização.</span><span class="sxs-lookup"><span data-stu-id="2082f-135">The NapAgent does not trigger a SoH exchange as a result of initialization.</span></span> <span data-ttu-id="2082f-136">Um agente de integridade do sistema deve chamar [**NotifySoHChange**](inapsystemhealthagentbinding-notifysohchange-method.md) para solicitar uma troca de pacotes soh após a inicialização com o NapAgent.</span><span class="sxs-lookup"><span data-stu-id="2082f-136">A system health agent must call [**NotifySoHChange**](inapsystemhealthagentbinding-notifysohchange-method.md) to request an exchange of SoH packets after initializing with the NapAgent.</span></span>

## <a name="requirements"></a><span data-ttu-id="2082f-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2082f-137">Requirements</span></span>



| <span data-ttu-id="2082f-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="2082f-138">Requirement</span></span> | <span data-ttu-id="2082f-139">Valor</span><span class="sxs-lookup"><span data-stu-id="2082f-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2082f-140">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2082f-140">Minimum supported client</span></span><br/> | <span data-ttu-id="2082f-141">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2082f-141">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="2082f-142">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2082f-142">Minimum supported server</span></span><br/> | <span data-ttu-id="2082f-143">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2082f-143">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="2082f-144">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2082f-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="2082f-145"><dt>NapSystemHealthAgent. h</dt></span><span class="sxs-lookup"><span data-stu-id="2082f-145"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="2082f-146">INSERI</span><span class="sxs-lookup"><span data-stu-id="2082f-146">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2082f-147"><dt>NapSystemHealthAgent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2082f-147"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="2082f-148">DLL</span><span class="sxs-lookup"><span data-stu-id="2082f-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2082f-149"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2082f-149"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="2082f-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="2082f-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2082f-151">**INapSystemHealthAgentBinding**</span><span class="sxs-lookup"><span data-stu-id="2082f-151">**INapSystemHealthAgentBinding**</span></span>](inapsystemhealthagentbinding.md)
</dt> </dl>

 

 





