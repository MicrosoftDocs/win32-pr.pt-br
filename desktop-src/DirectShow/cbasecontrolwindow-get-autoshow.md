---
description: O \_ método obter AutoShow recupera o sinalizador de estado atual do AutoShow.
ms.assetid: b27651d1-3ac5-4a52-9549-b63bacda5dc8
title: Método de CBaseControlWindow.get_AutoShow (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_AutoShow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f45679b9d036f1c5386cd2c1d18a31fa3d6bd64f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758877"
---
# <a name="cbasecontrolwindowget_autoshow-method"></a><span data-ttu-id="e6300-103">Método de automostrar CBaseControlWindow. get \_</span><span class="sxs-lookup"><span data-stu-id="e6300-103">CBaseControlWindow.get\_AutoShow method</span></span>

<span data-ttu-id="e6300-104">O `get_AutoShow` método recupera o sinalizador de estado atual do AutoShow.</span><span class="sxs-lookup"><span data-stu-id="e6300-104">The `get_AutoShow` method retrieves the current AutoShow state flag.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6300-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e6300-105">Syntax</span></span>


```C++
HRESULT get_AutoShow(
   long *AutoShow
);
```



## <a name="parameters"></a><span data-ttu-id="e6300-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e6300-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6300-107">*Mostrar automostrações*</span><span class="sxs-lookup"><span data-stu-id="e6300-107">*AutoShow*</span></span> 
</dt> <dd>

<span data-ttu-id="e6300-108">Ponteiro para um sinalizador booliano de automação (0 está desativado, 1 está ativado).</span><span class="sxs-lookup"><span data-stu-id="e6300-108">Pointer to an Automation Boolean flag (0 is off,  1 is on).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6300-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e6300-109">Return value</span></span>

<span data-ttu-id="e6300-110">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e6300-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6300-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="e6300-111">Remarks</span></span>

<span data-ttu-id="e6300-112">Essa função de membro implementa o método de [**\_ automostrar IVideoWindow:: Get**](/windows/desktop/api/Control/nf-control-ivideowindow-get_autoshow) .</span><span class="sxs-lookup"><span data-stu-id="e6300-112">This member function implements the [**IVideoWindow::get\_AutoShow**](/windows/desktop/api/Control/nf-control-ivideowindow-get_autoshow) method.</span></span> <span data-ttu-id="e6300-113">Essa propriedade simplifica o acesso de exibição da janela para aplicativos.</span><span class="sxs-lookup"><span data-stu-id="e6300-113">This property simplifies window display access for applications.</span></span> <span data-ttu-id="e6300-114">Se isso for definido como 1 (ativado), a janela, que normalmente é ocultada após a conexão do filtro, será exibida automaticamente quando o filtro for pausado ou executado.</span><span class="sxs-lookup"><span data-stu-id="e6300-114">If this is set to  1 (on), the window, which is typically hidden after connection of the filter, will be displayed automatically when the filter pauses or runs.</span></span> <span data-ttu-id="e6300-115">No entanto, a janela não deve ser ocultada quando o filtro é interrompido.</span><span class="sxs-lookup"><span data-stu-id="e6300-115">The window should not be hidden when the filter stops, however.</span></span> <span data-ttu-id="e6300-116">Se esse parâmetro for definido como 0 (off), a janela ficará visível somente quando o aplicativo chamar [**CBaseControlWindow::p UT \_ Visible**](cbasecontrolwindow-put-visible.md) ou [**CBaseControlWindow::p UT \_ WindowState**](cbasecontrolwindow-put-windowstate.md) com os parâmetros apropriados.</span><span class="sxs-lookup"><span data-stu-id="e6300-116">If this parameter is set to 0 (off), the window is made visible only when the application calls [**CBaseControlWindow::put\_Visible**](cbasecontrolwindow-put-visible.md) or [**CBaseControlWindow::put\_WindowState**](cbasecontrolwindow-put-windowstate.md) with the appropriate parameters.</span></span>

<span data-ttu-id="e6300-117">Essa função de membro deve ser chamada por objetos externos por meio da interface [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) e, portanto, bloqueia a seção crítica para sincronizar com o filtro associado.</span><span class="sxs-lookup"><span data-stu-id="e6300-117">This member function is meant to be called by external objects through the [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) interface, and therefore locks the critical section to synchronize with the associated filter.</span></span> <span data-ttu-id="e6300-118">Chame a função de membro [**CBaseControlWindow:: IsAutoShowEnabled**](cbasecontrolwindow-isautoshowenabled.md) para recuperar essa propriedade se você não estiver chamando de um objeto externo.</span><span class="sxs-lookup"><span data-stu-id="e6300-118">Call the [**CBaseControlWindow::IsAutoShowEnabled**](cbasecontrolwindow-isautoshowenabled.md) member function to retrieve this property if you are not calling from an external object.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6300-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e6300-119">Requirements</span></span>



| <span data-ttu-id="e6300-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6300-120">Requirement</span></span> | <span data-ttu-id="e6300-121">Valor</span><span class="sxs-lookup"><span data-stu-id="e6300-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6300-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e6300-122">Header</span></span><br/>  | <dl> <span data-ttu-id="e6300-123"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e6300-123"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e6300-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e6300-124">Library</span></span><br/> | <dl> <span data-ttu-id="e6300-125"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="e6300-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6300-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="e6300-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6300-127">**Classe CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="e6300-127">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




