---
description: 'O método SetProperties define as propriedades do exemplo. Esse método implementa o método IMediaSample2:: SetProperties.'
ms.assetid: 639aedf5-0c21-4578-b336-91859e40f3be
title: Método CMediaSample. SetProperties (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetProperties
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c5e6ef3c3839825586bf47259cf44783d167f503
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105785364"
---
# <a name="cmediasamplesetproperties-method"></a><span data-ttu-id="f65ad-104">Método CMediaSample. SetProperties</span><span class="sxs-lookup"><span data-stu-id="f65ad-104">CMediaSample.SetProperties method</span></span>

<span data-ttu-id="f65ad-105">O `SetProperties` método define as propriedades do exemplo.</span><span class="sxs-lookup"><span data-stu-id="f65ad-105">The `SetProperties` method sets the properties of the sample.</span></span> <span data-ttu-id="f65ad-106">Esse método implementa o método [**IMediaSample2:: SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-setproperties) .</span><span class="sxs-lookup"><span data-stu-id="f65ad-106">This method implements the [**IMediaSample2::SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-setproperties) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f65ad-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f65ad-107">Syntax</span></span>


```C++
HRESULT SetProperties(
         DWORD cbProperties,
   const BYTE  *pbProperties
);
```



## <a name="parameters"></a><span data-ttu-id="f65ad-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f65ad-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f65ad-109">*cbProperties*</span><span class="sxs-lookup"><span data-stu-id="f65ad-109">*cbProperties*</span></span> 
</dt> <dd>

<span data-ttu-id="f65ad-110">Comprimento dos dados de propriedade a serem definidos, em bytes.</span><span class="sxs-lookup"><span data-stu-id="f65ad-110">Length of property data to set, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="f65ad-111">*pbProperties*</span><span class="sxs-lookup"><span data-stu-id="f65ad-111">*pbProperties*</span></span> 
</dt> <dd>

<span data-ttu-id="f65ad-112">Ponteiro para um buffer de tamanho *cbProperties*.</span><span class="sxs-lookup"><span data-stu-id="f65ad-112">Pointer to a buffer of size *cbProperties*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f65ad-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f65ad-113">Return value</span></span>

<span data-ttu-id="f65ad-114">Retorna um dos valores **HRESULT** mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="f65ad-114">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="f65ad-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="f65ad-115">Return code</span></span>                                                                                   | <span data-ttu-id="f65ad-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="f65ad-116">Description</span></span>                          |
|-----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="f65ad-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f65ad-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="f65ad-118">Sucesso</span><span class="sxs-lookup"><span data-stu-id="f65ad-118">Success</span></span><br/>                   |
| <dl> <span data-ttu-id="f65ad-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="f65ad-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="f65ad-120">Argumento inválido</span><span class="sxs-lookup"><span data-stu-id="f65ad-120">Invalid argument</span></span><br/>          |
| <dl> <span data-ttu-id="f65ad-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="f65ad-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="f65ad-122">Memória insuficiente</span><span class="sxs-lookup"><span data-stu-id="f65ad-122">Insufficient memory</span></span><br/>       |
| <dl> <span data-ttu-id="f65ad-123"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="f65ad-123"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="f65ad-124">Argumento de ponteiro **nulo**</span><span class="sxs-lookup"><span data-stu-id="f65ad-124">**NULL** pointer argument</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="f65ad-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f65ad-125">Requirements</span></span>



| <span data-ttu-id="f65ad-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="f65ad-126">Requirement</span></span> | <span data-ttu-id="f65ad-127">Valor</span><span class="sxs-lookup"><span data-stu-id="f65ad-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f65ad-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f65ad-128">Header</span></span><br/>  | <dl> <span data-ttu-id="f65ad-129"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f65ad-129"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="f65ad-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f65ad-130">Library</span></span><br/> | <dl> <span data-ttu-id="f65ad-131"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="f65ad-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f65ad-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="f65ad-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f65ad-133">**Classe CMediaSample**</span><span class="sxs-lookup"><span data-stu-id="f65ad-133">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




