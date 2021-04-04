---
title: Método INapSystemHealthAgentRequest GetSoHResponse (NapSystemHealthAgent. h)
description: É usado pelo agente de integridade para recuperar seu blob SoHResponse quando o NapAgent chama INapSystemHealthAgentCallback ProcessSoHResponse.
ms.assetid: 60319256-d5c2-46cc-a59b-f81732e21a7f
keywords:
- Método GetSoHResponse NAP
- Método GetSoHResponse NAP, interface INapSystemHealthAgentRequest
- INapSystemHealthAgentRequest interface NAP, método GetSoHResponse
topic_type:
- apiref
api_name:
- INapSystemHealthAgentRequest.GetSoHResponse
api_location:
- qagentrt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d593ff897e69b86b554365561e43308adead5250
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085370"
---
# <a name="inapsystemhealthagentrequestgetsohresponse-method"></a><span data-ttu-id="0fca3-106">Método INapSystemHealthAgentRequest:: GetSoHResponse</span><span class="sxs-lookup"><span data-stu-id="0fca3-106">INapSystemHealthAgentRequest::GetSoHResponse method</span></span>

> [!Note]  
> <span data-ttu-id="0fca3-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="0fca3-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="0fca3-108">O método **INapSystemHealthAgentRequest:: GetSoHResponse** é usado pelo agente de integridade para recuperar seu blob SoHResponse quando o NapAgent chama [**INapSystemHealthAgentCallback::P rocesssohresponse**](inapsystemhealthagentcallback-processsohresponse-method.md).</span><span class="sxs-lookup"><span data-stu-id="0fca3-108">The **INapSystemHealthAgentRequest::GetSoHResponse** method is used by the health agent to retrieve their SoHResponse blob when the NapAgent calls [**INapSystemHealthAgentCallback::ProcessSoHResponse**](inapsystemhealthagentcallback-processsohresponse-method.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="0fca3-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0fca3-109">Syntax</span></span>


```C++
HRESULT GetSoHResponse(
  [out] SoHResponse **sohResponse,
  [out] UINT8       *flags
);
```



## <a name="parameters"></a><span data-ttu-id="0fca3-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0fca3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0fca3-111">*sohResponse* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="0fca3-111">*sohResponse* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0fca3-112">Um ponteiro para um ponteiro para um pacote [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) .</span><span class="sxs-lookup"><span data-stu-id="0fca3-112">A pointer to a pointer to a [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) packet.</span></span>

</dd> <dt>

<span data-ttu-id="0fca3-113">*sinalizadores* \[ de fora\]</span><span class="sxs-lookup"><span data-stu-id="0fca3-113">*flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0fca3-114">Um ponteiro para um sinalizador que habilita a correção pelo SHA se o bit [**shaFixup**](nap-type-constants.md) for definido, caso contrário, a correção será desabilitada.</span><span class="sxs-lookup"><span data-stu-id="0fca3-114">A pointer to a flag that enables fix-up by the SHA if the [**shaFixup**](nap-type-constants.md) bit is set, otherwise fix-up is disabled.</span></span>



| <span data-ttu-id="0fca3-115">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="0fca3-115">Possible Values</span></span>                                                                                                                                                          | <span data-ttu-id="0fca3-116">Significado</span><span class="sxs-lookup"><span data-stu-id="0fca3-116">Meaning</span></span>                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="shaFixup"></span><span id="shafixup"></span><span id="SHAFIXUP"></span><dl> <span data-ttu-id="0fca3-117"><dt>**shaFixup**</dt></span><span class="sxs-lookup"><span data-stu-id="0fca3-117"><dt>**shaFixup**</dt></span></span> </dl> | <span data-ttu-id="0fca3-118">Espera-se que o SHA execute a correção com base na resposta.</span><span class="sxs-lookup"><span data-stu-id="0fca3-118">The SHA is expected to perform the fixup based on the response.</span></span> <span data-ttu-id="0fca3-119">Se esse sinalizador não for definido, o SHA não deverá executar uma correção, mesmo que o [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) indique que ele não está íntegro.</span><span class="sxs-lookup"><span data-stu-id="0fca3-119">If this flag is not set, the SHA should not perform a fix-up even though the [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) indicates that it is unhealthy.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0fca3-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0fca3-120">Return value</span></span>

<span data-ttu-id="0fca3-121">Outros códigos de erro específicos de COM também podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="0fca3-121">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="0fca3-122">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="0fca3-122">Return code</span></span>                                                                                     | <span data-ttu-id="0fca3-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="0fca3-123">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="0fca3-124"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0fca3-124"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="0fca3-125">Operação bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="0fca3-125">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="0fca3-126"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="0fca3-126"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="0fca3-127">Erro de permissões, acesso negado.</span><span class="sxs-lookup"><span data-stu-id="0fca3-127">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="0fca3-128"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="0fca3-128"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="0fca3-129">O limite de recursos do sistema não pôde executar a operação.</span><span class="sxs-lookup"><span data-stu-id="0fca3-129">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="0fca3-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0fca3-130">Requirements</span></span>



| <span data-ttu-id="0fca3-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="0fca3-131">Requirement</span></span> | <span data-ttu-id="0fca3-132">Valor</span><span class="sxs-lookup"><span data-stu-id="0fca3-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0fca3-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0fca3-133">Minimum supported client</span></span><br/> | <span data-ttu-id="0fca3-134">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0fca3-134">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="0fca3-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0fca3-135">Minimum supported server</span></span><br/> | <span data-ttu-id="0fca3-136">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0fca3-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="0fca3-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0fca3-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="0fca3-138"><dt>NapSystemHealthAgent. h</dt></span><span class="sxs-lookup"><span data-stu-id="0fca3-138"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="0fca3-139">INSERI</span><span class="sxs-lookup"><span data-stu-id="0fca3-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0fca3-140"><dt>NapSystemHealthAgent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0fca3-140"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="0fca3-141">DLL</span><span class="sxs-lookup"><span data-stu-id="0fca3-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0fca3-142"><dt>Qagentrt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0fca3-142"><dt>Qagentrt.dll</dt></span></span> </dl>             |



## <a name="see-also"></a><span data-ttu-id="0fca3-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="0fca3-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fca3-144">**INapSystemHealthAgentRequest**</span><span class="sxs-lookup"><span data-stu-id="0fca3-144">**INapSystemHealthAgentRequest**</span></span>](inapsystemhealthagentrequest.md)
</dt> </dl>

 

 





