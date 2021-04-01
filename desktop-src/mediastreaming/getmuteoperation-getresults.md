---
title: Método GetMuteOperation. GetResults
description: Retorna os resultados da operação assíncrona iniciada pelo GetMuteAsync.
ms.assetid: 5B6DB1B3-54D4-486D-AA03-5FEEC92304B0
keywords:
- API de streaming de mídia do método GetResults
- API de streaming de mídia do método GetResults, interface GetMuteOperation
- API de streaming de mídia da interface GetMuteOperation, método GetResults
topic_type:
- apiref
api_name:
- GetMuteOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 33c43dc7fee228b1808ff4f607ee6a72faf1e770
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104084480"
---
# <a name="getmuteoperationgetresults-method"></a><span data-ttu-id="63601-106">Método GetMuteOperation. GetResults</span><span class="sxs-lookup"><span data-stu-id="63601-106">GetMuteOperation.GetResults method</span></span>

<span data-ttu-id="63601-107">Retorna os resultados da operação assíncrona iniciada pelo [**GetMuteAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getmuteasync).</span><span class="sxs-lookup"><span data-stu-id="63601-107">Returns the results of the asynchronous operation started by [**GetMuteAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getmuteasync).</span></span>

## <a name="syntax"></a><span data-ttu-id="63601-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="63601-108">Syntax</span></span>


```C++
HRESULT GetResults(
  [out, retval] boolean *value
);
```



## <a name="parameters"></a><span data-ttu-id="63601-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="63601-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63601-110">*valor* \[ do out, retval\]</span><span class="sxs-lookup"><span data-stu-id="63601-110">*value* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="63601-111">O valor de mudo.</span><span class="sxs-lookup"><span data-stu-id="63601-111">The mute value.</span></span> <span data-ttu-id="63601-112">Um valor true indica que o áudio está mudo no momento.</span><span class="sxs-lookup"><span data-stu-id="63601-112">A value of true indicates that audio is currently muted.</span></span> <span data-ttu-id="63601-113">Um valor false indica que o áudio não está mudo.</span><span class="sxs-lookup"><span data-stu-id="63601-113">A value of false indicates that audio is not muted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63601-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="63601-114">Return value</span></span>

<span data-ttu-id="63601-115">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="63601-115">The method returns an **HRESULT**.</span></span> <span data-ttu-id="63601-116">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="63601-116">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="63601-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="63601-117">Return code</span></span>                                                                          | <span data-ttu-id="63601-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="63601-118">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="63601-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="63601-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="63601-120">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="63601-120">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="63601-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="63601-121">Remarks</span></span>

<span data-ttu-id="63601-122">O método **GetResults** é normalmente chamado a partir do manipulador de eventos que foi registrado pela configuração da propriedade [**Completed**](getmuteoperation-completed.md) .</span><span class="sxs-lookup"><span data-stu-id="63601-122">The **GetResults** method is typically called from the event handler that was registered by setting the [**Completed**](getmuteoperation-completed.md) property.</span></span>

## <a name="see-also"></a><span data-ttu-id="63601-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="63601-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63601-124">**GetMuteOperation**</span><span class="sxs-lookup"><span data-stu-id="63601-124">**GetMuteOperation**</span></span>](getmuteoperation.md)
</dt> </dl>

 

