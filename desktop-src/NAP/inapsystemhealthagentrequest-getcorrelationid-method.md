---
title: Método CorrelationId INapSystemHealthAgentRequest (NapSystemHealthAgent. h)
description: É usado pelos agentes de integridade do sistema para correlacionar as respostas soh e SoH.
ms.assetid: 220db71a-31d7-45a7-a8e7-ddb4955d546e
keywords:
- Método CorrelationId NAP
- Método CorrelationId NAP, interface INapSystemHealthAgentRequest
- INapSystemHealthAgentRequest interface NAP, método CorrelationId
topic_type:
- apiref
api_name:
- INapSystemHealthAgentRequest.GetCorrelationId
api_location:
- qagentrt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7af5b182df738ec22c75f2afffd1adb3591007be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499854"
---
# <a name="inapsystemhealthagentrequestgetcorrelationid-method"></a><span data-ttu-id="ac48d-106">Método INapSystemHealthAgentRequest:: CorrelationId</span><span class="sxs-lookup"><span data-stu-id="ac48d-106">INapSystemHealthAgentRequest::GetCorrelationId method</span></span>

> [!Note]  
> <span data-ttu-id="ac48d-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="ac48d-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="ac48d-108">O método **INapSystemHealthAgentRequest:: CorrelationId** é usado pelos agentes de integridade do sistema para correlacionar as respostas soh e soh.</span><span class="sxs-lookup"><span data-stu-id="ac48d-108">The **INapSystemHealthAgentRequest::GetCorrelationId** method is used by system health agents to correlate SoH's and SoH-Responses.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac48d-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ac48d-109">Syntax</span></span>


```C++
HRESULT GetCorrelationId(
  [out] CorrelationId *correlationId
);
```



## <a name="parameters"></a><span data-ttu-id="ac48d-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ac48d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac48d-111">*CorrelationId* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ac48d-111">*correlationId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ac48d-112">Um ponteiro para uma [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) exclusiva para a troca soh.</span><span class="sxs-lookup"><span data-stu-id="ac48d-112">A pointer to a unique [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) for the SoH exchange.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac48d-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ac48d-113">Return value</span></span>

<span data-ttu-id="ac48d-114">Outros códigos de erro específicos de COM também podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="ac48d-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="ac48d-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="ac48d-115">Return code</span></span>                                                                                     | <span data-ttu-id="ac48d-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="ac48d-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="ac48d-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ac48d-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="ac48d-118">Operação bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="ac48d-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="ac48d-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="ac48d-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="ac48d-120">Erro de permissões, acesso negado.</span><span class="sxs-lookup"><span data-stu-id="ac48d-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="ac48d-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="ac48d-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="ac48d-122">O limite de recursos do sistema não pôde executar a operação.</span><span class="sxs-lookup"><span data-stu-id="ac48d-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ac48d-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ac48d-123">Requirements</span></span>



| <span data-ttu-id="ac48d-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac48d-124">Requirement</span></span> | <span data-ttu-id="ac48d-125">Valor</span><span class="sxs-lookup"><span data-stu-id="ac48d-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac48d-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ac48d-126">Minimum supported client</span></span><br/> | <span data-ttu-id="ac48d-127">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ac48d-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="ac48d-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ac48d-128">Minimum supported server</span></span><br/> | <span data-ttu-id="ac48d-129">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ac48d-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="ac48d-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ac48d-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="ac48d-131"><dt>NapSystemHealthAgent. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac48d-131"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="ac48d-132">INSERI</span><span class="sxs-lookup"><span data-stu-id="ac48d-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ac48d-133"><dt>NapSystemHealthAgent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ac48d-133"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="ac48d-134">DLL</span><span class="sxs-lookup"><span data-stu-id="ac48d-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ac48d-135"><dt>Qagentrt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ac48d-135"><dt>Qagentrt.dll</dt></span></span> </dl>             |



## <a name="see-also"></a><span data-ttu-id="ac48d-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="ac48d-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac48d-137">**INapSystemHealthAgentRequest**</span><span class="sxs-lookup"><span data-stu-id="ac48d-137">**INapSystemHealthAgentRequest**</span></span>](inapsystemhealthagentrequest.md)
</dt> </dl>

 

 





