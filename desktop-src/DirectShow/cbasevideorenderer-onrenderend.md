---
description: O método OnRenderEnd executa a suavização para casos em que o tempo de renderização varia devido a interrupções.
ms.assetid: 561b3306-0c41-4f04-b73a-78e7b4038e86
title: Método CBaseVideoRenderer. OnRenderEnd (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.OnRenderEnd
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8f37b4d03f77090f4cac40a218fd3ac27c0c349d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748634"
---
# <a name="cbasevideorendereronrenderend-method"></a><span data-ttu-id="cbc41-103">Método CBaseVideoRenderer. OnRenderEnd</span><span class="sxs-lookup"><span data-stu-id="cbc41-103">CBaseVideoRenderer.OnRenderEnd method</span></span>

<span data-ttu-id="cbc41-104">O `OnRenderEnd` método executa a suavização para casos em que o tempo de renderização varia devido a interrupções.</span><span class="sxs-lookup"><span data-stu-id="cbc41-104">The `OnRenderEnd` method performs smoothing for cases where the rendering time varies due to interruptions.</span></span>

## <a name="syntax"></a><span data-ttu-id="cbc41-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cbc41-105">Syntax</span></span>


```C++
void OnRenderEnd(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="cbc41-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cbc41-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cbc41-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="cbc41-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="cbc41-108">Ponteiro para o exemplo de mídia.</span><span class="sxs-lookup"><span data-stu-id="cbc41-108">Pointer to the media sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cbc41-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cbc41-109">Return value</span></span>

<span data-ttu-id="cbc41-110">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="cbc41-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cbc41-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="cbc41-111">Remarks</span></span>

<span data-ttu-id="cbc41-112">Essa função de membro deve ser chamada logo após o desenho de uma imagem.</span><span class="sxs-lookup"><span data-stu-id="cbc41-112">This member function should be called just after drawing an image.</span></span>

<span data-ttu-id="cbc41-113">Essa função de membro substitui [**CBaseRenderer:: OnRenderEnd**](cbaserenderer-onrenderend.md).</span><span class="sxs-lookup"><span data-stu-id="cbc41-113">This member function overrides [**CBaseRenderer::OnRenderEnd**](cbaserenderer-onrenderend.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cbc41-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cbc41-114">Requirements</span></span>



| <span data-ttu-id="cbc41-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="cbc41-115">Requirement</span></span> | <span data-ttu-id="cbc41-116">Valor</span><span class="sxs-lookup"><span data-stu-id="cbc41-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbc41-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cbc41-117">Header</span></span><br/>  | <dl> <span data-ttu-id="cbc41-118"><dt>Renbase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cbc41-118"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="cbc41-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cbc41-119">Library</span></span><br/> | <dl> <span data-ttu-id="cbc41-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="cbc41-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cbc41-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="cbc41-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbc41-122">**Classe CBaseVideoRenderer**</span><span class="sxs-lookup"><span data-stu-id="cbc41-122">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




