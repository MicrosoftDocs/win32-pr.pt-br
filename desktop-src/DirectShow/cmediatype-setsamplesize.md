---
description: O método setamostrate especifica um tamanho de amostra fixo ou especifica que os exemplos têm um tamanho variável.
ms.assetid: b0f9dd7b-4ff9-4d11-9c13-b52d7b1549b5
title: Método CMediaType. setsampleize (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetSampleSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0992afd0576c1039397e6ecaa2119a989283136e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105775630"
---
# <a name="cmediatypesetsamplesize-method"></a><span data-ttu-id="2ba08-103">Método CMediaType. setsampleize</span><span class="sxs-lookup"><span data-stu-id="2ba08-103">CMediaType.SetSampleSize method</span></span>

<span data-ttu-id="2ba08-104">O `SetSampleSize` método especifica um tamanho de amostra fixo ou especifica que os exemplos têm um tamanho variável.</span><span class="sxs-lookup"><span data-stu-id="2ba08-104">The `SetSampleSize` method specifies a fixed sample size, or specifies that samples have a variable size.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ba08-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2ba08-105">Syntax</span></span>


```C++
void SetSampleSize(
   ULONG sz
);
```



## <a name="parameters"></a><span data-ttu-id="2ba08-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2ba08-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ba08-107">*sz*</span><span class="sxs-lookup"><span data-stu-id="2ba08-107">*sz*</span></span> 
</dt> <dd>

<span data-ttu-id="2ba08-108">Tamanho da amostra, em bytes ou zero.</span><span class="sxs-lookup"><span data-stu-id="2ba08-108">Sample size, in bytes, or zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ba08-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2ba08-109">Return value</span></span>

<span data-ttu-id="2ba08-110">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="2ba08-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ba08-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="2ba08-111">Remarks</span></span>

<span data-ttu-id="2ba08-112">Se o valor de *sz* for zero, o tipo de mídia usará tamanhos de amostra variáveis.</span><span class="sxs-lookup"><span data-stu-id="2ba08-112">If value of *sz* is zero, the media type uses variable sample sizes.</span></span> <span data-ttu-id="2ba08-113">Caso contrário, o tamanho da amostra será corrigido em *sz* bytes.</span><span class="sxs-lookup"><span data-stu-id="2ba08-113">Otherwise, the sample size is fixed at *sz* bytes.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ba08-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2ba08-114">Requirements</span></span>



| <span data-ttu-id="2ba08-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ba08-115">Requirement</span></span> | <span data-ttu-id="2ba08-116">Valor</span><span class="sxs-lookup"><span data-stu-id="2ba08-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ba08-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2ba08-117">Header</span></span><br/>  | <dl> <span data-ttu-id="2ba08-118"><dt>Mtype. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2ba08-118"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="2ba08-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2ba08-119">Library</span></span><br/> | <dl> <span data-ttu-id="2ba08-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="2ba08-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ba08-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="2ba08-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ba08-122">**Classe CMediaType**</span><span class="sxs-lookup"><span data-stu-id="2ba08-122">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




