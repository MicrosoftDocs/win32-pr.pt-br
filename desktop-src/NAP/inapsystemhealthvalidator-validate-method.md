---
title: Método de validação de INapSystemHealthValidator (NapSystemHealthValidator. h)
description: O sistema NAP para validar o SoHRequest recebido de um cliente.
ms.assetid: d67dc2c8-f18c-4e06-a51e-a538ca75c3f1
keywords:
- Validar método NAP
- Validar método NAP, interface INapSystemHealthValidator
- INapSystemHealthValidator interface NAP, método Validate
topic_type:
- apiref
api_name:
- INapSystemHealthValidator.Validate
api_location:
- NapSystemHealthValidator.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f7589a67b9a3b1454e3c65b17ad6f584ce0e655
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105779610"
---
# <a name="inapsystemhealthvalidatorvalidate-method"></a><span data-ttu-id="79fee-106">Método INapSystemHealthValidator:: Validate</span><span class="sxs-lookup"><span data-stu-id="79fee-106">INapSystemHealthValidator::Validate method</span></span>

> [!Note]  
> <span data-ttu-id="79fee-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="79fee-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="79fee-108">O método **INapSystemHealthValidator:: Validate** é definido pelo desenvolvedor SHV e chamado pelo sistema NAP para validar o [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) recebido de um cliente.</span><span class="sxs-lookup"><span data-stu-id="79fee-108">The **INapSystemHealthValidator::Validate** method is defined by the SHV developer and called by the NAP system to validate the [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) received from a client.</span></span>

## <a name="syntax"></a><span data-ttu-id="79fee-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="79fee-109">Syntax</span></span>


```C++
HRESULT Validate(
  [in] INapSystemHealthValidationRequest *request,
  [in] UINT32                            hintTimeOutInMsec,
  [in] INapServerCallback                *callback
);
```



## <a name="parameters"></a><span data-ttu-id="79fee-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="79fee-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79fee-111">*solicitação* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="79fee-111">*request* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79fee-112">Um ponteiro COM para um objeto [**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md) que identifica o objeto de solicitação de validação.</span><span class="sxs-lookup"><span data-stu-id="79fee-112">A COM pointer to an [**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md) object that identifies the validation request object.</span></span>

</dd> <dt>

<span data-ttu-id="79fee-113">*hintTimeOutInMsec* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="79fee-113">*hintTimeOutInMsec* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79fee-114">A duração, em milissegundos, do período de tempo limite de comunicação.</span><span class="sxs-lookup"><span data-stu-id="79fee-114">The duration, in milliseconds, of the communication timeout period.</span></span> <span data-ttu-id="79fee-115">O SHV (validador da integridade do sistema) deve responder dentro desse período de tempo; caso contrário, a resposta será descartada.</span><span class="sxs-lookup"><span data-stu-id="79fee-115">The System Health Validator (SHV) should respond within this amount of time; otherwise the response is dropped.</span></span>

> [!Note]  
> <span data-ttu-id="79fee-116">O tempo limite padrão para todos os SHVs é de 2000 milissegundos.</span><span class="sxs-lookup"><span data-stu-id="79fee-116">The default timeout for all SHVs is 2000 milliseconds.</span></span> <span data-ttu-id="79fee-117">Usar um valor diferente do padrão irá alterar o tempo limite de todos os SHVs registrados.</span><span class="sxs-lookup"><span data-stu-id="79fee-117">Using a value other than the default will change the timeout for all registered SHVs.</span></span>

 

</dd> <dt>

<span data-ttu-id="79fee-118">*retorno de chamada* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="79fee-118">*callback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79fee-119">Um ponteiro para o objeto de retorno de chamada [**INapServerCallback**](inapservercallback.md).</span><span class="sxs-lookup"><span data-stu-id="79fee-119">A pointer to the callback object [**INapServerCallback**](inapservercallback.md).</span></span> <span data-ttu-id="79fee-120">Esse ponteiro de retorno de chamada é usado pelos SHVs quando eles retornam **E \_ pendentes** da chamada para **INapSystemHealthValidator:: Validate**.</span><span class="sxs-lookup"><span data-stu-id="79fee-120">This callback pointer is used by the SHVs when they return **E\_PENDING** from the call to **INapSystemHealthValidator::Validate**.</span></span> <span data-ttu-id="79fee-121">Isso é usado para validação assíncrona.</span><span class="sxs-lookup"><span data-stu-id="79fee-121">This is used for asynchronous validation.</span></span> <span data-ttu-id="79fee-122">Espera-se que os SHVs respondam dentro do horário *hintTimeOutInMsec* ou que a resposta seja descartada.</span><span class="sxs-lookup"><span data-stu-id="79fee-122">The SHVs are expected to respond within the *hintTimeOutInMsec* time or else the response will be dropped.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79fee-123">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="79fee-123">Return value</span></span>

