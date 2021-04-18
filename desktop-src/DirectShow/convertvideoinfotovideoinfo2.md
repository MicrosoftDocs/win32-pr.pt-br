---
description: A função ConvertVideoInfoToVideoInfo2 converte um tipo de mídia que usa VIDEOINFOHEADER para um que usa VIDEOINFOHEADER2.
ms.assetid: d938bfc0-a5ae-475b-b183-56ff39b4bae1
title: Função ConvertVideoInfoToVideoInfo2 (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConvertVideoInfoToVideoInfo2
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 54611c83c30ad65a806a077dc51c933a9f881636
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105778495"
---
# <a name="convertvideoinfotovideoinfo2-function"></a><span data-ttu-id="f34e4-103">Função ConvertVideoInfoToVideoInfo2</span><span class="sxs-lookup"><span data-stu-id="f34e4-103">ConvertVideoInfoToVideoInfo2 function</span></span>

<span data-ttu-id="f34e4-104">A `ConvertVideoInfoToVideoInfo2` função converte um tipo de mídia que usa [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) para um que usa [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2).</span><span class="sxs-lookup"><span data-stu-id="f34e4-104">The `ConvertVideoInfoToVideoInfo2` function converts a media type that uses [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) to one that uses [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2).</span></span>

## <a name="syntax"></a><span data-ttu-id="f34e4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f34e4-105">Syntax</span></span>


```C++
HRESULT STDAPI ConvertVideoInfoToVideoInfo2(
   AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="f34e4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f34e4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f34e4-107">*PMT*</span><span class="sxs-lookup"><span data-stu-id="f34e4-107">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="f34e4-108">Ponteiro para a estrutura do [**\_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) a ser convertida.</span><span class="sxs-lookup"><span data-stu-id="f34e4-108">Pointer to the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure to convert.</span></span> <span data-ttu-id="f34e4-109">A estrutura deve ter formato de tipo de formato \_ VideoInfo.</span><span class="sxs-lookup"><span data-stu-id="f34e4-109">The structure must have format type FORMAT\_VideoInfo.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f34e4-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f34e4-110">Return value</span></span>

<span data-ttu-id="f34e4-111">Retorna S \_ OK ou E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="f34e4-111">Returns S\_OK or E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="f34e4-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="f34e4-112">Remarks</span></span>

<span data-ttu-id="f34e4-113">Essa função aloca uma nova estrutura **VIDEOINFOHEADER2** , copia os membros da estrutura **VIDEOINFOHEADER** nela e substitui a estrutura antiga pela nova estrutura no bloco de formato do tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="f34e4-113">This function allocates a new **VIDEOINFOHEADER2** structure, copies the members of the **VIDEOINFOHEADER** structure into it, and replaces the old structure with the new structure in the format block of the media type.</span></span>

## <a name="requirements"></a><span data-ttu-id="f34e4-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f34e4-114">Requirements</span></span>



| <span data-ttu-id="f34e4-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="f34e4-115">Requirement</span></span> | <span data-ttu-id="f34e4-116">Valor</span><span class="sxs-lookup"><span data-stu-id="f34e4-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f34e4-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f34e4-117">Header</span></span><br/>  | <dl> <span data-ttu-id="f34e4-118"><dt>Winutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f34e4-118"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f34e4-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f34e4-119">Library</span></span><br/> | <dl> <span data-ttu-id="f34e4-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="f34e4-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f34e4-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="f34e4-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f34e4-122">Funções de vídeo e imagem</span><span class="sxs-lookup"><span data-stu-id="f34e4-122">Video and Image Functions</span></span>](video-and-image-functions.md)
</dt> </dl>

 

 




