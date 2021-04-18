---
description: O método OnDisplayChange posta um \_ evento EC display \_ Changed no Gerenciador do grafo de filtro.
ms.assetid: e4cdcdf2-7fc2-4893-9897-97bcf2c12610
title: Método CBaseRenderer. OnDisplayChange (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnDisplayChange
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1e99a8626d523e8b14b013acc9d2ead462f48df3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751258"
---
# <a name="cbaserendererondisplaychange-method"></a><span data-ttu-id="99aa6-103">Método CBaseRenderer. OnDisplayChange</span><span class="sxs-lookup"><span data-stu-id="99aa6-103">CBaseRenderer.OnDisplayChange method</span></span>

<span data-ttu-id="99aa6-104">O `OnDisplayChange` método posta um evento [**EC \_ Display \_ Changed**](ec-display-changed.md) no Gerenciador do grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="99aa6-104">The `OnDisplayChange` method posts an [**EC\_DISPLAY\_CHANGED**](ec-display-changed.md) event to the filter graph manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="99aa6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="99aa6-105">Syntax</span></span>


```C++
BOOL OnDisplayChange();
```



## <a name="parameters"></a><span data-ttu-id="99aa6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="99aa6-106">Parameters</span></span>

<span data-ttu-id="99aa6-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="99aa6-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="99aa6-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="99aa6-108">Return value</span></span>

<span data-ttu-id="99aa6-109">Retorna **true** se o evento foi Postado ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="99aa6-109">Returns **TRUE** if the event was posted, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="99aa6-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="99aa6-110">Remarks</span></span>

<span data-ttu-id="99aa6-111">Os renderizadores de vídeo devem chamar esse método em resposta às mensagens do WM \_ DISPLAYCHANGE.</span><span class="sxs-lookup"><span data-stu-id="99aa6-111">Video renderers should call this method in response to WM\_DISPLAYCHANGE messages.</span></span> <span data-ttu-id="99aa6-112">Se o pino de entrada estiver conectado, o método enviará um evento de exibição de EC \_ \_ alterado para o Gerenciador do grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="99aa6-112">If the input pin is connected, the method sends an EC\_DISPLAY\_CHANGED event to the filter graph manager.</span></span>

## <a name="requirements"></a><span data-ttu-id="99aa6-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="99aa6-113">Requirements</span></span>



| <span data-ttu-id="99aa6-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="99aa6-114">Requirement</span></span> | <span data-ttu-id="99aa6-115">Valor</span><span class="sxs-lookup"><span data-stu-id="99aa6-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99aa6-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="99aa6-116">Header</span></span><br/>  | <dl> <span data-ttu-id="99aa6-117"><dt>Renbase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="99aa6-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="99aa6-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="99aa6-118">Library</span></span><br/> | <dl> <span data-ttu-id="99aa6-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="99aa6-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99aa6-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="99aa6-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99aa6-121">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="99aa6-121">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




