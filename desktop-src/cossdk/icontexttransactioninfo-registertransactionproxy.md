---
description: Associa uma implementação de ITransactionProxy com o contexto atual.
ms.assetid: 64009632-b536-41fb-95ac-b23e2cbf18da
title: 'Método IContextTransactionInfo:: RegisterTransactionProxy'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextTransactionInfo.RegisterTransactionProxy
api_type:
- COM
api_location: ''
ms.openlocfilehash: 7b559453b0d4ed75f92f7a421be4c3a47e07fdf7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296127"
---
# <a name="icontexttransactioninforegistertransactionproxy-method"></a><span data-ttu-id="a245b-103">Método IContextTransactionInfo:: RegisterTransactionProxy</span><span class="sxs-lookup"><span data-stu-id="a245b-103">IContextTransactionInfo::RegisterTransactionProxy method</span></span>

<span data-ttu-id="a245b-104">Associa uma implementação de [**ITransactionProxy**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactionproxy) com o contexto atual.</span><span class="sxs-lookup"><span data-stu-id="a245b-104">Associates an [**ITransactionProxy**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactionproxy) implementation with the current context.</span></span>

## <a name="syntax"></a><span data-ttu-id="a245b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a245b-105">Syntax</span></span>


```C++
HRESULT RegisterTransactionProxy(
  [in]  ITransactionProxy *pProxy,
  [out] GUID              *pGuid
);
```



## <a name="parameters"></a><span data-ttu-id="a245b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a245b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a245b-107">*pProxy* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a245b-107">*pProxy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a245b-108">Uma implementação de [**ITransactionProxy**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactionproxy) para associar ao contexto atual.</span><span class="sxs-lookup"><span data-stu-id="a245b-108">An [**ITransactionProxy**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactionproxy) implementation to associate with the current context.</span></span>

</dd> <dt>

<span data-ttu-id="a245b-109">*pGuid* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="a245b-109">*pGuid* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a245b-110">Um GUID que identifica o proxy de transação.</span><span class="sxs-lookup"><span data-stu-id="a245b-110">A GUID that identifies the transaction proxy.</span></span> <span data-ttu-id="a245b-111">O COM+ usa esse GUID ao chamar [**ITransactionProxy:: Commit**](/windows/desktop/api/ComSvcs/nf-comsvcs-itransactionproxy-commit) no proxy de transação.</span><span class="sxs-lookup"><span data-stu-id="a245b-111">COM+ uses this GUID when calling [**ITransactionProxy::Commit**](/windows/desktop/api/ComSvcs/nf-comsvcs-itransactionproxy-commit) on the transaction proxy.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a245b-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a245b-112">Return value</span></span>

<span data-ttu-id="a245b-113">Esse método pode retornar os valores de retorno padrão E \_ INVALIDARG, e \_ OUTOFMEMORY E e e \_ inesperados, bem como os valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="a245b-113">This method can return the standard return values E\_INVALIDARG, E\_OUTOFMEMORY, and E\_UNEXPECTED, as well as the following values.</span></span>



| <span data-ttu-id="a245b-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="a245b-114">Return code</span></span>                                                                                                     | <span data-ttu-id="a245b-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="a245b-115">Description</span></span>                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a245b-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a245b-116"><dt>**S\_OK**</dt></span></span> </dl>                            | <span data-ttu-id="a245b-117">O método foi concluído com êxito.</span><span class="sxs-lookup"><span data-stu-id="a245b-117">The method completed successfully.</span></span><br/>                                                                           |
| <dl> <span data-ttu-id="a245b-118"><dt>**CONTEXTO \_ E \_ ALREADYINTRANSACTION**</dt></span><span class="sxs-lookup"><span data-stu-id="a245b-118"><dt>**CONTEXT\_E\_ALREADYINTRANSACTION**</dt></span></span> </dl> | <span data-ttu-id="a245b-119">O contexto atual já tem uma implementação [**ITransactionProxy**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactionproxy) associada.</span><span class="sxs-lookup"><span data-stu-id="a245b-119">The current context already has an associated [**ITransactionProxy**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactionproxy) implementation.</span></span><br/> |
| <dl> <span data-ttu-id="a245b-120"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="a245b-120"><dt>**E\_NOTIMPL**</dt></span></span> </dl>                       | <span data-ttu-id="a245b-121">O contexto atual está hospedando uma transação de BYOT (traga sua própria transação) ou uma transação não raiz.</span><span class="sxs-lookup"><span data-stu-id="a245b-121">The current context is hosting a Bring Your Own Transaction (BYOT) transaction or a non-root transaction.</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="a245b-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="a245b-122">Remarks</span></span>

<span data-ttu-id="a245b-123">O método **RegisterTransactionProxy** só poderá ser chamado se o contexto atual for um contexto de transação raiz.</span><span class="sxs-lookup"><span data-stu-id="a245b-123">The **RegisterTransactionProxy** method can only be called if the current context is a root transaction context.</span></span> <span data-ttu-id="a245b-124">Ele não poderá ser chamado se o contexto estiver hospedando uma transação de BYOT ou uma transação não raiz.</span><span class="sxs-lookup"><span data-stu-id="a245b-124">It cannot be called if the context is hosting a BYOT transaction or a non-root transaction.</span></span>

## <a name="requirements"></a><span data-ttu-id="a245b-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a245b-125">Requirements</span></span>



| <span data-ttu-id="a245b-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="a245b-126">Requirement</span></span> | <span data-ttu-id="a245b-127">Valor</span><span class="sxs-lookup"><span data-stu-id="a245b-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="a245b-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a245b-128">Minimum supported client</span></span><br/> | <span data-ttu-id="a245b-129">\[Somente aplicativos de área de trabalho do Windows XP com SP2\]</span><span class="sxs-lookup"><span data-stu-id="a245b-129">Windows XP with SP2 \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="a245b-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a245b-130">Minimum supported server</span></span><br/> | <span data-ttu-id="a245b-131">\[Somente aplicativos da área de trabalho do Windows Server 2003 com SP1\]</span><span class="sxs-lookup"><span data-stu-id="a245b-131">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a245b-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="a245b-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a245b-133">**IContextTransactionInfo**</span><span class="sxs-lookup"><span data-stu-id="a245b-133">**IContextTransactionInfo**</span></span>](icontexttransactioninfo.md)
</dt> </dl>

 

 




