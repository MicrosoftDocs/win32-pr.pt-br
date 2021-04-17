---
description: O método Transform transforma um exemplo de entrada para produzir um exemplo de saída.
ms.assetid: 30ef8c0c-e834-481a-93ff-d06e6fa1ddeb
title: Método CTransformFilter. Transform (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.Transform
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8498a9a6ce266e0646dbbdcb4f322c093d6e0cc3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754220"
---
# <a name="ctransformfiltertransform-method"></a><span data-ttu-id="3d51c-103">Método CTransformFilter. Transform</span><span class="sxs-lookup"><span data-stu-id="3d51c-103">CTransformFilter.Transform method</span></span>

<span data-ttu-id="3d51c-104">O `Transform` método transforma um exemplo de entrada para produzir um exemplo de saída.</span><span class="sxs-lookup"><span data-stu-id="3d51c-104">The `Transform` method transforms an input sample to produce an output sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d51c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3d51c-105">Syntax</span></span>


```C++
virtual HRESULT Transform(
   IMediaSample *pIn,
   IMediaSample *pOut
);
```



## <a name="parameters"></a><span data-ttu-id="3d51c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3d51c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d51c-107">*Afixa*</span><span class="sxs-lookup"><span data-stu-id="3d51c-107">*pIn*</span></span> 
</dt> <dd>

<span data-ttu-id="3d51c-108">Ponteiro para a interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) do exemplo de entrada.</span><span class="sxs-lookup"><span data-stu-id="3d51c-108">Pointer to the input sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> <dt>

<span data-ttu-id="3d51c-109">*pOut*</span><span class="sxs-lookup"><span data-stu-id="3d51c-109">*pOut*</span></span> 
</dt> <dd>

<span data-ttu-id="3d51c-110">Ponteiro para a interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) da amostra de saída.</span><span class="sxs-lookup"><span data-stu-id="3d51c-110">Pointer to the output sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d51c-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3d51c-111">Return value</span></span>

<span data-ttu-id="3d51c-112">A classe base retorna E \_ inesperada.</span><span class="sxs-lookup"><span data-stu-id="3d51c-112">The base class returns E\_UNEXPECTED.</span></span>

<span data-ttu-id="3d51c-113">A classe derivada deve retornar um valor **HRESULT** , indicando êxito ou falha.</span><span class="sxs-lookup"><span data-stu-id="3d51c-113">The derived class should return an **HRESULT** value, indicating success or failure.</span></span> <span data-ttu-id="3d51c-114">Os valores possíveis incluem os mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="3d51c-114">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="3d51c-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="3d51c-115">Return code</span></span>                                                                             | <span data-ttu-id="3d51c-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="3d51c-116">Description</span></span>                            |
|-----------------------------------------------------------------------------------------|----------------------------------------|
| <dl> <span data-ttu-id="3d51c-117"><dt>**\_falso**</dt></span><span class="sxs-lookup"><span data-stu-id="3d51c-117"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="3d51c-118">Não entregar este exemplo.</span><span class="sxs-lookup"><span data-stu-id="3d51c-118">Do not deliver this sample.</span></span><br/> |
| <dl> <span data-ttu-id="3d51c-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3d51c-119"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="3d51c-120">Êxito.</span><span class="sxs-lookup"><span data-stu-id="3d51c-120">Success.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="3d51c-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="3d51c-121">Remarks</span></span>

<span data-ttu-id="3d51c-122">Substitua esse método para produzir dados de saída.</span><span class="sxs-lookup"><span data-stu-id="3d51c-122">Override this method to produce output data.</span></span> <span data-ttu-id="3d51c-123">Leia os dados de entrada do exemplo especificado pelo parâmetro *pIn* e grave os novos dados no exemplo especificado pelo parâmetro *pout* .</span><span class="sxs-lookup"><span data-stu-id="3d51c-123">Read the input data from the sample specified by the *pIn* parameter, and write the new data into the sample specified by the *pOut* parameter.</span></span>

<span data-ttu-id="3d51c-124">Antes que o filtro Chame esse método, ele copia as propriedades do exemplo de entrada para o exemplo de saída.</span><span class="sxs-lookup"><span data-stu-id="3d51c-124">Before the filter calls this method, it copies the properties from the input sample to the output sample.</span></span> <span data-ttu-id="3d51c-125">O `Transform` método deve definir todas as propriedades que diferem entre os dois exemplos, usando métodos **IMediaSample** ou a interface [**IMediaSample2**](/windows/desktop/api/Strmif/nn-strmif-imediasample2) (se disponível).</span><span class="sxs-lookup"><span data-stu-id="3d51c-125">The `Transform` method should set any properties that differ between the two samples, using **IMediaSample** methods or the [**IMediaSample2**](/windows/desktop/api/Strmif/nn-strmif-imediasample2) interface (if available).</span></span>

<span data-ttu-id="3d51c-126">Se o filtro não deve entregar este exemplo (por exemplo, para dar suporte ao controle de qualidade), o método deve retornar S \_ false.</span><span class="sxs-lookup"><span data-stu-id="3d51c-126">If the filter should not deliver this sample (for example, to support quality control), the method should return S\_FALSE.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d51c-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3d51c-127">Requirements</span></span>



| <span data-ttu-id="3d51c-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d51c-128">Requirement</span></span> | <span data-ttu-id="3d51c-129">Valor</span><span class="sxs-lookup"><span data-stu-id="3d51c-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d51c-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3d51c-130">Header</span></span><br/>  | <dl> <span data-ttu-id="3d51c-131"><dt>Transfrm. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3d51c-131"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="3d51c-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3d51c-132">Library</span></span><br/> | <dl> <span data-ttu-id="3d51c-133"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="3d51c-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d51c-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="3d51c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d51c-135">**Classe CTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="3d51c-135">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




