---
description: A função CreateMediaType aloca uma nova \_ estrutura de tipo de mídia am \_ , incluindo o bloco de formato.
ms.assetid: 841a8c51-6027-49d6-b3d8-b5e21e3d5f13
title: Função CreateMediaType (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateMediaType
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 03ea3eaee03ebf98ac22d702bde9a165fda21e51
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782253"
---
# <a name="createmediatype-function"></a><span data-ttu-id="ce625-103">Função CreateMediaType</span><span class="sxs-lookup"><span data-stu-id="ce625-103">CreateMediaType function</span></span>

<span data-ttu-id="ce625-104">A função **CreateMediaType** aloca uma nova estrutura de [**\_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) , incluindo o bloco de formato.</span><span class="sxs-lookup"><span data-stu-id="ce625-104">The **CreateMediaType** function allocates a new [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure, including the format block.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce625-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ce625-105">Syntax</span></span>


```C++
AM_MEDIA_TYPE* WINAPI CreateMediaType(
   AM_MEDIA_TYPE const *pSrc
);
```



## <a name="parameters"></a><span data-ttu-id="ce625-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ce625-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce625-107">*pSrc*</span><span class="sxs-lookup"><span data-stu-id="ce625-107">*pSrc*</span></span> 
</dt> <dd>

<span data-ttu-id="ce625-108">Ponteiro para uma estrutura de [**\_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="ce625-108">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span> <span data-ttu-id="ce625-109">O método copia essa estrutura na nova estrutura.</span><span class="sxs-lookup"><span data-stu-id="ce625-109">The method copies this structure into the new structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce625-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ce625-110">Return value</span></span>

<span data-ttu-id="ce625-111">Retorna uma nova estrutura de [**\_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) ou **NULL** se houver um erro.</span><span class="sxs-lookup"><span data-stu-id="ce625-111">Returns a new [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure, or **NULL** if there is an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce625-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="ce625-112">Remarks</span></span>

<span data-ttu-id="ce625-113">Para liberar a memória alocada por essa função, chame [**DeleteMediaType**](deletemediatype.md).</span><span class="sxs-lookup"><span data-stu-id="ce625-113">To free the memory allocated by this function, call [**DeleteMediaType**](deletemediatype.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ce625-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ce625-114">Requirements</span></span>



| <span data-ttu-id="ce625-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce625-115">Requirement</span></span> | <span data-ttu-id="ce625-116">Valor</span><span class="sxs-lookup"><span data-stu-id="ce625-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce625-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ce625-117">Header</span></span><br/>  | <dl> <span data-ttu-id="ce625-118"><dt>Mtype. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ce625-118"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="ce625-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ce625-119">Library</span></span><br/> | <dl> <span data-ttu-id="ce625-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="ce625-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce625-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="ce625-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce625-122">**Funções de tipo de mídia**</span><span class="sxs-lookup"><span data-stu-id="ce625-122">**Media Type Functions**</span></span>](media-type-functions.md)
</dt> </dl>

 

 




