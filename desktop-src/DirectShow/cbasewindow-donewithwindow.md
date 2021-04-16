---
description: O método DoneWithWindow destrói a janela.
ms.assetid: 03c97884-7d91-4b59-b867-dda231d2a184
title: Método CBaseWindow. DoneWithWindow (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.DoneWithWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cc31e893a4015aa8b4356d265ca4065ee336c3ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750057"
---
# <a name="cbasewindowdonewithwindow-method"></a><span data-ttu-id="8afe7-103">Método CBaseWindow. DoneWithWindow</span><span class="sxs-lookup"><span data-stu-id="8afe7-103">CBaseWindow.DoneWithWindow method</span></span>

<span data-ttu-id="8afe7-104">O `DoneWithWindow` método destrói a janela.</span><span class="sxs-lookup"><span data-stu-id="8afe7-104">The `DoneWithWindow` method destroys the window.</span></span>

## <a name="syntax"></a><span data-ttu-id="8afe7-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8afe7-105">Syntax</span></span>


```C++
virtual HRESULT DoneWithWindow();
```



## <a name="parameters"></a><span data-ttu-id="8afe7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8afe7-106">Parameters</span></span>

<span data-ttu-id="8afe7-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="8afe7-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8afe7-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8afe7-108">Return value</span></span>

<span data-ttu-id="8afe7-109">Retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8afe7-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="8afe7-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="8afe7-110">Remarks</span></span>

<span data-ttu-id="8afe7-111">Chame esse método do método destruidor do objeto derivado.</span><span class="sxs-lookup"><span data-stu-id="8afe7-111">Call this method from the derived object's destructor method.</span></span>

<span data-ttu-id="8afe7-112">Se esse método for chamado do mesmo thread que criou a janela, o método executará as seguintes ações:</span><span class="sxs-lookup"><span data-stu-id="8afe7-112">If this method is called from the same thread that created the window, the method performs the following actions:</span></span>

-   <span data-ttu-id="8afe7-113">Chama o método [**CBaseWindow:: InactivateWindow**](cbasewindow-inactivatewindow.md) , que desativa a janela.</span><span class="sxs-lookup"><span data-stu-id="8afe7-113">Calls the [**CBaseWindow::InactivateWindow**](cbasewindow-inactivatewindow.md) method, which deactivates the window.</span></span>
-   <span data-ttu-id="8afe7-114">Chama o método [**CBaseWindow:: UninitialiseWindow**](cbasewindow-uninitialisewindow.md) , que libera os recursos usados pela janela.</span><span class="sxs-lookup"><span data-stu-id="8afe7-114">Calls the [**CBaseWindow::UninitialiseWindow**](cbasewindow-uninitialisewindow.md) method, which releases resources used by the window.</span></span>
-   <span data-ttu-id="8afe7-115">Destrói a janela.</span><span class="sxs-lookup"><span data-stu-id="8afe7-115">Destroys the window.</span></span>

<span data-ttu-id="8afe7-116">Se a chamada de thread `DoneWithWindow` não for o thread que criou a janela, o método enviará uma mensagem "Destroy" privada para a janela.</span><span class="sxs-lookup"><span data-stu-id="8afe7-116">If the thread calling `DoneWithWindow` is not the thread that created the window, the method sends a private "destroy" message to the window.</span></span> <span data-ttu-id="8afe7-117">Quando a janela recebe essa mensagem, ela chama a `DoneWithWindow` si mesma.</span><span class="sxs-lookup"><span data-stu-id="8afe7-117">When the window receives this message, it calls `DoneWithWindow` on itself.</span></span> <span data-ttu-id="8afe7-118">(Se [**CBaseWindow:: m \_ BDoPostToDestroy**](cbasewindow-m-bdoposttodestroy.md) for **true**, a janela postará a mensagem.)</span><span class="sxs-lookup"><span data-stu-id="8afe7-118">(If [**CBaseWindow::m\_bDoPostToDestroy**](cbasewindow-m-bdoposttodestroy.md) is **TRUE**, the window posts the message.)</span></span>

## <a name="requirements"></a><span data-ttu-id="8afe7-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8afe7-119">Requirements</span></span>



| <span data-ttu-id="8afe7-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="8afe7-120">Requirement</span></span> | <span data-ttu-id="8afe7-121">Valor</span><span class="sxs-lookup"><span data-stu-id="8afe7-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8afe7-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8afe7-122">Header</span></span><br/>  | <dl> <span data-ttu-id="8afe7-123"><dt>Winutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8afe7-123"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="8afe7-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8afe7-124">Library</span></span><br/> | <dl> <span data-ttu-id="8afe7-125"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="8afe7-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8afe7-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="8afe7-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8afe7-127">**Classe CBaseWindow**</span><span class="sxs-lookup"><span data-stu-id="8afe7-127">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




