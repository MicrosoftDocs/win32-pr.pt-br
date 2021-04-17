---
title: Método INapSystemHealthAgentRequest GetCacheSoHFlag (NapSystemHealthAgent. h)
description: É usado somente pelo NapAgent.
ms.assetid: 97dd4e95-30c2-48e2-9359-b1019299581d
keywords:
- Método GetCacheSoHFlag NAP
- Método GetCacheSoHFlag NAP, interface INapSystemHealthAgentRequest
- INapSystemHealthAgentRequest interface NAP, método GetCacheSoHFlag
topic_type:
- apiref
api_name:
- INapSystemHealthAgentRequest.GetCacheSoHFlag
api_location:
- qagentrt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53d8b458e4a49b690fe1f0f53482a72dd253c7c7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499588"
---
# <a name="inapsystemhealthagentrequestgetcachesohflag-method"></a><span data-ttu-id="9d300-106">Método INapSystemHealthAgentRequest:: GetCacheSoHFlag</span><span class="sxs-lookup"><span data-stu-id="9d300-106">INapSystemHealthAgentRequest::GetCacheSoHFlag method</span></span>

> [!Note]  
> <span data-ttu-id="9d300-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="9d300-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="9d300-108">O método **INapSystemHealthAgentRequest:: GetCacheSoHFlag** é usado somente pelo NapAgent.</span><span class="sxs-lookup"><span data-stu-id="9d300-108">The **INapSystemHealthAgentRequest::GetCacheSoHFlag** method is used only by the NapAgent.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d300-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9d300-109">Syntax</span></span>


```C++
HRESULT GetCacheSoHFlag(
   BOOL *cacheSohForLaterUse
);
```



## <a name="parameters"></a><span data-ttu-id="9d300-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9d300-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d300-111">*cacheSohForLaterUse*</span><span class="sxs-lookup"><span data-stu-id="9d300-111">*cacheSohForLaterUse*</span></span> 
</dt> <dd>

<span data-ttu-id="9d300-112">Um **bool** que é **verdadeiro** se o NapAgent deve armazenar em cache a [**soh**](/windows/win32/api/naptypes/ns-naptypes-soh) e **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="9d300-112">A **BOOL** that is **TRUE** if the NapAgent should cache the [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) and **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d300-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9d300-113">Return value</span></span>

<span data-ttu-id="9d300-114">Outros códigos de erro específicos de COM também podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="9d300-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="9d300-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="9d300-115">Return code</span></span>                                                                                     | <span data-ttu-id="9d300-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="9d300-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="9d300-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9d300-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="9d300-118">Operação bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="9d300-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="9d300-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="9d300-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="9d300-120">Erro de permissões, acesso negado.</span><span class="sxs-lookup"><span data-stu-id="9d300-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="9d300-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="9d300-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="9d300-122">O limite de recursos do sistema não pôde executar a operação.</span><span class="sxs-lookup"><span data-stu-id="9d300-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="9d300-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9d300-123">Requirements</span></span>



| <span data-ttu-id="9d300-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d300-124">Requirement</span></span> | <span data-ttu-id="9d300-125">Valor</span><span class="sxs-lookup"><span data-stu-id="9d300-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d300-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9d300-126">Minimum supported client</span></span><br/> | <span data-ttu-id="9d300-127">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9d300-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="9d300-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9d300-128">Minimum supported server</span></span><br/> | <span data-ttu-id="9d300-129">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9d300-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="9d300-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9d300-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="9d300-131"><dt>NapSystemHealthAgent. h</dt></span><span class="sxs-lookup"><span data-stu-id="9d300-131"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="9d300-132">INSERI</span><span class="sxs-lookup"><span data-stu-id="9d300-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9d300-133"><dt>NapSystemHealthAgent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9d300-133"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="9d300-134">DLL</span><span class="sxs-lookup"><span data-stu-id="9d300-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9d300-135"><dt>Qagentrt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9d300-135"><dt>Qagentrt.dll</dt></span></span> </dl>             |



## <a name="see-also"></a><span data-ttu-id="9d300-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="9d300-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d300-137">**INapSystemHealthAgentRequest**</span><span class="sxs-lookup"><span data-stu-id="9d300-137">**INapSystemHealthAgentRequest**</span></span>](inapsystemhealthagentrequest.md)
</dt> </dl>

 

 





