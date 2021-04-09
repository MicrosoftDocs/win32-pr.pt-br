---
description: Recupera a transação ou o proxy de transação que está associado ao contexto atual, se houver.
ms.assetid: 2f85f395-3ec5-4c5a-a6db-c902cb8f8486
title: 'Método IContextTransactionInfo:: FetchTransaction'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextTransactionInfo.FetchTransaction
api_type:
- COM
api_location: ''
ms.openlocfilehash: 0e753974f93539f051465f13a1ea92d7e0e3bfa1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089312"
---
# <a name="icontexttransactioninfofetchtransaction-method"></a><span data-ttu-id="5dc39-103">Método IContextTransactionInfo:: FetchTransaction</span><span class="sxs-lookup"><span data-stu-id="5dc39-103">IContextTransactionInfo::FetchTransaction method</span></span>

<span data-ttu-id="5dc39-104">Recupera a transação ou o proxy de transação que está associado ao contexto atual, se houver.</span><span class="sxs-lookup"><span data-stu-id="5dc39-104">Retrieves the transaction or transaction proxy that is associated with the current context, if any.</span></span>

## <a name="syntax"></a><span data-ttu-id="5dc39-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5dc39-105">Syntax</span></span>


```C++
HRESULT FetchTransaction(
  [out, retval] IUnknown **pUnk
);
```



## <a name="parameters"></a><span data-ttu-id="5dc39-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5dc39-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5dc39-107">*punk* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="5dc39-107">*pUnk* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="5dc39-108">A transação ou o proxy de transação que está associado ao contexto atual; caso contrário, **NULL**.</span><span class="sxs-lookup"><span data-stu-id="5dc39-108">The transaction or transaction proxy that is associated with the current context; otherwise, **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5dc39-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5dc39-109">Return value</span></span>

<span data-ttu-id="5dc39-110">Esse método pode retornar os valores de retorno padrão E \_ INVALIDARG, e \_ OUTOFMEMORY, e \_ inesperado, e S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5dc39-110">This method can return the standard return values E\_INVALIDARG, E\_OUTOFMEMORY, E\_UNEXPECTED, and S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="5dc39-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5dc39-111">Requirements</span></span>



| <span data-ttu-id="5dc39-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="5dc39-112">Requirement</span></span> | <span data-ttu-id="5dc39-113">Valor</span><span class="sxs-lookup"><span data-stu-id="5dc39-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="5dc39-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5dc39-114">Minimum supported client</span></span><br/> | <span data-ttu-id="5dc39-115">\[Somente aplicativos de área de trabalho do Windows XP com SP2\]</span><span class="sxs-lookup"><span data-stu-id="5dc39-115">Windows XP with SP2 \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="5dc39-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5dc39-116">Minimum supported server</span></span><br/> | <span data-ttu-id="5dc39-117">\[Somente aplicativos da área de trabalho do Windows Server 2003 com SP1\]</span><span class="sxs-lookup"><span data-stu-id="5dc39-117">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5dc39-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="5dc39-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5dc39-119">**IContextTransactionInfo**</span><span class="sxs-lookup"><span data-stu-id="5dc39-119">**IContextTransactionInfo**</span></span>](icontexttransactioninfo.md)
</dt> </dl>

 

 




