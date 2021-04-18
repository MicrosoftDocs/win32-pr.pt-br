---
title: Método INapSystemHealthAgentRequest SetSoHRequest (NapSystemHealthAgent. h)
description: É usado pelos agentes de integridade para gravar sua solicitação SoH resultante da chamada para INapSystemHealthAgentCallback GetSoHRequest.
ms.assetid: 76471cf2-e5df-4e07-b872-ccac0fd45998
keywords:
- Método SetSoHRequest NAP
- Método SetSoHRequest NAP, interface INapSystemHealthAgentRequest
- INapSystemHealthAgentRequest interface NAP, método SetSoHRequest
topic_type:
- apiref
api_name:
- INapSystemHealthAgentRequest.SetSoHRequest
api_location:
- qagentrt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be0fd1dcccad2a402d8455bcdf4f66052d41160b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105751414"
---
# <a name="inapsystemhealthagentrequestsetsohrequest-method"></a><span data-ttu-id="2e6f9-106">Método INapSystemHealthAgentRequest:: SetSoHRequest</span><span class="sxs-lookup"><span data-stu-id="2e6f9-106">INapSystemHealthAgentRequest::SetSoHRequest method</span></span>

> [!Note]  
> <span data-ttu-id="2e6f9-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="2e6f9-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="2e6f9-108">O método **INapSystemHealthAgentRequest:: SetSoHRequest** é usado pelos agentes de integridade para gravar sua solicitação soh resultante da chamada para [**INapSystemHealthAgentCallback:: GetSoHRequest**](inapsystemhealthagentcallback-getsohrequest-method.md).</span><span class="sxs-lookup"><span data-stu-id="2e6f9-108">The **INapSystemHealthAgentRequest::SetSoHRequest** method is used by health agents to write their SoH request resulting from the call to [**INapSystemHealthAgentCallback::GetSoHRequest**](inapsystemhealthagentcallback-getsohrequest-method.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="2e6f9-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2e6f9-109">Syntax</span></span>


```C++
HRESULT SetSoHRequest(
  [in] const SoHRequest *sohRequest,
  [in]       BOOL       cacheSohForLaterUse
);
```



## <a name="parameters"></a><span data-ttu-id="2e6f9-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2e6f9-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e6f9-111">*sohRequest* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2e6f9-111">*sohRequest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e6f9-112">Um ponteiro para um pacote [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) .</span><span class="sxs-lookup"><span data-stu-id="2e6f9-112">A pointer to a [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) packet.</span></span>

</dd> <dt>

<span data-ttu-id="2e6f9-113">*cacheSohForLaterUse* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2e6f9-113">*cacheSohForLaterUse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e6f9-114">Um **bool** que é **verdadeiro** se o NapAgent deve armazenar em cache a [**soh**](/windows/win32/api/naptypes/ns-naptypes-soh) e **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="2e6f9-114">A **BOOL** that is **TRUE** if the NapAgent should cache the [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) and **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e6f9-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2e6f9-115">Return value</span></span>

<span data-ttu-id="2e6f9-116">Outros códigos de erro específicos de COM também podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="2e6f9-116">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="2e6f9-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="2e6f9-117">Return code</span></span>                                                                                     | <span data-ttu-id="2e6f9-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="2e6f9-118">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="2e6f9-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="2e6f9-119"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="2e6f9-120">Operação bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="2e6f9-120">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="2e6f9-121"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="2e6f9-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="2e6f9-122">Erro de permissões, acesso negado.</span><span class="sxs-lookup"><span data-stu-id="2e6f9-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="2e6f9-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="2e6f9-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="2e6f9-124">O limite de recursos do sistema não pôde executar a operação.</span><span class="sxs-lookup"><span data-stu-id="2e6f9-124">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="2e6f9-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e6f9-125">Requirements</span></span>



| <span data-ttu-id="2e6f9-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e6f9-126">Requirement</span></span> | <span data-ttu-id="2e6f9-127">Valor</span><span class="sxs-lookup"><span data-stu-id="2e6f9-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e6f9-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2e6f9-128">Minimum supported client</span></span><br/> | <span data-ttu-id="2e6f9-129">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2e6f9-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="2e6f9-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2e6f9-130">Minimum supported server</span></span><br/> | <span data-ttu-id="2e6f9-131">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2e6f9-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="2e6f9-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2e6f9-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e6f9-133"><dt>NapSystemHealthAgent. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e6f9-133"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="2e6f9-134">INSERI</span><span class="sxs-lookup"><span data-stu-id="2e6f9-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2e6f9-135"><dt>NapSystemHealthAgent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2e6f9-135"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="2e6f9-136">DLL</span><span class="sxs-lookup"><span data-stu-id="2e6f9-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2e6f9-137"><dt>Qagentrt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2e6f9-137"><dt>Qagentrt.dll</dt></span></span> </dl>             |



## <a name="see-also"></a><span data-ttu-id="2e6f9-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="2e6f9-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e6f9-139">**INapSystemHealthAgentRequest**</span><span class="sxs-lookup"><span data-stu-id="2e6f9-139">**INapSystemHealthAgentRequest**</span></span>](inapsystemhealthagentrequest.md)
</dt> </dl>

 

 





