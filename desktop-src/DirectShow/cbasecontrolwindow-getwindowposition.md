---
description: O método GetWindowPosition recupera as coordenadas atuais para a janela.
ms.assetid: a2f46a87-b2cd-450f-8d2b-0f8695432fda
title: Método CBaseControlWindow. GetWindowPosition (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.GetWindowPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: af2b1bdb8b2c839644e8c0629e3e272c123d3c21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751280"
---
# <a name="cbasecontrolwindowgetwindowposition-method"></a><span data-ttu-id="2e8e0-103">Método CBaseControlWindow. GetWindowPosition</span><span class="sxs-lookup"><span data-stu-id="2e8e0-103">CBaseControlWindow.GetWindowPosition method</span></span>

<span data-ttu-id="2e8e0-104">O `GetWindowPosition` método recupera as coordenadas atuais para a janela.</span><span class="sxs-lookup"><span data-stu-id="2e8e0-104">The `GetWindowPosition` method retrieves the current coordinates for the window.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e8e0-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2e8e0-105">Syntax</span></span>


```C++
HRESULT GetWindowPosition(
   long *pLeft,
   long *pTop,
   long *pWidth,
   long *pHeight
);
```



## <a name="parameters"></a><span data-ttu-id="2e8e0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2e8e0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e8e0-107">*pLeft*</span><span class="sxs-lookup"><span data-stu-id="2e8e0-107">*pLeft*</span></span> 
</dt> <dd>

<span data-ttu-id="2e8e0-108">Ponteiro para a coordenada esquerda, em coordenadas da tela.</span><span class="sxs-lookup"><span data-stu-id="2e8e0-108">Pointer to the left coordinate, in screen coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="2e8e0-109">*pTop*</span><span class="sxs-lookup"><span data-stu-id="2e8e0-109">*pTop*</span></span> 
</dt> <dd>

<span data-ttu-id="2e8e0-110">Ponteiro para a coordenada superior, em coordenadas da tela.</span><span class="sxs-lookup"><span data-stu-id="2e8e0-110">Pointer to the top coordinate, in screen coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="2e8e0-111">*pWidth*</span><span class="sxs-lookup"><span data-stu-id="2e8e0-111">*pWidth*</span></span> 
</dt> <dd>

<span data-ttu-id="2e8e0-112">Ponteiro para a largura da janela, em coordenadas da tela.</span><span class="sxs-lookup"><span data-stu-id="2e8e0-112">Pointer to the window width, in screen coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="2e8e0-113">*pHeight*</span><span class="sxs-lookup"><span data-stu-id="2e8e0-113">*pHeight*</span></span> 
</dt> <dd>

<span data-ttu-id="2e8e0-114">Ponteiro para a altura da janela, em coordenadas da tela.</span><span class="sxs-lookup"><span data-stu-id="2e8e0-114">Pointer to the window height, in screen coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e8e0-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2e8e0-115">Return value</span></span>

<span data-ttu-id="2e8e0-116">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2e8e0-116">Returns an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e8e0-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e8e0-117">Requirements</span></span>



| <span data-ttu-id="2e8e0-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e8e0-118">Requirement</span></span> | <span data-ttu-id="2e8e0-119">Valor</span><span class="sxs-lookup"><span data-stu-id="2e8e0-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e8e0-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2e8e0-120">Header</span></span><br/>  | <dl> <span data-ttu-id="2e8e0-121"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2e8e0-121"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2e8e0-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2e8e0-122">Library</span></span><br/> | <dl> <span data-ttu-id="2e8e0-123"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="2e8e0-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e8e0-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="2e8e0-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e8e0-125">**Classe CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="2e8e0-125">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




