---
title: Interface INapSystemHealthValidationRequest (NapSystemHealthValidator. h)
description: São usados para dar suporte a validadores de integridade do sistema que são definidos pelo desenvolvedor do aplicativo.
ms.assetid: faa91ff5-49f5-4aec-81d7-02ec59274f23
keywords:
- INapSystemHealthValidationRequest da interface NAP
- INapSystemHealthValidationRequest interface NAP, descrita
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf09f93e00401251a3d0e2296323edeb84ad6007
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645158"
---
# <a name="inapsystemhealthvalidationrequest-interface"></a><span data-ttu-id="54d9b-105">Interface INapSystemHealthValidationRequest</span><span class="sxs-lookup"><span data-stu-id="54d9b-105">INapSystemHealthValidationRequest interface</span></span>

> [!Note]  
> <span data-ttu-id="54d9b-106">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="54d9b-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="54d9b-107">A interface **INapSystemHealthValidationRequest** fornece métodos que são usados para dar suporte a validadores de integridade do sistema que são definidos pelo desenvolvedor do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="54d9b-107">The **INapSystemHealthValidationRequest** interface provides methods that are used to support system health validators which are defined by the application developer.</span></span>

> [!Note]  
> <span data-ttu-id="54d9b-108">[**INapSystemHealthValidationRequest2**](inapsystemhealthvalidationrequest2.md) herda todos os métodos dessa interface e deve ser usado em seu lugar.</span><span class="sxs-lookup"><span data-stu-id="54d9b-108">[**INapSystemHealthValidationRequest2**](inapsystemhealthvalidationrequest2.md) inherits all the methods of this interface and should be used instead.</span></span>

 

## <a name="members"></a><span data-ttu-id="54d9b-109">Membros</span><span class="sxs-lookup"><span data-stu-id="54d9b-109">Members</span></span>

<span data-ttu-id="54d9b-110">A interface **INapSystemHealthValidationRequest** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="54d9b-110">The **INapSystemHealthValidationRequest** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="54d9b-111">**INapSystemHealthValidationRequest** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="54d9b-111">**INapSystemHealthValidationRequest** also has these types of members:</span></span>

