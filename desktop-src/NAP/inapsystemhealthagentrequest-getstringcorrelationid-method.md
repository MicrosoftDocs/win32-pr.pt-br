---
title: Método INapSystemHealthAgentRequest GetStringCorrelationId (NapSystemHealthAgent. h)
description: É usado pelos agentes de integridade do sistema para registrar a ID de correlação.
ms.assetid: 5d6f2392-2ada-474a-b150-31e0583c2ea7
keywords:
- Método GetStringCorrelationId NAP
- Método GetStringCorrelationId NAP, interface INapSystemHealthAgentRequest
- INapSystemHealthAgentRequest interface NAP, método GetStringCorrelationId
topic_type:
- apiref
api_name:
- INapSystemHealthAgentRequest.GetStringCorrelationId
api_location:
- qagentrt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f33e98ae4b0fd76d97e85fb3588bcd1f2d33fd2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644501"
---
# <a name="inapsystemhealthagentrequestgetstringcorrelationid-method"></a><span data-ttu-id="0f3c8-106">Método INapSystemHealthAgentRequest:: GetStringCorrelationId</span><span class="sxs-lookup"><span data-stu-id="0f3c8-106">INapSystemHealthAgentRequest::GetStringCorrelationId method</span></span>

> [!Note]  
> <span data-ttu-id="0f3c8-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="0f3c8-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="0f3c8-108">O método **INapSystemHealthAgentRequest:: GetStringCorrelationId** é usado pelos agentes de integridade do sistema para registrar a ID de correlação.</span><span class="sxs-lookup"><span data-stu-id="0f3c8-108">The **INapSystemHealthAgentRequest::GetStringCorrelationId** method is used by system health agents to log the correlation ID.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f3c8-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0f3c8-109">Syntax</span></span>


```C++
HRESULT GetStringCorrelationId(
  [out] StringCorrelationId **correlationId
);
```



## <a name="parameters"></a><span data-ttu-id="0f3c8-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0f3c8-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f3c8-111">*CorrelationId* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="0f3c8-111">*correlationId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0f3c8-112">Um ponteiro para um ponteiro para uma [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) exclusiva para essa troca soh.</span><span class="sxs-lookup"><span data-stu-id="0f3c8-112">A pointer to a pointer to a unique [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) for this SoH exchange.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f3c8-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0f3c8-113">Return value</span></span>

<span data-ttu-id="0f3c8-114">Outros códigos de erro específicos de COM também podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="0f3c8-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="0f3c8-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="0f3c8-115">Return code</span></span>                                                                                     | <span data-ttu-id="0f3c8-116">Description</span><span class="sxs-lookup"><span data-stu-id="0f3c8-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="0f3c8-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0f3c8-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="0f3c8-118">Operação bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="0f3c8-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="0f3c8-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="0f3c8-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="0f3c8-120">Erro de permissões, acesso negado.</span><span class="sxs-lookup"><span data-stu-id="0f3c8-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="0f3c8-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="0f3c8-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="0f3c8-122">O limite de recursos do sistema não pôde executar a operação.</span><span class="sxs-lookup"><span data-stu-id="0f3c8-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="0f3c8-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0f3c8-123">Requirements</span></span>



| <span data-ttu-id="0f3c8-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f3c8-124">Requirement</span></span> | <span data-ttu-id="0f3c8-125">Valor</span><span class="sxs-lookup"><span data-stu-id="0f3c8-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f3c8-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0f3c8-126">Minimum supported client</span></span><br/> | <span data-ttu-id="0f3c8-127">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0f3c8-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="0f3c8-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0f3c8-128">Minimum supported server</span></span><br/> | <span data-ttu-id="0f3c8-129">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0f3c8-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="0f3c8-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0f3c8-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f3c8-131"><dt>NapSystemHealthAgent. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f3c8-131"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="0f3c8-132">INSERI</span><span class="sxs-lookup"><span data-stu-id="0f3c8-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0f3c8-133"><dt>NapSystemHealthAgent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0f3c8-133"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="0f3c8-134">DLL</span><span class="sxs-lookup"><span data-stu-id="0f3c8-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0f3c8-135"><dt>Qagentrt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0f3c8-135"><dt>Qagentrt.dll</dt></span></span> </dl>             |



## <a name="see-also"></a><span data-ttu-id="0f3c8-136">Consulte também</span><span class="sxs-lookup"><span data-stu-id="0f3c8-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f3c8-137">**INapSystemHealthAgentRequest**</span><span class="sxs-lookup"><span data-stu-id="0f3c8-137">**INapSystemHealthAgentRequest**</span></span>](inapsystemhealthagentrequest.md)
</dt> </dl>

 

 