<span data-ttu-id="79fee-124">Se qualquer outro código de erro for retornado, o sistema assumirá que ocorreu uma falha serverComponent e o mapeamento apropriado será feito para ser aprovado/reprovado.</span><span class="sxs-lookup"><span data-stu-id="79fee-124">If any other error code is returned, then the system assumes serverComponent failure has occurred, and the appropriate mapping is done to pass/fail.</span></span>



| <span data-ttu-id="79fee-125">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="79fee-125">Return code</span></span>                                                                                                | <span data-ttu-id="79fee-126">Descrição</span><span class="sxs-lookup"><span data-stu-id="79fee-126">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="79fee-127"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="79fee-127"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="79fee-128">Indica que o validador definiu um SoHResponse no objeto ' request '.</span><span class="sxs-lookup"><span data-stu-id="79fee-128">Indicates that the validator has set an SoHResponse on the 'request' object.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                        |
| <dl> <span data-ttu-id="79fee-129"><dt>**E \_ pendente**</dt></span><span class="sxs-lookup"><span data-stu-id="79fee-129"><dt>**E\_PENDING**</dt></span></span> </dl>                  | <span data-ttu-id="79fee-130">Indica que OnComplete () será chamado em um thread separado.</span><span class="sxs-lookup"><span data-stu-id="79fee-130">Indicates that OnComplete() will be called on a separate thread.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <dl> <span data-ttu-id="79fee-131"><dt>**\_servidor RPC \_ S \_ não disponível**</dt></span><span class="sxs-lookup"><span data-stu-id="79fee-131"><dt>**RPC\_S\_SERVER\_UNAVAILABLE**</dt></span></span> </dl> | <span data-ttu-id="79fee-132">Indica que o processo do validador da integridade do sistema (SHV) foi encerrado sem o NapServer de fato liberar uma referência a ele.</span><span class="sxs-lookup"><span data-stu-id="79fee-132">Indicates that the System Health Validator (SHV) process terminated without the NapServer actually releasing a reference to it.</span></span> <span data-ttu-id="79fee-133">O NapServer tentará recriar uma nova referência para o SHV e executará novamente a chamada Validate uma vez.</span><span class="sxs-lookup"><span data-stu-id="79fee-133">The NapServer will try to re-create a new reference to the SHV and will reexecute the Validate call once.</span></span> <span data-ttu-id="79fee-134">Se a criação do objeto ou a validação de reexecução falhar, o SHV será removido da lista de SHVs carregados.</span><span class="sxs-lookup"><span data-stu-id="79fee-134">If the creation of the object or the re-executed Validate fails, the SHV is removed from the list of loaded SHVs.</span></span> <span data-ttu-id="79fee-135">A única maneira de que esse SHV agora pode ser recarregado é cancelar o registro e registrar novamente o SHV novamente ou quando o NapServer é reiniciado</span><span class="sxs-lookup"><span data-stu-id="79fee-135">The only way this SHV can now be reloaded is to unregister and reregister the SHV again, or when the NapServer restarts</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="79fee-136">Comentários</span><span class="sxs-lookup"><span data-stu-id="79fee-136">Remarks</span></span>

<span data-ttu-id="79fee-137">Para dar suporte à detecção de intrusão, os SHVs serão solicitados a validar o computador cliente, independentemente de o cliente ter enviado um [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) destinado ao SHV.</span><span class="sxs-lookup"><span data-stu-id="79fee-137">In order to support intrusion detection, SHVs will be asked to validate the client machine regardless of whether the client sent an [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) intended for the SHV.</span></span>

<span data-ttu-id="79fee-138">O SHV deve fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="79fee-138">The SHV must do the following:</span></span>

-   <span data-ttu-id="79fee-139">Recupere o [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) da *solicitação* chamando [**solicitação. GetSoHRequest ()**](inapsystemhealthvalidationrequest-getsohrequest-method.md).</span><span class="sxs-lookup"><span data-stu-id="79fee-139">Retrieve the [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) from *request* by calling [**request.GetSoHRequest()**](inapsystemhealthvalidationrequest-getsohrequest-method.md).</span></span>
-   <span data-ttu-id="79fee-140">Se o pacote [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) for nulo:</span><span class="sxs-lookup"><span data-stu-id="79fee-140">If the [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) packet is null:</span></span>
    -   <span data-ttu-id="79fee-141">Se o SHV for um sistema de detecção de intrusão, preencha um pacote [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) com o [**código de erro NAP**](nap-error-constants.md) apropriado para o motivo pelo qual o computador cliente é mal-intencionado.</span><span class="sxs-lookup"><span data-stu-id="79fee-141">If the SHV is an intrusion detection system, populate an [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) packet with the appropriate [**NAP error code**](nap-error-constants.md) as to why the client machine is malicious.</span></span>
    -   <span data-ttu-id="79fee-142">Todos os outros SHVs devem preencher um pacote [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) com um código de erro de [**NAP \_ E \_ faltando \_ soh**](nap-error-constants.md).</span><span class="sxs-lookup"><span data-stu-id="79fee-142">All other SHVs should populate an [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) packet with an error code of [**NAP\_E\_MISSING\_SOH**](nap-error-constants.md).</span></span>
