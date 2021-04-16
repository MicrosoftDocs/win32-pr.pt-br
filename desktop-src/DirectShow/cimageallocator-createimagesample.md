---
description: O método CreateImageSample cria um exemplo de mídia.
ms.assetid: dae71692-5cbc-4bc7-a363-41766ef17c58
title: Método CImageAllocator. CreateImageSample (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator.CreateImageSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 57463a7025ea816b6fe6bcaa8b964231458903de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750045"
---
# <a name="cimageallocatorcreateimagesample-method"></a><span data-ttu-id="685a8-103">Método CImageAllocator. CreateImageSample</span><span class="sxs-lookup"><span data-stu-id="685a8-103">CImageAllocator.CreateImageSample method</span></span>

<span data-ttu-id="685a8-104">O `CreateImageSample` método cria um exemplo de mídia.</span><span class="sxs-lookup"><span data-stu-id="685a8-104">The `CreateImageSample` method creates a media sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="685a8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="685a8-105">Syntax</span></span>


```C++
virtual CImageSample* CreateImageSample(
   LPBYTE pData,
   LONG   Length
);
```



## <a name="parameters"></a><span data-ttu-id="685a8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="685a8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="685a8-107">*pData*</span><span class="sxs-lookup"><span data-stu-id="685a8-107">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="685a8-108">Ponteiro para um buffer de *comprimento* de tamanho, alocado pelo chamador.</span><span class="sxs-lookup"><span data-stu-id="685a8-108">Pointer to a buffer of size *Length*, allocated by the caller.</span></span>

</dd> <dt>

<span data-ttu-id="685a8-109">*Comprimento*</span><span class="sxs-lookup"><span data-stu-id="685a8-109">*Length*</span></span> 
</dt> <dd>

<span data-ttu-id="685a8-110">Comprimento do buffer.</span><span class="sxs-lookup"><span data-stu-id="685a8-110">Length of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="685a8-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="685a8-111">Return value</span></span>

<span data-ttu-id="685a8-112">Retorna um objeto [**CImageSample**](cimagesample.md) .</span><span class="sxs-lookup"><span data-stu-id="685a8-112">Returns a [**CImageSample**](cimagesample.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="685a8-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="685a8-113">Remarks</span></span>

<span data-ttu-id="685a8-114">Esse método cria um novo exemplo de mídia, implementado como um objeto **CImageSample** .</span><span class="sxs-lookup"><span data-stu-id="685a8-114">This method creates a new media sample, implemented as a **CImageSample** object.</span></span> <span data-ttu-id="685a8-115">O método [**IMediaSample:: GetPointer**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) do exemplo retorna um ponteiro para o buffer especificado no parâmetro *pData* .</span><span class="sxs-lookup"><span data-stu-id="685a8-115">The sample's [**IMediaSample::GetPointer**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) method returns a pointer to the buffer specified in the *pData* parameter.</span></span>

<span data-ttu-id="685a8-116">Se você derivar uma nova classe de alocador de [**CImageAllocator**](cimageallocator.md) e uma nova classe de exemplo de mídia de [**CImageSample**](cimagesample.md), deverá substituir esse método para criar uma instância da classe de exemplo de mídia.</span><span class="sxs-lookup"><span data-stu-id="685a8-116">If you derive a new allocator class from [**CImageAllocator**](cimageallocator.md) and a new media sample class from [**CImageSample**](cimagesample.md), you should override this method to create an instance of your media sample class.</span></span>

## <a name="requirements"></a><span data-ttu-id="685a8-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="685a8-117">Requirements</span></span>



| <span data-ttu-id="685a8-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="685a8-118">Requirement</span></span> | <span data-ttu-id="685a8-119">Valor</span><span class="sxs-lookup"><span data-stu-id="685a8-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="685a8-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="685a8-120">Header</span></span><br/>  | <dl> <span data-ttu-id="685a8-121"><dt>Winutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="685a8-121"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="685a8-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="685a8-122">Library</span></span><br/> | <dl> <span data-ttu-id="685a8-123"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="685a8-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="685a8-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="685a8-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="685a8-125">**Classe CImageAllocator**</span><span class="sxs-lookup"><span data-stu-id="685a8-125">**CImageAllocator Class**</span></span>](cimageallocator.md)
</dt> <dt>

[<span data-ttu-id="685a8-126">**CImageAllocator:: Alloc**</span><span class="sxs-lookup"><span data-stu-id="685a8-126">**CImageAllocator::Alloc**</span></span>](cimageallocator-alloc.md)
</dt> </dl>

 

 




