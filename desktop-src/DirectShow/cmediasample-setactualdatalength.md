---
description: 'O método SetActualDataLength define o comprimento dos dados válidos no buffer. Esse método implementa o método IMediaSample:: SetActualDataLength.'
ms.assetid: a80a67ef-e490-4874-a123-f2d193cec4d7
title: Método CMediaSample. SetActualDataLength (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetActualDataLength
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 825b02f43195424f9ceb5ecd23c4dcf26727ef8f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811327"
---
# <a name="cmediasamplesetactualdatalength-method"></a><span data-ttu-id="ce289-104">Método CMediaSample. SetActualDataLength</span><span class="sxs-lookup"><span data-stu-id="ce289-104">CMediaSample.SetActualDataLength method</span></span>

<span data-ttu-id="ce289-105">O `SetActualDataLength` método define o comprimento dos dados válidos no buffer.</span><span class="sxs-lookup"><span data-stu-id="ce289-105">The `SetActualDataLength` method sets the length of the valid data in the buffer.</span></span> <span data-ttu-id="ce289-106">Esse método implementa o método [**IMediaSample:: SetActualDataLength**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setactualdatalength) .</span><span class="sxs-lookup"><span data-stu-id="ce289-106">This method implements the [**IMediaSample::SetActualDataLength**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setactualdatalength) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce289-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ce289-107">Syntax</span></span>


```C++
HRESULT SetActualDataLength(
   long lLen
);
```



## <a name="parameters"></a><span data-ttu-id="ce289-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ce289-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce289-109">*lLen*</span><span class="sxs-lookup"><span data-stu-id="ce289-109">*lLen*</span></span> 
</dt> <dd>

<span data-ttu-id="ce289-110">Comprimento dos dados válidos, em bytes.</span><span class="sxs-lookup"><span data-stu-id="ce289-110">Length of the valid data, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce289-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ce289-111">Return value</span></span>

<span data-ttu-id="ce289-112">Retorna um dos valores **HRESULT** mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="ce289-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="ce289-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="ce289-113">Return code</span></span>                                                                                             | <span data-ttu-id="ce289-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="ce289-114">Description</span></span>                                                 |
|---------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <span data-ttu-id="ce289-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ce289-115"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="ce289-116">Êxito.</span><span class="sxs-lookup"><span data-stu-id="ce289-116">Success.</span></span><br/>                                         |
| <dl> <span data-ttu-id="ce289-117"><dt>**\_estouro de \_ buffer VFW E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ce289-117"><dt>**VFW\_E\_BUFFER\_OVERFLOW**</dt></span></span> </dl> | <span data-ttu-id="ce289-118">*llen* é maior do que o tamanho do buffer alocado.</span><span class="sxs-lookup"><span data-stu-id="ce289-118">*lLen* is larger than the allocated buffer size.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ce289-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="ce289-119">Remarks</span></span>

<span data-ttu-id="ce289-120">Esse método define a variável de membro [**CMediaSample:: m \_ lActual**](cmediasample-m-lactual.md) .</span><span class="sxs-lookup"><span data-stu-id="ce289-120">This method sets the [**CMediaSample::m\_lActual**](cmediasample-m-lactual.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce289-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ce289-121">Requirements</span></span>



| <span data-ttu-id="ce289-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce289-122">Requirement</span></span> | <span data-ttu-id="ce289-123">Valor</span><span class="sxs-lookup"><span data-stu-id="ce289-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce289-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ce289-124">Header</span></span><br/>  | <dl> <span data-ttu-id="ce289-125"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ce289-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="ce289-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ce289-126">Library</span></span><br/> | <dl> <span data-ttu-id="ce289-127"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="ce289-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce289-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="ce289-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce289-129">**Classe CMediaSample**</span><span class="sxs-lookup"><span data-stu-id="ce289-129">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




