---
description: O método PrepareWindow cria a janela.
ms.assetid: c4c0d177-6351-4ecc-b1eb-399b4a94c463
title: Método CBaseWindow. PrepareWindow (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.PrepareWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 91331ede15feb756f3ddd08d0d368621b35eda00
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747596"
---
# <a name="cbasewindowpreparewindow-method"></a><span data-ttu-id="637ba-103">Método CBaseWindow. PrepareWindow</span><span class="sxs-lookup"><span data-stu-id="637ba-103">CBaseWindow.PrepareWindow method</span></span>

<span data-ttu-id="637ba-104">O `PrepareWindow` método cria a janela.</span><span class="sxs-lookup"><span data-stu-id="637ba-104">The `PrepareWindow` method creates the window.</span></span>

## <a name="syntax"></a><span data-ttu-id="637ba-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="637ba-105">Syntax</span></span>


```C++
virtual HRESULT PrepareWindow();
```



## <a name="parameters"></a><span data-ttu-id="637ba-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="637ba-106">Parameters</span></span>

<span data-ttu-id="637ba-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="637ba-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="637ba-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="637ba-108">Return value</span></span>

<span data-ttu-id="637ba-109">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="637ba-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="637ba-110">Os valores possíveis incluem os mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="637ba-110">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="637ba-111">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="637ba-111">Return code</span></span>                                                                            | <span data-ttu-id="637ba-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="637ba-112">Description</span></span>         |
|----------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="637ba-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="637ba-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="637ba-114">Êxito.</span><span class="sxs-lookup"><span data-stu-id="637ba-114">Success.</span></span><br/> |
| <dl> <span data-ttu-id="637ba-115"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="637ba-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="637ba-116">Falha.</span><span class="sxs-lookup"><span data-stu-id="637ba-116">Failure.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="637ba-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="637ba-117">Remarks</span></span>

<span data-ttu-id="637ba-118">Chame esse método depois de criar o objeto.</span><span class="sxs-lookup"><span data-stu-id="637ba-118">Call this method after creating the object.</span></span> <span data-ttu-id="637ba-119">Esse método executa algumas escriturações iniciais e, em seguida, chama o método [**CBaseWindow::D ocreatewindow**](cbasewindow-docreatewindow.md) para criar a janela.</span><span class="sxs-lookup"><span data-stu-id="637ba-119">This method performs some initial bookkeeping and then calls the [**CBaseWindow::DoCreateWindow**](cbasewindow-docreatewindow.md) method to create the window.</span></span>

## <a name="requirements"></a><span data-ttu-id="637ba-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="637ba-120">Requirements</span></span>



| <span data-ttu-id="637ba-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="637ba-121">Requirement</span></span> | <span data-ttu-id="637ba-122">Valor</span><span class="sxs-lookup"><span data-stu-id="637ba-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="637ba-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="637ba-123">Header</span></span><br/>  | <dl> <span data-ttu-id="637ba-124"><dt>Winutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="637ba-124"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="637ba-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="637ba-125">Library</span></span><br/> | <dl> <span data-ttu-id="637ba-126"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="637ba-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="637ba-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="637ba-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="637ba-128">**Classe CBaseWindow**</span><span class="sxs-lookup"><span data-stu-id="637ba-128">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




