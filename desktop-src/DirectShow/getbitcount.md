---
description: A função GetBitCount retorna o número de bits por pixel usado por um subtipo de vídeo especificado. Esta função é válida somente para subtipos RGB não compactados.
ms.assetid: 876b91c8-50ba-4217-b79c-7f7ec1c22b83
title: Função GetBitCount (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetBitCount
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6fed9b24ebf2e95b2408de30a407904e6bd3c1c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789950"
---
# <a name="getbitcount-function"></a><span data-ttu-id="77f49-104">Função GetBitCount</span><span class="sxs-lookup"><span data-stu-id="77f49-104">GetBitCount function</span></span>

<span data-ttu-id="77f49-105">A `GetBitCount` função retorna o número de bits por pixel usado por um subtipo de vídeo especificado.</span><span class="sxs-lookup"><span data-stu-id="77f49-105">The `GetBitCount` function returns the number of bits per pixel used by a specified video subtype.</span></span> <span data-ttu-id="77f49-106">Esta função é válida somente para subtipos RGB não compactados.</span><span class="sxs-lookup"><span data-stu-id="77f49-106">This function is valid for uncompressed RGB subtypes only.</span></span>

## <a name="syntax"></a><span data-ttu-id="77f49-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="77f49-107">Syntax</span></span>


```C++
WORD GetBitCount(
   const GUID *pSubtype
);
```



## <a name="parameters"></a><span data-ttu-id="77f49-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="77f49-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77f49-109">*pSubtype*</span><span class="sxs-lookup"><span data-stu-id="77f49-109">*pSubtype*</span></span> 
</dt> <dd>

<span data-ttu-id="77f49-110">Ponteiro para um **GUID** de subtipo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="77f49-110">Pointer to a video subtype **GUID**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77f49-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="77f49-111">Return value</span></span>

<span data-ttu-id="77f49-112">Retorna o número de bits por pixel para esse subtipo ou o valor **USHRT \_ Max** se o subtipo não for reconhecido.</span><span class="sxs-lookup"><span data-stu-id="77f49-112">Returns the number of bits per pixel for this subtype, or the value **USHRT\_MAX** if the subtype is not recognized.</span></span>

## <a name="requirements"></a><span data-ttu-id="77f49-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="77f49-113">Requirements</span></span>



| <span data-ttu-id="77f49-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="77f49-114">Requirement</span></span> | <span data-ttu-id="77f49-115">Valor</span><span class="sxs-lookup"><span data-stu-id="77f49-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77f49-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="77f49-116">Header</span></span><br/>  | <dl> <span data-ttu-id="77f49-117"><dt>Wxutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="77f49-117"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="77f49-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="77f49-118">Library</span></span><br/> | <dl> <span data-ttu-id="77f49-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="77f49-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77f49-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="77f49-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77f49-121">Funções de vídeo e imagem</span><span class="sxs-lookup"><span data-stu-id="77f49-121">Video and Image Functions</span></span>](video-and-image-functions.md)
</dt> </dl>

 

 




