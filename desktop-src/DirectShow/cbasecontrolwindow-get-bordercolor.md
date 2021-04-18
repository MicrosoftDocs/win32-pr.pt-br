---
description: O \_ método Get BorderColor recupera a cor da borda atual.
ms.assetid: 4b4cae1d-bef7-4f8d-8011-c220fcfb73eb
title: Método de CBaseControlWindow.get_BorderColor (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_BorderColor
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d889f211b204c2c0180ae757a0240c8588552e83
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753364"
---
# <a name="cbasecontrolwindowget_bordercolor-method"></a><span data-ttu-id="a6a27-103">CBaseControlWindow. obter \_ método BorderColor</span><span class="sxs-lookup"><span data-stu-id="a6a27-103">CBaseControlWindow.get\_BorderColor method</span></span>

<span data-ttu-id="a6a27-104">O `get_BorderColor` método recupera a cor da borda atual.</span><span class="sxs-lookup"><span data-stu-id="a6a27-104">The `get_BorderColor` method retrieves the current border color.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6a27-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a6a27-105">Syntax</span></span>


```C++
HRESULT get_BorderColor(
   long *Color
);
```



## <a name="parameters"></a><span data-ttu-id="a6a27-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a6a27-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6a27-107">*Cor*</span><span class="sxs-lookup"><span data-stu-id="a6a27-107">*Color*</span></span> 
</dt> <dd>

<span data-ttu-id="a6a27-108">Ponteiro para a cor da borda atual.</span><span class="sxs-lookup"><span data-stu-id="a6a27-108">Pointer to the current border color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6a27-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a6a27-109">Return value</span></span>

<span data-ttu-id="a6a27-110">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a6a27-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a6a27-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="a6a27-111">Remarks</span></span>

<span data-ttu-id="a6a27-112">Um aplicativo pode definir um retângulo de destino no qual o vídeo deve ser exibido.</span><span class="sxs-lookup"><span data-stu-id="a6a27-112">An application can set a destination rectangle in which the video should be displayed.</span></span> <span data-ttu-id="a6a27-113">Esse retângulo é relativo à área do cliente para a janela.</span><span class="sxs-lookup"><span data-stu-id="a6a27-113">This rectangle is relative to the client area for the window.</span></span> <span data-ttu-id="a6a27-114">Se isso for feito (o padrão é sempre pintar toda a janela), haverá uma borda ao redor do vídeo.</span><span class="sxs-lookup"><span data-stu-id="a6a27-114">If this is done (the default is to always paint the entire window), there is a border surrounding the video.</span></span> <span data-ttu-id="a6a27-115">Essa propriedade afeta a cor usada pela borda.</span><span class="sxs-lookup"><span data-stu-id="a6a27-115">This property affects the color used by the border.</span></span> <span data-ttu-id="a6a27-116">Embora o parâmetro seja especificado como um tipo **longo** , na verdade ele é um valor **COLORREF** .</span><span class="sxs-lookup"><span data-stu-id="a6a27-116">Although the parameter is specified as a **LONG** type, it is actually a **COLORREF** value.</span></span>

<span data-ttu-id="a6a27-117">Essa função de membro deve ser chamada por objetos externos por meio da interface [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) e, portanto, bloqueia a seção crítica para sincronizar com o filtro associado.</span><span class="sxs-lookup"><span data-stu-id="a6a27-117">This member function is meant to be called by external objects through the [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) interface, and therefore locks the critical section to synchronize with the associated filter.</span></span> <span data-ttu-id="a6a27-118">Chame a função de membro [**CBaseControlWindow:: GetBorderColour**](cbasecontrolwindow-getbordercolour.md) para recuperar essa propriedade se não estiver chamando de um objeto externo.</span><span class="sxs-lookup"><span data-stu-id="a6a27-118">Call the [**CBaseControlWindow::GetBorderColour**](cbasecontrolwindow-getbordercolour.md) member function to retrieve this property if not calling from an external object.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6a27-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a6a27-119">Requirements</span></span>



| <span data-ttu-id="a6a27-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6a27-120">Requirement</span></span> | <span data-ttu-id="a6a27-121">Valor</span><span class="sxs-lookup"><span data-stu-id="a6a27-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6a27-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a6a27-122">Header</span></span><br/>  | <dl> <span data-ttu-id="a6a27-123"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a6a27-123"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a6a27-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a6a27-124">Library</span></span><br/> | <dl> <span data-ttu-id="a6a27-125"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="a6a27-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6a27-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="a6a27-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6a27-127">**Classe CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="a6a27-127">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




