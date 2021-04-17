---
description: O método DisplaySampleTimes desenha os carimbos de data/hora de uma amostra de mídia na parte superior da imagem de vídeo.
ms.assetid: 3741dc74-5311-4cb1-9e6b-4a8bf6113477
title: Método CDrawImage. DisplaySampleTimes (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.DisplaySampleTimes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9988aaedf9a1c01c83412cdbe9e00533556c9b15
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755597"
---
# <a name="cdrawimagedisplaysampletimes-method"></a><span data-ttu-id="e0101-103">Método CDrawImage. DisplaySampleTimes</span><span class="sxs-lookup"><span data-stu-id="e0101-103">CDrawImage.DisplaySampleTimes method</span></span>

<span data-ttu-id="e0101-104">O `DisplaySampleTimes` método desenha os carimbos de data/hora de uma amostra de mídia na parte superior da imagem de vídeo.</span><span class="sxs-lookup"><span data-stu-id="e0101-104">The `DisplaySampleTimes` method draws the time stamps of a media sample on top of the video image.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0101-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e0101-105">Syntax</span></span>


```C++
void DisplaySampleTimes(
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="e0101-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e0101-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0101-107">*pSample*</span><span class="sxs-lookup"><span data-stu-id="e0101-107">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="e0101-108">Ponteiro para a interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) do exemplo.</span><span class="sxs-lookup"><span data-stu-id="e0101-108">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface of the sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0101-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e0101-109">Return value</span></span>

<span data-ttu-id="e0101-110">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="e0101-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0101-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="e0101-111">Remarks</span></span>

<span data-ttu-id="e0101-112">Esse método é chamado somente em compilações de depuração.</span><span class="sxs-lookup"><span data-stu-id="e0101-112">This method is called only in debug builds.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0101-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e0101-113">Requirements</span></span>



| <span data-ttu-id="e0101-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0101-114">Requirement</span></span> | <span data-ttu-id="e0101-115">Valor</span><span class="sxs-lookup"><span data-stu-id="e0101-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0101-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e0101-116">Header</span></span><br/>  | <dl> <span data-ttu-id="e0101-117"><dt>Winutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e0101-117"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e0101-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e0101-118">Library</span></span><br/> | <dl> <span data-ttu-id="e0101-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="e0101-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0101-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="e0101-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0101-121">**Classe CDrawImage**</span><span class="sxs-lookup"><span data-stu-id="e0101-121">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> </dl>

 

 




