---
description: O método GetDisplayFormat recupera um formato de vídeo que descreve o modo de exibição atual.
ms.assetid: 98134704-0453-4090-94de-d92cdf324538
title: Método CImageDisplay. GetDisplayFormat (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.GetDisplayFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 901d61f3597156853b0f2d6f93b43c3cf99ec5e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758857"
---
# <a name="cimagedisplaygetdisplayformat-method"></a><span data-ttu-id="74606-103">Método CImageDisplay. GetDisplayFormat</span><span class="sxs-lookup"><span data-stu-id="74606-103">CImageDisplay.GetDisplayFormat method</span></span>

<span data-ttu-id="74606-104">O `GetDisplayFormat` método recupera um formato de vídeo que descreve o modo de exibição atual.</span><span class="sxs-lookup"><span data-stu-id="74606-104">The `GetDisplayFormat` method retrieves a video format that describes the current display mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="74606-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="74606-105">Syntax</span></span>


```C++
const VIDEOINFO* GetDisplayFormat();
```



## <a name="parameters"></a><span data-ttu-id="74606-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="74606-106">Parameters</span></span>

<span data-ttu-id="74606-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="74606-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="74606-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="74606-108">Return value</span></span>

<span data-ttu-id="74606-109">Retorna um ponteiro para uma estrutura [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) .</span><span class="sxs-lookup"><span data-stu-id="74606-109">Returns a pointer to a [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="74606-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="74606-110">Requirements</span></span>



| <span data-ttu-id="74606-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="74606-111">Requirement</span></span> | <span data-ttu-id="74606-112">Valor</span><span class="sxs-lookup"><span data-stu-id="74606-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74606-113">parâmetro</span><span class="sxs-lookup"><span data-stu-id="74606-113">Header</span></span><br/>  | <dl> <span data-ttu-id="74606-114"><dt>Winutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="74606-114"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="74606-115">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="74606-115">Library</span></span><br/> | <dl> <span data-ttu-id="74606-116"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="74606-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74606-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="74606-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74606-118">**Classe CImageDisplay**</span><span class="sxs-lookup"><span data-stu-id="74606-118">**CImageDisplay Class**</span></span>](cimagedisplay.md)
</dt> </dl>

 

 




