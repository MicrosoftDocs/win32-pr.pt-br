---
description: O método CheckHeaderValidity valida uma estrutura BITMAPINFOHEADER. Esse método é útil apenas para tipos RGB não compactados, não para tipos não compactados ou tipos YUV.
ms.assetid: 24b547b6-b730-48b2-9a1b-6e77f9cb1ce1
title: Método CImageDisplay. CheckHeaderValidity (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.CheckHeaderValidity
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 803e8cd1a70c68f3e20c320978e9a350bdf23bdb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105770098"
---
# <a name="cimagedisplaycheckheadervalidity-method"></a><span data-ttu-id="a7c1f-104">Método CImageDisplay. CheckHeaderValidity</span><span class="sxs-lookup"><span data-stu-id="a7c1f-104">CImageDisplay.CheckHeaderValidity method</span></span>

<span data-ttu-id="a7c1f-105">O `CheckHeaderValidity` método valida uma estrutura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) .</span><span class="sxs-lookup"><span data-stu-id="a7c1f-105">The `CheckHeaderValidity` method validates a [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure.</span></span> <span data-ttu-id="a7c1f-106">Esse método é útil apenas para tipos RGB não compactados, não para tipos não compactados ou tipos YUV.</span><span class="sxs-lookup"><span data-stu-id="a7c1f-106">This method is useful only for uncompressed RGB types, not for compressed types or YUV types.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7c1f-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a7c1f-107">Syntax</span></span>


```C++
BOOL CheckHeaderValidity(
   const VIDEOINFO *pInput
);
```



## <a name="parameters"></a><span data-ttu-id="a7c1f-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a7c1f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7c1f-109">*pInput*</span><span class="sxs-lookup"><span data-stu-id="a7c1f-109">*pInput*</span></span> 
</dt> <dd>

<span data-ttu-id="a7c1f-110">Ponteiro para uma estrutura [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) que contém a estrutura **BITMAPINFOHEADER** .</span><span class="sxs-lookup"><span data-stu-id="a7c1f-110">Pointer to a [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) structure containing the **BITMAPINFOHEADER** structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7c1f-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a7c1f-111">Return value</span></span>

<span data-ttu-id="a7c1f-112">Retornará **true** se **BITMAPINFOHEADER** for válido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="a7c1f-112">Returns **TRUE** if the **BITMAPINFOHEADER** is valid, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="a7c1f-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="a7c1f-113">Remarks</span></span>

<span data-ttu-id="a7c1f-114">Esse método verifica se as dimensões da imagem são não negativas; o tipo de compactação é BI \_ RGB ou bi \_ BITFIELDS; a profundidade de cor e as máscaras de cor são válidas; o membro **Biplans** é igual a um; e os membros **biSize** e **biSizeImage** estão corretos.</span><span class="sxs-lookup"><span data-stu-id="a7c1f-114">This method checks that the image dimensions are non-negative; the compression type is BI\_RGB or BI\_BITFIELDS; the color depth and color masks are valid; the **biPlanes** member equals one; and the **biSize** and **biSizeImage** members are correct.</span></span> <span data-ttu-id="a7c1f-115">Ele também verifica erros comuns nas entradas da paleta, se houver.</span><span class="sxs-lookup"><span data-stu-id="a7c1f-115">It also checks for common errors in the palette entries, if any.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7c1f-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a7c1f-116">Requirements</span></span>



| <span data-ttu-id="a7c1f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="a7c1f-117">Requirement</span></span> | <span data-ttu-id="a7c1f-118">Valor</span><span class="sxs-lookup"><span data-stu-id="a7c1f-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7c1f-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a7c1f-119">Header</span></span><br/>  | <dl> <span data-ttu-id="a7c1f-120"><dt>Winutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a7c1f-120"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a7c1f-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a7c1f-121">Library</span></span><br/> | <dl> <span data-ttu-id="a7c1f-122"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="a7c1f-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7c1f-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="a7c1f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7c1f-124">**Classe CImageDisplay**</span><span class="sxs-lookup"><span data-stu-id="a7c1f-124">**CImageDisplay Class**</span></span>](cimagedisplay.md)
</dt> </dl>

 

 




