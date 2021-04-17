---
description: A função GetBitmapPalette retorna a primeira entrada da paleta em uma estrutura VIDEOINFOHEADER.
ms.assetid: 7c620f81-31d9-408f-954d-aeff39f93956
title: Função GetBitmapPalette (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetBitmapPalette
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ffa4139c7aaece3e92a26fbf69fc02b8759f1613
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105785346"
---
# <a name="getbitmappalette-function"></a><span data-ttu-id="6eed8-103">Função GetBitmapPalette</span><span class="sxs-lookup"><span data-stu-id="6eed8-103">GetBitmapPalette function</span></span>

<span data-ttu-id="6eed8-104">A `GetBitmapPalette` função retorna a primeira entrada da paleta em uma estrutura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) .</span><span class="sxs-lookup"><span data-stu-id="6eed8-104">The `GetBitmapPalette` function returns the first palette entry in a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="6eed8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6eed8-105">Syntax</span></span>


```C++
const RGBQUAD* GetBitmapPalette(
   const VIDEOINFOHEADER *pVideoInfo
);
```



## <a name="parameters"></a><span data-ttu-id="6eed8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6eed8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6eed8-107">*pVideoInfo*</span><span class="sxs-lookup"><span data-stu-id="6eed8-107">*pVideoInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="6eed8-108">Ponteiro para uma estrutura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) .</span><span class="sxs-lookup"><span data-stu-id="6eed8-108">Pointer to a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6eed8-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6eed8-109">Return value</span></span>

<span data-ttu-id="6eed8-110">Retorna um ponteiro para a primeira entrada da paleta.</span><span class="sxs-lookup"><span data-stu-id="6eed8-110">Returns a pointer to the first palette entry.</span></span>

## <a name="requirements"></a><span data-ttu-id="6eed8-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6eed8-111">Requirements</span></span>



| <span data-ttu-id="6eed8-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="6eed8-112">Requirement</span></span> | <span data-ttu-id="6eed8-113">Valor</span><span class="sxs-lookup"><span data-stu-id="6eed8-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6eed8-114">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6eed8-114">Header</span></span><br/>  | <dl> <span data-ttu-id="6eed8-115"><dt>Wxutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6eed8-115"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="6eed8-116">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6eed8-116">Library</span></span><br/> | <dl> <span data-ttu-id="6eed8-117"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="6eed8-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




