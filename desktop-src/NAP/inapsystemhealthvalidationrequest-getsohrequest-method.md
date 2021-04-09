---
title: Método INapSystemHealthValidationRequest GetSoHRequest (NapSystemHealthValidator. h)
description: Permite que os SHVs (validadores da integridade do sistema) recuperem e validem as informações de SoHRequest enviadas por seus equivalentes de SHA (agente de integridade do sistema) no cliente.
ms.assetid: e06e07c6-7305-4171-b94e-19c360e94c67
keywords:
- Método GetSoHRequest NAP
- Método GetSoHRequest NAP, interface INapSystemHealthValidationRequest
- INapSystemHealthValidationRequest interface NAP, método GetSoHRequest
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest.GetSoHRequest
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 306c9307f99f91e0b0a48a1c5ffeaf19b4ea1f12
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086468"
---
# <a name="inapsystemhealthvalidationrequestgetsohrequest-method"></a><span data-ttu-id="fb3c3-106">Método INapSystemHealthValidationRequest:: GetSoHRequest</span><span class="sxs-lookup"><span data-stu-id="fb3c3-106">INapSystemHealthValidationRequest::GetSoHRequest method</span></span>

> [!Note]  
> <span data-ttu-id="fb3c3-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="fb3c3-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="fb3c3-108">O método **INapSystemHealthValidationRequest:: GetSoHRequest** permite que os SHVs (validadores da integridade do sistema) recuperem e validem as informações de [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) enviadas por suas contrapartes do Sha (agente de integridade do sistema) no cliente.</span><span class="sxs-lookup"><span data-stu-id="fb3c3-108">The **INapSystemHealthValidationRequest::GetSoHRequest** method allows System Health Validators (SHVs) to retrieve and validate the [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) information sent by their System Health Agent (SHA) counterparts on the client.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb3c3-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fb3c3-109">Syntax</span></span>


```C++
HRESULT GetSoHRequest(
  [out] SoHRequest **sohRequest,
  [out] BOOL       *napSystemGenerated
);
```



## <a name="parameters"></a><span data-ttu-id="fb3c3-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fb3c3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb3c3-111">*sohRequest* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="fb3c3-111">*sohRequest* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fb3c3-112">Um ponteiro para um ponteiro para uma estrutura [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) .</span><span class="sxs-lookup"><span data-stu-id="fb3c3-112">A pointer to a pointer to an [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) structure.</span></span>

</dd> <dt>

<span data-ttu-id="fb3c3-113">*napSystemGenerated* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="fb3c3-113">*napSystemGenerated* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fb3c3-114">Um **bool** que é **verdadeiro** se a soh foi criada pelo NAPAGENT em nome do Sha e **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="fb3c3-114">A **BOOL** that is **TRUE** if the SoH was created by the NapAgent on behalf of the SHA and **FALSE** otherwise.</span></span> <span data-ttu-id="fb3c3-115">Ele é usado principalmente para indicar uma falha de SHA para o SHV.</span><span class="sxs-lookup"><span data-stu-id="fb3c3-115">It is primarily used to indicate an SHA failure to the SHV.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb3c3-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fb3c3-116">Return value</span></span>

<span data-ttu-id="fb3c3-117">Outros códigos de erro específicos de COM também podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="fb3c3-117">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="fb3c3-118">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="fb3c3-118">Return code</span></span>                                                                                     | <span data-ttu-id="fb3c3-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="fb3c3-119">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="fb3c3-120"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="fb3c3-120"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="fb3c3-121">Operação bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="fb3c3-121">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="fb3c3-122"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="fb3c3-122"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="fb3c3-123">Erro de permissões, acesso negado.</span><span class="sxs-lookup"><span data-stu-id="fb3c3-123">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="fb3c3-124"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="fb3c3-124"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="fb3c3-125">O limite de recursos do sistema não pôde executar a operação.</span><span class="sxs-lookup"><span data-stu-id="fb3c3-125">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="fb3c3-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="fb3c3-126">Remarks</span></span>

