---
title: Método INapSystemHealthAgentBinding GetSystemIsolationInfo (NapSystemHealthAgent. h)
description: É chamado por SHAs para determinar o estado de isolamento do sistema.
ms.assetid: 0401a846-0da2-4975-87bc-3e9fe8b5b67d
keywords:
- Método GetSystemIsolationInfo NAP
- Método GetSystemIsolationInfo NAP, interface INapSystemHealthAgentBinding
- INapSystemHealthAgentBinding interface NAP, método GetSystemIsolationInfo
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding.GetSystemIsolationInfo
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0323149be50cd8896a191ca57584cea0c015487
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455923"
---
# <a name="inapsystemhealthagentbindinggetsystemisolationinfo-method"></a><span data-ttu-id="ea8d6-106">Método INapSystemHealthAgentBinding:: GetSystemIsolationInfo</span><span class="sxs-lookup"><span data-stu-id="ea8d6-106">INapSystemHealthAgentBinding::GetSystemIsolationInfo method</span></span>

> [!Note]  
> <span data-ttu-id="ea8d6-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="ea8d6-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="ea8d6-108">O método **INapSystemHealthAgentBinding:: GetSystemIsolationInfo** é chamado por SHAs para determinar o estado de isolamento do sistema.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-108">The **INapSystemHealthAgentBinding::GetSystemIsolationInfo** method is called by SHAs to determine the system isolation state.</span></span>

> [!Note]  
> <span data-ttu-id="ea8d6-109">Use [**INapSystemHealthAgentBinding2:: GetSystemIsolationInfoEx**](inapsystemhealthagentbinding2-getsystemisolationinfoex.md) para determinar o estado de isolamento estendido do sistema.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-109">Use [**INapSystemHealthAgentBinding2::GetSystemIsolationInfoEx**](inapsystemhealthagentbinding2-getsystemisolationinfoex.md) in order to determine the extended isolation state of the system.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="ea8d6-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ea8d6-110">Syntax</span></span>


```C++
HRESULT GetSystemIsolationInfo(
  [out] IsolationInfo **isolationInfo,
  [out] BOOL          *unknownConnections
);
```



## <a name="parameters"></a><span data-ttu-id="ea8d6-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ea8d6-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea8d6-112">*isolationInfo* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ea8d6-112">*isolationInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ea8d6-113">Um ponteiro para um ponteiro para uma estrutura [**IsolationInfo**](/windows/win32/api/naptypes/ns-naptypes-isolationinfo) que contém o estado de isolamento do sistema para conexões conhecidas.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-113">A pointer to a pointer to an [**IsolationInfo**](/windows/win32/api/naptypes/ns-naptypes-isolationinfo) structure that contains the isolation state of the system for known connections.</span></span> <span data-ttu-id="ea8d6-114">*isolationInfoindicates* se o sistema estiver em um estado de acesso restrito, experiência ou acesso irrestrito.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-114">*isolationInfoindicates* if the system is in a state of restricted access, probation, or unrestricted access.</span></span>

</dd> <dt>

<span data-ttu-id="ea8d6-115">*unknownConnections* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ea8d6-115">*unknownConnections* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ea8d6-116">Um ponteiro para um **bool** que será **verdadeiro** se qualquer conexão estiver em um estado desconhecido e **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-116">A pointer to a **BOOL** that is **TRUE** if any connections are in an unknown state and **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea8d6-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ea8d6-117">Return value</span></span>

<span data-ttu-id="ea8d6-118">Outros códigos de erro específicos de COM também podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-118">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="ea8d6-119">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="ea8d6-119">Return code</span></span>                                                                                             | <span data-ttu-id="ea8d6-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="ea8d6-120">Description</span></span>                                                                                                                    |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ea8d6-121"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ea8d6-121"><dt>**S\_OK** </dt></span></span> </dl>                   | <span data-ttu-id="ea8d6-122">Operação bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-122">Operation succeeded.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="ea8d6-123"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="ea8d6-123"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>         | <span data-ttu-id="ea8d6-124">Erro de permissões, acesso negado.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-124">Permissions error, access denied.</span></span><br/>                                                                                   |
| <dl> <span data-ttu-id="ea8d6-125"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="ea8d6-125"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>          | <span data-ttu-id="ea8d6-126">O limite de recursos do sistema não pôde executar a operação.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-126">System resource limit, could not perform the operation.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="ea8d6-127"><dt>**NAP \_ E \_ não \_ inicializado**</dt></span><span class="sxs-lookup"><span data-stu-id="ea8d6-127"><dt>**NAP\_E\_NOT\_INITIALIZED**</dt></span></span> </dl> | <span data-ttu-id="ea8d6-128">O SHA não foi inicializado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-128">The SHA has not been previously initialized.</span></span><br/>                                                                        |
| <dl> <span data-ttu-id="ea8d6-129"><dt>**RPC \_ E \_ desconectado**</dt></span><span class="sxs-lookup"><span data-stu-id="ea8d6-129"><dt>**RPC\_E\_DISCONNECTED**</dt></span></span> </dl>     | <span data-ttu-id="ea8d6-130">O NapAgent foi interrompido.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-130">The NapAgent has been stopped.</span></span> <span data-ttu-id="ea8d6-131">Este objeto será recuperado automaticamente e reassociado ao NapAgent, depois que ele for reiniciado.</span><span class="sxs-lookup"><span data-stu-id="ea8d6-131">This object will recover automatically and rebind to the NapAgent, once it restarts.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ea8d6-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="ea8d6-132">Remarks</span></span>

<span data-ttu-id="ea8d6-133">O SHA deve chamar [**Initialize**](inapsystemhealthagentbinding-initialize-method.md) antes de chamar este método ou qualquer outro método da interface [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) .</span><span class="sxs-lookup"><span data-stu-id="ea8d6-133">The SHA must call [**Initialize**](inapsystemhealthagentbinding-initialize-method.md) before calling this method or any other method of the [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea8d6-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ea8d6-134">Requirements</span></span>



| <span data-ttu-id="ea8d6-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea8d6-135">Requirement</span></span> | <span data-ttu-id="ea8d6-136">Valor</span><span class="sxs-lookup"><span data-stu-id="ea8d6-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea8d6-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ea8d6-137">Minimum supported client</span></span><br/> | <span data-ttu-id="ea8d6-138">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ea8d6-138">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="ea8d6-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ea8d6-139">Minimum supported server</span></span><br/> | <span data-ttu-id="ea8d6-140">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ea8d6-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="ea8d6-141">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ea8d6-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea8d6-142"><dt>NapSystemHealthAgent. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea8d6-142"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="ea8d6-143">INSERI</span><span class="sxs-lookup"><span data-stu-id="ea8d6-143">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ea8d6-144"><dt>NapSystemHealthAgent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ea8d6-144"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="ea8d6-145">DLL</span><span class="sxs-lookup"><span data-stu-id="ea8d6-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ea8d6-146"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ea8d6-146"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="ea8d6-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="ea8d6-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea8d6-148">**INapSystemHealthAgentBinding**</span><span class="sxs-lookup"><span data-stu-id="ea8d6-148">**INapSystemHealthAgentBinding**</span></span>](inapsystemhealthagentbinding.md)
</dt> </dl>

 

 





