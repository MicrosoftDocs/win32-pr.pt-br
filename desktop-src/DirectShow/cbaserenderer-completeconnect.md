---
description: O método CompleteConnect conclui a conexão do pino de entrada com outro PIN.
ms.assetid: 8dfc1a50-bc73-436a-a471-d8d3218410d3
title: Método CBaseRenderer. CompleteConnect (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a9d2d35f99a3b3b8dc5b668b8ee9a9f94f0a53dd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751501"
---
# <a name="cbaserenderercompleteconnect-method"></a><span data-ttu-id="0bc56-103">Método CBaseRenderer. CompleteConnect</span><span class="sxs-lookup"><span data-stu-id="0bc56-103">CBaseRenderer.CompleteConnect method</span></span>

<span data-ttu-id="0bc56-104">O `CompleteConnect` método conclui a conexão do pino de entrada com outro PIN.</span><span class="sxs-lookup"><span data-stu-id="0bc56-104">The `CompleteConnect` method completes the input pin's connection to another pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="0bc56-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0bc56-105">Syntax</span></span>


```C++
virtual HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a><span data-ttu-id="0bc56-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0bc56-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0bc56-107">*pReceivePin*</span><span class="sxs-lookup"><span data-stu-id="0bc56-107">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="0bc56-108">Ponteiro para a interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) do pino de saída.</span><span class="sxs-lookup"><span data-stu-id="0bc56-108">Pointer to the output pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0bc56-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0bc56-109">Return value</span></span>

<span data-ttu-id="0bc56-110">Retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0bc56-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="0bc56-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="0bc56-111">Remarks</span></span>

<span data-ttu-id="0bc56-112">O pino de entrada do filtro chama esse método de dentro de seu próprio `CompleteConnect` método, que é chamado para concluir uma conexão de PIN.</span><span class="sxs-lookup"><span data-stu-id="0bc56-112">The filter's input pin calls this method from inside its own `CompleteConnect` method, which is called in order to complete a pin connection.</span></span> <span data-ttu-id="0bc56-113">(Para obter mais informações, consulte [**CBasePin:: CompleteConnect**](cbasepin-completeconnect.md).) O filtro chama o método [**CBaseRenderer:: SetRepaintStatus**](cbaserenderer-setrepaintstatus.md) para habilitar os eventos [**\_ repaintes do EC**](ec-repaint.md) .</span><span class="sxs-lookup"><span data-stu-id="0bc56-113">(For more information, see [**CBasePin::CompleteConnect**](cbasepin-completeconnect.md).) The filter calls the [**CBaseRenderer::SetRepaintStatus**](cbaserenderer-setrepaintstatus.md) method to enable [**EC\_REPAINT**](ec-repaint.md) events.</span></span>

## <a name="requirements"></a><span data-ttu-id="0bc56-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0bc56-114">Requirements</span></span>



| <span data-ttu-id="0bc56-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="0bc56-115">Requirement</span></span> | <span data-ttu-id="0bc56-116">Valor</span><span class="sxs-lookup"><span data-stu-id="0bc56-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0bc56-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0bc56-117">Header</span></span><br/>  | <dl> <span data-ttu-id="0bc56-118"><dt>Renbase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0bc56-118"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0bc56-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0bc56-119">Library</span></span><br/> | <dl> <span data-ttu-id="0bc56-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="0bc56-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0bc56-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="0bc56-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0bc56-122">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="0bc56-122">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




