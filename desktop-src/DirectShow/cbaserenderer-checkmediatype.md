---
description: O método CheckMediaType determina se o filtro aceita um tipo de mídia específico.
ms.assetid: 90d26cf6-443c-4a06-98c6-ffa14e27ee41
title: Método CBaseRenderer. CheckMediaType (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dc0d4fc70e9ed64f9481d827cb678eb3ff9721d4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758241"
---
# <a name="cbaserenderercheckmediatype-method"></a><span data-ttu-id="eea54-103">Método CBaseRenderer. CheckMediaType</span><span class="sxs-lookup"><span data-stu-id="eea54-103">CBaseRenderer.CheckMediaType method</span></span>

<span data-ttu-id="eea54-104">O `CheckMediaType` método determina se o filtro aceita um tipo de mídia específico.</span><span class="sxs-lookup"><span data-stu-id="eea54-104">The `CheckMediaType` method determines if the filter accepts a specific media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="eea54-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="eea54-105">Syntax</span></span>


```C++
virtual HRESULT CheckMediaType(
   const CMediaType *pmt
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="eea54-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="eea54-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eea54-107">*PMT*</span><span class="sxs-lookup"><span data-stu-id="eea54-107">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="eea54-108">Ponteiro para um objeto [**CMediaType**](cmediatype.md) que contém o tipo de mídia proposto.</span><span class="sxs-lookup"><span data-stu-id="eea54-108">Pointer to a [**CMediaType**](cmediatype.md) object that contains the proposed media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eea54-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="eea54-109">Return value</span></span>

<span data-ttu-id="eea54-110">Retornará S \_ OK se o tipo de mídia proposto for aceitável.</span><span class="sxs-lookup"><span data-stu-id="eea54-110">Returns S\_OK if the proposed media type is acceptable.</span></span> <span data-ttu-id="eea54-111">Caso contrário, retorna S \_ false ou um código de erro.</span><span class="sxs-lookup"><span data-stu-id="eea54-111">Otherwise, returns S\_FALSE or an error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="eea54-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="eea54-112">Remarks</span></span>

<span data-ttu-id="eea54-113">O pino de entrada chama esse método de seu próprio método [**CBasePin:: CheckMediaType**](cbasepin-checkmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="eea54-113">The input pin calls this method from its own [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) method.</span></span> <span data-ttu-id="eea54-114">A classe derivada deve implementar esse método.</span><span class="sxs-lookup"><span data-stu-id="eea54-114">The derived class must implement this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="eea54-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eea54-115">Requirements</span></span>



| <span data-ttu-id="eea54-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="eea54-116">Requirement</span></span> | <span data-ttu-id="eea54-117">Valor</span><span class="sxs-lookup"><span data-stu-id="eea54-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eea54-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="eea54-118">Header</span></span><br/>  | <dl> <span data-ttu-id="eea54-119"><dt>Renbase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="eea54-119"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="eea54-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="eea54-120">Library</span></span><br/> | <dl> <span data-ttu-id="eea54-121"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="eea54-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eea54-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="eea54-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eea54-123">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="eea54-123">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




