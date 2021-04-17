---
description: O \_ método Put AutoShow define o sinalizador de estado de AutoApresentação.
ms.assetid: 857472b8-845b-46d3-8593-3fba9a9c8cdc
title: Método de CBaseControlWindow.put_AutoShow (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_AutoShow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: eda5c0c4055979537c5cc471053715e29a348f1a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755619"
---
# <a name="cbasecontrolwindowput_autoshow-method"></a><span data-ttu-id="8247d-103">Método de automostrar CBaseControlWindow. put \_</span><span class="sxs-lookup"><span data-stu-id="8247d-103">CBaseControlWindow.put\_AutoShow method</span></span>

<span data-ttu-id="8247d-104">O `put_AutoShow` método define o sinalizador de estado de AutoShow.</span><span class="sxs-lookup"><span data-stu-id="8247d-104">The `put_AutoShow` method sets the AutoShow state flag.</span></span>

## <a name="syntax"></a><span data-ttu-id="8247d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8247d-105">Syntax</span></span>


```C++
HRESULT put_AutoShow(
   long AutoShow
);
```



## <a name="parameters"></a><span data-ttu-id="8247d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8247d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8247d-107">*Mostrar automostrações*</span><span class="sxs-lookup"><span data-stu-id="8247d-107">*AutoShow*</span></span> 
</dt> <dd>

<span data-ttu-id="8247d-108">Sinalizador booliano de automação (0 está desativado, 1 está ativado).</span><span class="sxs-lookup"><span data-stu-id="8247d-108">Automation Boolean flag (0 is off,  1 is on).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8247d-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8247d-109">Return value</span></span>

<span data-ttu-id="8247d-110">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8247d-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8247d-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="8247d-111">Remarks</span></span>

<span data-ttu-id="8247d-112">Essa propriedade simplifica o acesso de exibição da janela para aplicativos.</span><span class="sxs-lookup"><span data-stu-id="8247d-112">This property simplifies window display access for applications.</span></span> <span data-ttu-id="8247d-113">Se isso for definido como 1 (ativado), a janela, que normalmente é ocultada após o filtro ser conectado, será exibida automaticamente quando o filtro for pausado ou executado.</span><span class="sxs-lookup"><span data-stu-id="8247d-113">If this is set to  1 (on), the window, which is typically hidden after the filter is connected, will be displayed automatically when the filter pauses or runs.</span></span> <span data-ttu-id="8247d-114">No entanto, a janela não deve ser ocultada quando o filtro é interrompido.</span><span class="sxs-lookup"><span data-stu-id="8247d-114">The window should not be hidden when the filter stops, however.</span></span> <span data-ttu-id="8247d-115">Se for definido como 0 (off), a janela ficará visível somente quando o aplicativo chamar [**CBaseControlWindow::p UT \_ Visible**](cbasecontrolwindow-put-visible.md) ou [**CBaseControlWindow::p UT \_ WindowState**](cbasecontrolwindow-put-windowstate.md) com os parâmetros apropriados.</span><span class="sxs-lookup"><span data-stu-id="8247d-115">If this is set to 0 (off), the window is made visible only when the application calls [**CBaseControlWindow::put\_Visible**](cbasecontrolwindow-put-visible.md) or [**CBaseControlWindow::put\_WindowState**](cbasecontrolwindow-put-windowstate.md) with the appropriate parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="8247d-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8247d-116">Requirements</span></span>



| <span data-ttu-id="8247d-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="8247d-117">Requirement</span></span> | <span data-ttu-id="8247d-118">Valor</span><span class="sxs-lookup"><span data-stu-id="8247d-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8247d-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8247d-119">Header</span></span><br/>  | <dl> <span data-ttu-id="8247d-120"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8247d-120"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="8247d-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8247d-121">Library</span></span><br/> | <dl> <span data-ttu-id="8247d-122"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="8247d-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8247d-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="8247d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8247d-124">**Classe CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="8247d-124">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




