---
description: A classe CImageDisplay é uma classe auxiliar para renderizadores de vídeo GDI gerenciar o formato de exibição.
ms.assetid: c9221e5c-30c6-489a-89d7-132203314dc8
title: Classe CImageDisplay (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a5a7cbb28c53d8ff357d4e5174d24f92ba2d0cad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760769"
---
# <a name="cimagedisplay-class"></a><span data-ttu-id="e9241-103">Classe CImageDisplay</span><span class="sxs-lookup"><span data-stu-id="e9241-103">CImageDisplay class</span></span>

![cimagedisplayclasshierarchy](images/wutil06.png)

<span data-ttu-id="e9241-105">A `CImageDisplay` classe é uma classe auxiliar para renderizadores de vídeo GDI gerenciar o formato de exibição.</span><span class="sxs-lookup"><span data-stu-id="e9241-105">The `CImageDisplay` class is a helper class for GDI video renderers to manage the display format.</span></span> <span data-ttu-id="e9241-106">O objeto armazena uma estrutura [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) que descreve o modo de exibição atual, que é inicializado no método de construtor do objeto.</span><span class="sxs-lookup"><span data-stu-id="e9241-106">The object stores a [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) structure that describes the current display mode, which is initialized in the object's constructor method.</span></span> <span data-ttu-id="e9241-107">O método **CheckMediaType** do objeto verifica se um tipo de mídia proposto pode ser renderizado com eficiência usando GDI.</span><span class="sxs-lookup"><span data-stu-id="e9241-107">The object's **CheckMediaType** method checks whether a proposed media type can be rendered efficiently using GDI.</span></span>



| <span data-ttu-id="e9241-108">Variáveis de membro protegido</span><span class="sxs-lookup"><span data-stu-id="e9241-108">Protected Member Variables</span></span>                                       | <span data-ttu-id="e9241-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="e9241-109">Description</span></span>                                                                            |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [<span data-ttu-id="e9241-110">**\_exibição m**</span><span class="sxs-lookup"><span data-stu-id="e9241-110">**m\_Display**</span></span>](cimagedisplay-m-display.md)                    | <span data-ttu-id="e9241-111">Estrutura **VIDEOINFO** que descreve o formato de exibição atual.</span><span class="sxs-lookup"><span data-stu-id="e9241-111">**VIDEOINFO** structure that describes the current display format.</span></span>                     |
| <span data-ttu-id="e9241-112">Métodos Protegidos</span><span class="sxs-lookup"><span data-stu-id="e9241-112">Protected Methods</span></span>                                                | <span data-ttu-id="e9241-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="e9241-113">Description</span></span>                                                                            |
| [<span data-ttu-id="e9241-114">**CheckBitFields**</span><span class="sxs-lookup"><span data-stu-id="e9241-114">**CheckBitFields**</span></span>](cimagedisplay-checkbitfields.md)           | <span data-ttu-id="e9241-115">Valida as máscaras de cores em uma estrutura **VIDEOINFO** .</span><span class="sxs-lookup"><span data-stu-id="e9241-115">Validates the color masks in a **VIDEOINFO** structure.</span></span>                                |
| [<span data-ttu-id="e9241-116">**CountPrefixBits**</span><span class="sxs-lookup"><span data-stu-id="e9241-116">**CountPrefixBits**</span></span>](cimagedisplay-countprefixbits.md)         | <span data-ttu-id="e9241-117">Calcula o número de zero bits no início de um campo de bits especificado.</span><span class="sxs-lookup"><span data-stu-id="e9241-117">Calculates the number of zero bits at the start of a specified bit field.</span></span>              |
| [<span data-ttu-id="e9241-118">**CountSetBits**</span><span class="sxs-lookup"><span data-stu-id="e9241-118">**CountSetBits**</span></span>](cimagedisplay-countsetbits.md)               | <span data-ttu-id="e9241-119">Retorna o número de bits definido como 1 em um campo de bit especificado.</span><span class="sxs-lookup"><span data-stu-id="e9241-119">Returns the number of bits set to 1 in a specified bit field.</span></span>                          |
| <span data-ttu-id="e9241-120">Métodos públicos</span><span class="sxs-lookup"><span data-stu-id="e9241-120">Public Methods</span></span>                                                   | <span data-ttu-id="e9241-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="e9241-121">Description</span></span>                                                                            |
| [<span data-ttu-id="e9241-122">**CheckHeaderValidity**</span><span class="sxs-lookup"><span data-stu-id="e9241-122">**CheckHeaderValidity**</span></span>](cimagedisplay-checkheadervalidity.md) | <span data-ttu-id="e9241-123">Valida uma estrutura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) .</span><span class="sxs-lookup"><span data-stu-id="e9241-123">Validates a [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure.</span></span>                    |
| [<span data-ttu-id="e9241-124">**CheckMediaType**</span><span class="sxs-lookup"><span data-stu-id="e9241-124">**CheckMediaType**</span></span>](cimagedisplay-checkmediatype.md)           | <span data-ttu-id="e9241-125">Determina se um tipo de mídia proposto é compatível com o formato de exibição.</span><span class="sxs-lookup"><span data-stu-id="e9241-125">Determines whether a proposed media type is compatible with the display format.</span></span>        |
| [<span data-ttu-id="e9241-126">**CheckPaletteHeader**</span><span class="sxs-lookup"><span data-stu-id="e9241-126">**CheckPaletteHeader**</span></span>](cimagedisplay-checkpaletteheader.md)   | <span data-ttu-id="e9241-127">Valida as entradas da paleta em uma estrutura **VIDEOINFO** .</span><span class="sxs-lookup"><span data-stu-id="e9241-127">Validates the palette entries in a **VIDEOINFO** structure.</span></span>                            |
| [<span data-ttu-id="e9241-128">**CheckVideoType**</span><span class="sxs-lookup"><span data-stu-id="e9241-128">**CheckVideoType**</span></span>](cimagedisplay-checkvideotype.md)           | <span data-ttu-id="e9241-129">Verifica se um formato **VIDEOINFO** especificado é compatível com o formato de exibição.</span><span class="sxs-lookup"><span data-stu-id="e9241-129">Checks whether a specified **VIDEOINFO** format is compatible with the display format.</span></span> |
| [<span data-ttu-id="e9241-130">**CImageDisplay**</span><span class="sxs-lookup"><span data-stu-id="e9241-130">**CImageDisplay**</span></span>](cimagedisplay-cimagedisplay.md)             | <span data-ttu-id="e9241-131">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="e9241-131">Constructor method.</span></span>                                                                    |
| [<span data-ttu-id="e9241-132">**Getbitmasks**</span><span class="sxs-lookup"><span data-stu-id="e9241-132">**GetBitMasks**</span></span>](cimagedisplay-getbitmasks.md)                 | <span data-ttu-id="e9241-133">Recupera as máscaras de cores para um formato **VIDEOINFO** especificado.</span><span class="sxs-lookup"><span data-stu-id="e9241-133">Retrieves the color masks for a specified **VIDEOINFO** format.</span></span>                        |
| [<span data-ttu-id="e9241-134">**GetColourMask**</span><span class="sxs-lookup"><span data-stu-id="e9241-134">**GetColourMask**</span></span>](cimagedisplay-getcolourmask.md)             | <span data-ttu-id="e9241-135">Recupera as máscaras de cores para o formato de exibição atual.</span><span class="sxs-lookup"><span data-stu-id="e9241-135">Retrieves the color masks for the current display format.</span></span>                              |
| [<span data-ttu-id="e9241-136">**GetDisplayDepth**</span><span class="sxs-lookup"><span data-stu-id="e9241-136">**GetDisplayDepth**</span></span>](cimagedisplay-getdisplaydepth.md)         | <span data-ttu-id="e9241-137">Recupera a profundidade de bits do modo de exibição atual.</span><span class="sxs-lookup"><span data-stu-id="e9241-137">Retrieves the bit depth of the current display mode.</span></span>                                   |
| [<span data-ttu-id="e9241-138">**GetDisplayFormat**</span><span class="sxs-lookup"><span data-stu-id="e9241-138">**GetDisplayFormat**</span></span>](cimagedisplay-getdisplayformat.md)       | <span data-ttu-id="e9241-139">Recupera um formato de vídeo que descreve o modo de exibição atual.</span><span class="sxs-lookup"><span data-stu-id="e9241-139">Retrieves a video format that describes the current display mode.</span></span>                      |
| [<span data-ttu-id="e9241-140">**IsPalettised**</span><span class="sxs-lookup"><span data-stu-id="e9241-140">**IsPalettised**</span></span>](cimagedisplay-ispalettised.md)               | <span data-ttu-id="e9241-141">Retermines se o formato de exibição atual é palettized.</span><span class="sxs-lookup"><span data-stu-id="e9241-141">Retermines whether the current display format is palettized.</span></span>                           |
| [<span data-ttu-id="e9241-142">**RefreshDisplayType**</span><span class="sxs-lookup"><span data-stu-id="e9241-142">**RefreshDisplayType**</span></span>](cimagedisplay-refreshdisplaytype.md)   | <span data-ttu-id="e9241-143">Atualiza o formato de vídeo do objeto para corresponder à exibição especificada</span><span class="sxs-lookup"><span data-stu-id="e9241-143">Updates the object's video format to match the specified display</span></span>                       |



 

## <a name="requirements"></a><span data-ttu-id="e9241-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e9241-144">Requirements</span></span>



| <span data-ttu-id="e9241-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9241-145">Requirement</span></span> | <span data-ttu-id="e9241-146">Valor</span><span class="sxs-lookup"><span data-stu-id="e9241-146">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9241-147">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e9241-147">Header</span></span><br/>  | <dl> <span data-ttu-id="e9241-148"><dt>Winutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e9241-148"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e9241-149">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e9241-149">Library</span></span><br/> | <dl> <span data-ttu-id="e9241-150"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="e9241-150"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




