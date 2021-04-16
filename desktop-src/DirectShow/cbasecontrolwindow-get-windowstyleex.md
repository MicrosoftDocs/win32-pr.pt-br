---
description: O \_ método Get WindowStyleEx recupera os estilos de janela estendidos.
ms.assetid: 72955958-bbda-4b8f-9c28-6d3f5eb56a82
title: Método de CBaseControlWindow.get_WindowStyleEx (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_WindowStyleEx
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c59336ab57e92e99366494a272f2b995191b494b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750689"
---
# <a name="cbasecontrolwindowget_windowstyleex-method"></a><span data-ttu-id="5f57b-103">CBaseControlWindow. obter \_ método WindowStyleEx</span><span class="sxs-lookup"><span data-stu-id="5f57b-103">CBaseControlWindow.get\_WindowStyleEx method</span></span>

<span data-ttu-id="5f57b-104">O `get_WindowStyleEx` método recupera os estilos de janela estendidos.</span><span class="sxs-lookup"><span data-stu-id="5f57b-104">The `get_WindowStyleEx` method retrieves the extended window styles.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f57b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5f57b-105">Syntax</span></span>


```C++
HRESULT get_WindowStyleEx(
   long *pWindowStyleEx
);
```



## <a name="parameters"></a><span data-ttu-id="5f57b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5f57b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f57b-107">*pWindowStyleEx*</span><span class="sxs-lookup"><span data-stu-id="5f57b-107">*pWindowStyleEx*</span></span> 
</dt> <dd>

<span data-ttu-id="5f57b-108">Ponteiro para estilos de janela estendidos.</span><span class="sxs-lookup"><span data-stu-id="5f57b-108">Pointer to extended window styles.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f57b-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5f57b-109">Return value</span></span>

<span data-ttu-id="5f57b-110">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5f57b-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f57b-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="5f57b-111">Remarks</span></span>

<span data-ttu-id="5f57b-112">Essa função de membro recupera os estilos de janela estendida.</span><span class="sxs-lookup"><span data-stu-id="5f57b-112">This member function retrieves the extended window styles.</span></span> <span data-ttu-id="5f57b-113">Ele chama a função de membro [**CBaseControlWindow::D ogetwindowstyle**](cbasecontrolwindow-dogetwindowstyle.md) .</span><span class="sxs-lookup"><span data-stu-id="5f57b-113">It calls the [**CBaseControlWindow::DoGetWindowStyle**](cbasecontrolwindow-dogetwindowstyle.md) member function.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f57b-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5f57b-114">Requirements</span></span>



| <span data-ttu-id="5f57b-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f57b-115">Requirement</span></span> | <span data-ttu-id="5f57b-116">Valor</span><span class="sxs-lookup"><span data-stu-id="5f57b-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f57b-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5f57b-117">Header</span></span><br/>  | <dl> <span data-ttu-id="5f57b-118"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5f57b-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5f57b-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5f57b-119">Library</span></span><br/> | <dl> <span data-ttu-id="5f57b-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="5f57b-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f57b-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="5f57b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f57b-122">**Classe CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="5f57b-122">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




