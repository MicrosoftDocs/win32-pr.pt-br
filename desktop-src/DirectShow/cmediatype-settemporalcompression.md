---
description: O método SetTemporalCompression especifica se os exemplos são compactados usando a compactação temporal (entre quadros).
ms.assetid: cdd181ee-d1e9-48b0-96f6-e76db9f3f933
title: Método CMediaType. SetTemporalCompression (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetTemporalCompression
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a0aba07375c5b5c760c432de704562efb2bea148
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754261"
---
# <a name="cmediatypesettemporalcompression-method"></a><span data-ttu-id="742fb-103">Método CMediaType. SetTemporalCompression</span><span class="sxs-lookup"><span data-stu-id="742fb-103">CMediaType.SetTemporalCompression method</span></span>

<span data-ttu-id="742fb-104">O `SetTemporalCompression` método especifica se os exemplos são compactados usando a compactação temporal (entre quadros).</span><span class="sxs-lookup"><span data-stu-id="742fb-104">The `SetTemporalCompression` method specifies whether samples are compressed using temporal (interframe) compression.</span></span>

## <a name="syntax"></a><span data-ttu-id="742fb-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="742fb-105">Syntax</span></span>


```C++
void SetTemporalCompression(
   BOOL bCompressed
);
```



## <a name="parameters"></a><span data-ttu-id="742fb-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="742fb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="742fb-107">*bCompressed*</span><span class="sxs-lookup"><span data-stu-id="742fb-107">*bCompressed*</span></span> 
</dt> <dd>

<span data-ttu-id="742fb-108">Valor booliano que especifica se o fluxo usa compactação temporal.</span><span class="sxs-lookup"><span data-stu-id="742fb-108">Boolean value that specifies whether the stream uses temporal compression.</span></span> <span data-ttu-id="742fb-109">Se o fluxo usar a compactação temporal, defina o valor como **true**.</span><span class="sxs-lookup"><span data-stu-id="742fb-109">If the stream uses temporal compression, set the value to **TRUE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="742fb-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="742fb-110">Return value</span></span>

<span data-ttu-id="742fb-111">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="742fb-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="742fb-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="742fb-112">Remarks</span></span>

<span data-ttu-id="742fb-113">Esse método define o membro **bTemporalCompression** .</span><span class="sxs-lookup"><span data-stu-id="742fb-113">This method sets the **bTemporalCompression** member.</span></span>

## <a name="requirements"></a><span data-ttu-id="742fb-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="742fb-114">Requirements</span></span>



| <span data-ttu-id="742fb-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="742fb-115">Requirement</span></span> | <span data-ttu-id="742fb-116">Valor</span><span class="sxs-lookup"><span data-stu-id="742fb-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="742fb-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="742fb-117">Header</span></span><br/>  | <dl> <span data-ttu-id="742fb-118"><dt>Mtype. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="742fb-118"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="742fb-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="742fb-119">Library</span></span><br/> | <dl> <span data-ttu-id="742fb-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="742fb-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="742fb-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="742fb-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="742fb-122">**Classe CMediaType**</span><span class="sxs-lookup"><span data-stu-id="742fb-122">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




