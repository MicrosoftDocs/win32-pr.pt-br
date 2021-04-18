---
description: O método OnRenderStart define informações para renderização.
ms.assetid: 698fe778-e2cb-4b87-a668-084b6c12c71f
title: Método CBaseVideoRenderer. OnRenderStart (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.OnRenderStart
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7327d25aafa6f6673b7ed70b658f675a9dab8f4d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757330"
---
# <a name="cbasevideorendereronrenderstart-method"></a><span data-ttu-id="7ca46-103">Método CBaseVideoRenderer. OnRenderStart</span><span class="sxs-lookup"><span data-stu-id="7ca46-103">CBaseVideoRenderer.OnRenderStart method</span></span>

<span data-ttu-id="7ca46-104">O `OnRenderStart` método define informações para renderização.</span><span class="sxs-lookup"><span data-stu-id="7ca46-104">The `OnRenderStart` method sets information for rendering.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ca46-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7ca46-105">Syntax</span></span>


```C++
void OnRenderStart(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="7ca46-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7ca46-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ca46-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="7ca46-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="7ca46-108">Ponteiro para o exemplo de mídia.</span><span class="sxs-lookup"><span data-stu-id="7ca46-108">Pointer to the media sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ca46-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7ca46-109">Return value</span></span>

<span data-ttu-id="7ca46-110">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="7ca46-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7ca46-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="7ca46-111">Remarks</span></span>

<span data-ttu-id="7ca46-112">Essa função de membro recupera a hora do relógio atual do sistema e a armazena em uma variável de membro a ser usada quando o desenho for concluído.</span><span class="sxs-lookup"><span data-stu-id="7ca46-112">This member function retrieves the current clock time from the system and stores it in a member variable to be used when the drawing is complete.</span></span> <span data-ttu-id="7ca46-113">A função também executa o log de desempenho.</span><span class="sxs-lookup"><span data-stu-id="7ca46-113">The function also performs performance logging.</span></span> <span data-ttu-id="7ca46-114">Essa função de membro deve ser chamada logo antes do início do desenho.</span><span class="sxs-lookup"><span data-stu-id="7ca46-114">This member function should be called just before drawing starts.</span></span>

<span data-ttu-id="7ca46-115">Essa função de membro substitui [**CBaseRenderer:: OnRenderStart**](cbaserenderer-onrenderstart.md).</span><span class="sxs-lookup"><span data-stu-id="7ca46-115">This member function overrides [**CBaseRenderer::OnRenderStart**](cbaserenderer-onrenderstart.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7ca46-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7ca46-116">Requirements</span></span>



| <span data-ttu-id="7ca46-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ca46-117">Requirement</span></span> | <span data-ttu-id="7ca46-118">Valor</span><span class="sxs-lookup"><span data-stu-id="7ca46-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ca46-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7ca46-119">Header</span></span><br/>  | <dl> <span data-ttu-id="7ca46-120"><dt>Renbase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7ca46-120"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7ca46-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7ca46-121">Library</span></span><br/> | <dl> <span data-ttu-id="7ca46-122"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="7ca46-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ca46-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="7ca46-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ca46-124">**Classe CBaseVideoRenderer**</span><span class="sxs-lookup"><span data-stu-id="7ca46-124">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




