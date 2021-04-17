---
description: O método CheckBitFields valida as máscaras de cores em uma estrutura VIDEOINFO.
ms.assetid: b03455aa-8d90-4fab-999d-7408d8417021
title: Método CImageDisplay. CheckBitFields (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.CheckBitFields
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ade581dad5e53c2454df52e387653e44d6d4ad2f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748199"
---
# <a name="cimagedisplaycheckbitfields-method"></a><span data-ttu-id="9cbcf-103">Método CImageDisplay. CheckBitFields</span><span class="sxs-lookup"><span data-stu-id="9cbcf-103">CImageDisplay.CheckBitFields method</span></span>

<span data-ttu-id="9cbcf-104">O `CheckBitFields` método valida as máscaras de cores em uma estrutura [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) .</span><span class="sxs-lookup"><span data-stu-id="9cbcf-104">The `CheckBitFields` method validates the color masks in a [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="9cbcf-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9cbcf-105">Syntax</span></span>


```C++
BOOL CheckBitFields(
   const VIDEOINFO *pInput
);
```



## <a name="parameters"></a><span data-ttu-id="9cbcf-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9cbcf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9cbcf-107">*pInput*</span><span class="sxs-lookup"><span data-stu-id="9cbcf-107">*pInput*</span></span> 
</dt> <dd>

<span data-ttu-id="9cbcf-108">Ponteiro para uma estrutura **VIDEOINFO** .</span><span class="sxs-lookup"><span data-stu-id="9cbcf-108">Pointer to a **VIDEOINFO** structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9cbcf-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9cbcf-109">Return value</span></span>

<span data-ttu-id="9cbcf-110">Retornará **true** se as máscaras de cor forem válidas ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="9cbcf-110">Returns **TRUE** if the color masks are valid, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="9cbcf-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="9cbcf-111">Remarks</span></span>

<span data-ttu-id="9cbcf-112">Esse método verifica se a máscara de cor de cada componente de cor está entre um e oito bits e se cada máscara de cor é uma sequência contígua de bits.</span><span class="sxs-lookup"><span data-stu-id="9cbcf-112">This method verifies that the color mask for each color component is between one and eight bits long, and that each color mask is a contiguous sequence of bits.</span></span> <span data-ttu-id="9cbcf-113">Chame esse método somente quando o membro **bicompressão** estiver definido como bi \_ BITFIELDS.</span><span class="sxs-lookup"><span data-stu-id="9cbcf-113">Call this method only when the **biCompression** member is set to BI\_BITFIELDS.</span></span>

## <a name="requirements"></a><span data-ttu-id="9cbcf-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9cbcf-114">Requirements</span></span>



| <span data-ttu-id="9cbcf-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="9cbcf-115">Requirement</span></span> | <span data-ttu-id="9cbcf-116">Valor</span><span class="sxs-lookup"><span data-stu-id="9cbcf-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9cbcf-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9cbcf-117">Header</span></span><br/>  | <dl> <span data-ttu-id="9cbcf-118"><dt>Winutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9cbcf-118"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="9cbcf-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9cbcf-119">Library</span></span><br/> | <dl> <span data-ttu-id="9cbcf-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="9cbcf-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9cbcf-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="9cbcf-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9cbcf-122">**Classe CImageDisplay**</span><span class="sxs-lookup"><span data-stu-id="9cbcf-122">**CImageDisplay Class**</span></span>](cimagedisplay.md)
</dt> </dl>

 

 




