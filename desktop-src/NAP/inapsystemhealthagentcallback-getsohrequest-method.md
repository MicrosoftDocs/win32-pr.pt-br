---
title: Método INapSystemHealthAgentCallback GetSoHRequest (NapSystemHealthAgent. h)
description: É chamado pelo NapAgent para consultar a solicitação SoH do agente de integridade do sistema.
ms.assetid: 4161a3e7-2f7a-40d1-b973-47f991bba5d0
keywords:
- Método GetSoHRequest NAP
- Método GetSoHRequest NAP, interface INapSystemHealthAgentCallback
- INapSystemHealthAgentCallback interface NAP, método GetSoHRequest
topic_type:
- apiref
api_name:
- INapSystemHealthAgentCallback.GetSoHRequest
api_location:
- NapSystemHealthAgent.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0fd95ce79587b5e7e259323286cfce138dd2df2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369705"
---
# <a name="inapsystemhealthagentcallbackgetsohrequest-method"></a><span data-ttu-id="26e0b-106">Método INapSystemHealthAgentCallback:: GetSoHRequest</span><span class="sxs-lookup"><span data-stu-id="26e0b-106">INapSystemHealthAgentCallback::GetSoHRequest method</span></span>

> [!Note]  
> <span data-ttu-id="26e0b-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="26e0b-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="26e0b-108">O método **INapSystemHealthAgentCallback:: GetSoHRequest** é chamado pelo NapAgent para consultar a solicitação soh do agente de integridade do sistema.</span><span class="sxs-lookup"><span data-stu-id="26e0b-108">The **INapSystemHealthAgentCallback::GetSoHRequest** method is called by the NapAgent to query the system health agent's SoH request.</span></span>

## <a name="syntax"></a><span data-ttu-id="26e0b-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="26e0b-109">Syntax</span></span>


```C++
HRESULT GetSoHRequest(
  [in] INapSystemHealthAgentRequest *request
);
```



## <a name="parameters"></a><span data-ttu-id="26e0b-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="26e0b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26e0b-111">*solicitação* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="26e0b-111">*request* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26e0b-112">Um ponteiro COM para um objeto [**INapSystemHealthAgentRequest**](inapsystemhealthagentrequest.md) que identifica o objeto de solicitação.</span><span class="sxs-lookup"><span data-stu-id="26e0b-112">A COM pointer to an [**INapSystemHealthAgentRequest**](inapsystemhealthagentrequest.md) object that identifies the request object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26e0b-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="26e0b-113">Return value</span></span>



| <span data-ttu-id="26e0b-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="26e0b-114">Return code</span></span>                                                                                                                      | <span data-ttu-id="26e0b-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="26e0b-115">Description</span></span>                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="26e0b-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="26e0b-116"><dt>**S\_OK**</dt></span></span> </dl>                                             | <span data-ttu-id="26e0b-117">Indica êxito.</span><span class="sxs-lookup"><span data-stu-id="26e0b-117">Indicates success.</span></span><br/>                                                                                                                      |
| <dl> <span data-ttu-id="26e0b-118"><dt>**HRESULT \_ do \_ Win32 ( \_ servidor RPC \_ S \_ indisponível)**</dt></span><span class="sxs-lookup"><span data-stu-id="26e0b-118"><dt>**HRESULT\_FROM\_WIN32(RPC\_S\_SERVER\_UNAVAILABLE)**</dt></span></span> </dl> | <span data-ttu-id="26e0b-119">Se esse código for retornado pela sua implementação, o NapAgent removerá o SHA da lista Bound-SHA e liberará sua entrada de cache.</span><span class="sxs-lookup"><span data-stu-id="26e0b-119">If this code is returned by your implementation, the NapAgent then removes the SHA from the bound-SHA list and flushes its cache entry.</span></span><br/> |



 

<span data-ttu-id="26e0b-120">Quando qualquer valor de retorno (exceto **HRESULT \_ do \_ Win32 ( \_ servidor RPC S \_ \_ indisponível)**) é RETORNADO pela sua implementação, o sistema NAP constrói e retorna um [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) para o SHV correspondente com os seguintes tipos de atributo e valores:</span><span class="sxs-lookup"><span data-stu-id="26e0b-120">When any return value (except **HRESULT\_FROM\_WIN32(RPC\_S\_SERVER\_UNAVAILABLE)**) is returned by your implementation, the NAP system constructs and returns a [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) to the corresponding SHV with the following attribute types and values:</span></span>

-   <span data-ttu-id="26e0b-121">[**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md)= <id></span><span class="sxs-lookup"><span data-stu-id="26e0b-121">[**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md)= <id></span></span>
-   <span data-ttu-id="26e0b-122">[**sohAttributeTypeFailureCategory**](sohattributetype-enum.md) =  [ **failureCategoryClientComponent**](/windows/win32/api/naptypes/ne-naptypes-failurecategory)</span><span class="sxs-lookup"><span data-stu-id="26e0b-122">[**sohAttributeTypeFailureCategory**](sohattributetype-enum.md)= [**failureCategoryClientComponent**](/windows/win32/api/naptypes/ne-naptypes-failurecategory)</span></span>
-   <span data-ttu-id="26e0b-123">[**sohAttributeTypeErrorCodes**](sohattributetype-enum.md) = <de código de erro></span><span class="sxs-lookup"><span data-stu-id="26e0b-123">[**sohAttributeTypeErrorCodes**](sohattributetype-enum.md) = <error-code></span></span>

