---
description: O método CheckTransform verifica se um tipo de mídia de entrada é compatível com um tipo de mídia de saída.
ms.assetid: 349145e5-c12d-41df-ae37-7846f8aaa423
title: Método CTransformFilter. CheckTransform (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.CheckTransform
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2b3302304e6a0f9df41005f7ed63d9316a3cd410
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747586"
---
# <a name="ctransformfilterchecktransform-method"></a><span data-ttu-id="a2b41-103">Método CTransformFilter. CheckTransform</span><span class="sxs-lookup"><span data-stu-id="a2b41-103">CTransformFilter.CheckTransform method</span></span>

<span data-ttu-id="a2b41-104">O `CheckTransform` método verifica se um tipo de mídia de entrada é compatível com um tipo de mídia de saída.</span><span class="sxs-lookup"><span data-stu-id="a2b41-104">The `CheckTransform` method checks whether an input media type is compatible with an output media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2b41-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a2b41-105">Syntax</span></span>


```C++
virtual HRESULT CheckTransform(
   const CMediaType *mtIn,
   const CMediaType *mtOut
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="a2b41-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a2b41-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2b41-107">*mtIn*</span><span class="sxs-lookup"><span data-stu-id="a2b41-107">*mtIn*</span></span> 
</dt> <dd>

<span data-ttu-id="a2b41-108">Ponteiro para um objeto [**CMediaType**](cmediatype.md) que especifica o tipo de entrada.</span><span class="sxs-lookup"><span data-stu-id="a2b41-108">Pointer to a [**CMediaType**](cmediatype.md) object that specifies the input type.</span></span>

</dd> <dt>

<span data-ttu-id="a2b41-109">*mtOut*</span><span class="sxs-lookup"><span data-stu-id="a2b41-109">*mtOut*</span></span> 
</dt> <dd>

<span data-ttu-id="a2b41-110">Ponteiro para um objeto [**CMediaType**](cmediatype.md) que especifica o tipo de saída.</span><span class="sxs-lookup"><span data-stu-id="a2b41-110">Pointer to a [**CMediaType**](cmediatype.md) object that specifies the output type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2b41-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a2b41-111">Return value</span></span>

<span data-ttu-id="a2b41-112">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a2b41-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="a2b41-113">Os valores possíveis incluem os mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="a2b41-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="a2b41-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="a2b41-114">Return code</span></span>                                                                                                | <span data-ttu-id="a2b41-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="a2b41-115">Description</span></span>                                    |
|------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="a2b41-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a2b41-116"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="a2b41-117">Os tipos de mídia são compatíveis.</span><span class="sxs-lookup"><span data-stu-id="a2b41-117">The media types are compatible.</span></span><br/>     |
| <dl> <span data-ttu-id="a2b41-118"><dt>**\_tipo E \_ VFW \_ não \_ aceito**</dt></span><span class="sxs-lookup"><span data-stu-id="a2b41-118"><dt>**VFW\_E\_TYPE\_NOT\_ACCEPTED**</dt></span></span> </dl> | <span data-ttu-id="a2b41-119">Os tipos de mídia não são compatíveis.</span><span class="sxs-lookup"><span data-stu-id="a2b41-119">The media types are not compatible.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a2b41-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="a2b41-120">Remarks</span></span>

<span data-ttu-id="a2b41-121">A classe derivada deve implementar esse método.</span><span class="sxs-lookup"><span data-stu-id="a2b41-121">The derived class must implement this method.</span></span> <span data-ttu-id="a2b41-122">Retorne \_ os S ok se o filtro puder aceitar os dois tipos de mídia especificados ou se um código de erro for diferente.</span><span class="sxs-lookup"><span data-stu-id="a2b41-122">Return S\_OK if the filter can accept both of the specified media types, or an error code otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2b41-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a2b41-123">Requirements</span></span>



| <span data-ttu-id="a2b41-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2b41-124">Requirement</span></span> | <span data-ttu-id="a2b41-125">Valor</span><span class="sxs-lookup"><span data-stu-id="a2b41-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2b41-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a2b41-126">Header</span></span><br/>  | <dl> <span data-ttu-id="a2b41-127"><dt>Transfrm. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a2b41-127"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="a2b41-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a2b41-128">Library</span></span><br/> | <dl> <span data-ttu-id="a2b41-129"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="a2b41-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




