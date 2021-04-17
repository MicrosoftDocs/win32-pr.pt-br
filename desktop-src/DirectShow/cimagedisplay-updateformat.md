---
description: O método updateformat preenche alguns membros opcionais da estrutura VIDEOINFO.
ms.assetid: 5ca34fa0-eef4-44f5-bbcc-e686e5181d86
title: Método CImageDisplay. updateformat (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.UpdateFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c6966da171e37e1cc285afc1872d221ca7aad99e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752893"
---
# <a name="cimagedisplayupdateformat-method"></a><span data-ttu-id="029e4-103">Método CImageDisplay. updateformat</span><span class="sxs-lookup"><span data-stu-id="029e4-103">CImageDisplay.UpdateFormat method</span></span>

<span data-ttu-id="029e4-104">O `UpdateFormat` método preenche alguns membros opcionais da estrutura [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) .</span><span class="sxs-lookup"><span data-stu-id="029e4-104">The `UpdateFormat` method fills in some optional members of the [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="029e4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="029e4-105">Syntax</span></span>


```C++
HRESULT UpdateFormat(
   VIDEOINFO *pVideoInfo
);
```



## <a name="parameters"></a><span data-ttu-id="029e4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="029e4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="029e4-107">*pVideoInfo*</span><span class="sxs-lookup"><span data-stu-id="029e4-107">*pVideoInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="029e4-108">Ponteiro para uma estrutura **VIDEOINFO** .</span><span class="sxs-lookup"><span data-stu-id="029e4-108">Pointer to a **VIDEOINFO** structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="029e4-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="029e4-109">Return value</span></span>

<span data-ttu-id="029e4-110">Retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="029e4-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="029e4-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="029e4-111">Remarks</span></span>

<span data-ttu-id="029e4-112">Esse método define os membros **biClrUsed**, **biClrImportant** e **biSizeImage** com os valores corretos e limpa os retângulos de origem e de destino.</span><span class="sxs-lookup"><span data-stu-id="029e4-112">This method sets the **biClrUsed**, **biClrImportant**, and **biSizeImage** members to the correct values, and clears the source and target rectangles.</span></span>

## <a name="requirements"></a><span data-ttu-id="029e4-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="029e4-113">Requirements</span></span>



| <span data-ttu-id="029e4-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="029e4-114">Requirement</span></span> | <span data-ttu-id="029e4-115">Valor</span><span class="sxs-lookup"><span data-stu-id="029e4-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="029e4-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="029e4-116">Header</span></span><br/>  | <dl> <span data-ttu-id="029e4-117"><dt>Winutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="029e4-117"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="029e4-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="029e4-118">Library</span></span><br/> | <dl> <span data-ttu-id="029e4-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="029e4-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="029e4-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="029e4-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="029e4-121">**Classe CImageDisplay**</span><span class="sxs-lookup"><span data-stu-id="029e4-121">**CImageDisplay Class**</span></span>](cimagedisplay.md)
</dt> </dl>

 

 




