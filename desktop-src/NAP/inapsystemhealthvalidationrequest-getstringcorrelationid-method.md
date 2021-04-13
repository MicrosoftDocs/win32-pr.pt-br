---
title: Método INapSystemHealthValidationRequest GetStringCorrelationId (NapSystemHealthValidator. h)
description: É usado por SHVs (validadores de integridade do sistema) que devem registrar essas informações.
ms.assetid: c3e45857-463b-4048-a178-ec26a318b63b
keywords:
- Método GetStringCorrelationId NAP
- Método GetStringCorrelationId NAP, interface INapSystemHealthValidationRequest
- INapSystemHealthValidationRequest interface NAP, método GetStringCorrelationId
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest.GetStringCorrelationId
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 554a5a31f0aa46f6bcbd7a750662d47ab2c78040
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499828"
---
# <a name="inapsystemhealthvalidationrequestgetstringcorrelationid-method"></a><span data-ttu-id="3f6f7-106">Método INapSystemHealthValidationRequest:: GetStringCorrelationId</span><span class="sxs-lookup"><span data-stu-id="3f6f7-106">INapSystemHealthValidationRequest::GetStringCorrelationId method</span></span>

> [!Note]  
> <span data-ttu-id="3f6f7-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="3f6f7-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="3f6f7-108">O método **INapSystemHealthValidationRequest:: GetStringCorrelationId** é usado pelos SHVs (validadores da integridade do sistema) que devem registrar essas informações.</span><span class="sxs-lookup"><span data-stu-id="3f6f7-108">The **INapSystemHealthValidationRequest::GetStringCorrelationId** method is used by System Health Validators (SHVs) which must log this information.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f6f7-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3f6f7-109">Syntax</span></span>


```C++
HRESULT GetStringCorrelationId(
  [out] StringCorrelationId **correlationId
);
```



## <a name="parameters"></a><span data-ttu-id="3f6f7-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3f6f7-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f6f7-111">*CorrelationId* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="3f6f7-111">*correlationId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3f6f7-112">Um ponteiro para um ponteiro para um [**StringCorrelationId**](nap-type-constants.md) exclusivo para a troca de soh.</span><span class="sxs-lookup"><span data-stu-id="3f6f7-112">A pointer to a pointer to a unique [**StringCorrelationId**](nap-type-constants.md) for the SoH exchange.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f6f7-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3f6f7-113">Return value</span></span>

<span data-ttu-id="3f6f7-114">Outros códigos de erro específicos de COM também podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="3f6f7-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="3f6f7-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="3f6f7-115">Return code</span></span>                                                                                     | <span data-ttu-id="3f6f7-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="3f6f7-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="3f6f7-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3f6f7-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="3f6f7-118">Operação bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="3f6f7-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="3f6f7-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="3f6f7-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="3f6f7-120">Erro de permissões, acesso negado.</span><span class="sxs-lookup"><span data-stu-id="3f6f7-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="3f6f7-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="3f6f7-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="3f6f7-122">O limite de recursos do sistema não pôde executar a operação.</span><span class="sxs-lookup"><span data-stu-id="3f6f7-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="3f6f7-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3f6f7-123">Requirements</span></span>



| <span data-ttu-id="3f6f7-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f6f7-124">Requirement</span></span> | <span data-ttu-id="3f6f7-125">Valor</span><span class="sxs-lookup"><span data-stu-id="3f6f7-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f6f7-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3f6f7-126">Minimum supported client</span></span><br/> | <span data-ttu-id="3f6f7-127">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="3f6f7-127">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="3f6f7-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3f6f7-128">Minimum supported server</span></span><br/> | <span data-ttu-id="3f6f7-129">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3f6f7-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3f6f7-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3f6f7-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="3f6f7-131"><dt>NapSystemHealthValidator. h</dt></span><span class="sxs-lookup"><span data-stu-id="3f6f7-131"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="3f6f7-132">INSERI</span><span class="sxs-lookup"><span data-stu-id="3f6f7-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3f6f7-133"><dt>NapSystemHealthValidator. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3f6f7-133"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |
| <span data-ttu-id="3f6f7-134">DLL</span><span class="sxs-lookup"><span data-stu-id="3f6f7-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3f6f7-135"><dt>Qshvhost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3f6f7-135"><dt>Qshvhost.dll</dt></span></span> </dl>                 |



## <a name="see-also"></a><span data-ttu-id="3f6f7-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="3f6f7-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f6f7-137">**INapSystemHealthValidationRequest**</span><span class="sxs-lookup"><span data-stu-id="3f6f7-137">**INapSystemHealthValidationRequest**</span></span>](inapsystemhealthvalidationrequest.md)
</dt> </dl>

 

 





