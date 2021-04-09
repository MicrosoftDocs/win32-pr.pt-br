---
description: Invoca o método que é chamado quando a operação assíncrona especificada relata o progresso.
ms.assetid: FB60DDC0-7521-4999-8DD8-175556004198
title: 'IAsyncOperationWithProgressCompletedHandler<TResult, TProgress>:: Invoke Method'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAsyncOperationWithProgressCompletedHandler<TResult,TProgress>.Invoke
api_type:
- COM
api_location: ''
ms.openlocfilehash: 469686cbd96dedc7f816fdd1f482d3474362688e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090414"
---
# <a name="iasyncoperationwithprogresscompletedhandlertresulttprogressinvoke-method"></a><span data-ttu-id="68998-103">IAsyncOperationWithProgressCompletedHandler<TResult, TProgress>:: Invoke Method</span><span class="sxs-lookup"><span data-stu-id="68998-103">IAsyncOperationWithProgressCompletedHandler<TResult,TProgress>::Invoke method</span></span>

<span data-ttu-id="68998-104">Invoca o método que é chamado quando a operação assíncrona especificada relata o progresso.</span><span class="sxs-lookup"><span data-stu-id="68998-104">Invokes the method that is called when the specified asynchronous operation reports progress.</span></span>

## <a name="syntax"></a><span data-ttu-id="68998-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="68998-105">Syntax</span></span>


```C++
HRESULT Invoke(
  [in] IAsyncOperationWithProgress<TResult,TProgress> *asyncInfo
);
```



## <a name="parameters"></a><span data-ttu-id="68998-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="68998-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68998-107">*asyncInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="68998-107">*asyncInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68998-108">Tipo: \**[**IAsyncOperationWithProgress<TResult, TProgress>**](/previous-versions//br205807(v=vs.85)) \** _</span><span class="sxs-lookup"><span data-stu-id="68998-108">Type: \**[**IAsyncOperationWithProgress<TResult,TProgress>**](/previous-versions//br205807(v=vs.85))\** _</span></span>

<span data-ttu-id="68998-109">A ação assíncrona que relata a conclusão.</span><span class="sxs-lookup"><span data-stu-id="68998-109">The asynchronous action that reports completion.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68998-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="68998-110">Return value</span></span>

<span data-ttu-id="68998-111">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="68998-111">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="68998-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="68998-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="68998-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="68998-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="68998-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="68998-114">Requirements</span></span>



| <span data-ttu-id="68998-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="68998-115">Requirement</span></span> | <span data-ttu-id="68998-116">Valor</span><span class="sxs-lookup"><span data-stu-id="68998-116">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="68998-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="68998-117">Minimum supported client</span></span><br/> | <span data-ttu-id="68998-118">Windows 8</span><span class="sxs-lookup"><span data-stu-id="68998-118">Windows 8</span></span><br/>           |
| <span data-ttu-id="68998-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="68998-119">Minimum supported server</span></span><br/> | <span data-ttu-id="68998-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="68998-120">Windows Server 2012</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="68998-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="68998-121">See also</span></span>

<dl> <dt>

<span data-ttu-id="68998-122">[**IAsyncOperationWithProgressCompletedHandler<TResult, TProgress>**](/previous-versions//br205808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="68998-122">[**IAsyncOperationWithProgressCompletedHandler<TResult,TProgress>**](/previous-versions//br205808(v=vs.85))</span></span>
</dt> </dl>

 

 
