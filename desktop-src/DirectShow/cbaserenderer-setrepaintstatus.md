---
description: O método SetRepaintStatus habilita ou desabilita os eventos redesenhados.
ms.assetid: 94ae4935-459e-4009-9f64-c7c5b14504ae
title: Método CBaseRenderer. SetRepaintStatus (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SetRepaintStatus
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 39822b535680a699654e969abc316c10c54ba51b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811747"
---
# <a name="cbaserenderersetrepaintstatus-method"></a><span data-ttu-id="70029-103">Método CBaseRenderer. SetRepaintStatus</span><span class="sxs-lookup"><span data-stu-id="70029-103">CBaseRenderer.SetRepaintStatus method</span></span>

<span data-ttu-id="70029-104">O `SetRepaintStatus` método habilita ou desabilita os eventos redesenhados.</span><span class="sxs-lookup"><span data-stu-id="70029-104">The `SetRepaintStatus` method enables or disables repaint events.</span></span>

## <a name="syntax"></a><span data-ttu-id="70029-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="70029-105">Syntax</span></span>


```C++
void SetRepaintStatus(
   BOOL bRepaint
);
```



## <a name="parameters"></a><span data-ttu-id="70029-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="70029-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70029-107">*bRepaint*</span><span class="sxs-lookup"><span data-stu-id="70029-107">*bRepaint*</span></span> 
</dt> <dd>

<span data-ttu-id="70029-108">Valor booliano que indica se os eventos redesenhados estão habilitados.</span><span class="sxs-lookup"><span data-stu-id="70029-108">Boolean value indicating whether repaint events are enabled.</span></span> <span data-ttu-id="70029-109">Se **for true**, o filtro enviará eventos [**\_ Repaints do EC**](ec-repaint.md) para o Gerenciador do grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="70029-109">If **TRUE**, the filter will sent [**EC\_REPAINT**](ec-repaint.md) events to the filter graph manager.</span></span> <span data-ttu-id="70029-110">Caso contrário, ele não enviará \_ eventos de REdesenhos do EC.</span><span class="sxs-lookup"><span data-stu-id="70029-110">Otherwise, it will not send EC\_REPAINT events.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70029-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="70029-111">Return value</span></span>

<span data-ttu-id="70029-112">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="70029-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="70029-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="70029-113">Remarks</span></span>

<span data-ttu-id="70029-114">Esse método garante que o Gerenciador de gráficos de filtro não seja inundado com \_ eventos de REdesenhos de EC redundantes.</span><span class="sxs-lookup"><span data-stu-id="70029-114">This method ensures that the filter graph manager is not flooded with redundant EC\_REPAINT events.</span></span> <span data-ttu-id="70029-115">Depois que o filtro envia um evento de [**\_ redesenho de EC**](ec-repaint.md) , ele chama esse método com o valor **true**.</span><span class="sxs-lookup"><span data-stu-id="70029-115">After the filter sends an [**EC\_REPAINT**](ec-repaint.md) event, it calls this method with the value **TRUE**.</span></span> <span data-ttu-id="70029-116">O filtro não envia mais eventos de \_ REdesenho de EC até receber mais dados.</span><span class="sxs-lookup"><span data-stu-id="70029-116">The filter does not send more EC\_REPAINT events until it receives more data.</span></span>

## <a name="requirements"></a><span data-ttu-id="70029-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="70029-117">Requirements</span></span>



| <span data-ttu-id="70029-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="70029-118">Requirement</span></span> | <span data-ttu-id="70029-119">Valor</span><span class="sxs-lookup"><span data-stu-id="70029-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70029-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="70029-120">Header</span></span><br/>  | <dl> <span data-ttu-id="70029-121"><dt>Renbase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="70029-121"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="70029-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="70029-122">Library</span></span><br/> | <dl> <span data-ttu-id="70029-123"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="70029-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70029-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="70029-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70029-125">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="70029-125">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