-   [<span data-ttu-id="54d9b-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="54d9b-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="54d9b-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="54d9b-113">Methods</span></span>

<span data-ttu-id="54d9b-114">A interface **INapSystemHealthValidationRequest** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="54d9b-114">The **INapSystemHealthValidationRequest** interface has these methods.</span></span>



| <span data-ttu-id="54d9b-115">Método</span><span class="sxs-lookup"><span data-stu-id="54d9b-115">Method</span></span>                                                                                                                               | <span data-ttu-id="54d9b-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="54d9b-116">Description</span></span>                                                                                                           |
|:-------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="54d9b-117">**INapSystemHealthValidationRequest:: CorrelationId**</span><span class="sxs-lookup"><span data-stu-id="54d9b-117">**INapSystemHealthValidationRequest::GetCorrelationId**</span></span>](inapsystemhealthvalidationrequest-getcorrelationid-method.md)             | <span data-ttu-id="54d9b-118">Usado por validadores para recuperar a ID de correlação.</span><span class="sxs-lookup"><span data-stu-id="54d9b-118">Used by validators to retrieve the correlation ID.</span></span> <span data-ttu-id="54d9b-119">Em seguida, o validador deve registrar essas informações.</span><span class="sxs-lookup"><span data-stu-id="54d9b-119">The validator must then log this information.</span></span><br/>           |
| [<span data-ttu-id="54d9b-120">**INapSystemHealthValidationRequest:: GetMachineName**</span><span class="sxs-lookup"><span data-stu-id="54d9b-120">**INapSystemHealthValidationRequest::GetMachineName**</span></span>](inapsystemhealthvalidationrequest-getmachinename-method.md)                 | <span data-ttu-id="54d9b-121">Usado por validadores para recuperar o nome do computador.</span><span class="sxs-lookup"><span data-stu-id="54d9b-121">Used by validators to retrieve the machine name.</span></span> <span data-ttu-id="54d9b-122">Em seguida, o validador deve registrar essas informações.</span><span class="sxs-lookup"><span data-stu-id="54d9b-122">The validator must then log this information.</span></span><br/>             |
| [<span data-ttu-id="54d9b-123">**INapSystemHealthValidationRequest::GetPrivateData**</span><span class="sxs-lookup"><span data-stu-id="54d9b-123">**INapSystemHealthValidationRequest::GetPrivateData**</span></span>](inapsystemhealthvalidationrequest-getprivatedata-method.md)                 | <span data-ttu-id="54d9b-124">Permite que o NapServer recupere informações de estado.</span><span class="sxs-lookup"><span data-stu-id="54d9b-124">Allows the NapServer to retrieve state information.</span></span><br/>                                                        |
| [<span data-ttu-id="54d9b-125">**INapSystemHealthValidationRequest::GetSoHRequest**</span><span class="sxs-lookup"><span data-stu-id="54d9b-125">**INapSystemHealthValidationRequest::GetSoHRequest**</span></span>](inapsystemhealthvalidationrequest-getsohrequest-method.md)                   | <span data-ttu-id="54d9b-126">Permite que os validadores recuperem e validem as informações de SoHRequest.</span><span class="sxs-lookup"><span data-stu-id="54d9b-126">Allows Validators to retrieve and validate the SoHRequest information.</span></span><br/>                                     |
| [<span data-ttu-id="54d9b-127">**INapSystemHealthValidationRequest::GetSoHResponse**</span><span class="sxs-lookup"><span data-stu-id="54d9b-127">**INapSystemHealthValidationRequest::GetSoHResponse**</span></span>](inapsystemhealthvalidationrequest-getsohresponse-method.md)                 | <span data-ttu-id="54d9b-128">Obtém o objeto SoHResponse.</span><span class="sxs-lookup"><span data-stu-id="54d9b-128">Gets the SoHResponse object.</span></span><br/>                                                                               |
| [<span data-ttu-id="54d9b-129">**INapSystemHealthValidationRequest::GetStringCorrelationId**</span><span class="sxs-lookup"><span data-stu-id="54d9b-129">**INapSystemHealthValidationRequest::GetStringCorrelationId**</span></span>](inapsystemhealthvalidationrequest-getstringcorrelationid-method.md) | <span data-ttu-id="54d9b-130">Usado por validadores para recuperar um identificador de troca exclusivo.</span><span class="sxs-lookup"><span data-stu-id="54d9b-130">Used by validators to retrieve a unique exchange identifier.</span></span> <span data-ttu-id="54d9b-131">Em seguida, o validador deve registrar essas informações.</span><span class="sxs-lookup"><span data-stu-id="54d9b-131">The validator must then log this information.</span></span><br/> |
| [<span data-ttu-id="54d9b-132">**INapSystemHealthValidationRequest::SetPrivateData**</span><span class="sxs-lookup"><span data-stu-id="54d9b-132">**INapSystemHealthValidationRequest::SetPrivateData**</span></span>](inapsystemhealthvalidationrequest-setprivatedata-method.md)                 | <span data-ttu-id="54d9b-133">Permite que o NapServer armazene informações de estado.</span><span class="sxs-lookup"><span data-stu-id="54d9b-133">Allows the NapServer to store state information.</span></span><br/>                                                           |
| [<span data-ttu-id="54d9b-134">**INapSystemHealthValidationRequest::SetSoHResponse**</span><span class="sxs-lookup"><span data-stu-id="54d9b-134">**INapSystemHealthValidationRequest::SetSoHResponse**</span></span>](inapsystemhealthvalidationrequest-setsohresponse-method.md)                 | <span data-ttu-id="54d9b-135">Permite que os validadores definam o SoHResponse.</span><span class="sxs-lookup"><span data-stu-id="54d9b-135">Allows validators to set the SoHResponse.</span></span><br/>                                                                  |



 

## <a name="requirements"></a><span data-ttu-id="54d9b-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="54d9b-136">Requirements</span></span>



| <span data-ttu-id="54d9b-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="54d9b-137">Requirement</span></span> | <span data-ttu-id="54d9b-138">Valor</span><span class="sxs-lookup"><span data-stu-id="54d9b-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54d9b-139">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="54d9b-139">Minimum supported client</span></span><br/> | <span data-ttu-id="54d9b-140">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="54d9b-140">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="54d9b-141">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="54d9b-141">Minimum supported server</span></span><br/> | <span data-ttu-id="54d9b-142">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="54d9b-142">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="54d9b-143">parâmetro</span><span class="sxs-lookup"><span data-stu-id="54d9b-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="54d9b-144"><dt>NapSystemHealthValidator. h</dt></span><span class="sxs-lookup"><span data-stu-id="54d9b-144"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="54d9b-145">INSERI</span><span class="sxs-lookup"><span data-stu-id="54d9b-145">IDL</span></span><br/>                      | <dl> <span data-ttu-id="54d9b-146"><dt>NapSystemHealthValidator. idl</dt></span><span class="sxs-lookup"><span data-stu-id="54d9b-146"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |
| <span data-ttu-id="54d9b-147">DLL</span><span class="sxs-lookup"><span data-stu-id="54d9b-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="54d9b-148"><dt>Qshvhost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="54d9b-148"><dt>Qshvhost.dll</dt></span></span> </dl>                 |



## <a name="see-also"></a><span data-ttu-id="54d9b-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="54d9b-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54d9b-150">Interfaces NAP</span><span class="sxs-lookup"><span data-stu-id="54d9b-150">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="54d9b-151">Referência de NAP</span><span class="sxs-lookup"><span data-stu-id="54d9b-151">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

