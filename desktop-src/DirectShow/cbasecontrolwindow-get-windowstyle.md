---
description: O \_ método Get WindowStyle recupera os estilos de janela padrão.
ms.assetid: 5c204814-5c7c-47e2-95dd-86455ed77cc7
title: Método de CBaseControlWindow.get_WindowStyle (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_WindowStyle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 91e04efac3a67c262b4eeb85948f846dbb06086a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752111"
---
# <a name="cbasecontrolwindowget_windowstyle-method"></a><span data-ttu-id="e52b5-103">CBaseControlWindow. obter \_ método WindowStyle</span><span class="sxs-lookup"><span data-stu-id="e52b5-103">CBaseControlWindow.get\_WindowStyle method</span></span>

<span data-ttu-id="e52b5-104">O `get_WindowStyle` método recupera os estilos de janela padrão.</span><span class="sxs-lookup"><span data-stu-id="e52b5-104">The `get_WindowStyle` method retrieves the standard window styles.</span></span>

## <a name="syntax"></a><span data-ttu-id="e52b5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e52b5-105">Syntax</span></span>


```C++
HRESULT get_WindowStyle(
   long *pWindowStyle
);
```



## <a name="parameters"></a><span data-ttu-id="e52b5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e52b5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e52b5-107">*pWindowStyle*</span><span class="sxs-lookup"><span data-stu-id="e52b5-107">*pWindowStyle*</span></span> 
</dt> <dd>

<span data-ttu-id="e52b5-108">Ponteiro para estilos de janela.</span><span class="sxs-lookup"><span data-stu-id="e52b5-108">Pointer to window styles.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e52b5-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e52b5-109">Return value</span></span>

<span data-ttu-id="e52b5-110">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e52b5-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e52b5-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="e52b5-111">Remarks</span></span>

<span data-ttu-id="e52b5-112">Essa função de membro retorna os estilos de janela padrão, como WS \_ Child e WS \_ Visible.</span><span class="sxs-lookup"><span data-stu-id="e52b5-112">This member function returns the standard window styles, such as WS\_CHILD and WS\_VISIBLE.</span></span> <span data-ttu-id="e52b5-113">Ele chama a função de membro [**CBaseControlWindow::D ogetwindowstyle**](cbasecontrolwindow-dogetwindowstyle.md) .</span><span class="sxs-lookup"><span data-stu-id="e52b5-113">It calls the [**CBaseControlWindow::DoGetWindowStyle**](cbasecontrolwindow-dogetwindowstyle.md) member function.</span></span>

## <a name="requirements"></a><span data-ttu-id="e52b5-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e52b5-114">Requirements</span></span>



| <span data-ttu-id="e52b5-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="e52b5-115">Requirement</span></span> | <span data-ttu-id="e52b5-116">Valor</span><span class="sxs-lookup"><span data-stu-id="e52b5-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e52b5-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e52b5-117">Header</span></span><br/>  | <dl> <span data-ttu-id="e52b5-118"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e52b5-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e52b5-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e52b5-119">Library</span></span><br/> | <dl> <span data-ttu-id="e52b5-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="e52b5-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e52b5-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="e52b5-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e52b5-122">**Classe CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="e52b5-122">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




