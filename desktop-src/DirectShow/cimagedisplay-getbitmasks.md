---
description: O método getbitmasks recupera as máscaras de cores para um formato VIDEOINFO especificado.
ms.assetid: 72a9ba44-96de-4fff-a3fb-675d3dd080d8
title: Método CImageDisplay. getbitmasks (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.GetBitMasks
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a2defe5e80a0d7311adcd19dca67119019623993
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752086"
---
# <a name="cimagedisplaygetbitmasks-method"></a><span data-ttu-id="7c372-103">Método CImageDisplay. getbitmasks</span><span class="sxs-lookup"><span data-stu-id="7c372-103">CImageDisplay.GetBitMasks method</span></span>

<span data-ttu-id="7c372-104">O `GetBitMasks` método recupera as máscaras de cores para um formato [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) especificado.</span><span class="sxs-lookup"><span data-stu-id="7c372-104">The `GetBitMasks` method retrieves the color masks for a specified [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) format.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c372-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7c372-105">Syntax</span></span>


```C++
const DWORD* GetBitMasks(
   const VIDEOINFO *pVideoInfo
);
```



## <a name="parameters"></a><span data-ttu-id="7c372-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7c372-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c372-107">*pVideoInfo*</span><span class="sxs-lookup"><span data-stu-id="7c372-107">*pVideoInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="7c372-108">Ponteiro para a estrutura **VIDEOINFO** .</span><span class="sxs-lookup"><span data-stu-id="7c372-108">Pointer to the **VIDEOINFO** structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c372-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7c372-109">Return value</span></span>

<span data-ttu-id="7c372-110">Retorna uma matriz de três valores **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="7c372-110">Returns an array of three **DWORD** values.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c372-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="7c372-111">Remarks</span></span>

<span data-ttu-id="7c372-112">Se o membro de **bicompressão** for bi \_ BITFIELDS, o método retornará um ponteiro para as máscaras de cores que são fornecidas no membro **dwBitMasks** .</span><span class="sxs-lookup"><span data-stu-id="7c372-112">If the **biCompression** member is BI\_BITFIELDS, the method returns a pointer to the color masks that are supplied in the **dwBitMasks** member.</span></span> <span data-ttu-id="7c372-113">Se o membro de **bicompressão** for bi \_ RGB, o método retornará as máscaras de cores que correspondem à profundidade de bits.</span><span class="sxs-lookup"><span data-stu-id="7c372-113">If the **biCompression** member is BI\_RGB, the method returns the color masks that correspond to the bit depth.</span></span> <span data-ttu-id="7c372-114">Se o método falhar (por exemplo, a profundidade de bit é menor que 16), o método retornará a matriz {0,0,0} .</span><span class="sxs-lookup"><span data-stu-id="7c372-114">If the method fails (for example, the bit depth is less than 16), the method returns the array {0,0,0}.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c372-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7c372-115">Requirements</span></span>



| <span data-ttu-id="7c372-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c372-116">Requirement</span></span> | <span data-ttu-id="7c372-117">Valor</span><span class="sxs-lookup"><span data-stu-id="7c372-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c372-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7c372-118">Header</span></span><br/>  | <dl> <span data-ttu-id="7c372-119"><dt>Winutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7c372-119"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7c372-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7c372-120">Library</span></span><br/> | <dl> <span data-ttu-id="7c372-121"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="7c372-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c372-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="7c372-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c372-123">**Classe CImageDisplay**</span><span class="sxs-lookup"><span data-stu-id="7c372-123">**CImageDisplay Class**</span></span>](cimagedisplay.md)
</dt> </dl>

 

 




