---
description: O método GetReader retorna um ponteiro para a interface IAsyncReader do pino de saída.
ms.assetid: bb7ed3f2-a5bc-496c-8a52-f9915a75105e
title: Método CPullPin. GetReader (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.GetReader
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3a20bbb689c4ee5e3ac12c510098163d9fbb224e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754976"
---
# <a name="cpullpingetreader-method"></a><span data-ttu-id="66f37-103">Método CPullPin. GetReader</span><span class="sxs-lookup"><span data-stu-id="66f37-103">CPullPin.GetReader method</span></span>

<span data-ttu-id="66f37-104">O `GetReader` método retorna um ponteiro para a interface [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) do pino de saída.</span><span class="sxs-lookup"><span data-stu-id="66f37-104">The `GetReader` method returns a pointer to the output pin's [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="66f37-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="66f37-105">Syntax</span></span>


```C++
IAsyncReader* GetReader();
```



## <a name="parameters"></a><span data-ttu-id="66f37-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="66f37-106">Parameters</span></span>

<span data-ttu-id="66f37-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="66f37-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="66f37-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="66f37-108">Return value</span></span>

<span data-ttu-id="66f37-109">Retorna um ponteiro para a interface [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) .</span><span class="sxs-lookup"><span data-stu-id="66f37-109">Returns a pointer to the [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) interface.</span></span>

## <a name="remarks"></a><span data-ttu-id="66f37-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="66f37-110">Remarks</span></span>

<span data-ttu-id="66f37-111">A interface retornada tem uma contagem de referência pendente.</span><span class="sxs-lookup"><span data-stu-id="66f37-111">The returned interface has an outstanding reference count.</span></span> <span data-ttu-id="66f37-112">O chamador deve liberar a interface.</span><span class="sxs-lookup"><span data-stu-id="66f37-112">The caller must release the interface.</span></span>

<span data-ttu-id="66f37-113">O método não verifica o valor do ponteiro de interface antes de chamar **AddRef**, portanto, não chame isso até que você tenha chamado o método [**CPullPin:: Connect**](cpullpin-connect.md) com êxito.</span><span class="sxs-lookup"><span data-stu-id="66f37-113">The method does not check the value of the interface pointer before calling **AddRef**, so do not call this until you have successfully called the [**CPullPin::Connect**](cpullpin-connect.md) method.</span></span> <span data-ttu-id="66f37-114">Caso contrário, o ponteiro de interface pode ser **nulo** e chamar **AddRef** gerará uma exceção.</span><span class="sxs-lookup"><span data-stu-id="66f37-114">Otherwise, the interface pointer might be **NULL** and calling **AddRef** will throw an exception.</span></span>

## <a name="requirements"></a><span data-ttu-id="66f37-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="66f37-115">Requirements</span></span>



| <span data-ttu-id="66f37-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="66f37-116">Requirement</span></span> | <span data-ttu-id="66f37-117">Valor</span><span class="sxs-lookup"><span data-stu-id="66f37-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66f37-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="66f37-118">Header</span></span><br/>  | <dl> <span data-ttu-id="66f37-119"><dt>Pullpin. h</dt></span><span class="sxs-lookup"><span data-stu-id="66f37-119"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="66f37-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="66f37-120">Library</span></span><br/> | <dl> <span data-ttu-id="66f37-121"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="66f37-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66f37-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="66f37-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66f37-123">**Classe CPullPin**</span><span class="sxs-lookup"><span data-stu-id="66f37-123">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 




