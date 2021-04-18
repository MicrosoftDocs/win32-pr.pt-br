---
title: Método StreamSelectOperation. GetResults
description: Retorna os resultados da operação assíncrona iniciada pelo SelectBestStreamAsync.
ms.assetid: 2D9887E7-17C8-4161-984F-FA44591D2052
keywords:
- API de streaming de mídia do método GetResults
- API de streaming de mídia do método GetResults, interface StreamSelectOperation
- API de streaming de mídia da interface StreamSelectOperation, método GetResults
topic_type:
- apiref
api_name:
- StreamSelectOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c52479949413d32ca54654f355a06a2dee70866e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105815478"
---
# <a name="streamselectoperationgetresults-method"></a><span data-ttu-id="b090c-106">Método StreamSelectOperation. GetResults</span><span class="sxs-lookup"><span data-stu-id="b090c-106">StreamSelectOperation.GetResults method</span></span>

<span data-ttu-id="b090c-107">Retorna os resultados da operação assíncrona iniciada pelo [**SelectBestStreamAsync**](/previous-versions/windows/desktop/legacy/hh829001(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b090c-107">Returns the results of the asynchronous operation started by [**SelectBestStreamAsync**](/previous-versions/windows/desktop/legacy/hh829001(v=vs.85)).</span></span>

## <a name="syntax"></a><span data-ttu-id="b090c-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b090c-108">Syntax</span></span>


```C++
HRESULT GetResults(
  [out, retval] UINT32 *value
);
```



## <a name="parameters"></a><span data-ttu-id="b090c-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b090c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b090c-110">*valor* \[ do out, retval\]</span><span class="sxs-lookup"><span data-stu-id="b090c-110">*value* \[out, retval\]</span></span>
<span data-ttu-id="b090c-111"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="b090c-111"></dt> <dd></dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="b090c-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b090c-112">Return value</span></span>

<span data-ttu-id="b090c-113">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="b090c-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="b090c-114">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="b090c-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="b090c-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="b090c-115">Return code</span></span>                                                                          | <span data-ttu-id="b090c-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="b090c-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="b090c-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b090c-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="b090c-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="b090c-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="b090c-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="b090c-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b090c-120">**StreamSelectOperation**</span><span class="sxs-lookup"><span data-stu-id="b090c-120">**StreamSelectOperation**</span></span>](streamselectoperation.md)
</dt> </dl>

 

