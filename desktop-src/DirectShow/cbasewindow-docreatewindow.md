---
description: O método docreatewindow cria a janela.
ms.assetid: bbe38a71-bbf7-4380-96a3-074b992a1d1e
title: CBaseWindow.DoCmétodo reateWindow (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.DoCreateWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 76bea1523f48a6e22a3c2d9370fa32bcea022621
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751900"
---
# <a name="cbasewindowdocreatewindow-method"></a><span data-ttu-id="bc4f7-103">CBaseWindow.DoCmétodo reateWindow</span><span class="sxs-lookup"><span data-stu-id="bc4f7-103">CBaseWindow.DoCreateWindow method</span></span>

<span data-ttu-id="bc4f7-104">O `DoCreateWindow` método cria a janela.</span><span class="sxs-lookup"><span data-stu-id="bc4f7-104">The `DoCreateWindow` method creates the window.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc4f7-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bc4f7-105">Syntax</span></span>


```C++
HRESULT DoCreateWindow();
```



## <a name="parameters"></a><span data-ttu-id="bc4f7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bc4f7-106">Parameters</span></span>

<span data-ttu-id="bc4f7-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="bc4f7-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bc4f7-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bc4f7-108">Return value</span></span>

<span data-ttu-id="bc4f7-109">Retorna S \_ OK se bem-sucedido ou um valor **HRESULT** que indica a causa da falha.</span><span class="sxs-lookup"><span data-stu-id="bc4f7-109">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc4f7-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="bc4f7-110">Remarks</span></span>

<span data-ttu-id="bc4f7-111">O método [**CBaseWindow::P reparewindow**](cbasewindow-preparewindow.md) chama esse método.</span><span class="sxs-lookup"><span data-stu-id="bc4f7-111">The [**CBaseWindow::PrepareWindow**](cbasewindow-preparewindow.md) method calls this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc4f7-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bc4f7-112">Requirements</span></span>



| <span data-ttu-id="bc4f7-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc4f7-113">Requirement</span></span> | <span data-ttu-id="bc4f7-114">Valor</span><span class="sxs-lookup"><span data-stu-id="bc4f7-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc4f7-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bc4f7-115">Header</span></span><br/>  | <dl> <span data-ttu-id="bc4f7-116"><dt>Winutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bc4f7-116"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="bc4f7-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bc4f7-117">Library</span></span><br/> | <dl> <span data-ttu-id="bc4f7-118"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="bc4f7-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc4f7-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="bc4f7-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc4f7-120">**Classe CBaseWindow**</span><span class="sxs-lookup"><span data-stu-id="bc4f7-120">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




