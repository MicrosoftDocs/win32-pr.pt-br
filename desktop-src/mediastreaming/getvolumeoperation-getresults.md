---
title: Método GetVolumeOperation. GetResults
description: Retorna os resultados da operação assíncrona iniciada pelo GetVolumeAsync.
ms.assetid: 71DC4D76-4CC2-4D40-960F-AF56E1F33557
keywords:
- API de streaming de mídia do método GetResults
- API de streaming de mídia do método GetResults, interface GetVolumeOperation
- API de streaming de mídia da interface GetVolumeOperation, método GetResults
topic_type:
- apiref
api_name:
- GetVolumeOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 444eaf590e5afc5d4f5185bcd3793698d6fe4535
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105784613"
---
# <a name="getvolumeoperationgetresults-method"></a><span data-ttu-id="f461f-106">Método GetVolumeOperation. GetResults</span><span class="sxs-lookup"><span data-stu-id="f461f-106">GetVolumeOperation.GetResults method</span></span>

<span data-ttu-id="f461f-107">Retorna os resultados da operação assíncrona iniciada pelo [**GetVolumeAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getvolumeasync).</span><span class="sxs-lookup"><span data-stu-id="f461f-107">Returns the results of the asynchronous operation started by [**GetVolumeAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getvolumeasync).</span></span>

## <a name="syntax"></a><span data-ttu-id="f461f-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f461f-108">Syntax</span></span>


```C++
HRESULT GetResults(
  [out, retval] UINT32 *value
);
```



## <a name="parameters"></a><span data-ttu-id="f461f-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f461f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f461f-110">*valor* \[ do out, retval\]</span><span class="sxs-lookup"><span data-stu-id="f461f-110">*value* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="f461f-111">O volume.</span><span class="sxs-lookup"><span data-stu-id="f461f-111">The volume.</span></span> <span data-ttu-id="f461f-112">Um valor entre 0 e 100.</span><span class="sxs-lookup"><span data-stu-id="f461f-112">A value between 0 and 100.</span></span> <span data-ttu-id="f461f-113">0 indica o volume mínimo e 100 indica o volume máximo.</span><span class="sxs-lookup"><span data-stu-id="f461f-113">0 indicates minimum volume, and 100 indicates maximum volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f461f-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f461f-114">Return value</span></span>

<span data-ttu-id="f461f-115">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="f461f-115">The method returns an **HRESULT**.</span></span> <span data-ttu-id="f461f-116">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="f461f-116">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="f461f-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="f461f-117">Return code</span></span>                                                                          | <span data-ttu-id="f461f-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="f461f-118">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="f461f-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f461f-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="f461f-120">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="f461f-120">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f461f-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="f461f-121">Remarks</span></span>

<span data-ttu-id="f461f-122">O método **GetResults** é normalmente chamado a partir do manipulador de eventos que foi registrado pela configuração da propriedade [**Completed**](getvolumeoperation-completed.md) .</span><span class="sxs-lookup"><span data-stu-id="f461f-122">The **GetResults** method is typically called from the event handler that was registered by setting the [**Completed**](getvolumeoperation-completed.md) property.</span></span>

## <a name="see-also"></a><span data-ttu-id="f461f-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="f461f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f461f-124">**GetVolumeOperation**</span><span class="sxs-lookup"><span data-stu-id="f461f-124">**GetVolumeOperation**</span></span>](getvolumeoperation.md)
</dt> </dl>

 

