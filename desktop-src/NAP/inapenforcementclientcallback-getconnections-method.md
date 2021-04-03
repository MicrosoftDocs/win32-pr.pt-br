---
title: Método GetConnections INapEnforcementClientCallback (NapEnforcementClient. h)
description: É chamado pelo NapAgent e implementado pelo cliente de imposição para retornar um conjunto de conexões.
ms.assetid: 8f697217-5799-48e4-9f0b-715f516e48d9
keywords:
- Método GetConnections NAP
- Método GetConnections NAP, interface INapEnforcementClientCallback
- Interface INapEnforcementClientCallback NAP, método GetConnections
topic_type:
- apiref
api_name:
- INapEnforcementClientCallback.GetConnections
api_location:
- NapEnforcementClient.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9acdc68dbc69cabe710414f3fa2501585f3e384e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824799"
---
# <a name="inapenforcementclientcallbackgetconnections-method"></a><span data-ttu-id="066d3-106">Método INapEnforcementClientCallback:: GetConnections</span><span class="sxs-lookup"><span data-stu-id="066d3-106">INapEnforcementClientCallback::GetConnections method</span></span>

> [!Note]  
> <span data-ttu-id="066d3-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="066d3-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="066d3-108">O método de retorno de chamada **INapEnforcementClientCallback:: GetConnections** é chamado pelo NapAgent e implementado pelo cliente de imposição para retornar um conjunto de conexões.</span><span class="sxs-lookup"><span data-stu-id="066d3-108">The **INapEnforcementClientCallback::GetConnections** callback method is called by the NapAgent and implemented by the enforcement client to return a set of connections.</span></span>

## <a name="syntax"></a><span data-ttu-id="066d3-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="066d3-109">Syntax</span></span>


```C++
HRESULT GetConnections(
  [out] Connections **connections
);
```



## <a name="parameters"></a><span data-ttu-id="066d3-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="066d3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="066d3-111">*conexões* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="066d3-111">*connections* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="066d3-112">Um ponteiro para o conjunto atual de [**conexões**](connections-struct.md)mantidas.</span><span class="sxs-lookup"><span data-stu-id="066d3-112">A pointer to the current set of maintained [**Connections**](connections-struct.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="066d3-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="066d3-113">Return value</span></span>

<span data-ttu-id="066d3-114">Esse método de retorno de chamada deve retornar um dos seguintes códigos de erro.</span><span class="sxs-lookup"><span data-stu-id="066d3-114">This callback method must return one the following error codes.</span></span>



| <span data-ttu-id="066d3-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="066d3-115">Return code</span></span>                                                                                                | <span data-ttu-id="066d3-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="066d3-116">Description</span></span>                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="066d3-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="066d3-117"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="066d3-118">Retorne esse valor se a operação tiver êxito.</span><span class="sxs-lookup"><span data-stu-id="066d3-118">Return this value if the operation succeeded.</span></span><br/>                                                                                                                                                              |
| <dl> <span data-ttu-id="066d3-119"><dt>**\_servidor RPC \_ S \_ não disponível**</dt></span><span class="sxs-lookup"><span data-stu-id="066d3-119"><dt>**RPC\_S\_SERVER\_UNAVAILABLE**</dt></span></span> </dl> | <span data-ttu-id="066d3-120">Retornar esse valor faz com que o imforcer seja removido da lista Bound-SHA e a entrada de cache NapAgent correspondente seja liberada.</span><span class="sxs-lookup"><span data-stu-id="066d3-120">Returning this value causes the enforcer to be removed from the bound-SHA list, and the corresponding NapAgent cache entry to be flushed.</span></span> <span data-ttu-id="066d3-121">O SHA com falha pode inicializar novamente com o NapAgent.</span><span class="sxs-lookup"><span data-stu-id="066d3-121">The failing SHA can then re-initialize itself with the NapAgent.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="066d3-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="066d3-122">Requirements</span></span>



| <span data-ttu-id="066d3-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="066d3-123">Requirement</span></span> | <span data-ttu-id="066d3-124">Valor</span><span class="sxs-lookup"><span data-stu-id="066d3-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="066d3-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="066d3-125">Minimum supported client</span></span><br/> | <span data-ttu-id="066d3-126">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="066d3-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="066d3-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="066d3-127">Minimum supported server</span></span><br/> | <span data-ttu-id="066d3-128">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="066d3-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="066d3-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="066d3-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="066d3-130"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="066d3-130"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="066d3-131">INSERI</span><span class="sxs-lookup"><span data-stu-id="066d3-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="066d3-132"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="066d3-132"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="066d3-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="066d3-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="066d3-134">**INapEnforcementClientCallback**</span><span class="sxs-lookup"><span data-stu-id="066d3-134">**INapEnforcementClientCallback**</span></span>](inapenforcementclientcallback.md)
</dt> </dl>

 

 





