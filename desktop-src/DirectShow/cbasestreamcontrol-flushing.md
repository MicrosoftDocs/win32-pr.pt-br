---
description: O método de liberação notifica a classe base de que o PIN foi iniciado ou parou de ser liberado.
ms.assetid: a3c000e1-18a1-48f7-9e2e-fe63cf13fc5c
title: Método CBaseStreamControl. Flushing (Strmctl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.Flushing
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5d4a3a2375ca799f5dd35def03295f29f61c0583
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754993"
---
# <a name="cbasestreamcontrolflushing-method"></a><span data-ttu-id="ce921-103">Método CBaseStreamControl. Flushing</span><span class="sxs-lookup"><span data-stu-id="ce921-103">CBaseStreamControl.Flushing method</span></span>

<span data-ttu-id="ce921-104">O `Flushing` método notifica a classe base de que o PIN foi iniciado ou parou de ser liberado.</span><span class="sxs-lookup"><span data-stu-id="ce921-104">The `Flushing` method notifies the base class that the pin has started or stopped flushing.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce921-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ce921-105">Syntax</span></span>


```C++
void Flushing(
   BOOL bInProgress
);
```



## <a name="parameters"></a><span data-ttu-id="ce921-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ce921-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce921-107">*bInProgress*</span><span class="sxs-lookup"><span data-stu-id="ce921-107">*bInProgress*</span></span> 
</dt> <dd>

<span data-ttu-id="ce921-108">Especifica um valor booliano que indica se o PIN está sendo liberado.</span><span class="sxs-lookup"><span data-stu-id="ce921-108">Specifies a Boolean value that indicates whether the pin is flushing.</span></span> <span data-ttu-id="ce921-109">Use o valor **true** quando o PIN iniciar uma operação de liberação e **false** quando o PIN terminar uma operação de liberação.</span><span class="sxs-lookup"><span data-stu-id="ce921-109">Use the value **TRUE** when the pin begins a flush operation, and **FALSE** when the pin ends a flush operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce921-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ce921-110">Return value</span></span>

<span data-ttu-id="ce921-111">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="ce921-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce921-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="ce921-112">Remarks</span></span>

<span data-ttu-id="ce921-113">O PIN deve chamar esse método de dentro dos métodos [**IPin:: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) e [**IPin:: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) .</span><span class="sxs-lookup"><span data-stu-id="ce921-113">The pin must call this method from within its [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) and [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) methods.</span></span> <span data-ttu-id="ce921-114">Especifique **true** em **BeginFlush** e **false** em **EndFlush**.</span><span class="sxs-lookup"><span data-stu-id="ce921-114">Specify **TRUE** in **BeginFlush** and **FALSE** in **EndFlush**.</span></span>

<span data-ttu-id="ce921-115">Esse método faz com que o método [**CBaseStreamControl:: CheckStreamState**](cbasestreamcontrol-checkstreamstate.md) pare de esperar.</span><span class="sxs-lookup"><span data-stu-id="ce921-115">This method causes the [**CBaseStreamControl::CheckStreamState**](cbasestreamcontrol-checkstreamstate.md) method to stop waiting.</span></span> <span data-ttu-id="ce921-116">Enquanto o PIN está sendo liberado, **CheckStreamState** sempre retorna a \_ descartação de fluxo.</span><span class="sxs-lookup"><span data-stu-id="ce921-116">While the pin is flushing, **CheckStreamState** always returns STREAM\_DISCARDING.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce921-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ce921-117">Requirements</span></span>



| <span data-ttu-id="ce921-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce921-118">Requirement</span></span> | <span data-ttu-id="ce921-119">Valor</span><span class="sxs-lookup"><span data-stu-id="ce921-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce921-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ce921-120">Header</span></span><br/>  | <dl> <span data-ttu-id="ce921-121"><dt>Strmctl. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ce921-121"><dt>Strmctl.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ce921-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ce921-122">Library</span></span><br/> | <dl> <span data-ttu-id="ce921-123"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="ce921-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce921-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="ce921-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce921-125">**Classe CBaseStreamControl**</span><span class="sxs-lookup"><span data-stu-id="ce921-125">**CBaseStreamControl Class**</span></span>](cbasestreamcontrol.md)
</dt> </dl>

 

 




