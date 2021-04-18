---
description: O método SetDrawContext define os contextos de dispositivo usados para desenhar.
ms.assetid: dd752970-99b3-42bb-95a5-8103cab276da
title: Método CDrawImage. SetDrawContext (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.SetDrawContext
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1d329dd45d1a02afd2cbd0daf8d0da8390b0b395
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751490"
---
# <a name="cdrawimagesetdrawcontext-method"></a><span data-ttu-id="ed74f-103">Método CDrawImage. SetDrawContext</span><span class="sxs-lookup"><span data-stu-id="ed74f-103">CDrawImage.SetDrawContext method</span></span>

<span data-ttu-id="ed74f-104">O `SetDrawContext` método define os contextos de dispositivo usados para desenhar.</span><span class="sxs-lookup"><span data-stu-id="ed74f-104">The `SetDrawContext` method sets the device contexts used for drawing.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed74f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ed74f-105">Syntax</span></span>


```C++
void SetDrawContext();
```



## <a name="parameters"></a><span data-ttu-id="ed74f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ed74f-106">Parameters</span></span>

<span data-ttu-id="ed74f-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="ed74f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ed74f-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ed74f-108">Return value</span></span>

<span data-ttu-id="ed74f-109">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="ed74f-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed74f-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="ed74f-110">Remarks</span></span>

<span data-ttu-id="ed74f-111">Esse método recupera os contextos de dispositivo de janela e de memória do objeto [**CBaseWindow**](cbasewindow.md) proprietário.</span><span class="sxs-lookup"><span data-stu-id="ed74f-111">This method retrieves the window and memory device contexts from the owning [**CBaseWindow**](cbasewindow.md) object.</span></span> <span data-ttu-id="ed74f-112">Chame esse método após a janela ser inicializada, mas antes de começar a desenhar.</span><span class="sxs-lookup"><span data-stu-id="ed74f-112">Call this method after the window is initialized, but before you begin drawing.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed74f-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ed74f-113">Requirements</span></span>



| <span data-ttu-id="ed74f-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed74f-114">Requirement</span></span> | <span data-ttu-id="ed74f-115">Valor</span><span class="sxs-lookup"><span data-stu-id="ed74f-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed74f-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ed74f-116">Header</span></span><br/>  | <dl> <span data-ttu-id="ed74f-117"><dt>Winutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ed74f-117"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ed74f-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ed74f-118">Library</span></span><br/> | <dl> <span data-ttu-id="ed74f-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="ed74f-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed74f-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="ed74f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed74f-121">**Classe CDrawImage**</span><span class="sxs-lookup"><span data-stu-id="ed74f-121">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> </dl>

 

 