## <a name="remarks"></a><span data-ttu-id="26e0b-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="26e0b-124">Remarks</span></span>

<span data-ttu-id="26e0b-125">Esse método de retorno de chamada é declarado pelo sistema NAP e deve ser implementado pelo gravador SHA.</span><span class="sxs-lookup"><span data-stu-id="26e0b-125">This callback method is declared by the NAP system and is to be implemented by the SHA writer.</span></span>

<span data-ttu-id="26e0b-126">Esse método deve processar a solicitação e retornar imediatamente.</span><span class="sxs-lookup"><span data-stu-id="26e0b-126">This method must process the request and return immediately.</span></span> <span data-ttu-id="26e0b-127">Atrasar o retorno desse método afeta negativamente o desempenho e a capacidade de resposta do sistema e pode fazer com que outras partes do sistema operacional expirem o tempo limite.</span><span class="sxs-lookup"><span data-stu-id="26e0b-127">Delaying the return of this method negatively impacts system performance and responsiveness, and may cause other parts of the operating system to time out.</span></span>

<span data-ttu-id="26e0b-128">O monitoramento do estado de integridade não deve ser feito como parte dessa chamada, especialmente se for de computação intensiva e demorar muito.</span><span class="sxs-lookup"><span data-stu-id="26e0b-128">Health state monitoring should not be done as part of this call, especially if it is computation intensive and takes a long time.</span></span> <span data-ttu-id="26e0b-129">O monitoramento do estado de integridade e a computação SoH devem ser executados em um thread ou serviço separado.</span><span class="sxs-lookup"><span data-stu-id="26e0b-129">Health state monitoring and SoH computation should be performed in a separate thread or service.</span></span> <span data-ttu-id="26e0b-130">A única função desse método deve ser definir a SoH e o retorno do SHA.</span><span class="sxs-lookup"><span data-stu-id="26e0b-130">The sole function of this method should be to set the SHA's SoH and return.</span></span>

<span data-ttu-id="26e0b-131">Se levará muito tempo para que o SHA gere uma SoH, a SoH armazenada em cache deverá ser retornada ao NapAgent.</span><span class="sxs-lookup"><span data-stu-id="26e0b-131">If it will take a long time for the SHA to generate a SoH, then the cached SoH should be returned to the NapAgent.</span></span> <span data-ttu-id="26e0b-132">Se não houver nenhuma SoH armazenada em cache para retornar, o SHA deverá retornar imediatamente uma SoH com os seguintes tipos de atributo e valores:</span><span class="sxs-lookup"><span data-stu-id="26e0b-132">If there is no cached SoH to return, then the SHA should immediately return a SoH with the following attribute types and values:</span></span>

-   <span data-ttu-id="26e0b-133">[**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md)= <id></span><span class="sxs-lookup"><span data-stu-id="26e0b-133">[**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md)= <id></span></span>
-   <span data-ttu-id="26e0b-134">[**sohAttributeTypeFailureCategory**](sohattributetype-enum.md) =  [ **failureCategoryClientCommunication**](/windows/win32/api/naptypes/ne-naptypes-failurecategory)</span><span class="sxs-lookup"><span data-stu-id="26e0b-134">[**sohAttributeTypeFailureCategory**](sohattributetype-enum.md)= [**failureCategoryClientCommunication**](/windows/win32/api/naptypes/ne-naptypes-failurecategory)</span></span>
-   <span data-ttu-id="26e0b-135">[**sohAttributeTypeErrorCodes**](sohattributetype-enum.md)  =  [ **NAP \_ E \_ nenhum \_ \_ soh armazenado em cache**](nap-error-constants.md)</span><span class="sxs-lookup"><span data-stu-id="26e0b-135">[**sohAttributeTypeErrorCodes**](sohattributetype-enum.md) = [**NAP\_E\_NO\_CACHED\_SOH**](nap-error-constants.md)</span></span>

<span data-ttu-id="26e0b-136">Quando a SoH é gerada, o SHA deve chamar [**INapSystemHealthAgentBinding:: NotifySoHChange**](inapsystemhealthagentbinding-notifysohchange-method.md) para notificar o NapAgent da alteração de integridade do sistema.</span><span class="sxs-lookup"><span data-stu-id="26e0b-136">When the SoH has been generated, the SHA must call [**INapSystemHealthAgentBinding::NotifySoHChange**](inapsystemhealthagentbinding-notifysohchange-method.md) to notify the NapAgent of the system health change.</span></span>

