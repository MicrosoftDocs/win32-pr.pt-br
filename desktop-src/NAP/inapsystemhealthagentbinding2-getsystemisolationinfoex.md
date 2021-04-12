---
title: Método INapSystemHealthAgentBinding2 GetSystemIsolationInfoEx (NapSystemHealthAgent. h)
description: É chamado por SHAs para determinar o estado de isolamento do sistema e o estado de isolamento estendido.
ms.assetid: 237e5539-889c-457d-8db0-bf3379f28b85
keywords:
- Método GetSystemIsolationInfoEx NAP
- Método GetSystemIsolationInfoEx NAP, interface INapSystemHealthAgentBinding2
- INapSystemHealthAgentBinding2 interface NAP, método GetSystemIsolationInfoEx
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding2.GetSystemIsolationInfoEx
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2643d62afba1a35ebd96b8b39ea2fcf90397576
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499426"
---
# <a name="inapsystemhealthagentbinding2getsystemisolationinfoex-method"></a><span data-ttu-id="87510-106">Método INapSystemHealthAgentBinding2:: GetSystemIsolationInfoEx</span><span class="sxs-lookup"><span data-stu-id="87510-106">INapSystemHealthAgentBinding2::GetSystemIsolationInfoEx method</span></span>

> [!Note]  
> <span data-ttu-id="87510-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="87510-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="87510-108">O método **INapSystemHealthAgentBinding2:: GetSystemIsolationInfoEx** é chamado por SHAs para determinar o estado de isolamento do sistema e o estado de isolamento estendido.</span><span class="sxs-lookup"><span data-stu-id="87510-108">The **INapSystemHealthAgentBinding2::GetSystemIsolationInfoEx** method is called by SHAs to determine the system isolation state and extended isolation state.</span></span>

> [!Note]  
> <span data-ttu-id="87510-109">Use [**INapSystemHealthAgentBinding:: GetSystemIsolationInfo**](inapsystemhealthagentbinding-getsystemisolationinfo-method.md) para determinar apenas o estado de isolamento do sistema.</span><span class="sxs-lookup"><span data-stu-id="87510-109">Use [**INapSystemHealthAgentBinding::GetSystemIsolationInfo**](inapsystemhealthagentbinding-getsystemisolationinfo-method.md) in order to only determine the isolation state of the system.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="87510-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="87510-110">Syntax</span></span>


```C++
HRESULT GetSystemIsolationInfoEx(
  [out] IsolationInfoEx **isolationInfo,
  [out] BOOL            *unknownConnections
) const;
```



## <a name="parameters"></a><span data-ttu-id="87510-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="87510-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87510-112">*isolationInfo* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="87510-112">*isolationInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="87510-113">Um ponteiro para um ponteiro para uma estrutura [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) que contém o estado de isolamento estendido do sistema para conexões conhecidas.</span><span class="sxs-lookup"><span data-stu-id="87510-113">A pointer to a pointer to an [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) structure that contains the extended isolation state of the system for known connections.</span></span> <span data-ttu-id="87510-114">*isolationInfo* indica se o sistema está em um estado de acesso restrito, experiência ou acesso irrestrito, bem como informações de [**ExtendedIsolationState**](/windows/win32/api/naptypes/ne-naptypes-extendedisolationstate) .</span><span class="sxs-lookup"><span data-stu-id="87510-114">*isolationInfo* indicates if the system is in a state of restricted access, probation, or unrestricted access, as well as [**ExtendedIsolationState**](/windows/win32/api/naptypes/ne-naptypes-extendedisolationstate) information.</span></span>

</dd> <dt>

<span data-ttu-id="87510-115">*unknownConnections* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="87510-115">*unknownConnections* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="87510-116">Um ponteiro para um **bool** que será **verdadeiro** se qualquer conexão estiver em um estado desconhecido e **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="87510-116">A pointer to a **BOOL** that is **TRUE** if any connections are in an unknown state and **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87510-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="87510-117">Return value</span></span>

