---
description: O método Receive é chamado quando o objeto recebe um exemplo de mídia do pino de saída. A classe derivada deve implementar esse método.
ms.assetid: ef45388b-b038-4838-b76b-dbbdc5388495
title: Método CPullPin. Receive (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3a651822378b6a3c0754ecbd5ace4a5e464f014f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759562"
---
# <a name="cpullpinreceive-method"></a><span data-ttu-id="9e7eb-104">Método CPullPin. Receive</span><span class="sxs-lookup"><span data-stu-id="9e7eb-104">CPullPin.Receive method</span></span>

<span data-ttu-id="9e7eb-105">O `Receive` método é chamado quando o objeto recebe um exemplo de mídia do pino de saída.</span><span class="sxs-lookup"><span data-stu-id="9e7eb-105">The `Receive` method is called when the object receives a media sample from the output pin.</span></span> <span data-ttu-id="9e7eb-106">A classe derivada deve implementar esse método.</span><span class="sxs-lookup"><span data-stu-id="9e7eb-106">The derived class must implement this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e7eb-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9e7eb-107">Syntax</span></span>


```C++
virtual HRESULT Receive(
   IMediaSample *pSample
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="9e7eb-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9e7eb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e7eb-109">*pSample*</span><span class="sxs-lookup"><span data-stu-id="9e7eb-109">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="9e7eb-110">Ponteiro para a interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) do exemplo de mídia.</span><span class="sxs-lookup"><span data-stu-id="9e7eb-110">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface of the media sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e7eb-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9e7eb-111">Return value</span></span>

<span data-ttu-id="9e7eb-112">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9e7eb-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="9e7eb-113">Retornar um valor diferente de S \_ OK irá parar o thread de extração de dados.</span><span class="sxs-lookup"><span data-stu-id="9e7eb-113">Returning a value other than S\_OK will stop the data-pulling thread.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e7eb-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="9e7eb-114">Remarks</span></span>

<span data-ttu-id="9e7eb-115">Esse método é chamado sempre que um novo exemplo chega do pino de saída.</span><span class="sxs-lookup"><span data-stu-id="9e7eb-115">This method is called whenever a new sample arrives from the output pin.</span></span> <span data-ttu-id="9e7eb-116">Escreva esse método da mesma maneira que o método [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) .</span><span class="sxs-lookup"><span data-stu-id="9e7eb-116">Write this method in the same manner as the [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method.</span></span>

<span data-ttu-id="9e7eb-117">Os carimbos de data/hora no exemplo especificam os deslocamentos de byte, em relação à posição inicial original que foi especificada no método [**CPullPin:: Seek**](cpullpin-seek.md) .</span><span class="sxs-lookup"><span data-stu-id="9e7eb-117">The time stamps on the sample specify the byte offsets, relative to the original start position that was specified in [**CPullPin::Seek**](cpullpin-seek.md) method.</span></span>

<span data-ttu-id="9e7eb-118">A posição inicial é arredondada para baixo até o limite de alinhamento mais próximo e a posição de parada é arredondada para cima até o limite de alinhamento mais próximo.</span><span class="sxs-lookup"><span data-stu-id="9e7eb-118">The start position is rounded down to the nearest alignment boundary, and the stop position is rounded up to the nearest alignment boundary.</span></span> <span data-ttu-id="9e7eb-119">Além disso, se a posição de parada exceder a duração total, a duração será usada em vez disso.</span><span class="sxs-lookup"><span data-stu-id="9e7eb-119">Also, if the stop position exceeds the total duration, the duration is used instead.</span></span>

<span data-ttu-id="9e7eb-120">Todos os carimbos de data/hora são fornecidos como um deslocamento de byte multiplicado por 10 milhões, definidos como as unidades de constante.</span><span class="sxs-lookup"><span data-stu-id="9e7eb-120">All time stamps are given as a byte offset multiplied by 10,000,000, defined as the constant UNITS.</span></span> <span data-ttu-id="9e7eb-121">Portanto, a noção de um segundo é um byte.</span><span class="sxs-lookup"><span data-stu-id="9e7eb-121">Thus, notionally one second is one byte.</span></span> <span data-ttu-id="9e7eb-122">Para localizar os deslocamentos de bytes reais, chame [**IMediaSample:: getTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-gettime) e divida os resultados por unidades.</span><span class="sxs-lookup"><span data-stu-id="9e7eb-122">To find the actual byte offsets, call [**IMediaSample::GetTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-gettime) and divide the results by UNITS.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e7eb-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9e7eb-123">Requirements</span></span>



| <span data-ttu-id="9e7eb-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e7eb-124">Requirement</span></span> | <span data-ttu-id="9e7eb-125">Valor</span><span class="sxs-lookup"><span data-stu-id="9e7eb-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e7eb-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9e7eb-126">Header</span></span><br/>  | <dl> <span data-ttu-id="9e7eb-127"><dt>Pullpin. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e7eb-127"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="9e7eb-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9e7eb-128">Library</span></span><br/> | <dl> <span data-ttu-id="9e7eb-129"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="9e7eb-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e7eb-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="9e7eb-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e7eb-131">**Classe CPullPin**</span><span class="sxs-lookup"><span data-stu-id="9e7eb-131">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 




