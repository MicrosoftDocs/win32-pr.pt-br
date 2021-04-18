---
description: O método setvariableize especifica que os exemplos não têm um tamanho fixo.
ms.assetid: 2a207cdb-f8e6-44aa-8bf6-868267aeb42d
title: Método CMediaType. setvariableize (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetVariableSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4621a639b3bc18382bc41ae9425c4de50db920ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758545"
---
# <a name="cmediatypesetvariablesize-method"></a><span data-ttu-id="daf4f-103">Método CMediaType. setvariableize</span><span class="sxs-lookup"><span data-stu-id="daf4f-103">CMediaType.SetVariableSize method</span></span>

<span data-ttu-id="daf4f-104">O `SetVariableSize` método especifica que os exemplos não têm um tamanho fixo.</span><span class="sxs-lookup"><span data-stu-id="daf4f-104">The `SetVariableSize` method specifies that samples do not have a fixed size.</span></span>

## <a name="syntax"></a><span data-ttu-id="daf4f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="daf4f-105">Syntax</span></span>


```C++
void SetVariableSize();
```



## <a name="parameters"></a><span data-ttu-id="daf4f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="daf4f-106">Parameters</span></span>

<span data-ttu-id="daf4f-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="daf4f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="daf4f-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="daf4f-108">Return value</span></span>

<span data-ttu-id="daf4f-109">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="daf4f-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="daf4f-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="daf4f-110">Remarks</span></span>

<span data-ttu-id="daf4f-111">Esse método define o membro **bFixedSizeSamples** como **false**.</span><span class="sxs-lookup"><span data-stu-id="daf4f-111">This method sets the **bFixedSizeSamples** member to **FALSE**.</span></span> <span data-ttu-id="daf4f-112">As chamadas subsequentes para o método [**CMediaType:: Getsampleize**](cmediatype-getsamplesize.md) retornam zero.</span><span class="sxs-lookup"><span data-stu-id="daf4f-112">Subsequent calls to the [**CMediaType::GetSampleSize**](cmediatype-getsamplesize.md) method return zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="daf4f-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="daf4f-113">Requirements</span></span>



| <span data-ttu-id="daf4f-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="daf4f-114">Requirement</span></span> | <span data-ttu-id="daf4f-115">Valor</span><span class="sxs-lookup"><span data-stu-id="daf4f-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="daf4f-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="daf4f-116">Header</span></span><br/>  | <dl> <span data-ttu-id="daf4f-117"><dt>Mtype. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="daf4f-117"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="daf4f-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="daf4f-118">Library</span></span><br/> | <dl> <span data-ttu-id="daf4f-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="daf4f-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="daf4f-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="daf4f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="daf4f-121">**Classe CMediaType**</span><span class="sxs-lookup"><span data-stu-id="daf4f-121">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




