---
description: O método OnError será chamado se ocorrer um erro durante o streaming. A classe derivada deve implementar esse método.
ms.assetid: 0f135cab-611c-4464-9605-360a30de7eb3
title: Método CPullPin. OnError (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.OnError
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2dc8bf7f307ab56609b5f90f6955a1f666854270
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780860"
---
# <a name="cpullpinonerror-method"></a><span data-ttu-id="76bbf-104">Método CPullPin. OnError</span><span class="sxs-lookup"><span data-stu-id="76bbf-104">CPullPin.OnError method</span></span>

<span data-ttu-id="76bbf-105">O `OnError` método será chamado se ocorrer um erro durante o streaming.</span><span class="sxs-lookup"><span data-stu-id="76bbf-105">The `OnError` method is called if an error occurs during streaming.</span></span> <span data-ttu-id="76bbf-106">A classe derivada deve implementar esse método.</span><span class="sxs-lookup"><span data-stu-id="76bbf-106">The derived class must implement this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="76bbf-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="76bbf-107">Syntax</span></span>


```C++
virtual void OnError(
   HRESULT hr
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="76bbf-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="76bbf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76bbf-109">*h*</span><span class="sxs-lookup"><span data-stu-id="76bbf-109">*hr*</span></span> 
</dt> <dd>

<span data-ttu-id="76bbf-110">Especifica o valor **HRESULT** retornado pelo método que falhou.</span><span class="sxs-lookup"><span data-stu-id="76bbf-110">Specifies the **HRESULT** value returned by the method that failed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76bbf-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="76bbf-111">Return value</span></span>

<span data-ttu-id="76bbf-112">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="76bbf-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="76bbf-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="76bbf-113">Remarks</span></span>

<span data-ttu-id="76bbf-114">O objeto chama esse método sempre que ocorre um erro que interrompe o thread de extração de dados.</span><span class="sxs-lookup"><span data-stu-id="76bbf-114">The object calls this method whenever an error occurs that halts the data-pulling thread.</span></span> <span data-ttu-id="76bbf-115">O filtro pode usar esse método para se recuperar de erros de streaming normalmente.</span><span class="sxs-lookup"><span data-stu-id="76bbf-115">The filter can use this method to recover from streaming errors gracefully.</span></span> <span data-ttu-id="76bbf-116">Na maioria dos casos, o erro é retornado do filtro upstream, portanto, o filtro upstream é responsável por reportá-lo para o Gerenciador do grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="76bbf-116">In most cases, the error is returned from the upstream filter, so the upstream filter is responsible for reporting it to the Filter Graph Manager.</span></span> <span data-ttu-id="76bbf-117">Se o erro ocorrer dentro do método [**CPullPin:: Receive**](cpullpin-receive.md) , o filtro deverá enviar um evento de [**\_ ERRORABORT do EC**](ec-errorabort.md) .</span><span class="sxs-lookup"><span data-stu-id="76bbf-117">If the error occurs inside the [**CPullPin::Receive**](cpullpin-receive.md) method, your filter should send an [**EC\_ERRORABORT**](ec-errorabort.md) event.</span></span> <span data-ttu-id="76bbf-118">(Consulte [**IMediaEventSink:: Notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify).)</span><span class="sxs-lookup"><span data-stu-id="76bbf-118">(See [**IMediaEventSink::Notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify).)</span></span>

## <a name="requirements"></a><span data-ttu-id="76bbf-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="76bbf-119">Requirements</span></span>



| <span data-ttu-id="76bbf-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="76bbf-120">Requirement</span></span> | <span data-ttu-id="76bbf-121">Valor</span><span class="sxs-lookup"><span data-stu-id="76bbf-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76bbf-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="76bbf-122">Header</span></span><br/>  | <dl> <span data-ttu-id="76bbf-123"><dt>Pullpin. h</dt></span><span class="sxs-lookup"><span data-stu-id="76bbf-123"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="76bbf-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="76bbf-124">Library</span></span><br/> | <dl> <span data-ttu-id="76bbf-125"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="76bbf-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76bbf-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="76bbf-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76bbf-127">**Classe CPullPin**</span><span class="sxs-lookup"><span data-stu-id="76bbf-127">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 




