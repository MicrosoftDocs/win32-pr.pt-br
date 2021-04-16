---
description: O \_ método Get FramesDroppedInRenderer recupera o número de quadros descartados pelo renderizador.
ms.assetid: d890f285-b3bb-426c-80f6-e273cf0cccbb
title: Método de CBaseVideoRenderer.get_FramesDroppedInRenderer (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.get_FramesDroppedInRenderer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ef81678fce8d349c7c047b0453cc480d8673f8f8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750667"
---
# <a name="cbasevideorendererget_framesdroppedinrenderer-method"></a><span data-ttu-id="a7d1c-103">CBaseVideoRenderer. obter \_ método FramesDroppedInRenderer</span><span class="sxs-lookup"><span data-stu-id="a7d1c-103">CBaseVideoRenderer.get\_FramesDroppedInRenderer method</span></span>

<span data-ttu-id="a7d1c-104">O `get_FramesDroppedInRenderer` método recupera o número de quadros descartados pelo renderizador.</span><span class="sxs-lookup"><span data-stu-id="a7d1c-104">The `get_FramesDroppedInRenderer` method retrieves the number of frames dropped by the renderer.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7d1c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a7d1c-105">Syntax</span></span>


```C++
HRESULT get_FramesDroppedInRenderer(
   int *pcFramesDropped
);
```



## <a name="parameters"></a><span data-ttu-id="a7d1c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a7d1c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7d1c-107">*pcFramesDropped*</span><span class="sxs-lookup"><span data-stu-id="a7d1c-107">*pcFramesDropped*</span></span> 
</dt> <dd>

<span data-ttu-id="a7d1c-108">Ponteiro para o número de quadros descartados.</span><span class="sxs-lookup"><span data-stu-id="a7d1c-108">Pointer to the number of frames dropped.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7d1c-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a7d1c-109">Return value</span></span>

<span data-ttu-id="a7d1c-110">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a7d1c-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a7d1c-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="a7d1c-111">Remarks</span></span>

<span data-ttu-id="a7d1c-112">Essa função de membro implementa o método [**IQualProp:: get \_ FramesDroppedInRenderer**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_framesdroppedinrenderer) .</span><span class="sxs-lookup"><span data-stu-id="a7d1c-112">This member function implements the [**IQualProp::get\_FramesDroppedInRenderer**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_framesdroppedinrenderer) method.</span></span> <span data-ttu-id="a7d1c-113">É assim que a página de propriedades recupera os dados do Agendador.</span><span class="sxs-lookup"><span data-stu-id="a7d1c-113">This is how the property page retrieves the data from the scheduler.</span></span> <span data-ttu-id="a7d1c-114">Os quadros também podem ser retirados upstream sem o renderizador até mesmo vê-los.</span><span class="sxs-lookup"><span data-stu-id="a7d1c-114">Frames can also be dropped upstream without the renderer even seeing them.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7d1c-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a7d1c-115">Requirements</span></span>



| <span data-ttu-id="a7d1c-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="a7d1c-116">Requirement</span></span> | <span data-ttu-id="a7d1c-117">Valor</span><span class="sxs-lookup"><span data-stu-id="a7d1c-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7d1c-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a7d1c-118">Header</span></span><br/>  | <dl> <span data-ttu-id="a7d1c-119"><dt>Renbase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a7d1c-119"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a7d1c-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a7d1c-120">Library</span></span><br/> | <dl> <span data-ttu-id="a7d1c-121"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="a7d1c-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7d1c-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="a7d1c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7d1c-123">**Classe CBaseVideoRenderer**</span><span class="sxs-lookup"><span data-stu-id="a7d1c-123">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




