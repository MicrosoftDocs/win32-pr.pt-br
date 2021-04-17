---
description: O método UninitialiseWindow libera os recursos da janela.
ms.assetid: 8c5bb0c1-1d92-4025-bbbd-1e57ddde4456
title: Método CBaseWindow. UninitialiseWindow (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.UninitialiseWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ceeadd0ec7a61422f0127c957125caa9a01dcefb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748026"
---
# <a name="cbasewindowuninitialisewindow-method"></a><span data-ttu-id="6787e-103">Método CBaseWindow. UninitialiseWindow</span><span class="sxs-lookup"><span data-stu-id="6787e-103">CBaseWindow.UninitialiseWindow method</span></span>

<span data-ttu-id="6787e-104">O `UninitialiseWindow` método libera os recursos da janela.</span><span class="sxs-lookup"><span data-stu-id="6787e-104">The `UninitialiseWindow` method releases the window's resources.</span></span>

## <a name="syntax"></a><span data-ttu-id="6787e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6787e-105">Syntax</span></span>


```C++
virtual HRESULT UninitialiseWindow();
```



## <a name="parameters"></a><span data-ttu-id="6787e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6787e-106">Parameters</span></span>

<span data-ttu-id="6787e-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="6787e-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6787e-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6787e-108">Return value</span></span>

<span data-ttu-id="6787e-109">Retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6787e-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="6787e-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="6787e-110">Remarks</span></span>

<span data-ttu-id="6787e-111">Esse método libera recursos que foram adquiridos pelo método [**CBaseWindow:: InitialiseWindow**](cbasewindow-initialisewindow.md) .</span><span class="sxs-lookup"><span data-stu-id="6787e-111">This method frees resources that were acquired by the [**CBaseWindow::InitialiseWindow**](cbasewindow-initialisewindow.md) method.</span></span> <span data-ttu-id="6787e-112">O método [**CBaseWindow::D onewithwindow**](cbasewindow-donewithwindow.md) chama esse método.</span><span class="sxs-lookup"><span data-stu-id="6787e-112">The [**CBaseWindow::DoneWithWindow**](cbasewindow-donewithwindow.md) method calls this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="6787e-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6787e-113">Requirements</span></span>



| <span data-ttu-id="6787e-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="6787e-114">Requirement</span></span> | <span data-ttu-id="6787e-115">Valor</span><span class="sxs-lookup"><span data-stu-id="6787e-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6787e-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6787e-116">Header</span></span><br/>  | <dl> <span data-ttu-id="6787e-117"><dt>Winutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6787e-117"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="6787e-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6787e-118">Library</span></span><br/> | <dl> <span data-ttu-id="6787e-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="6787e-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6787e-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="6787e-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6787e-121">**Classe CBaseWindow**</span><span class="sxs-lookup"><span data-stu-id="6787e-121">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




