---
description: O método PreparePalette configura uma paleta, com base em um tipo de mídia do filtro proprietário.
ms.assetid: cb012391-39ab-4ad1-aeb7-ec25010ac64a
title: Método CImagePalette. PreparePalette (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette.PreparePalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a9b09804b2ee6ad9fbda394a7fb8f9f188b46453
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758855"
---
# <a name="cimagepalettepreparepalette-method"></a><span data-ttu-id="cabd5-103">Método CImagePalette. PreparePalette</span><span class="sxs-lookup"><span data-stu-id="cabd5-103">CImagePalette.PreparePalette method</span></span>

<span data-ttu-id="cabd5-104">O `PreparePalette` método configura uma paleta, com base em um tipo de mídia do filtro proprietário.</span><span class="sxs-lookup"><span data-stu-id="cabd5-104">The `PreparePalette` method sets up a palette, based on a media type from the owning filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="cabd5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cabd5-105">Syntax</span></span>


```C++
HRESULT PreparePalette(
   const CMediaType *pmtNew,
   const CMediaType *pmtOld,
         LPSTR      szDevice
);
```



## <a name="parameters"></a><span data-ttu-id="cabd5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cabd5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cabd5-107">*pmtNew*</span><span class="sxs-lookup"><span data-stu-id="cabd5-107">*pmtNew*</span></span> 
</dt> <dd>

<span data-ttu-id="cabd5-108">Ponteiro para o novo tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="cabd5-108">Pointer to the new media type.</span></span> <span data-ttu-id="cabd5-109">O bloco de formato deve ser uma estrutura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) .</span><span class="sxs-lookup"><span data-stu-id="cabd5-109">The format block must be a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure.</span></span>

</dd> <dt>

<span data-ttu-id="cabd5-110">*pmtOld*</span><span class="sxs-lookup"><span data-stu-id="cabd5-110">*pmtOld*</span></span> 
</dt> <dd>

<span data-ttu-id="cabd5-111">Ponteiro para o tipo de mídia antigo.</span><span class="sxs-lookup"><span data-stu-id="cabd5-111">Pointer to the old media type.</span></span> <span data-ttu-id="cabd5-112">Se o tipo de mídia estiver sendo definido pela primeira vez, esse parâmetro poderá ser um tipo vazio sem nenhum bloco de formato.</span><span class="sxs-lookup"><span data-stu-id="cabd5-112">If the media type is being set for the first time, this parameter can be an empty type with no format block.</span></span> <span data-ttu-id="cabd5-113">Caso contrário, o bloco de formato deve ser uma estrutura **VIDEOINFOHEADER** .</span><span class="sxs-lookup"><span data-stu-id="cabd5-113">Otherwise, the format block must be a **VIDEOINFOHEADER** structure.</span></span>

</dd> <dt>

<span data-ttu-id="cabd5-114">*szDevice*</span><span class="sxs-lookup"><span data-stu-id="cabd5-114">*szDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="cabd5-115">Ponteiro para uma cadeia de caracteres que contém o nome do dispositivo de vídeo, conforme retornado pela função **EnumDisplayDevices** do GDI.</span><span class="sxs-lookup"><span data-stu-id="cabd5-115">Pointer to a string that contains the name of the display device, as returned by the GDI **EnumDisplayDevices** function.</span></span> <span data-ttu-id="cabd5-116">Para usar o dispositivo de vídeo principal, defina esse parâmetro como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="cabd5-116">To use the main display device, set this parameter to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cabd5-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cabd5-117">Return value</span></span>

<span data-ttu-id="cabd5-118">Retornará S \_ OK se a paleta tiver sido atualizada ou S \_ false se a paleta não foi alterada.</span><span class="sxs-lookup"><span data-stu-id="cabd5-118">Returns S\_OK if the palette was updated, or S\_FALSE if the palette did not change.</span></span>

## <a name="remarks"></a><span data-ttu-id="cabd5-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="cabd5-119">Remarks</span></span>

<span data-ttu-id="cabd5-120">Se a paleta precisar ser atualizada, esse método executará as seguintes ações:</span><span class="sxs-lookup"><span data-stu-id="cabd5-120">If the palette needs to be updated, this method performs the following actions:</span></span>

-   <span data-ttu-id="cabd5-121">Chama [**CImagePalette:: MakePalette**](cimagepalette-makepalette.md) para criar uma nova paleta lógica.</span><span class="sxs-lookup"><span data-stu-id="cabd5-121">Calls [**CImagePalette::MakePalette**](cimagepalette-makepalette.md) to create a new logical palette.</span></span>
-   <span data-ttu-id="cabd5-122">Envia um evento de [**\_ \_ alteração de paleta do EC**](ec-palette-changed.md) para o Gerenciador do grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="cabd5-122">Sends an [**EC\_PALETTE\_CHANGED**](ec-palette-changed.md) event to the Filter Graph Manager.</span></span>
-   <span data-ttu-id="cabd5-123">Chama [**CBaseWindow:: SetPalette**](cbasewindow-setpalette.md) no objeto **CBaseWindow** .</span><span class="sxs-lookup"><span data-stu-id="cabd5-123">Calls [**CBaseWindow::SetPalette**](cbasewindow-setpalette.md) on the **CBaseWindow** object.</span></span>
-   <span data-ttu-id="cabd5-124">Chama [**CDrawImage:: IncrementPaletteVersion**](cdrawimage-incrementpaletteversion.md) no objeto **CDrawImage** .</span><span class="sxs-lookup"><span data-stu-id="cabd5-124">Calls [**CDrawImage::IncrementPaletteVersion**](cdrawimage-incrementpaletteversion.md) on the **CDrawImage** object.</span></span>

## <a name="requirements"></a><span data-ttu-id="cabd5-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cabd5-125">Requirements</span></span>



| <span data-ttu-id="cabd5-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="cabd5-126">Requirement</span></span> | <span data-ttu-id="cabd5-127">Valor</span><span class="sxs-lookup"><span data-stu-id="cabd5-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cabd5-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cabd5-128">Header</span></span><br/>  | <dl> <span data-ttu-id="cabd5-129"><dt>Winutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cabd5-129"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="cabd5-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cabd5-130">Library</span></span><br/> | <dl> <span data-ttu-id="cabd5-131"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="cabd5-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cabd5-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="cabd5-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cabd5-133">**Classe CImagePalette**</span><span class="sxs-lookup"><span data-stu-id="cabd5-133">**CImagePalette Class**</span></span>](cimagepalette.md)
</dt> </dl>

 

 




