---
description: O método IsAutoShowEnabled recupera informações sobre se a janela de vídeo é exibida automaticamente quando o filtro de renderização é pausado ou executado.
ms.assetid: 769e3023-a515-4b80-a979-2e4fa9612e65
title: Método CBaseControlWindow. IsAutoShowEnabled (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.IsAutoShowEnabled
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2c4b4a894593cb3be26a1034098cd2a0cdacf926
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747617"
---
# <a name="cbasecontrolwindowisautoshowenabled-method"></a><span data-ttu-id="c6df6-103">Método CBaseControlWindow. IsAutoShowEnabled</span><span class="sxs-lookup"><span data-stu-id="c6df6-103">CBaseControlWindow.IsAutoShowEnabled method</span></span>

<span data-ttu-id="c6df6-104">O `IsAutoShowEnabled` método recupera informações sobre se a janela de vídeo aparece automaticamente quando o filtro de renderização é pausado ou executado.</span><span class="sxs-lookup"><span data-stu-id="c6df6-104">The `IsAutoShowEnabled` method retrieves information about whether the video window automatically appears when the rendering filter pauses or runs.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6df6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c6df6-105">Syntax</span></span>


```C++
BOOL IsAutoShowEnabled();
```



## <a name="parameters"></a><span data-ttu-id="c6df6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c6df6-106">Parameters</span></span>

<span data-ttu-id="c6df6-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="c6df6-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c6df6-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c6df6-108">Return value</span></span>

<span data-ttu-id="c6df6-109">Retornará **true** se o membro **m \_ bAutoShow** for definido como 1 ou **false** se estiver definido como 0.</span><span class="sxs-lookup"><span data-stu-id="c6df6-109">Returns **TRUE** if the **m\_bAutoShow** member is set to  1 or **FALSE** if it is set to 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="c6df6-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="c6df6-110">Remarks</span></span>

<span data-ttu-id="c6df6-111">Se o membro **m \_ bAutoShow** for definido como 1 em uma janela de vídeo oculta, a janela ficará visível quando o filtro for pausado ou executado.</span><span class="sxs-lookup"><span data-stu-id="c6df6-111">If the **m\_bAutoShow** member is set to  1 on a video window that is hidden, the window becomes visible when the filter pauses or runs.</span></span> <span data-ttu-id="c6df6-112">Se esse membro for definido como 0, a janela será exibida somente se você usar a função de membro [**CBaseControlWindow::p UT \_ Visible**](cbasecontrolwindow-put-visible.md) ou [**CBaseControlWindow \_ ::p UT**](cbasecontrolwindow-put-windowstate.md) com os parâmetros apropriados.</span><span class="sxs-lookup"><span data-stu-id="c6df6-112">If this member is set to 0, the window will appear only if you use the [**CBaseControlWindow::put\_Visible**](cbasecontrolwindow-put-visible.md) or [**CBaseControlWindow::put\_WindowState**](cbasecontrolwindow-put-windowstate.md) member function with the appropriate parameters.</span></span>

<span data-ttu-id="c6df6-113">Essa função de membro recupera a configuração de membro **m \_ bAutoShow** e tem o mesmo resultado que usar o método [**IVideoWindow:: get \_ AutoShow**](/windows/desktop/api/Control/nf-control-ivideowindow-get_autoshow) .</span><span class="sxs-lookup"><span data-stu-id="c6df6-113">This member function retrieves the **m\_bAutoShow** member setting and has the same result as using the [**IVideoWindow::get\_AutoShow**](/windows/desktop/api/Control/nf-control-ivideowindow-get_autoshow) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6df6-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c6df6-114">Requirements</span></span>



| <span data-ttu-id="c6df6-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6df6-115">Requirement</span></span> | <span data-ttu-id="c6df6-116">Valor</span><span class="sxs-lookup"><span data-stu-id="c6df6-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6df6-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c6df6-117">Header</span></span><br/>  | <dl> <span data-ttu-id="c6df6-118"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c6df6-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c6df6-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c6df6-119">Library</span></span><br/> | <dl> <span data-ttu-id="c6df6-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="c6df6-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6df6-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="c6df6-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6df6-122">**Classe CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="c6df6-122">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




