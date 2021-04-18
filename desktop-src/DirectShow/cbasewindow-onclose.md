---
description: O método fechamento manipula mensagens de fechamento do WM \_ .
ms.assetid: e562add4-752e-4665-a75e-a5526fb7f045
title: Método CBaseWindow. fechamento (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.OnClose
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 189b08c116f66ff864ffe308befb990973c6ce43
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751899"
---
# <a name="cbasewindowonclose-method"></a><span data-ttu-id="59a34-103">Método CBaseWindow. fechamento</span><span class="sxs-lookup"><span data-stu-id="59a34-103">CBaseWindow.OnClose method</span></span>

<span data-ttu-id="59a34-104">O `OnClose` método manipula mensagens de fechamento do WM \_ .</span><span class="sxs-lookup"><span data-stu-id="59a34-104">The `OnClose` method handles WM\_CLOSE messages.</span></span>

## <a name="syntax"></a><span data-ttu-id="59a34-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="59a34-105">Syntax</span></span>


```C++
virtual BOOL OnClose();
```



## <a name="parameters"></a><span data-ttu-id="59a34-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="59a34-106">Parameters</span></span>

<span data-ttu-id="59a34-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="59a34-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="59a34-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="59a34-108">Return value</span></span>

<span data-ttu-id="59a34-109">Retorna **true**.</span><span class="sxs-lookup"><span data-stu-id="59a34-109">Returns **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="59a34-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="59a34-110">Remarks</span></span>

<span data-ttu-id="59a34-111">Na classe base, esse método simplesmente oculta a janela.</span><span class="sxs-lookup"><span data-stu-id="59a34-111">In the base class, this method simply hides the window.</span></span> <span data-ttu-id="59a34-112">Normalmente, uma classe derivada substituirá esse método para que ele envie um evento [**EC \_ userabort**](ec-userabort.md) também.</span><span class="sxs-lookup"><span data-stu-id="59a34-112">Typically, a derived class will override this method so that it sends an [**EC\_USERABORT**](ec-userabort.md) event as well.</span></span> <span data-ttu-id="59a34-113">Não substitua o método para destruir a janela.</span><span class="sxs-lookup"><span data-stu-id="59a34-113">Do not override the method to destroy the window.</span></span> <span data-ttu-id="59a34-114">Em vez disso, chame o método [**CBaseWindow::D onewithwindow**](cbasewindow-donewithwindow.md) quando o filtro proprietário for destruído.</span><span class="sxs-lookup"><span data-stu-id="59a34-114">Instead, call the [**CBaseWindow::DoneWithWindow**](cbasewindow-donewithwindow.md) method when the owning filter is destroyed.</span></span>

## <a name="requirements"></a><span data-ttu-id="59a34-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="59a34-115">Requirements</span></span>



| <span data-ttu-id="59a34-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="59a34-116">Requirement</span></span> | <span data-ttu-id="59a34-117">Valor</span><span class="sxs-lookup"><span data-stu-id="59a34-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59a34-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="59a34-118">Header</span></span><br/>  | <dl> <span data-ttu-id="59a34-119"><dt>Winutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="59a34-119"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="59a34-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="59a34-120">Library</span></span><br/> | <dl> <span data-ttu-id="59a34-121"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="59a34-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59a34-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="59a34-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59a34-123">**Classe CBaseWindow**</span><span class="sxs-lookup"><span data-stu-id="59a34-123">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




