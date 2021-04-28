---
description: Construtor CMediaType. CMediaType (mtype. h)-método de construtor.
ms.assetid: 35198320-d028-42d4-823f-4f8346d8f977
title: Construtor CMediaType. CMediaType (mtype. h)-parâmetros cmtype e PHR
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.CMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dd91252920c74d45e4218be3c3d03249a116bfcf
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095414"
---
# <a name="cmediatypecmediatype-constructor-mtypeh"></a><span data-ttu-id="82d1e-103">Construtor CMediaType. CMediaType (mtype. h)</span><span class="sxs-lookup"><span data-stu-id="82d1e-103">CMediaType.CMediaType constructor (Mtype.h)</span></span>

<span data-ttu-id="82d1e-104">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="82d1e-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="82d1e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="82d1e-105">Syntax</span></span>


```C++
CMediaType(
  [ref] const CMediaType &cmtype,
              HRESULT    *phr = NULL
);
```



## <a name="parameters"></a><span data-ttu-id="82d1e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="82d1e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82d1e-107">*cmtype* \[ referência\]</span><span class="sxs-lookup"><span data-stu-id="82d1e-107">*cmtype* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="82d1e-108">Referência a um `CMediaType` objeto.</span><span class="sxs-lookup"><span data-stu-id="82d1e-108">Reference to a `CMediaType` object.</span></span> <span data-ttu-id="82d1e-109">O construtor copia o tipo de mídia para o novo objeto, incluindo o bloco de formato, se houver.</span><span class="sxs-lookup"><span data-stu-id="82d1e-109">The constructor copies the media type to the new object, including the format block, if any.</span></span>

</dd> <dt>

<span data-ttu-id="82d1e-110">*phr*</span><span class="sxs-lookup"><span data-stu-id="82d1e-110">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="82d1e-111">Ponteiro para uma variável que recebe um valor HRESULT.</span><span class="sxs-lookup"><span data-stu-id="82d1e-111">Pointer to a variable that receives an HRESULT value.</span></span> <span data-ttu-id="82d1e-112">Esse parâmetro pode ser um ponteiro **nulo** .</span><span class="sxs-lookup"><span data-stu-id="82d1e-112">This parameter can be a **NULL** pointer.</span></span> <span data-ttu-id="82d1e-113">Caso contrário, o chamador deve definir o valor como S \_ OK antes de chamar o construtor.</span><span class="sxs-lookup"><span data-stu-id="82d1e-113">Otherwise, the caller must set the value to S\_OK before calling the constructor.</span></span> <span data-ttu-id="82d1e-114">Se o Construtor falhar, ele definirá o valor como um código de falha.</span><span class="sxs-lookup"><span data-stu-id="82d1e-114">If the constructor fails, it sets the value to a failure code.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="82d1e-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="82d1e-115">Remarks</span></span>

<span data-ttu-id="82d1e-116">O construtor chama o método [**CMediaType:: InitMediaType**](cmediatype-initmediatype.md) para inicializar o tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="82d1e-116">The constructor calls the [**CMediaType::InitMediaType**](cmediatype-initmediatype.md) method to initialize the media type.</span></span>

## <a name="requirements"></a><span data-ttu-id="82d1e-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="82d1e-117">Requirements</span></span>



| <span data-ttu-id="82d1e-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="82d1e-118">Requirement</span></span> | <span data-ttu-id="82d1e-119">Valor</span><span class="sxs-lookup"><span data-stu-id="82d1e-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82d1e-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="82d1e-120">Header</span></span><br/>  | <dl> <span data-ttu-id="82d1e-121"><dt>Mtype. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="82d1e-121"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="82d1e-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="82d1e-122">Library</span></span><br/> | <dl> <span data-ttu-id="82d1e-123"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="82d1e-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82d1e-124">Consulte também</span><span class="sxs-lookup"><span data-stu-id="82d1e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82d1e-125">**Classe CMediaType**</span><span class="sxs-lookup"><span data-stu-id="82d1e-125">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




