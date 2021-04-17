---
description: A classe CImageAllocator implementa um alocador que gerencia bitmaps independentes de dispositivo (DIBs) do GDI. Essa classe deriva da classe CBaseAllocator. Ele cria amostras de mídia que são implementadas usando a classe CImageSample.
ms.assetid: edda34a5-3916-4a41-9e2f-a19f12df0947
title: Classe CImageAllocator (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ea37dfe8cbbc7baf90e6065f0c54af1a60c3284b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758695"
---
# <a name="cimageallocator-class"></a><span data-ttu-id="462ad-105">Classe CImageAllocator</span><span class="sxs-lookup"><span data-stu-id="462ad-105">CImageAllocator class</span></span>

![hierarquia de classe cimageallocator](images/wutil04.png)

<span data-ttu-id="462ad-107">A `CImageAllocator` classe implementa um alocador que gerencia bitmaps (DIBs) independentes de dispositivo GDI.</span><span class="sxs-lookup"><span data-stu-id="462ad-107">The `CImageAllocator` class implements an allocator that manages GDI device-independent bitmaps (DIBs).</span></span> <span data-ttu-id="462ad-108">Essa classe deriva da classe [**CBaseAllocator**](cbaseallocator.md) .</span><span class="sxs-lookup"><span data-stu-id="462ad-108">This class derives from the [**CBaseAllocator**](cbaseallocator.md) class.</span></span> <span data-ttu-id="462ad-109">Ele cria amostras de mídia que são implementadas usando a classe [**CImageSample**](cimagesample.md) .</span><span class="sxs-lookup"><span data-stu-id="462ad-109">It creates media samples that are implemented using the [**CImageSample**](cimagesample.md) class.</span></span>

<span data-ttu-id="462ad-110">Um alocador é compartilhado por dois Pins conectados, mas sempre é de propriedade de um dos filtros na conexão.</span><span class="sxs-lookup"><span data-stu-id="462ad-110">An allocator is shared by two connected pins, but is always owned by one of the filters in the connection.</span></span> <span data-ttu-id="462ad-111">Um filtro que o usa `CImageAllocator` deve controlar se o alocador foi fornecido por si próprio ou por outro filtro.</span><span class="sxs-lookup"><span data-stu-id="462ad-111">A filter that uses `CImageAllocator` must keep track of whether the allocator was provided by itself or by the other filter.</span></span> <span data-ttu-id="462ad-112">Se o alocador tiver sido fornecido por si só, o filtro proprietário poderá contar com o fato de que todas as amostras de mídia do alocador são objetos **CImageSample** .</span><span class="sxs-lookup"><span data-stu-id="462ad-112">If the allocator was provided by itself, the owning filter can rely on the fact that all media samples from the allocator are **CImageSample** objects.</span></span> <span data-ttu-id="462ad-113">Portanto, ele pode usar o objeto **CImageSample** para obter informações sobre o DIB, que é armazenado em uma estrutura [**DIBDATA**](dibdata.md) .</span><span class="sxs-lookup"><span data-stu-id="462ad-113">It can therefore use the **CImageSample** object to obtain information about the DIB, which is stored in a [**DIBDATA**](dibdata.md) structure.</span></span>

<span data-ttu-id="462ad-114">O filtro proprietário deve chamar **NotifyMediaType** sempre que o tipo de mídia for alterado.</span><span class="sxs-lookup"><span data-stu-id="462ad-114">The owning filter should call **NotifyMediaType** whenever the media type changes.</span></span>



| <span data-ttu-id="462ad-115">Variáveis de membro protegido</span><span class="sxs-lookup"><span data-stu-id="462ad-115">Protected Member Variables</span></span>                                     | <span data-ttu-id="462ad-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="462ad-116">Description</span></span>                                                              |
|----------------------------------------------------------------|--------------------------------------------------------------------------|
| [<span data-ttu-id="462ad-117">**\_pFilter m**</span><span class="sxs-lookup"><span data-stu-id="462ad-117">**m\_pFilter**</span></span>](cimageallocator-m-pfilter.md)                | <span data-ttu-id="462ad-118">Ponteiro para o filtro proprietário.</span><span class="sxs-lookup"><span data-stu-id="462ad-118">Pointer to the owning filter.</span></span>                                            |
| [<span data-ttu-id="462ad-119">**\_pMediaType m**</span><span class="sxs-lookup"><span data-stu-id="462ad-119">**m\_pMediaType**</span></span>](cimageallocator-m-pmediatype.md)          | <span data-ttu-id="462ad-120">Ponteiro para o tipo de mídia atual.</span><span class="sxs-lookup"><span data-stu-id="462ad-120">Pointer to the current media type.</span></span>                                       |
| <span data-ttu-id="462ad-121">Métodos Protegidos</span><span class="sxs-lookup"><span data-stu-id="462ad-121">Protected Methods</span></span>                                              | <span data-ttu-id="462ad-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="462ad-122">Description</span></span>                                                              |
| [<span data-ttu-id="462ad-123">**Alocação**</span><span class="sxs-lookup"><span data-stu-id="462ad-123">**Alloc**</span></span>](cimageallocator-alloc.md)                         | <span data-ttu-id="462ad-124">Aloca memória para os buffers.</span><span class="sxs-lookup"><span data-stu-id="462ad-124">Allocates memory for the buffers.</span></span>                                        |
| [<span data-ttu-id="462ad-125">**CheckSizes**</span><span class="sxs-lookup"><span data-stu-id="462ad-125">**CheckSizes**</span></span>](cimageallocator-checksizes.md)               | <span data-ttu-id="462ad-126">Verifica as propriedades de alocador no tipo de mídia atual.</span><span class="sxs-lookup"><span data-stu-id="462ad-126">Checks allocator properties against the current media type.</span></span>              |
| [<span data-ttu-id="462ad-127">**CreateDIB**</span><span class="sxs-lookup"><span data-stu-id="462ad-127">**CreateDIB**</span></span>](cimageallocator-createdib.md)                 | <span data-ttu-id="462ad-128">Cria um DIB.</span><span class="sxs-lookup"><span data-stu-id="462ad-128">Creates a DIB.</span></span>                                                           |
| [<span data-ttu-id="462ad-129">**CreateImageSample**</span><span class="sxs-lookup"><span data-stu-id="462ad-129">**CreateImageSample**</span></span>](cimageallocator-createimagesample.md) | <span data-ttu-id="462ad-130">Cria um exemplo de mídia.</span><span class="sxs-lookup"><span data-stu-id="462ad-130">Creates a media sample.</span></span> <span data-ttu-id="462ad-131">VirtuaisLUNs.</span><span class="sxs-lookup"><span data-stu-id="462ad-131">Virtual.</span></span>                                         |
| [<span data-ttu-id="462ad-132">**Gratuita**</span><span class="sxs-lookup"><span data-stu-id="462ad-132">**Free**</span></span>](cimageallocator-free.md)                           | <span data-ttu-id="462ad-133">Libera toda a memória do buffer.</span><span class="sxs-lookup"><span data-stu-id="462ad-133">Releases all of the buffer memory.</span></span>                                       |
| <span data-ttu-id="462ad-134">Métodos públicos</span><span class="sxs-lookup"><span data-stu-id="462ad-134">Public Methods</span></span>                                                 | <span data-ttu-id="462ad-135">Descrição</span><span class="sxs-lookup"><span data-stu-id="462ad-135">Description</span></span>                                                              |
| [<span data-ttu-id="462ad-136">**CImageAllocator**</span><span class="sxs-lookup"><span data-stu-id="462ad-136">**CImageAllocator**</span></span>](cimageallocator-cimageallocator.md)     | <span data-ttu-id="462ad-137">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="462ad-137">Constructor method.</span></span>                                                      |
| [<span data-ttu-id="462ad-138">**NotifyMediaType**</span><span class="sxs-lookup"><span data-stu-id="462ad-138">**NotifyMediaType**</span></span>](cimageallocator-notifymediatype.md)     | <span data-ttu-id="462ad-139">Informa o objeto do tipo de mídia atual.</span><span class="sxs-lookup"><span data-stu-id="462ad-139">Informs the object of the current media type.</span></span>                            |
| <span data-ttu-id="462ad-140">Métodos IMemAllocator</span><span class="sxs-lookup"><span data-stu-id="462ad-140">IMemAllocator Methods</span></span>                                          | <span data-ttu-id="462ad-141">Descrição</span><span class="sxs-lookup"><span data-stu-id="462ad-141">Description</span></span>                                                              |
| [<span data-ttu-id="462ad-142">**SetProperties**</span><span class="sxs-lookup"><span data-stu-id="462ad-142">**SetProperties**</span></span>](cimageallocator-setproperties.md)         | <span data-ttu-id="462ad-143">Especifica o número de buffers a serem alocados e o tamanho de cada buffer.</span><span class="sxs-lookup"><span data-stu-id="462ad-143">Specifies the number of buffers to allocate and the size of each buffer.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="462ad-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="462ad-144">Requirements</span></span>



| <span data-ttu-id="462ad-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="462ad-145">Requirement</span></span> | <span data-ttu-id="462ad-146">Valor</span><span class="sxs-lookup"><span data-stu-id="462ad-146">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="462ad-147">parâmetro</span><span class="sxs-lookup"><span data-stu-id="462ad-147">Header</span></span><br/>  | <dl> <span data-ttu-id="462ad-148"><dt>Winutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="462ad-148"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="462ad-149">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="462ad-149">Library</span></span><br/> | <dl> <span data-ttu-id="462ad-150"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="462ad-150"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="462ad-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="462ad-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="462ad-152">**Classe CDrawImage**</span><span class="sxs-lookup"><span data-stu-id="462ad-152">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> </dl>

 

 




