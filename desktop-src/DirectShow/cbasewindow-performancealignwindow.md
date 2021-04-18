---
description: O método PerformanceAlignWindow alinha a posição da janela aos limites DWORD, para o desempenho máximo.
ms.assetid: e28950bc-2510-45b9-9c9c-c2a9dbc3dc02
title: Método CBaseWindow. PerformanceAlignWindow (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.PerformanceAlignWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e6e7a54372743d430cd904f47c79414d149cf033
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105778508"
---
# <a name="cbasewindowperformancealignwindow-method"></a><span data-ttu-id="3febf-103">Método CBaseWindow. PerformanceAlignWindow</span><span class="sxs-lookup"><span data-stu-id="3febf-103">CBaseWindow.PerformanceAlignWindow method</span></span>

<span data-ttu-id="3febf-104">O `PerformanceAlignWindow` método alinha a posição da janela com os limites **DWORD** , para o desempenho máximo.</span><span class="sxs-lookup"><span data-stu-id="3febf-104">The `PerformanceAlignWindow` method aligns the window position to **DWORD** boundaries, for maximum performance.</span></span>

## <a name="syntax"></a><span data-ttu-id="3febf-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3febf-105">Syntax</span></span>


```C++
HRESULT PerformanceAlignWindow();
```



## <a name="parameters"></a><span data-ttu-id="3febf-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3febf-106">Parameters</span></span>

<span data-ttu-id="3febf-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="3febf-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3febf-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3febf-108">Return value</span></span>

<span data-ttu-id="3febf-109">Retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3febf-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="3febf-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="3febf-110">Remarks</span></span>

<span data-ttu-id="3febf-111">Esse método alinha as bordas esquerda e superior da janela aos limites DWORD, o que pode melhorar o desempenho.</span><span class="sxs-lookup"><span data-stu-id="3febf-111">This method aligns the left and top edges of the window to DWORD boundaries, which can improve performance.</span></span> <span data-ttu-id="3febf-112">Se a janela tiver um pai, o método retornará S \_ OK, mas executará o alinhamento.</span><span class="sxs-lookup"><span data-stu-id="3febf-112">If the window has a parent, the method returns S\_OK but does perform the alignment.</span></span>

## <a name="requirements"></a><span data-ttu-id="3febf-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3febf-113">Requirements</span></span>



| <span data-ttu-id="3febf-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="3febf-114">Requirement</span></span> | <span data-ttu-id="3febf-115">Valor</span><span class="sxs-lookup"><span data-stu-id="3febf-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3febf-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3febf-116">Header</span></span><br/>  | <dl> <span data-ttu-id="3febf-117"><dt>Winutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3febf-117"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3febf-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3febf-118">Library</span></span><br/> | <dl> <span data-ttu-id="3febf-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="3febf-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3febf-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="3febf-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3febf-121">**Classe CBaseWindow**</span><span class="sxs-lookup"><span data-stu-id="3febf-121">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




