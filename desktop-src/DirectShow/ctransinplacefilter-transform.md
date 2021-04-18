---
description: O método Transform transforma um exemplo em vigor.
ms.assetid: 2268041b-70d4-48a9-9bb8-4ab921cce649
title: Método CTransInPlaceFilter. Transform (TRANSip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.Transform
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d5b84f326807f730745268a217b6066dacb9aaa7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758480"
---
# <a name="ctransinplacefiltertransform-method"></a><span data-ttu-id="74522-103">Método CTransInPlaceFilter. Transform</span><span class="sxs-lookup"><span data-stu-id="74522-103">CTransInPlaceFilter.Transform method</span></span>

<span data-ttu-id="74522-104">O `Transform` método transforma um exemplo em vigor.</span><span class="sxs-lookup"><span data-stu-id="74522-104">The `Transform` method transforms a sample in place.</span></span>

## <a name="syntax"></a><span data-ttu-id="74522-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="74522-105">Syntax</span></span>


```C++
virtual HRESULT Transform(
   IMediaSample *pSample
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="74522-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="74522-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74522-107">*pSample*</span><span class="sxs-lookup"><span data-stu-id="74522-107">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="74522-108">Ponteiro para a interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) do exemplo.</span><span class="sxs-lookup"><span data-stu-id="74522-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74522-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="74522-109">Return value</span></span>

<span data-ttu-id="74522-110">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="74522-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="74522-111">Os valores possíveis incluem os mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="74522-111">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="74522-112">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="74522-112">Return code</span></span>                                                                             | <span data-ttu-id="74522-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="74522-113">Description</span></span>                            |
|-----------------------------------------------------------------------------------------|----------------------------------------|
| <dl> <span data-ttu-id="74522-114"><dt>**\_falso**</dt></span><span class="sxs-lookup"><span data-stu-id="74522-114"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="74522-115">Não entregar este exemplo.</span><span class="sxs-lookup"><span data-stu-id="74522-115">Do not deliver this sample.</span></span><br/> |
| <dl> <span data-ttu-id="74522-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="74522-116"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="74522-117">Êxito.</span><span class="sxs-lookup"><span data-stu-id="74522-117">Success.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="74522-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="74522-118">Remarks</span></span>

<span data-ttu-id="74522-119">A classe derivada deve implementar esse método.</span><span class="sxs-lookup"><span data-stu-id="74522-119">The derived class must implement this method.</span></span> <span data-ttu-id="74522-120">Transforme os dados de exemplo em vigor.</span><span class="sxs-lookup"><span data-stu-id="74522-120">Transform the sample data in place.</span></span> <span data-ttu-id="74522-121">Se o filtro estiver usando dois alocadores, ele copiará os dados do exemplo de entrada para um novo exemplo e passará a cópia para esse método.</span><span class="sxs-lookup"><span data-stu-id="74522-121">If the filter is using two allocators, it copies the data from the input sample to a new sample, and passes the copy to this method.</span></span>

<span data-ttu-id="74522-122">Se o filtro não deve entregar este exemplo (por exemplo, para dar suporte ao controle de qualidade), o método deve retornar S \_ false.</span><span class="sxs-lookup"><span data-stu-id="74522-122">If the filter should not deliver this sample (for example, to support quality control), the method should return S\_FALSE.</span></span>

## <a name="requirements"></a><span data-ttu-id="74522-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="74522-123">Requirements</span></span>



| <span data-ttu-id="74522-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="74522-124">Requirement</span></span> | <span data-ttu-id="74522-125">Valor</span><span class="sxs-lookup"><span data-stu-id="74522-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74522-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="74522-126">Header</span></span><br/>  | <dl> <span data-ttu-id="74522-127"><dt>TRANSip. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="74522-127"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="74522-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="74522-128">Library</span></span><br/> | <dl> <span data-ttu-id="74522-129"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="74522-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74522-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="74522-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74522-131">**Classe CTransInPlaceFilter**</span><span class="sxs-lookup"><span data-stu-id="74522-131">**CTransInPlaceFilter Class**</span></span>](ctransinplacefilter.md)
</dt> </dl>

 

 




