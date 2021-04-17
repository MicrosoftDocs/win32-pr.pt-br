---
description: O método GetRestorePosition recupera a posição para a qual a janela será restaurada quando ela não for maximizada ou minimizada.
ms.assetid: 5f129be3-c4d8-4583-bbc8-870e0bcafd80
title: Método CBaseControlWindow. GetRestorePosition (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.GetRestorePosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f922a97f69f4dae03d4e61a54bd99c52d69a984a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752724"
---
# <a name="cbasecontrolwindowgetrestoreposition-method"></a><span data-ttu-id="53102-103">Método CBaseControlWindow. GetRestorePosition</span><span class="sxs-lookup"><span data-stu-id="53102-103">CBaseControlWindow.GetRestorePosition method</span></span>

<span data-ttu-id="53102-104">O `GetRestorePosition` método recupera a posição para a qual a janela será restaurada quando ela não for maximizada ou minimizada.</span><span class="sxs-lookup"><span data-stu-id="53102-104">The `GetRestorePosition` method retrieves the position to which the window will be restored when it is not maximized or minimized.</span></span>

## <a name="syntax"></a><span data-ttu-id="53102-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="53102-105">Syntax</span></span>


```C++
HRESULT GetRestorePosition(
   long *pLeft,
   long *pTop,
   long *pWidth,
   long *pHeight
);
```



## <a name="parameters"></a><span data-ttu-id="53102-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="53102-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53102-107">*pLeft*</span><span class="sxs-lookup"><span data-stu-id="53102-107">*pLeft*</span></span> 
</dt> <dd>

<span data-ttu-id="53102-108">Ponteiro para o valor da coordenada da extrema esquerda.</span><span class="sxs-lookup"><span data-stu-id="53102-108">Pointer to the value for leftmost coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="53102-109">*pTop*</span><span class="sxs-lookup"><span data-stu-id="53102-109">*pTop*</span></span> 
</dt> <dd>

<span data-ttu-id="53102-110">Ponteiro para o valor da parte superior da janela.</span><span class="sxs-lookup"><span data-stu-id="53102-110">Pointer to the value for top of the window.</span></span>

</dd> <dt>

<span data-ttu-id="53102-111">*pWidth*</span><span class="sxs-lookup"><span data-stu-id="53102-111">*pWidth*</span></span> 
</dt> <dd>

<span data-ttu-id="53102-112">Ponteiro para o valor da largura da janela.</span><span class="sxs-lookup"><span data-stu-id="53102-112">Pointer to the value for width of the window.</span></span>

</dd> <dt>

<span data-ttu-id="53102-113">*pHeight*</span><span class="sxs-lookup"><span data-stu-id="53102-113">*pHeight*</span></span> 
</dt> <dd>

<span data-ttu-id="53102-114">Ponteiro para o valor da altura da janela.</span><span class="sxs-lookup"><span data-stu-id="53102-114">Pointer to the value for height of window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53102-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="53102-115">Return value</span></span>

<span data-ttu-id="53102-116">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="53102-116">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="53102-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="53102-117">Remarks</span></span>

<span data-ttu-id="53102-118">Isso é o mesmo que os valores retornados pela função [**CBaseControlWindow:: GetWindowPosition**](cbasecontrolwindow-getwindowposition.md) quando a janela não é maximizada nem minimizada.</span><span class="sxs-lookup"><span data-stu-id="53102-118">This is the same as the values returned by the [**CBaseControlWindow::GetWindowPosition**](cbasecontrolwindow-getwindowposition.md) function when the window is neither maximized nor minimized.</span></span>

## <a name="requirements"></a><span data-ttu-id="53102-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="53102-119">Requirements</span></span>



| <span data-ttu-id="53102-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="53102-120">Requirement</span></span> | <span data-ttu-id="53102-121">Valor</span><span class="sxs-lookup"><span data-stu-id="53102-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53102-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="53102-122">Header</span></span><br/>  | <dl> <span data-ttu-id="53102-123"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="53102-123"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="53102-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="53102-124">Library</span></span><br/> | <dl> <span data-ttu-id="53102-125"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="53102-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53102-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="53102-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53102-127">**Classe CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="53102-127">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