<span data-ttu-id="26e0b-137">O NapAgent chama esse método para consultar o SoHRequest do agente de integridade do sistema.</span><span class="sxs-lookup"><span data-stu-id="26e0b-137">The NapAgent calls this method to query the system health agent's SoHRequest.</span></span> <span data-ttu-id="26e0b-138">O SHA pode consultar o objeto [**INapSystemHealthAgentRequest**](inapsystemhealthagentrequest.md) passado para parâmetros que ele precisa para calcular o SoHRequest.</span><span class="sxs-lookup"><span data-stu-id="26e0b-138">The SHA can query the passed [**INapSystemHealthAgentRequest**](inapsystemhealthagentrequest.md) object for parameters that it needs to compute the SoHRequest.</span></span> <span data-ttu-id="26e0b-139">O SHA deve definir o SoHRequest calculado no objeto de solicitação.</span><span class="sxs-lookup"><span data-stu-id="26e0b-139">The SHA must set the computed SoHRequest on the request object.</span></span> <span data-ttu-id="26e0b-140">O SHA não deve manter referências ao objeto de solicitação depois que essa chamada for concluída.</span><span class="sxs-lookup"><span data-stu-id="26e0b-140">The SHA must not hold references to the request object once this call has completed.</span></span>

<span data-ttu-id="26e0b-141">Quando esse método é chamado, se houver uma SoH no cache do NapAgent, ele será definido no objeto de solicitação.</span><span class="sxs-lookup"><span data-stu-id="26e0b-141">When this method is called, if there is a SoH in the NapAgent's cache, then it is set on the request object.</span></span> <span data-ttu-id="26e0b-142">O SHA pode consultá-lo usando **GetSoHRequest**.</span><span class="sxs-lookup"><span data-stu-id="26e0b-142">The SHA can query for it using **GetSoHRequest**.</span></span> <span data-ttu-id="26e0b-143">Se o SHA não definir uma nova SoH, o armazenado em cache será usado.</span><span class="sxs-lookup"><span data-stu-id="26e0b-143">If the SHA does not set a new SoH, then the cached one is used.</span></span>

<span data-ttu-id="26e0b-144">Para SHAs não associados que são registrados com o sistema, o sistema NAP constrói e envia um SoHRequest para o SHV correspondente com os seguintes tipos de atributo e valores:</span><span class="sxs-lookup"><span data-stu-id="26e0b-144">For unbound SHAs which are registered with the system, the NAP system constructs and sends a SoHRequest to the corresponding SHV with the following attribute types and values:</span></span>

-   <span data-ttu-id="26e0b-145">[**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md)= <id></span><span class="sxs-lookup"><span data-stu-id="26e0b-145">[**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md)= <id></span></span>
-   <span data-ttu-id="26e0b-146">[**sohAttributeTypeFailureCategory**](sohattributetype-enum.md) =  [ **failureCategoryClientComponent**](/windows/win32/api/naptypes/ne-naptypes-failurecategory)</span><span class="sxs-lookup"><span data-stu-id="26e0b-146">[**sohAttributeTypeFailureCategory**](sohattributetype-enum.md)= [**failureCategoryClientComponent**](/windows/win32/api/naptypes/ne-naptypes-failurecategory)</span></span>
-   <span data-ttu-id="26e0b-147">[**sohAttributeTypeErrorCodes**](sohattributetype-enum.md)  =  [ **NAP \_ E \_ não \_ inicializado**](nap-error-constants.md)</span><span class="sxs-lookup"><span data-stu-id="26e0b-147">[**sohAttributeTypeErrorCodes**](sohattributetype-enum.md) = [**NAP\_E\_NOT\_INITIALIZED**](nap-error-constants.md)</span></span>

## <a name="requirements"></a><span data-ttu-id="26e0b-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="26e0b-148">Requirements</span></span>



| <span data-ttu-id="26e0b-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="26e0b-149">Requirement</span></span> | <span data-ttu-id="26e0b-150">Valor</span><span class="sxs-lookup"><span data-stu-id="26e0b-150">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26e0b-151">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="26e0b-151">Minimum supported client</span></span><br/> | <span data-ttu-id="26e0b-152">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="26e0b-152">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="26e0b-153">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="26e0b-153">Minimum supported server</span></span><br/> | <span data-ttu-id="26e0b-154">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="26e0b-154">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="26e0b-155">parâmetro</span><span class="sxs-lookup"><span data-stu-id="26e0b-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="26e0b-156"><dt>NapSystemHealthAgent. h</dt></span><span class="sxs-lookup"><span data-stu-id="26e0b-156"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="26e0b-157">INSERI</span><span class="sxs-lookup"><span data-stu-id="26e0b-157">IDL</span></span><br/>                      | <dl> <span data-ttu-id="26e0b-158"><dt>NapSystemHealthAgent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="26e0b-158"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26e0b-159">Confira também</span><span class="sxs-lookup"><span data-stu-id="26e0b-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26e0b-160">**INapSystemHealthAgentCallback**</span><span class="sxs-lookup"><span data-stu-id="26e0b-160">**INapSystemHealthAgentCallback**</span></span>](inapsystemhealthagentcallback.md)
</dt> </dl>

 

 