-   <span data-ttu-id="79fee-143">Se *napSystemGenerated* for **true** da chamada a [**Request. GetSoHRequest ()**](inapsystemhealthvalidationrequest-getsohrequest-method.md), o SHV deve esperar um pacote [**soh**](/windows/win32/api/naptypes/ns-naptypes-soh) com os seguintes 3 TLVs: [**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md), **sohAttributeTypeFailureCategory**, **sohAttributeTypeErrorCodes**.</span><span class="sxs-lookup"><span data-stu-id="79fee-143">If *napSystemGenerated* is **TRUE** from the call to [**request.GetSoHRequest()**](inapsystemhealthvalidationrequest-getsohrequest-method.md), the SHV should expect an [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) packet with the following 3 TLVs: [**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md), **sohAttributeTypeFailureCategory**, **sohAttributeTypeErrorCodes**.</span></span> <span data-ttu-id="79fee-144">Esse **SoHRequest** é gerado pelo NapAgent em nome do Sha (agente de integridade do sistema), já que houve um erro na recuperação de um pacote de solicitação do Sha.</span><span class="sxs-lookup"><span data-stu-id="79fee-144">This **SoHRequest** is generated by the NapAgent on behalf of the System Health Agent (SHA) since there was an error in retrieving a request packet from the SHA.</span></span>
-   <span data-ttu-id="79fee-145">Valide o pacote [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) .</span><span class="sxs-lookup"><span data-stu-id="79fee-145">Validate the [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) packet.</span></span>
    -   <span data-ttu-id="79fee-146">Se o [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) estiver malformado, construa um pacote **SoHResponse** com código de erro [**NAP \_ E \_ \_ pacote inválido**](nap-error-constants.md).</span><span class="sxs-lookup"><span data-stu-id="79fee-146">If the [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) is malformed, then construct a **SoHResponse** packet with error code [**NAP\_E\_INVALID\_PACKET**](nap-error-constants.md).</span></span>
    -   <span data-ttu-id="79fee-147">Se o SHV estiver usando apenas informações armazenadas em cache para validar o pacote [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) (ou seja, nenhuma e/s é executada), ele poderá construir o **SoHResponse**, defini-lo no objeto na *solicitação* e retornar **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="79fee-147">If the SHV is only using cached information to validate the [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) packet (i.e. no I/O is performed), then it can construct the **SoHResponse**, set it on the object in *request* and return **S\_OK**.</span></span>
    -   <span data-ttu-id="79fee-148">Se o SHV estiver executando e/s para se comunicar com seus servidores back-end para validar a integridade do cliente, ele deverá enfileirar a e/s e retornar essa função com **E \_ pendente**.</span><span class="sxs-lookup"><span data-stu-id="79fee-148">If the SHV is performing I/O in order to talk to its back-end servers to validate the client's health, then it must queue up the I/O and return this function with **E\_PENDING**.</span></span> <span data-ttu-id="79fee-149">Nesse caso, o SHV deve chamar o [**retorno de chamada. OnComplete ()**](inapservercallback-oncomplete-method.md) em um thread separado dentro do período de tempo limite, *hintTimeOutInMsec*.</span><span class="sxs-lookup"><span data-stu-id="79fee-149">In this case, the SHV must call [**callback.OnComplete()**](inapservercallback-oncomplete-method.md) on a separate thread within the timeout period, *hintTimeOutInMsec*.</span></span> <span data-ttu-id="79fee-150">Caso contrário, a resposta do SHV será descartada.</span><span class="sxs-lookup"><span data-stu-id="79fee-150">Otherwise, the SHV's response will be dropped.</span></span>
