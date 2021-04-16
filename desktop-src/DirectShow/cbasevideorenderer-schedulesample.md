---
description: O método ScheduleSample substitui a classe base que faz o trabalho principal para manter uma contagem de amostras desenhada e descartada (que são usadas pela implementação de IQualProp).
ms.assetid: 66e4e318-a7ff-4ba0-9ac5-24ba39ac86f1
title: Método CBaseVideoRenderer. ScheduleSample (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.ScheduleSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 62827f1cda9423f9a5128c35289803027bfa78a6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758554"
---
# <a name="cbasevideorendererschedulesample-method"></a><span data-ttu-id="8d1c6-103">Método CBaseVideoRenderer. ScheduleSample</span><span class="sxs-lookup"><span data-stu-id="8d1c6-103">CBaseVideoRenderer.ScheduleSample method</span></span>

<span data-ttu-id="8d1c6-104">O `ScheduleSample` método substitui a classe base que faz o trabalho principal manter uma contagem de amostras desenhada e descartada (que são usadas pela implementação de [**IQualProp**](/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop) ).</span><span class="sxs-lookup"><span data-stu-id="8d1c6-104">The `ScheduleSample` method overrides the base class that does the main work to keep a count of samples drawn and dropped (which are used by the [**IQualProp**](/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop) implementation).</span></span>

## <a name="syntax"></a><span data-ttu-id="8d1c6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8d1c6-105">Syntax</span></span>


```C++
BOOL ScheduleSample(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="8d1c6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8d1c6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d1c6-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="8d1c6-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="8d1c6-108">Ponteiro para o exemplo de mídia.</span><span class="sxs-lookup"><span data-stu-id="8d1c6-108">Pointer to the media sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d1c6-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8d1c6-109">Return value</span></span>

<span data-ttu-id="8d1c6-110">Retornará **true** se o exemplo for agendado; caso contrário, retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="8d1c6-110">Returns **TRUE** if the sample is scheduled; otherwise, returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d1c6-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8d1c6-111">Requirements</span></span>



| <span data-ttu-id="8d1c6-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="8d1c6-112">Requirement</span></span> | <span data-ttu-id="8d1c6-113">Valor</span><span class="sxs-lookup"><span data-stu-id="8d1c6-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d1c6-114">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8d1c6-114">Header</span></span><br/>  | <dl> <span data-ttu-id="8d1c6-115"><dt>Renbase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8d1c6-115"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="8d1c6-116">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8d1c6-116">Library</span></span><br/> | <dl> <span data-ttu-id="8d1c6-117"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="8d1c6-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d1c6-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="8d1c6-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d1c6-119">**Classe CBaseVideoRenderer**</span><span class="sxs-lookup"><span data-stu-id="8d1c6-119">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




