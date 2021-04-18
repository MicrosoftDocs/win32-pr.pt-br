---
description: 'O método SetDiscontinuity especifica se este exemplo representa uma interrupção no fluxo de dados. Esse método implementa o método IMediaSample:: SetDiscontinuity.'
ms.assetid: 29072130-1ec7-4b5b-8a43-5308b1365527
title: Método CMediaSample. SetDiscontinuity (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetDiscontinuity
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 35565b2cee0284d0e5b9f85d7335a630b5f54e87
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810248"
---
# <a name="cmediasamplesetdiscontinuity-method"></a><span data-ttu-id="7e08b-104">Método CMediaSample. SetDiscontinuity</span><span class="sxs-lookup"><span data-stu-id="7e08b-104">CMediaSample.SetDiscontinuity method</span></span>

<span data-ttu-id="7e08b-105">O `SetDiscontinuity` método especifica se este exemplo representa uma interrupção no fluxo de dados.</span><span class="sxs-lookup"><span data-stu-id="7e08b-105">The `SetDiscontinuity` method specifies whether this sample represents a break in the data stream.</span></span> <span data-ttu-id="7e08b-106">Esse método implementa o método [**IMediaSample:: SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) .</span><span class="sxs-lookup"><span data-stu-id="7e08b-106">This method implements the [**IMediaSample::SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e08b-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7e08b-107">Syntax</span></span>


```C++
HRESULT SetDiscontinuity(
   BOOL bDiscont
);
```



## <a name="parameters"></a><span data-ttu-id="7e08b-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7e08b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e08b-109">*bDiscont*</span><span class="sxs-lookup"><span data-stu-id="7e08b-109">*bDiscont*</span></span> 
</dt> <dd>

<span data-ttu-id="7e08b-110">Valor booliano que especifica se este exemplo é uma descontinuidade.</span><span class="sxs-lookup"><span data-stu-id="7e08b-110">Boolean value that specifies whether this sample is a discontinuity.</span></span> <span data-ttu-id="7e08b-111">Se **for true**, o exemplo de mídia será descontínuo com o exemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="7e08b-111">If **TRUE**, the media sample is discontinuous with the previous sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e08b-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7e08b-112">Return value</span></span>

<span data-ttu-id="7e08b-113">Retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7e08b-113">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="7e08b-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="7e08b-114">Remarks</span></span>

<span data-ttu-id="7e08b-115">Esse método atualiza a variável de membro [**CMediaSample:: m \_ dwFlags**](cmediasample-m-dwflags.md) , que especifica a propriedade de descontinuidade.</span><span class="sxs-lookup"><span data-stu-id="7e08b-115">This method updates the [**CMediaSample::m\_dwFlags**](cmediasample-m-dwflags.md) member variable, which specifies the discontinuity property.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e08b-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7e08b-116">Requirements</span></span>



| <span data-ttu-id="7e08b-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e08b-117">Requirement</span></span> | <span data-ttu-id="7e08b-118">Valor</span><span class="sxs-lookup"><span data-stu-id="7e08b-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e08b-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7e08b-119">Header</span></span><br/>  | <dl> <span data-ttu-id="7e08b-120"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7e08b-120"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="7e08b-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7e08b-121">Library</span></span><br/> | <dl> <span data-ttu-id="7e08b-122"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="7e08b-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e08b-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="7e08b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e08b-124">**Classe CMediaSample**</span><span class="sxs-lookup"><span data-stu-id="7e08b-124">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