-   <span data-ttu-id="79fee-151">Não retornar outro erro além daqueles listados acima.</span><span class="sxs-lookup"><span data-stu-id="79fee-151">Do not return any other error other than those listed above.</span></span> <span data-ttu-id="79fee-152">Se qualquer outro código de erro for retornado pelo SHV (por exemplo,</span><span class="sxs-lookup"><span data-stu-id="79fee-152">If any other error code is returned by the SHV (eg.</span></span> <span data-ttu-id="79fee-153">algum erro do sistema), o pacote será Descartado.</span><span class="sxs-lookup"><span data-stu-id="79fee-153">some system error), the packet will be discarded.</span></span>

<span data-ttu-id="79fee-154">Um SHV deve retornar um TLV **sohAttributeTypeComplianceResultCodes** ou **SohAttributeTypeFailureCategory** em seu [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh).</span><span class="sxs-lookup"><span data-stu-id="79fee-154">An SHV must return either an **sohAttributeTypeComplianceResultCodes** or **sohAttributeTypeFailureCategory** TLV in its [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh).</span></span>

-   <span data-ttu-id="79fee-155">[**TLV sohAttributeTypeComplianceResultCodes**](sohattributetype-enum.md): se o SHV puder validar a integridade do cliente (ou seja, íntegro ou não íntegro), esse TLV será retornado.</span><span class="sxs-lookup"><span data-stu-id="79fee-155">[**sohAttributeTypeComplianceResultCodes TLV**](sohattributetype-enum.md): If the SHV could validate the health of the client (i.e. healthy or unhealthy), this TLV is returned.</span></span>
-   <span data-ttu-id="79fee-156">[**TLV sohAttributeTypeFailureCategory**](sohattributetype-enum.md): se houvesse alguma falha de componente ou de comunicação no cliente ou servidor, ele deve ser indicado por esse TLV.</span><span class="sxs-lookup"><span data-stu-id="79fee-156">[**sohAttributeTypeFailureCategory TLV**](sohattributetype-enum.md): If there was any component or communication failure on the client or server, it must be indicated by this TLV.</span></span> <span data-ttu-id="79fee-157">Esse TLV será mapeado para ser íntegro ou não íntegro dependendo da configuração do SHV.</span><span class="sxs-lookup"><span data-stu-id="79fee-157">This TLV will further be mapped to healthy or unhealthy depending upon the SHV's configuration.</span></span> <span data-ttu-id="79fee-158">Para obter mais detalhes, consulte a interface [**INapServerManagement**](inapservermanagement.md) e a estrutura [**FailureCategoryMapping**](/windows/win32/api/naptypes/ns-naptypes-failurecategorymapping) .</span><span class="sxs-lookup"><span data-stu-id="79fee-158">For more details, see the [**INapServerManagement**](inapservermanagement.md) interface and the [**FailureCategoryMapping**](/windows/win32/api/naptypes/ns-naptypes-failurecategorymapping) structure.</span></span>

<span data-ttu-id="79fee-159">O SHV não deve manter referências a *solicitação* ou *retorno* de chamada quando a chamada asyncronous for concluída.</span><span class="sxs-lookup"><span data-stu-id="79fee-159">The SHV must not hold references to *request* or *callback* once the asyncronous call completes.</span></span>

## <a name="requirements"></a><span data-ttu-id="79fee-160">Requisitos</span><span class="sxs-lookup"><span data-stu-id="79fee-160">Requirements</span></span>



| <span data-ttu-id="79fee-161">Requisito</span><span class="sxs-lookup"><span data-stu-id="79fee-161">Requirement</span></span> | <span data-ttu-id="79fee-162">Valor</span><span class="sxs-lookup"><span data-stu-id="79fee-162">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79fee-163">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="79fee-163">Minimum supported client</span></span><br/> | <span data-ttu-id="79fee-164">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="79fee-164">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="79fee-165">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="79fee-165">Minimum supported server</span></span><br/> | <span data-ttu-id="79fee-166">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="79fee-166">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="79fee-167">parâmetro</span><span class="sxs-lookup"><span data-stu-id="79fee-167">Header</span></span><br/>                   | <dl> <span data-ttu-id="79fee-168"><dt>NapSystemHealthValidator. h</dt></span><span class="sxs-lookup"><span data-stu-id="79fee-168"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="79fee-169">INSERI</span><span class="sxs-lookup"><span data-stu-id="79fee-169">IDL</span></span><br/>                      | <dl> <span data-ttu-id="79fee-170"><dt>NapSystemHealthValidator. idl</dt></span><span class="sxs-lookup"><span data-stu-id="79fee-170"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79fee-171">Confira também</span><span class="sxs-lookup"><span data-stu-id="79fee-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79fee-172">**INapSystemHealthValidator**</span><span class="sxs-lookup"><span data-stu-id="79fee-172">**INapSystemHealthValidator**</span></span>](inapsystemhealthvalidator.md)
</dt> </dl>

 

 





