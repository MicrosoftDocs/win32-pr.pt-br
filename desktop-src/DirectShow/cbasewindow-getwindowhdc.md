---
description: O método GetWindowHDC recupera um identificador para o contexto de dispositivo da janela (DC).
ms.assetid: 35ee2a66-ee56-44dc-ad59-fd467bb4aa63
title: Método CBaseWindow. GetWindowHDC (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.GetWindowHDC
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 16c2502b3a9de587e91ff43ddc45a84ae08492db
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748211"
---
# <a name="cbasewindowgetwindowhdc-method"></a><span data-ttu-id="f09a0-103">Método CBaseWindow. GetWindowHDC</span><span class="sxs-lookup"><span data-stu-id="f09a0-103">CBaseWindow.GetWindowHDC method</span></span>

<span data-ttu-id="f09a0-104">O `GetWindowHDC` método recupera um identificador para o contexto do dispositivo (DC) da janela.</span><span class="sxs-lookup"><span data-stu-id="f09a0-104">The `GetWindowHDC` method retrieves a handle to the window's device context (DC).</span></span>

## <a name="syntax"></a><span data-ttu-id="f09a0-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f09a0-105">Syntax</span></span>


```C++
HDC GetWindowHDC();
```



## <a name="parameters"></a><span data-ttu-id="f09a0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f09a0-106">Parameters</span></span>

<span data-ttu-id="f09a0-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="f09a0-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f09a0-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f09a0-108">Return value</span></span>

<span data-ttu-id="f09a0-109">Retorna um identificador para o controlador de domínio.</span><span class="sxs-lookup"><span data-stu-id="f09a0-109">Returns a handle to the DC.</span></span>

## <a name="requirements"></a><span data-ttu-id="f09a0-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f09a0-110">Requirements</span></span>



| <span data-ttu-id="f09a0-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="f09a0-111">Requirement</span></span> | <span data-ttu-id="f09a0-112">Valor</span><span class="sxs-lookup"><span data-stu-id="f09a0-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f09a0-113">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f09a0-113">Header</span></span><br/>  | <dl> <span data-ttu-id="f09a0-114"><dt>Winutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f09a0-114"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f09a0-115">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f09a0-115">Library</span></span><br/> | <dl> <span data-ttu-id="f09a0-116"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="f09a0-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f09a0-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="f09a0-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f09a0-118">**Classe CBaseWindow**</span><span class="sxs-lookup"><span data-stu-id="f09a0-118">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




