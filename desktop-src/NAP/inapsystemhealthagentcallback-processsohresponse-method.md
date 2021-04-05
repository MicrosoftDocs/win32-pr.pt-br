---
title: Método INapSystemHealthAgentCallback ProcessSoHResponse (NapSystemHealthAgent. h)
description: É chamado quando o NapAgent recebe um SoHResponse destinado a esse agente de integridade.
ms.assetid: 860b1012-7df8-456f-8f21-eb0e1abd2b3b
keywords:
- Método ProcessSoHResponse NAP
- Método ProcessSoHResponse NAP, interface INapSystemHealthAgentCallback
- INapSystemHealthAgentCallback interface NAP, método ProcessSoHResponse
topic_type:
- apiref
api_name:
- INapSystemHealthAgentCallback.ProcessSoHResponse
api_location:
- NapSystemHealthAgent.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95c62c585c36680dde2c54c95c255a85f69fc5ce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918589"
---
# <a name="inapsystemhealthagentcallbackprocesssohresponse-method"></a><span data-ttu-id="81078-106">INapSystemHealthAgentCallback: método rocessSoHResponse de:P</span><span class="sxs-lookup"><span data-stu-id="81078-106">INapSystemHealthAgentCallback::ProcessSoHResponse method</span></span>

> [!Note]  
> <span data-ttu-id="81078-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="81078-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="81078-108">O método **INapSystemHealthAgentCallback::P rocesssohresponse** é chamado quando o NapAgent recebe um [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) destinado a esse agente de integridade.</span><span class="sxs-lookup"><span data-stu-id="81078-108">The **INapSystemHealthAgentCallback::ProcessSoHResponse** method is called when the NapAgent receives an [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) destined for this health agent.</span></span>

## <a name="syntax"></a><span data-ttu-id="81078-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="81078-109">Syntax</span></span>


```C++
HRESULT ProcessSoHResponse(
  [in] INapSystemHealthAgentRequest *request
);
```



## <a name="parameters"></a><span data-ttu-id="81078-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="81078-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81078-111">*solicitação* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="81078-111">*request* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81078-112">Um ponteiro COM para um objeto [**INapSystemHealthAgentRequest**](inapsystemhealthagentrequest.md) que identifica o objeto de solicitação.</span><span class="sxs-lookup"><span data-stu-id="81078-112">A COM pointer to a [**INapSystemHealthAgentRequest**](inapsystemhealthagentrequest.md) object that identifies the request object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81078-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="81078-113">Return value</span></span>

<span data-ttu-id="81078-114">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="81078-114">This method can return one of these values.</span></span>



| <span data-ttu-id="81078-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="81078-115">Return code</span></span>                                                                                            | <span data-ttu-id="81078-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="81078-116">Description</span></span>                                                                              |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="81078-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="81078-117"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="81078-118">Indica êxito.</span><span class="sxs-lookup"><span data-stu-id="81078-118">Indicates success.</span></span><br/>                                                            |
| <dl> <span data-ttu-id="81078-119"><dt>**\_pacote NAP E \_ inválido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="81078-119"><dt>**NAP\_E\_INVALID\_PACKET**</dt></span></span> </dl> | <span data-ttu-id="81078-120">Retornado por essa implementação se a resposta não estiver no formato correto.</span><span class="sxs-lookup"><span data-stu-id="81078-120">Returned by this implementation if the response is not in the correct format.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="81078-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="81078-121">Remarks</span></span>

<span data-ttu-id="81078-122">Esse método de retorno de chamada é declarado pelo sistema NAP e deve ser implementado pelo gravador SHA.</span><span class="sxs-lookup"><span data-stu-id="81078-122">This callback method is declared by the NAP system and is to be implemented by the SHA writer.</span></span>

<span data-ttu-id="81078-123">Quando o NapAgent recebe um [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) destinado a esse agente de integridade, ele invoca esse método.</span><span class="sxs-lookup"><span data-stu-id="81078-123">When the NapAgent receives an [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) destined for this health agent, it invokes this method.</span></span> <span data-ttu-id="81078-124">O agente de integridade deve consultar o SoHResponse do objeto de solicitação.</span><span class="sxs-lookup"><span data-stu-id="81078-124">The health agent must query the SoHResponse from the request object.</span></span> <span data-ttu-id="81078-125">Ele não deve manter referências ao objeto de solicitação depois que essa chamada for concluída.</span><span class="sxs-lookup"><span data-stu-id="81078-125">It must not hold references to the request object once this call has completed.</span></span>

<span data-ttu-id="81078-126">O método **INapSystemHealthAgentCallback::P rocesssohresponse** não deve bloquear.</span><span class="sxs-lookup"><span data-stu-id="81078-126">The **INapSystemHealthAgentCallback::ProcessSoHResponse** method must not block.</span></span> <span data-ttu-id="81078-127">Se qualquer processamento de correção for necessário, qualquer implementação de **ProcessSoHResponse** deverá iniciar um novo thread para executar o processamento de correção.</span><span class="sxs-lookup"><span data-stu-id="81078-127">If any fix-up processing is required, any implementation of **ProcessSoHResponse** must start a new thread to perform fix-up processing.</span></span> <span data-ttu-id="81078-128">O NapAgent deve chamar [**INapSystemHealthAgentCallBack:: GetFixupInfo**](inapsystemhealthagentcallback-getfixupinfo-method.md) para determinar o status de correção do Sha.</span><span class="sxs-lookup"><span data-stu-id="81078-128">The NapAgent must call [**INapSystemHealthAgentCallBack::GetFixupInfo**](inapsystemhealthagentcallback-getfixupinfo-method.md) to determine the fix-up status of the SHA.</span></span>

<span data-ttu-id="81078-129">Esse método deve retornar **um \_ \_ \_ pacote NAP E inválido** se a resposta não estiver no formato correto.</span><span class="sxs-lookup"><span data-stu-id="81078-129">This method must return **NAP\_E\_INVALID\_PACKET** if the response is not in the correct format.</span></span>

## <a name="requirements"></a><span data-ttu-id="81078-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81078-130">Requirements</span></span>



| <span data-ttu-id="81078-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="81078-131">Requirement</span></span> | <span data-ttu-id="81078-132">Valor</span><span class="sxs-lookup"><span data-stu-id="81078-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81078-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="81078-133">Minimum supported client</span></span><br/> | <span data-ttu-id="81078-134">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="81078-134">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="81078-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="81078-135">Minimum supported server</span></span><br/> | <span data-ttu-id="81078-136">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="81078-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="81078-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="81078-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="81078-138"><dt>NapSystemHealthAgent. h</dt></span><span class="sxs-lookup"><span data-stu-id="81078-138"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="81078-139">INSERI</span><span class="sxs-lookup"><span data-stu-id="81078-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="81078-140"><dt>NapSystemHealthAgent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="81078-140"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81078-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="81078-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81078-142">**INapSystemHealthAgentCallback**</span><span class="sxs-lookup"><span data-stu-id="81078-142">**INapSystemHealthAgentCallback**</span></span>](inapsystemhealthagentcallback.md)
</dt> </dl>

 

 





