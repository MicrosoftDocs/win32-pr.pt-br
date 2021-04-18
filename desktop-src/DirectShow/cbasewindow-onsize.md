---
description: O método OnSize manipula mensagens de tamanho do WM \_ .
ms.assetid: 21d867a4-4321-478a-9beb-5d3053569369
title: Método CBaseWindow. OnSize (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.OnSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c9020510030d3b3d4b30e066adfe67367618fb3d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810259"
---
# <a name="cbasewindowonsize-method"></a><span data-ttu-id="a5b65-103">Método CBaseWindow. OnSize</span><span class="sxs-lookup"><span data-stu-id="a5b65-103">CBaseWindow.OnSize method</span></span>

<span data-ttu-id="a5b65-104">O `OnSize` método manipula mensagens de tamanho do WM \_ .</span><span class="sxs-lookup"><span data-stu-id="a5b65-104">The `OnSize` method handles WM\_SIZE messages.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5b65-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a5b65-105">Syntax</span></span>


```C++
virtual BOOL OnSize(
   LONG Width,
   LONG Height
);
```



## <a name="parameters"></a><span data-ttu-id="a5b65-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a5b65-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5b65-107">*Largura*</span><span class="sxs-lookup"><span data-stu-id="a5b65-107">*Width*</span></span> 
</dt> <dd>

<span data-ttu-id="a5b65-108">Largura da área do cliente, em pixels.</span><span class="sxs-lookup"><span data-stu-id="a5b65-108">Width of the client area, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="a5b65-109">*Altura*</span><span class="sxs-lookup"><span data-stu-id="a5b65-109">*Height*</span></span> 
</dt> <dd>

<span data-ttu-id="a5b65-110">Altura da área do cliente, em pixels.</span><span class="sxs-lookup"><span data-stu-id="a5b65-110">Height of the client area, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5b65-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a5b65-111">Return value</span></span>

<span data-ttu-id="a5b65-112">Retorna **true**.</span><span class="sxs-lookup"><span data-stu-id="a5b65-112">Returns **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="a5b65-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="a5b65-113">Remarks</span></span>

<span data-ttu-id="a5b65-114">Esse método armazena a nova largura e altura.</span><span class="sxs-lookup"><span data-stu-id="a5b65-114">This method stores the new width and height.</span></span> <span data-ttu-id="a5b65-115">Para recuperar esses valores, chame os métodos [**CBaseWindow:: GetWindowHeight**](cbasewindow-getwindowheight.md) e [**CBaseWindow:: GetWindowWidth**](cbasewindow-getwindowwidth.md) .</span><span class="sxs-lookup"><span data-stu-id="a5b65-115">To retrieve these values, call the [**CBaseWindow::GetWindowHeight**](cbasewindow-getwindowheight.md) and [**CBaseWindow::GetWindowWidth**](cbasewindow-getwindowwidth.md) methods.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5b65-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a5b65-116">Requirements</span></span>



| <span data-ttu-id="a5b65-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5b65-117">Requirement</span></span> | <span data-ttu-id="a5b65-118">Valor</span><span class="sxs-lookup"><span data-stu-id="a5b65-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5b65-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a5b65-119">Header</span></span><br/>  | <dl> <span data-ttu-id="a5b65-120"><dt>Winutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a5b65-120"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a5b65-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a5b65-121">Library</span></span><br/> | <dl> <span data-ttu-id="a5b65-122"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="a5b65-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5b65-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="a5b65-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5b65-124">**Classe CBaseWindow**</span><span class="sxs-lookup"><span data-stu-id="a5b65-124">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