<span data-ttu-id="fb3c3-127">O parâmetro *sohRequest* pode retornar **NULL** se o cliente não enviou um [**sohRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) para o SHV.</span><span class="sxs-lookup"><span data-stu-id="fb3c3-127">The *sohRequest* parameter may return **NULL** if the client did not send an [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) to the SHV.</span></span> <span data-ttu-id="fb3c3-128">Nesse cenário, o SHV pode popular um **SoHResponse** com o código de erro de [**NAP \_ E \_ faltando \_ soh**](nap-error-constants.md).</span><span class="sxs-lookup"><span data-stu-id="fb3c3-128">In that scenario the SHV can populate an **SoHResponse** with the error code of [**NAP\_E\_MISSING\_SOH**](nap-error-constants.md).</span></span>

<span data-ttu-id="fb3c3-129">Se o parâmetro *napSystemGenerated* for **true**, o formato de *SoHRequest* será o seguinte:</span><span class="sxs-lookup"><span data-stu-id="fb3c3-129">If the *napSystemGenerated* parameter is **TRUE**, the format of *SoHRequest* is as follows:</span></span>

-   <span data-ttu-id="fb3c3-130">[**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md)= <id></span><span class="sxs-lookup"><span data-stu-id="fb3c3-130">[**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md)= <id></span></span>
-   <span data-ttu-id="fb3c3-131">[**sohAttributeTypeFailureCategory**](sohattributetype-enum.md) =  [ **failureCategoryClientComponent**](/windows/win32/api/naptypes/ne-naptypes-failurecategory)</span><span class="sxs-lookup"><span data-stu-id="fb3c3-131">[**sohAttributeTypeFailureCategory**](sohattributetype-enum.md)= [**failureCategoryClientComponent**](/windows/win32/api/naptypes/ne-naptypes-failurecategory)</span></span>
-   <span data-ttu-id="fb3c3-132">[**sohAttributeTypeErrorCodes**](sohattributetype-enum.md)  =  [ **<Sha-falha-erro-código>**](nap-error-constants.md)</span><span class="sxs-lookup"><span data-stu-id="fb3c3-132">[**sohAttributeTypeErrorCodes**](sohattributetype-enum.md) = [**<sha-failure-error-code>**](nap-error-constants.md)</span></span>

## <a name="requirements"></a><span data-ttu-id="fb3c3-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fb3c3-133">Requirements</span></span>



| <span data-ttu-id="fb3c3-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb3c3-134">Requirement</span></span> | <span data-ttu-id="fb3c3-135">Valor</span><span class="sxs-lookup"><span data-stu-id="fb3c3-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb3c3-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fb3c3-136">Minimum supported client</span></span><br/> | <span data-ttu-id="fb3c3-137">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="fb3c3-137">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="fb3c3-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fb3c3-138">Minimum supported server</span></span><br/> | <span data-ttu-id="fb3c3-139">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fb3c3-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fb3c3-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fb3c3-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="fb3c3-141"><dt>NapSystemHealthValidator. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb3c3-141"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="fb3c3-142">INSERI</span><span class="sxs-lookup"><span data-stu-id="fb3c3-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fb3c3-143"><dt>NapSystemHealthValidator. idl</dt></span><span class="sxs-lookup"><span data-stu-id="fb3c3-143"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |
| <span data-ttu-id="fb3c3-144">DLL</span><span class="sxs-lookup"><span data-stu-id="fb3c3-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fb3c3-145"><dt>Qshvhost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb3c3-145"><dt>Qshvhost.dll</dt></span></span> </dl>                 |



## <a name="see-also"></a><span data-ttu-id="fb3c3-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="fb3c3-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb3c3-147">**INapSystemHealthValidationRequest**</span><span class="sxs-lookup"><span data-stu-id="fb3c3-147">**INapSystemHealthValidationRequest**</span></span>](inapsystemhealthvalidationrequest.md)
</dt> </dl>

 

 





