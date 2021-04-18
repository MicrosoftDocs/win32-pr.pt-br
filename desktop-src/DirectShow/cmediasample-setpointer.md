---
description: O método SetPointer define o ponteiro para o buffer de memória.
ms.assetid: 60627600-c982-462e-b540-327a58e57615
title: Método CMediaSample. setpointr (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetPointer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 67d9fc5d260cc627919a458593328c36f0de9a94
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779553"
---
# <a name="cmediasamplesetpointer-method"></a><span data-ttu-id="ab463-103">Método CMediaSample. setpointr</span><span class="sxs-lookup"><span data-stu-id="ab463-103">CMediaSample.SetPointer method</span></span>

<span data-ttu-id="ab463-104">O `SetPointer` método define o ponteiro para o buffer de memória.</span><span class="sxs-lookup"><span data-stu-id="ab463-104">The `SetPointer` method sets the pointer to the memory buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab463-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ab463-105">Syntax</span></span>


```C++
HRESULT SetPointer(
   BYTE *ptr,
   LONG cBytes
);
```



## <a name="parameters"></a><span data-ttu-id="ab463-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ab463-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab463-107">*ptr*</span><span class="sxs-lookup"><span data-stu-id="ab463-107">*ptr*</span></span> 
</dt> <dd>

<span data-ttu-id="ab463-108">Ponteiro para um buffer de memória alocado pelo chamador, de tamanho *cBytes*.</span><span class="sxs-lookup"><span data-stu-id="ab463-108">Pointer to a memory buffer allocated by the caller, of size *cBytes*.</span></span>

</dd> <dt>

<span data-ttu-id="ab463-109">*cBytes*</span><span class="sxs-lookup"><span data-stu-id="ab463-109">*cBytes*</span></span> 
</dt> <dd>

<span data-ttu-id="ab463-110">Comprimento do buffer, em bytes.</span><span class="sxs-lookup"><span data-stu-id="ab463-110">Length of the buffer, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab463-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ab463-111">Return value</span></span>

<span data-ttu-id="ab463-112">Retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ab463-112">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab463-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="ab463-113">Remarks</span></span>

<span data-ttu-id="ab463-114">Esse método permite que o alocador defina um novo ponteiro para o exemplo.</span><span class="sxs-lookup"><span data-stu-id="ab463-114">This method enables the allocator to set a new pointer for the sample.</span></span>

<span data-ttu-id="ab463-115">Esse método não está disponível por meio da interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) .</span><span class="sxs-lookup"><span data-stu-id="ab463-115">This method is not available through the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span> <span data-ttu-id="ab463-116">O objeto que cria o exemplo pode acessar esse método (por meio de **CMediaSample**), mas outros objetos não podem.</span><span class="sxs-lookup"><span data-stu-id="ab463-116">The object that creates the sample can access this method (through **CMediaSample**), but other objects cannot.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab463-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ab463-117">Requirements</span></span>



| <span data-ttu-id="ab463-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab463-118">Requirement</span></span> | <span data-ttu-id="ab463-119">Valor</span><span class="sxs-lookup"><span data-stu-id="ab463-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab463-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ab463-120">Header</span></span><br/>  | <dl> <span data-ttu-id="ab463-121"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ab463-121"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="ab463-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ab463-122">Library</span></span><br/> | <dl> <span data-ttu-id="ab463-123"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="ab463-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab463-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="ab463-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab463-125">**Classe CMediaSample**</span><span class="sxs-lookup"><span data-stu-id="ab463-125">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




