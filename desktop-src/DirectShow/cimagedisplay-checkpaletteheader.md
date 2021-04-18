---
description: O método CheckPaletteHeader valida as entradas da paleta em uma estrutura VIDEOINFO.
ms.assetid: bc18cbe6-0446-43a6-a50c-e587815b789d
title: Método CImageDisplay. CheckPaletteHeader (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.CheckPaletteHeader
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 54c4f401d2e75aeb35ffc19d26690fa04a769c27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105778503"
---
# <a name="cimagedisplaycheckpaletteheader-method"></a><span data-ttu-id="c4568-103">Método CImageDisplay. CheckPaletteHeader</span><span class="sxs-lookup"><span data-stu-id="c4568-103">CImageDisplay.CheckPaletteHeader method</span></span>

<span data-ttu-id="c4568-104">O `CheckPaletteHeader` método valida as entradas da paleta em uma estrutura [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) .</span><span class="sxs-lookup"><span data-stu-id="c4568-104">The `CheckPaletteHeader` method validates the palette entries in a [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4568-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c4568-105">Syntax</span></span>


```C++
BOOL CheckPaletteHeader(
   const VIDEOINFO *pInput
);
```



## <a name="parameters"></a><span data-ttu-id="c4568-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c4568-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4568-107">*pInput*</span><span class="sxs-lookup"><span data-stu-id="c4568-107">*pInput*</span></span> 
</dt> <dd>

<span data-ttu-id="c4568-108">Ponteiro para uma estrutura **VIDEOINFO** .</span><span class="sxs-lookup"><span data-stu-id="c4568-108">Pointer to a **VIDEOINFO** structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4568-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c4568-109">Return value</span></span>

<span data-ttu-id="c4568-110">Retornará **true** se as entradas da paleta forem válidas ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="c4568-110">Returns **TRUE** if the palette entries are valid, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="c4568-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="c4568-111">Remarks</span></span>

<span data-ttu-id="c4568-112">Se o formato de imagem não for palettized, o método verificará se **biClrUsed** é igual a zero.</span><span class="sxs-lookup"><span data-stu-id="c4568-112">If the image format is not palettized, the method verifies that **biClrUsed** equals zero.</span></span> <span data-ttu-id="c4568-113">Caso contrário, o método verifica se o sinalizador de **bicompressão** é bi \_ RGB; **biClrImportant** não é maior que **biClrUsed**; e o número de entradas da paleta não excede o máximo, considerando a intensidade de cor.</span><span class="sxs-lookup"><span data-stu-id="c4568-113">Otherwise, the method verifies that the **biCompression** flag is BI\_RGB; **biClrImportant** is not greater than **biClrUsed**; and the number of palette entries does not exceed the maximum, given the color depth.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4568-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c4568-114">Requirements</span></span>



| <span data-ttu-id="c4568-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4568-115">Requirement</span></span> | <span data-ttu-id="c4568-116">Valor</span><span class="sxs-lookup"><span data-stu-id="c4568-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4568-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c4568-117">Header</span></span><br/>  | <dl> <span data-ttu-id="c4568-118"><dt>Winutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c4568-118"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c4568-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c4568-119">Library</span></span><br/> | <dl> <span data-ttu-id="c4568-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="c4568-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4568-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="c4568-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4568-122">**Classe CImageDisplay**</span><span class="sxs-lookup"><span data-stu-id="c4568-122">**CImageDisplay Class**</span></span>](cimagedisplay.md)
</dt> </dl>

 

 




