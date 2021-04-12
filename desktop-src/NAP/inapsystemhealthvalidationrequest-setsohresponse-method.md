---
title: Método INapSystemHealthValidationRequest SetSoHResponse (NapSystemHealthValidator. h)
description: Permite que os SHVs (validadores da integridade do sistema) definam o SoHResponse a ser enviado para seu equivalente de SHA (agente de integridade do sistema) no lado do cliente.
ms.assetid: 250b90ac-ce8f-4771-9d20-84c491adfb2c
keywords:
- Método SetSoHResponse NAP
- Método SetSoHResponse NAP, interface INapSystemHealthValidationRequest
- INapSystemHealthValidationRequest interface NAP, método SetSoHResponse
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest.SetSoHResponse
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b818218ef4f8601ecf4927f5e8b90f93e5386b56
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369814"
---
# <a name="inapsystemhealthvalidationrequestsetsohresponse-method"></a><span data-ttu-id="ff776-106">Método INapSystemHealthValidationRequest:: SetSoHResponse</span><span class="sxs-lookup"><span data-stu-id="ff776-106">INapSystemHealthValidationRequest::SetSoHResponse method</span></span>

> [!Note]  
> <span data-ttu-id="ff776-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="ff776-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="ff776-108">O método **INapSystemHealthValidationRequest:: SetSoHResponse** permite que os SHVs (validadores da integridade do sistema) definam o [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) a ser enviado à sua contraparte do agente de integridade do sistema (SHA) no lado do cliente.</span><span class="sxs-lookup"><span data-stu-id="ff776-108">The **INapSystemHealthValidationRequest::SetSoHResponse** method allows System Health Validators (SHVs) to set the [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) to be sent to its System Health Agent (SHA) counterpart on the client-side.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff776-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ff776-109">Syntax</span></span>


```C++
HRESULT SetSoHResponse(
  [in] const SoHResponse *sohResponse
);
```



## <a name="parameters"></a><span data-ttu-id="ff776-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ff776-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff776-111">*sohResponse* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ff776-111">*sohResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff776-112">Um ponteiro para uma estrutura [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) .</span><span class="sxs-lookup"><span data-stu-id="ff776-112">A pointer to a [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff776-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ff776-113">Return value</span></span>

<span data-ttu-id="ff776-114">Outros códigos de erro específicos de COM também podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="ff776-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="ff776-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="ff776-115">Return code</span></span>                                                                                     | <span data-ttu-id="ff776-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="ff776-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="ff776-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ff776-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="ff776-118">Operação bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="ff776-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="ff776-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="ff776-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="ff776-120">Erro de permissões, acesso negado.</span><span class="sxs-lookup"><span data-stu-id="ff776-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="ff776-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="ff776-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="ff776-122">O limite de recursos do sistema não pôde executar a operação.</span><span class="sxs-lookup"><span data-stu-id="ff776-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ff776-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ff776-123">Requirements</span></span>



| <span data-ttu-id="ff776-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff776-124">Requirement</span></span> | <span data-ttu-id="ff776-125">Valor</span><span class="sxs-lookup"><span data-stu-id="ff776-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff776-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ff776-126">Minimum supported client</span></span><br/> | <span data-ttu-id="ff776-127">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="ff776-127">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="ff776-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ff776-128">Minimum supported server</span></span><br/> | <span data-ttu-id="ff776-129">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ff776-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ff776-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ff776-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="ff776-131"><dt>NapSystemHealthValidator. h</dt></span><span class="sxs-lookup"><span data-stu-id="ff776-131"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="ff776-132">INSERI</span><span class="sxs-lookup"><span data-stu-id="ff776-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ff776-133"><dt>NapSystemHealthValidator. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ff776-133"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |
| <span data-ttu-id="ff776-134">DLL</span><span class="sxs-lookup"><span data-stu-id="ff776-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ff776-135"><dt>Qshvhost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ff776-135"><dt>Qshvhost.dll</dt></span></span> </dl>                 |



## <a name="see-also"></a><span data-ttu-id="ff776-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="ff776-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff776-137">**INapSystemHealthValidationRequest**</span><span class="sxs-lookup"><span data-stu-id="ff776-137">**INapSystemHealthValidationRequest**</span></span>](inapsystemhealthvalidationrequest.md)
</dt> </dl>

 

 





