---
description: O método JoinFilterGraph envia a \_ \_ notificação de evento destruída da janela do EC quando um filtro é removido do gráfico de filtro.
ms.assetid: b54d2deb-d36f-43a9-aa00-d607f487d8b7
title: Método CBaseVideoRenderer. JoinFilterGraph (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.JoinFilterGraph
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: acabb6deeb6577fa04479fc4014e210d4a5654d5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757709"
---
# <a name="cbasevideorendererjoinfiltergraph-method"></a><span data-ttu-id="d2ea7-103">Método CBaseVideoRenderer. JoinFilterGraph</span><span class="sxs-lookup"><span data-stu-id="d2ea7-103">CBaseVideoRenderer.JoinFilterGraph method</span></span>

<span data-ttu-id="d2ea7-104">O `JoinFilterGraph` método envia a notificação de evento da [**janela do EC \_ \_ destruída**](ec-window-destroyed.md) quando um filtro é removido do gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="d2ea7-104">The `JoinFilterGraph` method sends [**EC\_WINDOW\_DESTROYED**](ec-window-destroyed.md) event notification when a filter is removed from the filter graph.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2ea7-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d2ea7-105">Syntax</span></span>


```C++
HRESULT JoinFilterGraph(
       IBaseFilterGraph *pGraph,
  [in] LPCWSTR          pName
);
```



## <a name="parameters"></a><span data-ttu-id="d2ea7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d2ea7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2ea7-107">*pGraph*</span><span class="sxs-lookup"><span data-stu-id="d2ea7-107">*pGraph*</span></span> 
</dt> <dd>

<span data-ttu-id="d2ea7-108">Ponteiro para o gráfico de filtro a ser associado.</span><span class="sxs-lookup"><span data-stu-id="d2ea7-108">Pointer to the filter graph to join.</span></span>

</dd> <dt>

<span data-ttu-id="d2ea7-109">*pname* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d2ea7-109">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2ea7-110">Ponteiro para o nome do filtro que está sendo adicionado.</span><span class="sxs-lookup"><span data-stu-id="d2ea7-110">Pointer to the name of the filter being added.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2ea7-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d2ea7-111">Return value</span></span>

<span data-ttu-id="d2ea7-112">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="d2ea7-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2ea7-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="d2ea7-113">Remarks</span></span>

<span data-ttu-id="d2ea7-114">Essa função de membro substitui a função de membro [**CBaseFilter:: JoinFilterGraph**](cbasefilter-joinfiltergraph.md) .</span><span class="sxs-lookup"><span data-stu-id="d2ea7-114">This member function overrides the [**CBaseFilter::JoinFilterGraph**](cbasefilter-joinfiltergraph.md) member function.</span></span> <span data-ttu-id="d2ea7-115">Se o filtro estiver deixando o grafo de filtro (*pGraph* é **nulo**), ele enviará uma notificação de evento de [**janela do EC \_ \_ destruída**](ec-window-destroyed.md) para que o Gerenciador de recursos não mantenha o processador como um objeto de foco.</span><span class="sxs-lookup"><span data-stu-id="d2ea7-115">If the filter is leaving the filter graph (*pGraph* is **NULL**), it sends an [**EC\_WINDOW\_DESTROYED**](ec-window-destroyed.md) event notification so that the resource manager does not hold on to the renderer as a focus object.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2ea7-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d2ea7-116">Requirements</span></span>



| <span data-ttu-id="d2ea7-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2ea7-117">Requirement</span></span> | <span data-ttu-id="d2ea7-118">Valor</span><span class="sxs-lookup"><span data-stu-id="d2ea7-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2ea7-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d2ea7-119">Header</span></span><br/>  | <dl> <span data-ttu-id="d2ea7-120"><dt>Renbase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d2ea7-120"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d2ea7-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d2ea7-121">Library</span></span><br/> | <dl> <span data-ttu-id="d2ea7-122"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="d2ea7-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2ea7-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="d2ea7-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2ea7-124">**Classe CBaseVideoRenderer**</span><span class="sxs-lookup"><span data-stu-id="d2ea7-124">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




