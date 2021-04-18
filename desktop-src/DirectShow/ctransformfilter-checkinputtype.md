---
description: O método CheckInputType verifica se um tipo de mídia especificado é aceitável para a entrada.
ms.assetid: 11f156f7-add2-45be-a0d3-05d21f596b89
title: Método CTransformFilter. CheckInputType (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.CheckInputType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 63c48a0502ee074b0940f85386dca0619a3ad12d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750037"
---
# <a name="ctransformfiltercheckinputtype-method"></a><span data-ttu-id="eb933-103">Método CTransformFilter. CheckInputType</span><span class="sxs-lookup"><span data-stu-id="eb933-103">CTransformFilter.CheckInputType method</span></span>

<span data-ttu-id="eb933-104">O `CheckInputType` método verifica se um tipo de mídia especificado é aceitável para entrada.</span><span class="sxs-lookup"><span data-stu-id="eb933-104">The `CheckInputType` method checks whether a specified media type is acceptable for input.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb933-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="eb933-105">Syntax</span></span>


```C++
virtual HRESULT CheckInputType(
   const CMediaType *mtIn
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="eb933-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="eb933-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb933-107">*mtIn*</span><span class="sxs-lookup"><span data-stu-id="eb933-107">*mtIn*</span></span> 
</dt> <dd>

<span data-ttu-id="eb933-108">Ponteiro para um objeto [**CMediaType**](cmediatype.md) que especifica o tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="eb933-108">Pointer to a [**CMediaType**](cmediatype.md) object that specifies the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb933-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="eb933-109">Return value</span></span>

<span data-ttu-id="eb933-110">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="eb933-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="eb933-111">Os valores possíveis incluem os mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="eb933-111">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="eb933-112">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="eb933-112">Return code</span></span>                                                                                                | <span data-ttu-id="eb933-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="eb933-113">Description</span></span>                              |
|------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <span data-ttu-id="eb933-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="eb933-114"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="eb933-115">O tipo de mídia é aceitável.</span><span class="sxs-lookup"><span data-stu-id="eb933-115">Media type is acceptable.</span></span><br/>     |
| <dl> <span data-ttu-id="eb933-116"><dt>**\_tipo E \_ VFW \_ não \_ aceito**</dt></span><span class="sxs-lookup"><span data-stu-id="eb933-116"><dt>**VFW\_E\_TYPE\_NOT\_ACCEPTED**</dt></span></span> </dl> | <span data-ttu-id="eb933-117">O tipo de mídia não é aceitável.</span><span class="sxs-lookup"><span data-stu-id="eb933-117">Media type is not acceptable.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="eb933-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="eb933-118">Remarks</span></span>

<span data-ttu-id="eb933-119">A classe derivada deve implementar esse método.</span><span class="sxs-lookup"><span data-stu-id="eb933-119">The derived class must implement this method.</span></span> <span data-ttu-id="eb933-120">Retorne \_ os S ok se o formato de entrada proposto for aceitável ou um código de erro do contrário.</span><span class="sxs-lookup"><span data-stu-id="eb933-120">Return S\_OK if the proposed input format is acceptable, or an error code otherwise.</span></span>

<span data-ttu-id="eb933-121">Esse método não precisa verificar se o formato de entrada é compatível com o formato de saída (se houver).</span><span class="sxs-lookup"><span data-stu-id="eb933-121">This method does not need to verify that the input format is compatible with the output format (if any).</span></span> <span data-ttu-id="eb933-122">O PIN de entrada verifica isso chamando o método [**CheckTransform**](ctransformfilter-checktransform.md) .</span><span class="sxs-lookup"><span data-stu-id="eb933-122">The input pin verifies that by calling the [**CheckTransform**](ctransformfilter-checktransform.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb933-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eb933-123">Requirements</span></span>



| <span data-ttu-id="eb933-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="eb933-124">Requirement</span></span> | <span data-ttu-id="eb933-125">Valor</span><span class="sxs-lookup"><span data-stu-id="eb933-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb933-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="eb933-126">Header</span></span><br/>  | <dl> <span data-ttu-id="eb933-127"><dt>Transfrm. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="eb933-127"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="eb933-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="eb933-128">Library</span></span><br/> | <dl> <span data-ttu-id="eb933-129"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="eb933-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb933-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="eb933-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb933-131">**Classe CTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="eb933-131">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




