---
description: A função ContainsPalette determina se uma estrutura VIDEOINFOHEADER especificada contém uma paleta.
ms.assetid: e87ab1af-a822-45d8-9326-08b450e11279
title: Função ContainsPalette (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ContainsPalette
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b9417d9dd39f958e4a4caf68ef368d231a2097de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782260"
---
# <a name="containspalette-function"></a><span data-ttu-id="0fdcc-103">Função ContainsPalette</span><span class="sxs-lookup"><span data-stu-id="0fdcc-103">ContainsPalette function</span></span>

<span data-ttu-id="0fdcc-104">A função **ContainsPalette** determina se uma estrutura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) especificada contém uma paleta.</span><span class="sxs-lookup"><span data-stu-id="0fdcc-104">The **ContainsPalette** function determines whether a specified [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure contains a palette.</span></span>

## <a name="syntax"></a><span data-ttu-id="0fdcc-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0fdcc-105">Syntax</span></span>


```C++
BOOL ContainsPalette(
   const VIDEOINFOHEADER *pVideoInfo

);
```



## <a name="parameters"></a><span data-ttu-id="0fdcc-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0fdcc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0fdcc-107">*pVideoInfo*</span><span class="sxs-lookup"><span data-stu-id="0fdcc-107">*pVideoInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="0fdcc-108">Ponteiro para uma estrutura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) .</span><span class="sxs-lookup"><span data-stu-id="0fdcc-108">Pointer to a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0fdcc-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0fdcc-109">Return value</span></span>

<span data-ttu-id="0fdcc-110">Retornará **true** se bitdepth for 8 ou menos (**bmiHeader. biBitCount**) ou o número de índices de cores for maior que zero (**bmiHeader. biClrUsed**).</span><span class="sxs-lookup"><span data-stu-id="0fdcc-110">Returns **TRUE** if the bitdepth is 8 or less (**bmiHeader.biBitCount**), or the number of color indexes is more than zero (**bmiHeader.biClrUsed**).</span></span> <span data-ttu-id="0fdcc-111">Retorna **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="0fdcc-111">Returns **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="0fdcc-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0fdcc-112">Requirements</span></span>



| <span data-ttu-id="0fdcc-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="0fdcc-113">Requirement</span></span> | <span data-ttu-id="0fdcc-114">Valor</span><span class="sxs-lookup"><span data-stu-id="0fdcc-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0fdcc-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0fdcc-115">Header</span></span><br/>  | <dl> <span data-ttu-id="0fdcc-116"><dt>Wxutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0fdcc-116"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="0fdcc-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0fdcc-117">Library</span></span><br/> | <dl> <span data-ttu-id="0fdcc-118"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="0fdcc-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0fdcc-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="0fdcc-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fdcc-120">Funções de vídeo e imagem</span><span class="sxs-lookup"><span data-stu-id="0fdcc-120">Video and Image Functions</span></span>](video-and-image-functions.md)
</dt> </dl>

 

 




