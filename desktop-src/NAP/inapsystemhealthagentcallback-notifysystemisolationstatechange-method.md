---
title: Método INapSystemHealthAgentCallback NotifySystemIsolationStateChange (NapSystemHealthAgent. h)
description: É chamado pelo NapAgent para indicar que o estado de isolamento do sistema ou o tempo de término da experiência foi alterado.
ms.assetid: 0837eea4-6d92-44dc-b8b8-eca6be5f63e6
keywords:
- Método NotifySystemIsolationStateChange NAP
- Método NotifySystemIsolationStateChange NAP, interface INapSystemHealthAgentCallback
- INapSystemHealthAgentCallback interface NAP, método NotifySystemIsolationStateChange
topic_type:
- apiref
api_name:
- INapSystemHealthAgentCallback.NotifySystemIsolationStateChange
api_location:
- NapSystemHealthAgent.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c519d1569fe2e43cc6012ffa30c5bfb4402cc56
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644763"
---
# <a name="inapsystemhealthagentcallbacknotifysystemisolationstatechange-method"></a><span data-ttu-id="24ec0-106">Método INapSystemHealthAgentCallback:: NotifySystemIsolationStateChange</span><span class="sxs-lookup"><span data-stu-id="24ec0-106">INapSystemHealthAgentCallback::NotifySystemIsolationStateChange method</span></span>

> [!Note]  
> <span data-ttu-id="24ec0-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="24ec0-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="24ec0-108">O método **INapSystemHealthAgentCallback:: NotifySystemIsolationStateChange** é chamado pelo NapAgent para indicar que o estado de isolamento do sistema ou o tempo de término da experiência foi alterado.</span><span class="sxs-lookup"><span data-stu-id="24ec0-108">The **INapSystemHealthAgentCallback::NotifySystemIsolationStateChange** method is called by the NapAgent to indicate that the system isolation state or the probation end-time has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="24ec0-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="24ec0-109">Syntax</span></span>


```C++
HRESULT NotifySystemIsolationStateChange();
```



## <a name="parameters"></a><span data-ttu-id="24ec0-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="24ec0-110">Parameters</span></span>

<span data-ttu-id="24ec0-111">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="24ec0-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="24ec0-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="24ec0-112">Return value</span></span>

<span data-ttu-id="24ec0-113">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="24ec0-113">This method can return one of these values.</span></span>



| <span data-ttu-id="24ec0-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="24ec0-114">Return code</span></span>                                                                          | <span data-ttu-id="24ec0-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="24ec0-115">Description</span></span>                   |
|--------------------------------------------------------------------------------------|-------------------------------|
| <dl> <span data-ttu-id="24ec0-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="24ec0-116"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="24ec0-117">Indica êxito.</span><span class="sxs-lookup"><span data-stu-id="24ec0-117">Indicates success.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="24ec0-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="24ec0-118">Remarks</span></span>

<span data-ttu-id="24ec0-119">Esse método de retorno de chamada é declarado pelo sistema NAP e deve ser implementado pelo gravador SHA.</span><span class="sxs-lookup"><span data-stu-id="24ec0-119">This callback method is declared by the NAP system and is to be implemented by the SHA writer.</span></span>

<span data-ttu-id="24ec0-120">O agente de integridade pode consultar o estado NAP do sistema usando [**INapSystemHealthAgentBinding:: GetSystemIsolationInfo**](inapsystemhealthagentbinding-getsystemisolationinfo-method.md).</span><span class="sxs-lookup"><span data-stu-id="24ec0-120">The health agent can query the system NAP state using the [**INapSystemHealthAgentBinding::GetSystemIsolationInfo**](inapsystemhealthagentbinding-getsystemisolationinfo-method.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="24ec0-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="24ec0-121">Requirements</span></span>



| <span data-ttu-id="24ec0-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="24ec0-122">Requirement</span></span> | <span data-ttu-id="24ec0-123">Valor</span><span class="sxs-lookup"><span data-stu-id="24ec0-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24ec0-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="24ec0-124">Minimum supported client</span></span><br/> | <span data-ttu-id="24ec0-125">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="24ec0-125">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="24ec0-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="24ec0-126">Minimum supported server</span></span><br/> | <span data-ttu-id="24ec0-127">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="24ec0-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="24ec0-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="24ec0-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="24ec0-129"><dt>NapSystemHealthAgent. h</dt></span><span class="sxs-lookup"><span data-stu-id="24ec0-129"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="24ec0-130">INSERI</span><span class="sxs-lookup"><span data-stu-id="24ec0-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="24ec0-131"><dt>NapSystemHealthAgent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="24ec0-131"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24ec0-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="24ec0-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24ec0-133">**INapSystemHealthAgentCallback**</span><span class="sxs-lookup"><span data-stu-id="24ec0-133">**INapSystemHealthAgentCallback**</span></span>](inapsystemhealthagentcallback.md)
</dt> </dl>

 

 





