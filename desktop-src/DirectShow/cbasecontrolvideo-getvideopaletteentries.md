---
description: O método GetVideoPaletteEntries recupera um intervalo de entradas de paleta para o vídeo.
ms.assetid: 7ac12e28-daa7-4d6c-9983-401971e6704d
title: Método CBaseControlVideo. GetVideoPaletteEntries (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetVideoPaletteEntries
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6fa354922e57436c0d9e3e18924dcf31afe1629e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759452"
---
# <a name="cbasecontrolvideogetvideopaletteentries-method"></a><span data-ttu-id="c80b2-103">Método CBaseControlVideo. GetVideoPaletteEntries</span><span class="sxs-lookup"><span data-stu-id="c80b2-103">CBaseControlVideo.GetVideoPaletteEntries method</span></span>

<span data-ttu-id="c80b2-104">O `GetVideoPaletteEntries` método recupera um intervalo de entradas de paleta para o vídeo.</span><span class="sxs-lookup"><span data-stu-id="c80b2-104">The `GetVideoPaletteEntries` method retrieves a range of palette entries for the video.</span></span>

## <a name="syntax"></a><span data-ttu-id="c80b2-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c80b2-105">Syntax</span></span>


```C++
HRESULT GetVideoPaletteEntries(
   long StartIndex,
   long Entries,
   long *pRetrieved,
   long *pPalette
);
```



## <a name="parameters"></a><span data-ttu-id="c80b2-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c80b2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c80b2-107">*StartIndex*</span><span class="sxs-lookup"><span data-stu-id="c80b2-107">*StartIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="c80b2-108">Entrada da paleta inicial com base em zero.</span><span class="sxs-lookup"><span data-stu-id="c80b2-108">Zero-based start palette entry.</span></span>

</dd> <dt>

<span data-ttu-id="c80b2-109">*Entradas*</span><span class="sxs-lookup"><span data-stu-id="c80b2-109">*Entries*</span></span> 
</dt> <dd>

<span data-ttu-id="c80b2-110">Número de entradas necessárias.</span><span class="sxs-lookup"><span data-stu-id="c80b2-110">Number of entries required.</span></span>

</dd> <dt>

<span data-ttu-id="c80b2-111">*pRetrieved*</span><span class="sxs-lookup"><span data-stu-id="c80b2-111">*pRetrieved*</span></span> 
</dt> <dd>

<span data-ttu-id="c80b2-112">Ponteiro para o número de cores obtidas.</span><span class="sxs-lookup"><span data-stu-id="c80b2-112">Pointer to the number of colors obtained.</span></span>

</dd> <dt>

<span data-ttu-id="c80b2-113">*pPalette*</span><span class="sxs-lookup"><span data-stu-id="c80b2-113">*pPalette*</span></span> 
</dt> <dd>

<span data-ttu-id="c80b2-114">Ponteiro para o buffer de saída para cores.</span><span class="sxs-lookup"><span data-stu-id="c80b2-114">Pointer to output buffer for colors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c80b2-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c80b2-115">Return value</span></span>

<span data-ttu-id="c80b2-116">Retorna NOERROR se for bem-sucedido, VFW \_ E \_ nenhuma \_ paleta \_ disponível se os exemplos de vídeo não tiverem paleta de cores, e \_ OUTOFMEMORY se não houver memória suficiente disponível, e \_ INVALIDARG se *startIndex* for inválido ou S false se não houver \_ nenhuma cor na paleta.</span><span class="sxs-lookup"><span data-stu-id="c80b2-116">Returns NOERROR if successful, VFW\_E\_NO\_PALETTE\_AVAILABLE if the video samples has no color palette, E\_OUTOFMEMORY if there is not enough memory available, E\_INVALIDARG if *StartIndex* is invalid, or S\_FALSE if there are no colors in the palette.</span></span>

## <a name="remarks"></a><span data-ttu-id="c80b2-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="c80b2-117">Remarks</span></span>

<span data-ttu-id="c80b2-118">Essa função de membro retorna a paleta atual do vídeo como uma matriz alocada pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="c80b2-118">This member function returns the current palette of the video as an array allocated by the user.</span></span> <span data-ttu-id="c80b2-119">Para permanecer consistente, use os membros na estrutura **PaletteEntry** do Win32 para retornar as cores, em vez dos membros na estrutura **RGBQUAD** (embora o parâmetro seja um **longo**).</span><span class="sxs-lookup"><span data-stu-id="c80b2-119">To remain consistent, use the members in the Win32 **PALETTEENTRY** structure to return the colors, rather than the members in the **RGBQUAD** structure (although the parameter is a **LONG**).</span></span> <span data-ttu-id="c80b2-120">A memória é alocada pelo chamador, portanto, basta copiar cada uma delas por vez.</span><span class="sxs-lookup"><span data-stu-id="c80b2-120">The memory is allocated by the caller, so simply copy each in turn.</span></span> <span data-ttu-id="c80b2-121">Determine se o número de entradas solicitadas e o deslocamento da posição inicial são válidos.</span><span class="sxs-lookup"><span data-stu-id="c80b2-121">Determine that the number of entries requested and the start position offset are both valid.</span></span> <span data-ttu-id="c80b2-122">Se o número de entradas for avaliado como zero, retorna um \_ código S falso.</span><span class="sxs-lookup"><span data-stu-id="c80b2-122">If the number of entries evaluates to zero, return an S\_FALSE code.</span></span>

## <a name="requirements"></a><span data-ttu-id="c80b2-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c80b2-123">Requirements</span></span>



| <span data-ttu-id="c80b2-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="c80b2-124">Requirement</span></span> | <span data-ttu-id="c80b2-125">Valor</span><span class="sxs-lookup"><span data-stu-id="c80b2-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c80b2-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c80b2-126">Header</span></span><br/>  | <dl> <span data-ttu-id="c80b2-127"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c80b2-127"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c80b2-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c80b2-128">Library</span></span><br/> | <dl> <span data-ttu-id="c80b2-129"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="c80b2-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c80b2-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="c80b2-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c80b2-131">**Classe CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="c80b2-131">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




