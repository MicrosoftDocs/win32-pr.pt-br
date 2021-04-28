---
description: Construtor de CImagePalette. CImagePalette-método de construtor.
ms.assetid: 50fa573c-a244-4a1e-9fd9-2b33a3427c84
title: Construtor CImagePalette. CImagePalette (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette.CImagePalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5021b165a8fa47bedc7961657d7cdbfa07af301d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085674"
---
# <a name="cimagepalettecimagepalette-constructor"></a><span data-ttu-id="835d3-103">Construtor CImagePalette. CImagePalette</span><span class="sxs-lookup"><span data-stu-id="835d3-103">CImagePalette.CImagePalette constructor</span></span>

<span data-ttu-id="835d3-104">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="835d3-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="835d3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="835d3-105">Syntax</span></span>


```C++
CImagePalette(
   CBaseFilter *pBaseFilter,
   CBaseWindow *pBaseWindow,
   CDrawImage  *pDrawImage
);
```



## <a name="parameters"></a><span data-ttu-id="835d3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="835d3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="835d3-107">*pBaseFilter*</span><span class="sxs-lookup"><span data-stu-id="835d3-107">*pBaseFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="835d3-108">Ponteiro para proprietário do filtro.</span><span class="sxs-lookup"><span data-stu-id="835d3-108">Pointer to owning filter.</span></span>

</dd> <dt>

<span data-ttu-id="835d3-109">*pBaseWindow*</span><span class="sxs-lookup"><span data-stu-id="835d3-109">*pBaseWindow*</span></span> 
</dt> <dd>

<span data-ttu-id="835d3-110">Ponteiro para um objeto **CBaseWindow** , que gerencia a janela onde a paleta é percebida.</span><span class="sxs-lookup"><span data-stu-id="835d3-110">Pointer to a **CBaseWindow** object, which manages the window where the palette is realized.</span></span> <span data-ttu-id="835d3-111">Este parâmetro pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="835d3-111">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="835d3-112">*pDrawImage*</span><span class="sxs-lookup"><span data-stu-id="835d3-112">*pDrawImage*</span></span> 
</dt> <dd>

<span data-ttu-id="835d3-113">Ponteiro para um objeto **CDrawImage** , que desenha a imagem de vídeo.</span><span class="sxs-lookup"><span data-stu-id="835d3-113">Pointer to a **CDrawImage** object, which draws the video image.</span></span> <span data-ttu-id="835d3-114">Este parâmetro pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="835d3-114">This parameter can be **NULL**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="835d3-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="835d3-115">Requirements</span></span>



| <span data-ttu-id="835d3-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="835d3-116">Requirement</span></span> | <span data-ttu-id="835d3-117">Valor</span><span class="sxs-lookup"><span data-stu-id="835d3-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="835d3-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="835d3-118">Header</span></span><br/>  | <dl> <span data-ttu-id="835d3-119"><dt>Winutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="835d3-119"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="835d3-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="835d3-120">Library</span></span><br/> | <dl> <span data-ttu-id="835d3-121"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="835d3-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="835d3-122">Consulte também</span><span class="sxs-lookup"><span data-stu-id="835d3-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="835d3-123">**Classe CImagePalette**</span><span class="sxs-lookup"><span data-stu-id="835d3-123">**CImagePalette Class**</span></span>](cimagepalette.md)
</dt> </dl>

 

 




