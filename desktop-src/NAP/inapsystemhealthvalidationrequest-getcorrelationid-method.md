---
title: Método CorrelationId INapSystemHealthValidationRequest (NapSystemHealthValidator. h)
description: É usado por SHVs (validadores da integridade do sistema) para recuperar a ID de correlação. Em seguida, o SHV deve registrar essas informações.
ms.assetid: 72603d24-219e-4bb0-9b2b-b58d42939da8
keywords:
- Método CorrelationId NAP
- Método CorrelationId NAP, interface INapSystemHealthValidationRequest
- INapSystemHealthValidationRequest interface NAP, método CorrelationId
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest.GetCorrelationId
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1095a2c3eec90ff33613b6d37b43f31fdabd107
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455063"
---
# <a name="inapsystemhealthvalidationrequestgetcorrelationid-method"></a><span data-ttu-id="e0008-107">Método INapSystemHealthValidationRequest:: CorrelationId</span><span class="sxs-lookup"><span data-stu-id="e0008-107">INapSystemHealthValidationRequest::GetCorrelationId method</span></span>

> [!Note]  
> <span data-ttu-id="e0008-108">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="e0008-108">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="e0008-109">O método **INapSystemHealthValidationRequest:: CorrelationId** é usado pelos SHVs (validadores da integridade do sistema) para recuperar a ID de correlação.</span><span class="sxs-lookup"><span data-stu-id="e0008-109">The **INapSystemHealthValidationRequest::GetCorrelationId** method is used by System Health Validators (SHVs) to retrieve the correlation ID.</span></span> <span data-ttu-id="e0008-110">Em seguida, o SHV deve registrar essas informações.</span><span class="sxs-lookup"><span data-stu-id="e0008-110">The SHV must then log this information.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0008-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e0008-111">Syntax</span></span>


```C++
HRESULT GetCorrelationId(
  [out] CorrelationId *correlationId
);
```



## <a name="parameters"></a><span data-ttu-id="e0008-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e0008-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0008-113">*CorrelationId* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e0008-113">*correlationId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e0008-114">Um ponteiro para uma [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) exclusiva para a troca soh.</span><span class="sxs-lookup"><span data-stu-id="e0008-114">A pointer to a unique [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) for the SoH exchange.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0008-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e0008-115">Return value</span></span>

<span data-ttu-id="e0008-116">Outros códigos de erro específicos de COM também podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="e0008-116">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="e0008-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="e0008-117">Return code</span></span>                                                                                     | <span data-ttu-id="e0008-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="e0008-118">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="e0008-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e0008-119"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="e0008-120">Operação bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="e0008-120">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="e0008-121"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="e0008-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="e0008-122">Erro de permissões, acesso negado.</span><span class="sxs-lookup"><span data-stu-id="e0008-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="e0008-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="e0008-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="e0008-124">O limite de recursos do sistema não pôde executar a operação.</span><span class="sxs-lookup"><span data-stu-id="e0008-124">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="e0008-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e0008-125">Requirements</span></span>



| <span data-ttu-id="e0008-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0008-126">Requirement</span></span> | <span data-ttu-id="e0008-127">Valor</span><span class="sxs-lookup"><span data-stu-id="e0008-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0008-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e0008-128">Minimum supported client</span></span><br/> | <span data-ttu-id="e0008-129">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="e0008-129">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="e0008-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e0008-130">Minimum supported server</span></span><br/> | <span data-ttu-id="e0008-131">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e0008-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e0008-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e0008-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="e0008-133"><dt>NapSystemHealthValidator. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0008-133"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="e0008-134">INSERI</span><span class="sxs-lookup"><span data-stu-id="e0008-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e0008-135"><dt>NapSystemHealthValidator. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e0008-135"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |
| <span data-ttu-id="e0008-136">DLL</span><span class="sxs-lookup"><span data-stu-id="e0008-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e0008-137"><dt>Qshvhost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e0008-137"><dt>Qshvhost.dll</dt></span></span> </dl>                 |



## <a name="see-also"></a><span data-ttu-id="e0008-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="e0008-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0008-139">**INapSystemHealthValidationRequest**</span><span class="sxs-lookup"><span data-stu-id="e0008-139">**INapSystemHealthValidationRequest**</span></span>](inapsystemhealthvalidationrequest.md)
</dt> </dl>

 

 