<span data-ttu-id="87510-118">Outros códigos de erro específicos de COM também podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="87510-118">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="87510-119">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="87510-119">Return code</span></span>                                                                                             | <span data-ttu-id="87510-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="87510-120">Description</span></span>                                                                                                                    |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="87510-121"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="87510-121"><dt>**S\_OK** </dt></span></span> </dl>                   | <span data-ttu-id="87510-122">Operação bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="87510-122">Operation succeeded.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="87510-123"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="87510-123"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>         | <span data-ttu-id="87510-124">Erro de permissões, acesso negado.</span><span class="sxs-lookup"><span data-stu-id="87510-124">Permissions error, access denied.</span></span><br/>                                                                                   |
| <dl> <span data-ttu-id="87510-125"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="87510-125"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>          | <span data-ttu-id="87510-126">O limite de recursos do sistema não pôde executar a operação.</span><span class="sxs-lookup"><span data-stu-id="87510-126">System resource limit, could not perform the operation.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="87510-127"><dt>**NAP \_ E \_ não \_ inicializado**</dt></span><span class="sxs-lookup"><span data-stu-id="87510-127"><dt>**NAP\_E\_NOT\_INITIALIZED**</dt></span></span> </dl> | <span data-ttu-id="87510-128">O SHA não foi inicializado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="87510-128">The SHA has not been previously initialized.</span></span><br/>                                                                        |
| <dl> <span data-ttu-id="87510-129"><dt>**RPC \_ E \_ desconectado**</dt></span><span class="sxs-lookup"><span data-stu-id="87510-129"><dt>**RPC\_E\_DISCONNECTED**</dt></span></span> </dl>     | <span data-ttu-id="87510-130">O NapAgent foi interrompido.</span><span class="sxs-lookup"><span data-stu-id="87510-130">The NapAgent has been stopped.</span></span> <span data-ttu-id="87510-131">Este objeto será recuperado automaticamente e reassociado ao NapAgent, depois que ele for reiniciado.</span><span class="sxs-lookup"><span data-stu-id="87510-131">This object will recover automatically and rebind to the NapAgent, once it restarts.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="87510-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="87510-132">Remarks</span></span>

<span data-ttu-id="87510-133">O SHA deve liberar a estrutura [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) chamando [**FreeIsolationInfoEx**](freeisolationinfoex.md).</span><span class="sxs-lookup"><span data-stu-id="87510-133">The SHA must free the [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) structure by calling [**FreeIsolationInfoEx**](freeisolationinfoex.md).</span></span>

<span data-ttu-id="87510-134">O SHA deve chamar [**Initialize**](inapsystemhealthagentbinding-initialize-method.md) antes de chamar este método ou qualquer outro método da interface [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) .</span><span class="sxs-lookup"><span data-stu-id="87510-134">The SHA must call [**Initialize**](inapsystemhealthagentbinding-initialize-method.md) before calling this method or any other method of the [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="87510-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="87510-135">Requirements</span></span>



| <span data-ttu-id="87510-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="87510-136">Requirement</span></span> | <span data-ttu-id="87510-137">Valor</span><span class="sxs-lookup"><span data-stu-id="87510-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87510-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="87510-138">Minimum supported client</span></span><br/> | <span data-ttu-id="87510-139">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="87510-139">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="87510-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="87510-140">Minimum supported server</span></span><br/> | <span data-ttu-id="87510-141">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="87510-141">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="87510-142">parâmetro</span><span class="sxs-lookup"><span data-stu-id="87510-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="87510-143"><dt>NapSystemHealthAgent. h</dt></span><span class="sxs-lookup"><span data-stu-id="87510-143"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="87510-144">INSERI</span><span class="sxs-lookup"><span data-stu-id="87510-144">IDL</span></span><br/>                      | <dl> <span data-ttu-id="87510-145"><dt>NapSystemHealthAgent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="87510-145"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="87510-146">DLL</span><span class="sxs-lookup"><span data-stu-id="87510-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="87510-147"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="87510-147"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="87510-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="87510-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87510-149">**INapSystemHealthAgentBinding2**</span><span class="sxs-lookup"><span data-stu-id="87510-149">**INapSystemHealthAgentBinding2**</span></span>](inapsystemhealthagentbinding2.md)
</dt> </dl>

 

 





