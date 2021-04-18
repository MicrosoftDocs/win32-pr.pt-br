---
description: O método ReallocFormatBuffer realoca o bloco de formato para um novo tamanho.
ms.assetid: 49bec677-09cc-4e1a-994a-13e873e61713
title: Método CMediaType. ReallocFormatBuffer (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.ReallocFormatBuffer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 22e861c61f01a7594d720833e2b3a4b923a1e183
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105771851"
---
# <a name="cmediatypereallocformatbuffer-method"></a><span data-ttu-id="5f377-103">Método CMediaType. ReallocFormatBuffer</span><span class="sxs-lookup"><span data-stu-id="5f377-103">CMediaType.ReallocFormatBuffer method</span></span>

<span data-ttu-id="5f377-104">O `ReallocFormatBuffer` método realoca o bloco de formato para um novo tamanho.</span><span class="sxs-lookup"><span data-stu-id="5f377-104">The `ReallocFormatBuffer` method reallocates the format block to a new size.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f377-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5f377-105">Syntax</span></span>


```C++
BYTE* ReallocFormatBuffer(
   ULONG length
);
```



## <a name="parameters"></a><span data-ttu-id="5f377-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5f377-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f377-107">*length*</span><span class="sxs-lookup"><span data-stu-id="5f377-107">*length*</span></span> 
</dt> <dd>

<span data-ttu-id="5f377-108">Novo tamanho necessário para o bloco de formato, em bytes.</span><span class="sxs-lookup"><span data-stu-id="5f377-108">New size required for the format block, in bytes.</span></span> <span data-ttu-id="5f377-109">Deve ser maior que zero.</span><span class="sxs-lookup"><span data-stu-id="5f377-109">Must be greater than zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f377-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5f377-110">Return value</span></span>

<span data-ttu-id="5f377-111">Retorna um ponteiro para o novo bloco se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="5f377-111">Returns a pointer to the new block if successful.</span></span> <span data-ttu-id="5f377-112">Caso contrário, retorna um ponteiro para o bloco de formato antigo ou **NULL**.</span><span class="sxs-lookup"><span data-stu-id="5f377-112">Otherwise, returns either a pointer to the old format block, or **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f377-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="5f377-113">Remarks</span></span>

<span data-ttu-id="5f377-114">Esse método aloca um novo bloco de formato.</span><span class="sxs-lookup"><span data-stu-id="5f377-114">This method allocates a new format block.</span></span> <span data-ttu-id="5f377-115">Ele copia o máximo possível de bloco de formato existente no novo bloco de formato.</span><span class="sxs-lookup"><span data-stu-id="5f377-115">It copies as much of the existing format block as possible into the new format block.</span></span> <span data-ttu-id="5f377-116">Se o novo bloco for menor do que o bloco existente, o bloco de formato existente será truncado.</span><span class="sxs-lookup"><span data-stu-id="5f377-116">If the new block is smaller than the existing block, the existing format block is truncated.</span></span> <span data-ttu-id="5f377-117">Se o novo bloco for maior, o conteúdo do espaço adicional será indefinido.</span><span class="sxs-lookup"><span data-stu-id="5f377-117">If the new block is larger, the contents of the additional space are undefined.</span></span> <span data-ttu-id="5f377-118">Eles não são definidos explicitamente como zero.</span><span class="sxs-lookup"><span data-stu-id="5f377-118">They are not explicitly set to zero.</span></span>

<span data-ttu-id="5f377-119">O método atualiza os membros **cbFormat** e **pbFormat** da estrutura **do \_ \_ tipo de mídia am** .</span><span class="sxs-lookup"><span data-stu-id="5f377-119">The method updates the **cbFormat** and **pbFormat** members of the **AM\_MEDIA\_TYPE** structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f377-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5f377-120">Requirements</span></span>



| <span data-ttu-id="5f377-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f377-121">Requirement</span></span> | <span data-ttu-id="5f377-122">Valor</span><span class="sxs-lookup"><span data-stu-id="5f377-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f377-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5f377-123">Header</span></span><br/>  | <dl> <span data-ttu-id="5f377-124"><dt>Mtype. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5f377-124"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="5f377-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5f377-125">Library</span></span><br/> | <dl> <span data-ttu-id="5f377-126"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="5f377-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f377-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="5f377-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f377-128">**Classe CMediaType**</span><span class="sxs-lookup"><span data-stu-id="5f377-128">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




