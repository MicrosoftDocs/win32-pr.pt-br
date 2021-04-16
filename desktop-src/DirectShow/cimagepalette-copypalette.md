---
description: O método CopyPalette copia a paleta de qualquer estrutura VIDEOINFO para qualquer estrutura palettized VIDEOINFO.
ms.assetid: ea06b40b-3f96-4c11-921c-52f3a44e0a30
title: Método CImagePalette. CopyPalette (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette.CopyPalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b429c5fd4d3d0e0e28cd0662fbee0a1ac926ddc5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754157"
---
# <a name="cimagepalettecopypalette-method"></a><span data-ttu-id="ccb9e-103">Método CImagePalette. CopyPalette</span><span class="sxs-lookup"><span data-stu-id="ccb9e-103">CImagePalette.CopyPalette method</span></span>

<span data-ttu-id="ccb9e-104">O `CopyPalette` método copia a paleta de qualquer estrutura [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) para qualquer estrutura **VIDEOINFO** palettized.</span><span class="sxs-lookup"><span data-stu-id="ccb9e-104">The `CopyPalette` method copies the palette from any [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) structure to any palettized **VIDEOINFO** structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="ccb9e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ccb9e-105">Syntax</span></span>


```C++
HRESULT CopyPalette(
   const CMediaType *pSrc,
   const CMediaType *pDest
);
```



## <a name="parameters"></a><span data-ttu-id="ccb9e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ccb9e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ccb9e-107">*pSrc*</span><span class="sxs-lookup"><span data-stu-id="ccb9e-107">*pSrc*</span></span> 
</dt> <dd>

<span data-ttu-id="ccb9e-108">Ponteiro para o tipo de mídia de origem.</span><span class="sxs-lookup"><span data-stu-id="ccb9e-108">Pointer to the source media type.</span></span>

</dd> <dt>

<span data-ttu-id="ccb9e-109">*pDest*</span><span class="sxs-lookup"><span data-stu-id="ccb9e-109">*pDest*</span></span> 
</dt> <dd>

<span data-ttu-id="ccb9e-110">Ponteiro para o tipo de mídia de destino.</span><span class="sxs-lookup"><span data-stu-id="ccb9e-110">Pointer to the destination media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ccb9e-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ccb9e-111">Return value</span></span>

<span data-ttu-id="ccb9e-112">Retornará S \_ OK se a paleta tiver sido copiada.</span><span class="sxs-lookup"><span data-stu-id="ccb9e-112">Returns S\_OK if the palette was copied.</span></span> <span data-ttu-id="ccb9e-113">Retornará S \_ false se o tipo de mídia de origem ou de destino não tiver uma paleta.</span><span class="sxs-lookup"><span data-stu-id="ccb9e-113">Returns S\_FALSE if either the source or destination media type does not have a palette.</span></span>

## <a name="remarks"></a><span data-ttu-id="ccb9e-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="ccb9e-114">Remarks</span></span>

<span data-ttu-id="ccb9e-115">O tipo de mídia *pDest* deve ser um formato palettized com uma intensidade de cor de 8 bits ou menos.</span><span class="sxs-lookup"><span data-stu-id="ccb9e-115">The *pDest* media type must be a palettized format with a color depth of 8 bits or less.</span></span> <span data-ttu-id="ccb9e-116">O tipo de mídia *pSrc* pode ser qualquer tipo de [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) com uma paleta, incluindo formatos YUV e true-color com entradas de paleta.</span><span class="sxs-lookup"><span data-stu-id="ccb9e-116">The *pSrc* media type can be any [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) type with a palette, including YUV and true-color formats with palette entries.</span></span> <span data-ttu-id="ccb9e-117">O método copia as entradas da paleta de *pSrc* em uma nova paleta e anexa a nova paleta a *pDest*.</span><span class="sxs-lookup"><span data-stu-id="ccb9e-117">The method copies the palette entries from *pSrc* into a new palette, and attaches the new palette to *pDest*.</span></span>

## <a name="requirements"></a><span data-ttu-id="ccb9e-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ccb9e-118">Requirements</span></span>



| <span data-ttu-id="ccb9e-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="ccb9e-119">Requirement</span></span> | <span data-ttu-id="ccb9e-120">Valor</span><span class="sxs-lookup"><span data-stu-id="ccb9e-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ccb9e-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ccb9e-121">Header</span></span><br/>  | <dl> <span data-ttu-id="ccb9e-122"><dt>Winutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ccb9e-122"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ccb9e-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ccb9e-123">Library</span></span><br/> | <dl> <span data-ttu-id="ccb9e-124"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="ccb9e-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ccb9e-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="ccb9e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ccb9e-126">**Classe CImagePalette**</span><span class="sxs-lookup"><span data-stu-id="ccb9e-126">**CImagePalette Class**</span></span>](cimagepalette.md)
</dt> </dl>

 

 




