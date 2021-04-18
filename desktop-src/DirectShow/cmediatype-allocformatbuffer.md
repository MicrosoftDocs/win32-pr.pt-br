---
description: O método AllocFormatBuffer aloca memória para o bloco de formato.
ms.assetid: 5ff716c7-f9cf-4b1c-9d3a-62ab955c1392
title: Método CMediaType. AllocFormatBuffer (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.AllocFormatBuffer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d6a9314fd06734adcc367b7be34dc8d6d1b9d996
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750474"
---
# <a name="cmediatypeallocformatbuffer-method"></a><span data-ttu-id="dc0a9-103">Método CMediaType. AllocFormatBuffer</span><span class="sxs-lookup"><span data-stu-id="dc0a9-103">CMediaType.AllocFormatBuffer method</span></span>

<span data-ttu-id="dc0a9-104">O `AllocFormatBuffer` método aloca memória para o bloco de formato.</span><span class="sxs-lookup"><span data-stu-id="dc0a9-104">The `AllocFormatBuffer` method allocates memory for the format block.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc0a9-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dc0a9-105">Syntax</span></span>


```C++
BYTE* AllocFormatBuffer(
   ULONG length
);
```



## <a name="parameters"></a><span data-ttu-id="dc0a9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dc0a9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc0a9-107">*length*</span><span class="sxs-lookup"><span data-stu-id="dc0a9-107">*length*</span></span> 
</dt> <dd>

<span data-ttu-id="dc0a9-108">Tamanho necessário para o bloco de formato, em bytes.</span><span class="sxs-lookup"><span data-stu-id="dc0a9-108">Size required for the format block, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc0a9-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="dc0a9-109">Return value</span></span>

<span data-ttu-id="dc0a9-110">Retorna um ponteiro para o novo bloco se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="dc0a9-110">Returns a pointer to the new block if successful.</span></span> <span data-ttu-id="dc0a9-111">Caso contrário, retornará **NULL**.</span><span class="sxs-lookup"><span data-stu-id="dc0a9-111">Otherwise, returns **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="dc0a9-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="dc0a9-112">Remarks</span></span>

<span data-ttu-id="dc0a9-113">Se o método alocar um novo bloco de formato com êxito, ele liberará o bloco de formato existente.</span><span class="sxs-lookup"><span data-stu-id="dc0a9-113">If the method successfully allocates a new format block, it frees the existing format block.</span></span> <span data-ttu-id="dc0a9-114">Se a alocação falhar, o método deixará o bloco de formato existente.</span><span class="sxs-lookup"><span data-stu-id="dc0a9-114">If the allocation fails, the method leaves the existing format block.</span></span>

<span data-ttu-id="dc0a9-115">O método atualiza os membros **cbFormat** e **pbFormat** da estrutura **do \_ \_ tipo de mídia am** .</span><span class="sxs-lookup"><span data-stu-id="dc0a9-115">The method updates the **cbFormat** and **pbFormat** members of the **AM\_MEDIA\_TYPE** structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc0a9-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dc0a9-116">Requirements</span></span>



| <span data-ttu-id="dc0a9-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc0a9-117">Requirement</span></span> | <span data-ttu-id="dc0a9-118">Valor</span><span class="sxs-lookup"><span data-stu-id="dc0a9-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc0a9-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="dc0a9-119">Header</span></span><br/>  | <dl> <span data-ttu-id="dc0a9-120"><dt>Mtype. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dc0a9-120"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="dc0a9-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="dc0a9-121">Library</span></span><br/> | <dl> <span data-ttu-id="dc0a9-122"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="dc0a9-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc0a9-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="dc0a9-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc0a9-124">**Classe CMediaType**</span><span class="sxs-lookup"><span data-stu-id="dc0a9-124">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




