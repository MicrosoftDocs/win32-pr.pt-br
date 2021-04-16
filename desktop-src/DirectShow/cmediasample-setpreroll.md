---
description: 'O método SetPreroll especifica se este exemplo é uma amostra de preversão. Um exemplo de preroll não deve ser exibido. Esse método implementa o método IMediaSample:: SetPreroll.'
ms.assetid: 2887e627-5999-407a-88d3-811c803c9a43
title: Método CMediaSample. SetPreroll (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetPreroll
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 594f26ebb738a986c85a14b88f8896b122b58f47
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754262"
---
# <a name="cmediasamplesetpreroll-method"></a><span data-ttu-id="7a2b2-105">Método CMediaSample. SetPreroll</span><span class="sxs-lookup"><span data-stu-id="7a2b2-105">CMediaSample.SetPreroll method</span></span>

<span data-ttu-id="7a2b2-106">O `SetPreroll` método especifica se este exemplo é uma amostra de preversão.</span><span class="sxs-lookup"><span data-stu-id="7a2b2-106">The `SetPreroll` method specifies whether this sample is a preroll sample.</span></span> <span data-ttu-id="7a2b2-107">Um exemplo de preroll não deve ser exibido.</span><span class="sxs-lookup"><span data-stu-id="7a2b2-107">A preroll sample should not be displayed.</span></span> <span data-ttu-id="7a2b2-108">Esse método implementa o método [**IMediaSample:: SetPreroll**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setpreroll) .</span><span class="sxs-lookup"><span data-stu-id="7a2b2-108">This method implements the [**IMediaSample::SetPreroll**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setpreroll) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a2b2-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7a2b2-109">Syntax</span></span>


```C++
HRESULT SetPreroll(
   BOOL bIsPreroll
);
```



## <a name="parameters"></a><span data-ttu-id="7a2b2-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7a2b2-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a2b2-111">*bIsPreroll*</span><span class="sxs-lookup"><span data-stu-id="7a2b2-111">*bIsPreroll*</span></span> 
</dt> <dd>

<span data-ttu-id="7a2b2-112">Valor booliano que especifica se este é um exemplo de preversão.</span><span class="sxs-lookup"><span data-stu-id="7a2b2-112">Boolean value that specifies whether this is a preroll sample.</span></span> <span data-ttu-id="7a2b2-113">Se for **verdadeiro**, este é um exemplo de preversão.</span><span class="sxs-lookup"><span data-stu-id="7a2b2-113">If **TRUE**, this is a preroll sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a2b2-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7a2b2-114">Return value</span></span>

<span data-ttu-id="7a2b2-115">Retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7a2b2-115">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a2b2-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="7a2b2-116">Remarks</span></span>

<span data-ttu-id="7a2b2-117">Esse método atualiza a variável de membro [**CMediaSample:: m \_ dwFlags**](cmediasample-m-dwflags.md) , que especifica a propriedade de preversão.</span><span class="sxs-lookup"><span data-stu-id="7a2b2-117">This method updates the [**CMediaSample::m\_dwFlags**](cmediasample-m-dwflags.md) member variable, which specifies the preroll property.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a2b2-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7a2b2-118">Requirements</span></span>



| <span data-ttu-id="7a2b2-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a2b2-119">Requirement</span></span> | <span data-ttu-id="7a2b2-120">Valor</span><span class="sxs-lookup"><span data-stu-id="7a2b2-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a2b2-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7a2b2-121">Header</span></span><br/>  | <dl> <span data-ttu-id="7a2b2-122"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7a2b2-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="7a2b2-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7a2b2-123">Library</span></span><br/> | <dl> <span data-ttu-id="7a2b2-124"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="7a2b2-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a2b2-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="7a2b2-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a2b2-126">**Classe CMediaSample**</span><span class="sxs-lookup"><span data-stu-id="7a2b2-126">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




