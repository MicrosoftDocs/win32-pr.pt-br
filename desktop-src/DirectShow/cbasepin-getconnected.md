---
description: O método getconnecty recupera o PIN conectado a este pin.
ms.assetid: 7b47aa8e-55a9-45f8-aa32-902fee037c72
title: Método CBasePin. GetConnected (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.GetConnected
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e5c583b06a9c25126a611736002c455a2c93ed90
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752904"
---
# <a name="cbasepingetconnected-method"></a><span data-ttu-id="22c47-103">Método CBasePin. GetConnected</span><span class="sxs-lookup"><span data-stu-id="22c47-103">CBasePin.GetConnected method</span></span>

<span data-ttu-id="22c47-104">O `GetConnected` método recupera o PIN conectado a esse PIN.</span><span class="sxs-lookup"><span data-stu-id="22c47-104">The `GetConnected` method retrieves the pin connected to this pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="22c47-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="22c47-105">Syntax</span></span>


```C++
IPin* GetConnected();
```



## <a name="parameters"></a><span data-ttu-id="22c47-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="22c47-106">Parameters</span></span>

<span data-ttu-id="22c47-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="22c47-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="22c47-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="22c47-108">Return value</span></span>

<span data-ttu-id="22c47-109">Retorna um ponteiro para a interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) do outro PIN.</span><span class="sxs-lookup"><span data-stu-id="22c47-109">Returns a pointer to the other pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

## <a name="remarks"></a><span data-ttu-id="22c47-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="22c47-110">Remarks</span></span>

<span data-ttu-id="22c47-111">Se o PIN não estiver conectado, esse método retornará **NULL**.</span><span class="sxs-lookup"><span data-stu-id="22c47-111">If the pin is not connected, this method returns **NULL**.</span></span> <span data-ttu-id="22c47-112">Chame o método [**CBasePin:: IsConnected**](cbasepin-isconnected.md) para determinar se o PIN está conectado.</span><span class="sxs-lookup"><span data-stu-id="22c47-112">Call the [**CBasePin::IsConnected**](cbasepin-isconnected.md) method to determine whether the pin is connected.</span></span>

<span data-ttu-id="22c47-113">O método não chama **AddRef** na interface **IPin** , portanto, o chamador não deve liberar a interface.</span><span class="sxs-lookup"><span data-stu-id="22c47-113">The method does not call **AddRef** on the **IPin** interface, so the caller should not release the interface.</span></span>

## <a name="examples"></a><span data-ttu-id="22c47-114">Exemplos</span><span class="sxs-lookup"><span data-stu-id="22c47-114">Examples</span></span>

<span data-ttu-id="22c47-115">Como a contagem de referência não é incrementada no ponteiro retornado, você pode encadear chamadas de método em conjunto:</span><span class="sxs-lookup"><span data-stu-id="22c47-115">Because the reference count is not incremented on the returned pointer, you can chain method calls together:</span></span>


```C++
if (m_MyPin->IsConnected())
{
    m_MyPin->GetConnected()->EndOfStream();
}
```



<span data-ttu-id="22c47-116">Esse padrão de codificação é muito conveniente; Mas como mostra o exemplo, você deve ter cuidado para não desreferenciar um ponteiro **nulo** quando o PIN não estiver conectado.</span><span class="sxs-lookup"><span data-stu-id="22c47-116">This coding pattern is very convenient; but as the example shows, you must be careful not to dereference a **NULL** pointer when the pin is unconnected.</span></span>

## <a name="requirements"></a><span data-ttu-id="22c47-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="22c47-117">Requirements</span></span>



| <span data-ttu-id="22c47-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="22c47-118">Requirement</span></span> | <span data-ttu-id="22c47-119">Valor</span><span class="sxs-lookup"><span data-stu-id="22c47-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22c47-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="22c47-120">Header</span></span><br/>  | <dl> <span data-ttu-id="22c47-121"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="22c47-121"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="22c47-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="22c47-122">Library</span></span><br/> | <dl> <span data-ttu-id="22c47-123"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="22c47-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22c47-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="22c47-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22c47-125">**Classe CBasePin**</span><span class="sxs-lookup"><span data-stu-id="22c47-125">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




