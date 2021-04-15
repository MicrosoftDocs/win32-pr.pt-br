---
description: O método GetOwnerWindow recupera o identificador de janela de propriedade, m \_ hwndOwner.
ms.assetid: fa576b42-b4a7-4374-8ba4-7d21e86d9d61
title: Método CBaseControlWindow. GetOwnerWindow (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.GetOwnerWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4e4d3811f85abd68bcd7d625dce0e9e8963be39a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747417"
---
# <a name="cbasecontrolwindowgetownerwindow-method"></a><span data-ttu-id="5a98b-103">Método CBaseControlWindow. GetOwnerWindow</span><span class="sxs-lookup"><span data-stu-id="5a98b-103">CBaseControlWindow.GetOwnerWindow method</span></span>

<span data-ttu-id="5a98b-104">O `GetOwnerWindow` método recupera o identificador de janela de propriedade, **m \_ hwndOwner**.</span><span class="sxs-lookup"><span data-stu-id="5a98b-104">The `GetOwnerWindow` method retrieves the owning window handle, **m\_hwndOwner**.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a98b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5a98b-105">Syntax</span></span>


```C++
HWND GetOwnerWindow();
```



## <a name="parameters"></a><span data-ttu-id="5a98b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5a98b-106">Parameters</span></span>

<span data-ttu-id="5a98b-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="5a98b-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5a98b-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5a98b-108">Return value</span></span>

<span data-ttu-id="5a98b-109">Retorna a janela do proprietário.</span><span class="sxs-lookup"><span data-stu-id="5a98b-109">Returns the owner window.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a98b-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="5a98b-110">Remarks</span></span>

<span data-ttu-id="5a98b-111">Recupera a janela proprietária sem chamar o método de interface.</span><span class="sxs-lookup"><span data-stu-id="5a98b-111">Retrieves the owning window without calling the interface method.</span></span> <span data-ttu-id="5a98b-112">Use essa função de membro em vez de [**CBaseControlWindow:: get \_ proprietário**](cbasecontrolwindow-get-owner.md), a menos que você esteja chamando isso externamente por meio do método [**IVideoWindow:: get \_ proprietário**](/windows/desktop/api/Control/nf-control-ivideowindow-get_owner) .</span><span class="sxs-lookup"><span data-stu-id="5a98b-112">Use this member function instead of [**CBaseControlWindow::get\_Owner**](cbasecontrolwindow-get-owner.md), unless you are calling this externally through the [**IVideoWindow::get\_Owner**](/windows/desktop/api/Control/nf-control-ivideowindow-get_owner) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a98b-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5a98b-113">Requirements</span></span>



| <span data-ttu-id="5a98b-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a98b-114">Requirement</span></span> | <span data-ttu-id="5a98b-115">Valor</span><span class="sxs-lookup"><span data-stu-id="5a98b-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a98b-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5a98b-116">Header</span></span><br/>  | <dl> <span data-ttu-id="5a98b-117"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5a98b-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5a98b-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5a98b-118">Library</span></span><br/> | <dl> <span data-ttu-id="5a98b-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="5a98b-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a98b-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="5a98b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a98b-121">**Classe CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="5a98b-121">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




