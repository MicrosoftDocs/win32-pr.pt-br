---
description: O método MakePalette cria uma paleta lógica da tabela de cores em um formato de vídeo.
ms.assetid: f158e529-d683-4210-818d-21a834fc7683
title: Método CImagePalette. MakePalette (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette.MakePalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 20c4484b2666b25b5d713ede450a9a5a99f93348
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789712"
---
# <a name="cimagepalettemakepalette-method"></a><span data-ttu-id="118ad-103">Método CImagePalette. MakePalette</span><span class="sxs-lookup"><span data-stu-id="118ad-103">CImagePalette.MakePalette method</span></span>

<span data-ttu-id="118ad-104">O `MakePalette` método cria uma paleta lógica da tabela de cores em um formato de vídeo.</span><span class="sxs-lookup"><span data-stu-id="118ad-104">The `MakePalette` method creates a logical palette from the color table in a video format.</span></span>

## <a name="syntax"></a><span data-ttu-id="118ad-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="118ad-105">Syntax</span></span>


```C++
HPALETTE MakePalette(
   const VIDEOINFOHEADER *pVideoInfo,
         LPSTR           szDevice
);
```



## <a name="parameters"></a><span data-ttu-id="118ad-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="118ad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="118ad-107">*pVideoInfo*</span><span class="sxs-lookup"><span data-stu-id="118ad-107">*pVideoInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="118ad-108">Ponteiro para uma estrutura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) que contém a tabela de cores.</span><span class="sxs-lookup"><span data-stu-id="118ad-108">Pointer to a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure that contains the color table.</span></span>

</dd> <dt>

<span data-ttu-id="118ad-109">*szDevice*</span><span class="sxs-lookup"><span data-stu-id="118ad-109">*szDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="118ad-110">Ponteiro para uma cadeia de caracteres que contém o nome do dispositivo de vídeo, conforme retornado pela função **EnumDisplayDevices** do GDI.</span><span class="sxs-lookup"><span data-stu-id="118ad-110">Pointer to a string that contains the name of the display device, as returned by the GDI **EnumDisplayDevices** function.</span></span> <span data-ttu-id="118ad-111">Para usar o dispositivo de vídeo principal, defina esse parâmetro como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="118ad-111">To use the main display device, set this parameter to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="118ad-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="118ad-112">Return value</span></span>

<span data-ttu-id="118ad-113">Se for bem-sucedido, retorna um identificador para a paleta.</span><span class="sxs-lookup"><span data-stu-id="118ad-113">If successful, returns a handle to the palette.</span></span> <span data-ttu-id="118ad-114">Caso contrário, retornará **NULL**.</span><span class="sxs-lookup"><span data-stu-id="118ad-114">Otherwise, returns **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="118ad-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="118ad-115">Requirements</span></span>



| <span data-ttu-id="118ad-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="118ad-116">Requirement</span></span> | <span data-ttu-id="118ad-117">Valor</span><span class="sxs-lookup"><span data-stu-id="118ad-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="118ad-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="118ad-118">Header</span></span><br/>  | <dl> <span data-ttu-id="118ad-119"><dt>Winutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="118ad-119"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="118ad-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="118ad-120">Library</span></span><br/> | <dl> <span data-ttu-id="118ad-121"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="118ad-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="118ad-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="118ad-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="118ad-123">**Classe CImagePalette**</span><span class="sxs-lookup"><span data-stu-id="118ad-123">**CImagePalette Class**</span></span>](cimagepalette.md)
</dt> </dl>

 

 




