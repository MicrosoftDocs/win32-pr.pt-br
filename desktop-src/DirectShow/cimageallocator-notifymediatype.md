---
description: O método NotifyMediaType informa o objeto do tipo de mídia atual.
ms.assetid: 6fb708ff-e968-4867-baca-ebe2515c9fab
title: Método CImageAllocator. NotifyMediaType (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator.NotifyMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cb9261884b8940b571876502741fcc52e1c40a33
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752894"
---
# <a name="cimageallocatornotifymediatype-method"></a><span data-ttu-id="800bb-103">Método CImageAllocator. NotifyMediaType</span><span class="sxs-lookup"><span data-stu-id="800bb-103">CImageAllocator.NotifyMediaType method</span></span>

<span data-ttu-id="800bb-104">O `NotifyMediaType` método informa o objeto do tipo de mídia atual.</span><span class="sxs-lookup"><span data-stu-id="800bb-104">The `NotifyMediaType` method informs the object of the current media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="800bb-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="800bb-105">Syntax</span></span>


```C++
void NotifyMediaType(
   CMediaType *pMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="800bb-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="800bb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="800bb-107">*pMediaType*</span><span class="sxs-lookup"><span data-stu-id="800bb-107">*pMediaType*</span></span> 
</dt> <dd>

<span data-ttu-id="800bb-108">Ponteiro para um objeto [**CMediaType**](cmediatype.md) ou **NULL** para limpar o tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="800bb-108">Pointer to a [**CMediaType**](cmediatype.md) object, or **NULL** to clear the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="800bb-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="800bb-109">Return value</span></span>

<span data-ttu-id="800bb-110">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="800bb-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="800bb-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="800bb-111">Remarks</span></span>

<span data-ttu-id="800bb-112">O filtro proprietário deve chamar esse método sempre que o tipo de mídia for alterado.</span><span class="sxs-lookup"><span data-stu-id="800bb-112">The owning filter should call this method whenever the media type changes.</span></span> <span data-ttu-id="800bb-113">Normalmente, isso ocorre quando o PIN se conecta pela primeira vez e após uma alteração de formato dinâmico.</span><span class="sxs-lookup"><span data-stu-id="800bb-113">Typically this occurs when the pin first connects, and after a dynamic format change.</span></span> <span data-ttu-id="800bb-114">O alocador usa o tipo de mídia para validar as propriedades de alocador propostas e também quando cria amostras de mídia.</span><span class="sxs-lookup"><span data-stu-id="800bb-114">The allocator uses the media type to validate proposed allocator properties, and also when it creates media samples.</span></span>

<span data-ttu-id="800bb-115">O objeto **CImageAllocator** armazena o ponteiro *pMediaType* na variável de membro **m \_ pMediaType** .</span><span class="sxs-lookup"><span data-stu-id="800bb-115">The **CImageAllocator** object stores the *pMediaType* pointer in the **m\_pMediaType** member variable.</span></span> <span data-ttu-id="800bb-116">Portanto, se o chamador precisar liberar o objeto **CMediaType** , ele deverá atualizar o alocador chamando esse método novamente, seja com um novo ponteiro ou com um valor **nulo** .</span><span class="sxs-lookup"><span data-stu-id="800bb-116">Therefore, if the caller needs to release the **CMediaType** object, it should update the allocator by calling this method again, either with a new pointer or with a **NULL** value.</span></span> <span data-ttu-id="800bb-117">Caso contrário, um erro pode ocorrer quando o alocador tenta referenciar o ponteiro antigo.</span><span class="sxs-lookup"><span data-stu-id="800bb-117">Otherwise, an error can occur when the allocator attempts to reference the old pointer.</span></span>

## <a name="requirements"></a><span data-ttu-id="800bb-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="800bb-118">Requirements</span></span>



| <span data-ttu-id="800bb-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="800bb-119">Requirement</span></span> | <span data-ttu-id="800bb-120">Valor</span><span class="sxs-lookup"><span data-stu-id="800bb-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="800bb-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="800bb-121">Header</span></span><br/>  | <dl> <span data-ttu-id="800bb-122"><dt>Winutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="800bb-122"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="800bb-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="800bb-123">Library</span></span><br/> | <dl> <span data-ttu-id="800bb-124"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="800bb-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="800bb-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="800bb-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="800bb-126">**Classe CImageAllocator**</span><span class="sxs-lookup"><span data-stu-id="800bb-126">**CImageAllocator Class**</span></span>](cimageallocator.md)
</dt> </dl>

 

 




