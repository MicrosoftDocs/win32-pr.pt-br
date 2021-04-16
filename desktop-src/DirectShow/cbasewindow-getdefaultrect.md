---
description: O método GetDefaultRect recupera o tamanho padrão da área do cliente.
ms.assetid: 9eb9e3a4-0d45-4aa3-a496-1b0bd92d4989
title: Método CBaseWindow. GetDefaultRect (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.GetDefaultRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1d7ec9612eab45e21262f8344daf7a52a6a888b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759147"
---
# <a name="cbasewindowgetdefaultrect-method"></a><span data-ttu-id="d8a93-103">Método CBaseWindow. GetDefaultRect</span><span class="sxs-lookup"><span data-stu-id="d8a93-103">CBaseWindow.GetDefaultRect method</span></span>

<span data-ttu-id="d8a93-104">O `GetDefaultRect` método recupera o tamanho padrão da área do cliente.</span><span class="sxs-lookup"><span data-stu-id="d8a93-104">The `GetDefaultRect` method retrieves the default size of the client area.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8a93-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d8a93-105">Syntax</span></span>


```C++
virtual RECT GetDefaultRect();
```



## <a name="parameters"></a><span data-ttu-id="d8a93-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d8a93-106">Parameters</span></span>

<span data-ttu-id="d8a93-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="d8a93-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d8a93-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d8a93-108">Return value</span></span>

<span data-ttu-id="d8a93-109">Retorna o retângulo padrão.</span><span class="sxs-lookup"><span data-stu-id="d8a93-109">Returns the default rectangle.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8a93-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="d8a93-110">Remarks</span></span>

<span data-ttu-id="d8a93-111">Quando a janela é ativada, o objeto chama esse método para determinar o tamanho que ele deve tornar a área do cliente da janela.</span><span class="sxs-lookup"><span data-stu-id="d8a93-111">When the window is activated, the object calls this method to determine how large it should make the window's client area.</span></span> <span data-ttu-id="d8a93-112">Na classe base, esse método retorna um retângulo cuja altura e largura são as constantes definidas DEFHEIGHT e DEFWIDTH.</span><span class="sxs-lookup"><span data-stu-id="d8a93-112">In the base class, this method returns a rectangle whose height and width are the defined constants DEFHEIGHT and DEFWIDTH.</span></span> <span data-ttu-id="d8a93-113">Uma classe derivada deve substituir esse método.</span><span class="sxs-lookup"><span data-stu-id="d8a93-113">A derived class should override this method.</span></span> <span data-ttu-id="d8a93-114">Para um processador de vídeo, a classe derivada normalmente retornará o tamanho da imagem de vídeo nativa.</span><span class="sxs-lookup"><span data-stu-id="d8a93-114">For a video renderer, the derived class will typically return the size of the native video image.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8a93-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d8a93-115">Requirements</span></span>



| <span data-ttu-id="d8a93-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8a93-116">Requirement</span></span> | <span data-ttu-id="d8a93-117">Valor</span><span class="sxs-lookup"><span data-stu-id="d8a93-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8a93-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d8a93-118">Header</span></span><br/>  | <dl> <span data-ttu-id="d8a93-119"><dt>Winutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d8a93-119"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d8a93-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d8a93-120">Library</span></span><br/> | <dl> <span data-ttu-id="d8a93-121"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="d8a93-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8a93-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="d8a93-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8a93-123">**Classe CBaseWindow**</span><span class="sxs-lookup"><span data-stu-id="d8a93-123">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




