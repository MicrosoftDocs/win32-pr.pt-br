---
description: O método IsValid determina se um tipo principal foi atribuído a esse objeto.
ms.assetid: 22d28019-f360-4b93-972c-d1dfe83938f0
title: Método CMediaType. IsValid (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.IsValid
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7d8e1731060021b61eb5037e1baeeda95021e8f5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757698"
---
# <a name="cmediatypeisvalid-method"></a><span data-ttu-id="2937c-103">Método CMediaType. IsValid</span><span class="sxs-lookup"><span data-stu-id="2937c-103">CMediaType.IsValid method</span></span>

<span data-ttu-id="2937c-104">O `IsValid` método determina se um tipo principal foi atribuído a este objeto.</span><span class="sxs-lookup"><span data-stu-id="2937c-104">The `IsValid` method determines whether a major type has been assigned to this object.</span></span>

## <a name="syntax"></a><span data-ttu-id="2937c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2937c-105">Syntax</span></span>


```C++
BOOL IsValid() const;
```



## <a name="parameters"></a><span data-ttu-id="2937c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2937c-106">Parameters</span></span>

<span data-ttu-id="2937c-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="2937c-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2937c-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2937c-108">Return value</span></span>

<span data-ttu-id="2937c-109">Retornará **true** se um tipo principal tiver sido atribuído a este objeto.</span><span class="sxs-lookup"><span data-stu-id="2937c-109">Returns **TRUE** if a major type has been assigned to this object.</span></span> <span data-ttu-id="2937c-110">Caso contrário, retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="2937c-110">Otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="2937c-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="2937c-111">Remarks</span></span>

<span data-ttu-id="2937c-112">Por padrão, os objetos [**CMediaType**](cmediatype.md) são inicializados com um tipo principal de GUID \_ NULL.</span><span class="sxs-lookup"><span data-stu-id="2937c-112">By default, [**CMediaType**](cmediatype.md) objects are initialized with a major type of GUID\_NULL.</span></span> <span data-ttu-id="2937c-113">Chame esse método para determinar se o objeto foi inicializado corretamente.</span><span class="sxs-lookup"><span data-stu-id="2937c-113">Call this method to determine whether the object has been correctly initialized.</span></span>

## <a name="requirements"></a><span data-ttu-id="2937c-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2937c-114">Requirements</span></span>



| <span data-ttu-id="2937c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="2937c-115">Requirement</span></span> | <span data-ttu-id="2937c-116">Valor</span><span class="sxs-lookup"><span data-stu-id="2937c-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2937c-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2937c-117">Header</span></span><br/>  | <dl> <span data-ttu-id="2937c-118"><dt>Mtype. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2937c-118"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="2937c-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2937c-119">Library</span></span><br/> | <dl> <span data-ttu-id="2937c-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="2937c-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2937c-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="2937c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2937c-122">**Classe CMediaType**</span><span class="sxs-lookup"><span data-stu-id="2937c-122">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




