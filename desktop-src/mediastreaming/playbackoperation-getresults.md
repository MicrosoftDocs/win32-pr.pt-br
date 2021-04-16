---
title: Método PlaybackOperation. GetResults
description: Retorna os resultados de uma operação assíncrona iniciada por um dos métodos de reprodução MediaRenderer.
ms.assetid: EAA5B342-51EF-449A-A7E2-FFBDBE07757C
keywords:
- API de streaming de mídia do método GetResults
- API de streaming de mídia do método GetResults, interface PlaybackOperation
- API de streaming de mídia da interface PlaybackOperation, método GetResults
topic_type:
- apiref
api_name:
- PlaybackOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f146876966cc4e003bd88ad295c9938e5240abfe
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104364605"
---
# <a name="playbackoperationgetresults-method"></a><span data-ttu-id="a6a95-106">Método PlaybackOperation. GetResults</span><span class="sxs-lookup"><span data-stu-id="a6a95-106">PlaybackOperation.GetResults method</span></span>

<span data-ttu-id="a6a95-107">Retorna os resultados de uma operação assíncrona iniciada por um dos métodos de reprodução [**MediaRenderer**](mediarenderer.md) .</span><span class="sxs-lookup"><span data-stu-id="a6a95-107">Returns the results of an asynchronous operation started by one of the [**MediaRenderer**](mediarenderer.md) playback methods.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6a95-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a6a95-108">Syntax</span></span>


```C++
HRESULT GetResults(
  [out, retval] UINT32 *value
);
```



## <a name="parameters"></a><span data-ttu-id="a6a95-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a6a95-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6a95-110">*valor* \[ do out, retval\]</span><span class="sxs-lookup"><span data-stu-id="a6a95-110">*value* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="a6a95-111">O resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="a6a95-111">The result of the operation.</span></span> <span data-ttu-id="a6a95-112">Um valor de 0 indica que a operação foi concluída.</span><span class="sxs-lookup"><span data-stu-id="a6a95-112">A value of 0 indicates that the operation completed.</span></span> <span data-ttu-id="a6a95-113">Outros valores são reservados.</span><span class="sxs-lookup"><span data-stu-id="a6a95-113">Other values are reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6a95-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a6a95-114">Return value</span></span>

<span data-ttu-id="a6a95-115">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="a6a95-115">The method returns an **HRESULT**.</span></span> <span data-ttu-id="a6a95-116">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="a6a95-116">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="a6a95-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="a6a95-117">Return code</span></span>                                                                          | <span data-ttu-id="a6a95-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="a6a95-118">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="a6a95-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a6a95-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="a6a95-120">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="a6a95-120">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a6a95-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="a6a95-121">Remarks</span></span>

<span data-ttu-id="a6a95-122">O método **GetResults** é normalmente chamado a partir do manipulador de eventos que foi registrado pela configuração da propriedade [**Completed**](playbackoperation-completed.md) .</span><span class="sxs-lookup"><span data-stu-id="a6a95-122">The **GetResults** method is typically called from the event handler that was registered by setting the [**Completed**](playbackoperation-completed.md) property.</span></span>

## <a name="see-also"></a><span data-ttu-id="a6a95-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="a6a95-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6a95-124">**PlaybackOperation**</span><span class="sxs-lookup"><span data-stu-id="a6a95-124">**PlaybackOperation**</span></span>](playbackoperation.md)
</dt> </dl>

 

 





