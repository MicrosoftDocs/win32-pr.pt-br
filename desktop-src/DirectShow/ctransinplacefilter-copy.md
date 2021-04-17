---
description: O método Copy copia um exemplo de mídia.
ms.assetid: 3fbc6925-6e9c-4419-ab0d-0bbdbdf9bb8e
title: Método CTransInPlaceFilter. Copy (TRANSip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.Copy
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3063427611cd3a5aae74fecf6be273c07fdb917c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105766273"
---
# <a name="ctransinplacefiltercopy-method"></a><span data-ttu-id="8496c-103">Método CTransInPlaceFilter. Copy</span><span class="sxs-lookup"><span data-stu-id="8496c-103">CTransInPlaceFilter.Copy method</span></span>

<span data-ttu-id="8496c-104">O `Copy` método copia um exemplo de mídia.</span><span class="sxs-lookup"><span data-stu-id="8496c-104">The `Copy` method copies a media sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="8496c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8496c-105">Syntax</span></span>


```C++
IMediaSample* Copy(
   IMediaSample *pSource
);
```



## <a name="parameters"></a><span data-ttu-id="8496c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8496c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8496c-107">*pSource*</span><span class="sxs-lookup"><span data-stu-id="8496c-107">*pSource*</span></span> 
</dt> <dd>

<span data-ttu-id="8496c-108">Ponteiro para a interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) do exemplo.</span><span class="sxs-lookup"><span data-stu-id="8496c-108">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface of the sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8496c-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8496c-109">Return value</span></span>

<span data-ttu-id="8496c-110">Retorna um ponteiro para a interface **IMediaSample** no novo exemplo.</span><span class="sxs-lookup"><span data-stu-id="8496c-110">Returns a pointer to the **IMediaSample** interface on the new sample.</span></span>

## <a name="remarks"></a><span data-ttu-id="8496c-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="8496c-111">Remarks</span></span>

<span data-ttu-id="8496c-112">Esse método recupera um buffer vazio do alocador downstream.</span><span class="sxs-lookup"><span data-stu-id="8496c-112">This method retrieves an empty buffer from the downstream allocator.</span></span> <span data-ttu-id="8496c-113">Ele copia Todas as propriedades de exemplo de *pSource* para o novo exemplo, juntamente com os dados reais no exemplo.</span><span class="sxs-lookup"><span data-stu-id="8496c-113">It copies all of the sample properties from *pSource* into the new sample, along with the actual data in the sample.</span></span> <span data-ttu-id="8496c-114">Se o filtro estiver usando dois alocadores, ele chamará esse método para copiar dados entre buffers.</span><span class="sxs-lookup"><span data-stu-id="8496c-114">If the filter is using two allocators, it calls this method to copy data across buffers.</span></span>

## <a name="requirements"></a><span data-ttu-id="8496c-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8496c-115">Requirements</span></span>



| <span data-ttu-id="8496c-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="8496c-116">Requirement</span></span> | <span data-ttu-id="8496c-117">Valor</span><span class="sxs-lookup"><span data-stu-id="8496c-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8496c-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8496c-118">Header</span></span><br/>  | <dl> <span data-ttu-id="8496c-119"><dt>TRANSip. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8496c-119"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="8496c-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8496c-120">Library</span></span><br/> | <dl> <span data-ttu-id="8496c-121"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="8496c-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8496c-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="8496c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8496c-123">**Classe CTransInPlaceFilter**</span><span class="sxs-lookup"><span data-stu-id="8496c-123">**CTransInPlaceFilter Class**</span></span>](ctransinplacefilter.md)
</dt> </dl>

 

 




