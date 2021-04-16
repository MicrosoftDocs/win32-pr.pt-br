---
description: O método GetBorderColour recupera a cor de borda da janela atual, m \_ BorderColour.
ms.assetid: 5cd9b834-5438-475e-9671-ee9917f9a485
title: Método CBaseControlWindow. GetBorderColour (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.GetBorderColour
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0ba6e1be9babf96d03235c49d9cde0f11cae1b83
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753757"
---
# <a name="cbasecontrolwindowgetbordercolour-method"></a><span data-ttu-id="fc943-103">Método CBaseControlWindow. GetBorderColour</span><span class="sxs-lookup"><span data-stu-id="fc943-103">CBaseControlWindow.GetBorderColour method</span></span>

<span data-ttu-id="fc943-104">O `GetBorderColour` método recupera a cor da borda da janela atual, **m \_ BorderColour**.</span><span class="sxs-lookup"><span data-stu-id="fc943-104">The `GetBorderColour` method retrieves the current window border color, **m\_BorderColour**.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc943-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fc943-105">Syntax</span></span>


```C++
COLORREF GetBorderColour();
```



## <a name="parameters"></a><span data-ttu-id="fc943-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fc943-106">Parameters</span></span>

<span data-ttu-id="fc943-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="fc943-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fc943-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fc943-108">Return value</span></span>

<span data-ttu-id="fc943-109">Retorna a cor da borda.</span><span class="sxs-lookup"><span data-stu-id="fc943-109">Returns the color of the border.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc943-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="fc943-110">Remarks</span></span>

<span data-ttu-id="fc943-111">Um aplicativo pode definir um retângulo de destino para exibir o vídeo.</span><span class="sxs-lookup"><span data-stu-id="fc943-111">An application can set a destination rectangle to display the video.</span></span> <span data-ttu-id="fc943-112">Esse retângulo deve ser relativo à área do cliente para a janela.</span><span class="sxs-lookup"><span data-stu-id="fc943-112">This rectangle should be relative to the client area for the window.</span></span> <span data-ttu-id="fc943-113">Se isso for feito (o padrão é sempre pintar toda a janela), há uma área que circunda o vídeo; ou seja, a borda.</span><span class="sxs-lookup"><span data-stu-id="fc943-113">If this is done (the default is to always paint the entire window), there is an area that surrounds the video; that is, the border.</span></span> <span data-ttu-id="fc943-114">A cor da borda pode ser definida por meio da função de membro [**CBaseControlWindow::p UT \_ BorderColor**](cbasecontrolwindow-put-bordercolor.md) .</span><span class="sxs-lookup"><span data-stu-id="fc943-114">The border color can be set through the [**CBaseControlWindow::put\_BorderColor**](cbasecontrolwindow-put-bordercolor.md) member function.</span></span> <span data-ttu-id="fc943-115">Essa propriedade afeta a cor da borda.</span><span class="sxs-lookup"><span data-stu-id="fc943-115">This property affects the color of the border.</span></span> <span data-ttu-id="fc943-116">Use essa função de membro em vez de [**CBaseControlWindow:: get \_ BorderColor**](cbasecontrolwindow-get-bordercolor.md), a menos que você esteja chamando isso externamente por meio do método [**IVideoWindow:: get \_ BorderColor**](/windows/desktop/api/Control/nf-control-ivideowindow-get_bordercolor) .</span><span class="sxs-lookup"><span data-stu-id="fc943-116">Use this member function instead of [**CBaseControlWindow::get\_BorderColor**](cbasecontrolwindow-get-bordercolor.md), unless you are calling this externally through the [**IVideoWindow::get\_BorderColor**](/windows/desktop/api/Control/nf-control-ivideowindow-get_bordercolor) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc943-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fc943-117">Requirements</span></span>



| <span data-ttu-id="fc943-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc943-118">Requirement</span></span> | <span data-ttu-id="fc943-119">Valor</span><span class="sxs-lookup"><span data-stu-id="fc943-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc943-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fc943-120">Header</span></span><br/>  | <dl> <span data-ttu-id="fc943-121"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fc943-121"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="fc943-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fc943-122">Library</span></span><br/> | <dl> <span data-ttu-id="fc943-123"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="fc943-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc943-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="fc943-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc943-125">**Classe CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="fc943-125">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




