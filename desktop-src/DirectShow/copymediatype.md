---
description: A função CopyMediaType copia uma \_ estrutura de tipo de mídia am \_ para outra estrutura, incluindo o bloco de formato
ms.assetid: 5b47e197-abb5-4b2c-ad65-a506c5e239be
title: Função CopyMediaType (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CopyMediaType
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2e37f277244ae9b82c395d7901917e1fc1e78b35
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759311"
---
# <a name="copymediatype-function"></a><span data-ttu-id="620a7-103">Função CopyMediaType</span><span class="sxs-lookup"><span data-stu-id="620a7-103">CopyMediaType function</span></span>

<span data-ttu-id="620a7-104">A função **CopyMediaType** copia uma estrutura de [**\_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) para outra estrutura, incluindo o bloco de formato</span><span class="sxs-lookup"><span data-stu-id="620a7-104">The **CopyMediaType** function copies an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure into another structure, including the format block</span></span>

## <a name="syntax"></a><span data-ttu-id="620a7-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="620a7-105">Syntax</span></span>


```C++
HRESULT WINAPI CopyMediaType(
         AM_MEDIA_TYPE *pmtTarget,
   const AM_MEDIA_TYPE *pmtSource
);
```



## <a name="parameters"></a><span data-ttu-id="620a7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="620a7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="620a7-107">*pmtTarget*</span><span class="sxs-lookup"><span data-stu-id="620a7-107">*pmtTarget*</span></span> 
</dt> <dd>

<span data-ttu-id="620a7-108">Ponteiro para uma estrutura de [**\_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="620a7-108">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span> <span data-ttu-id="620a7-109">O método copia o tipo de mídia nessa estrutura.</span><span class="sxs-lookup"><span data-stu-id="620a7-109">The method copies the media type into this structure.</span></span>

</dd> <dt>

<span data-ttu-id="620a7-110">*pmtSource*</span><span class="sxs-lookup"><span data-stu-id="620a7-110">*pmtSource*</span></span> 
</dt> <dd>

<span data-ttu-id="620a7-111">Ponteiro para uma estrutura [**de \_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) de origem a ser copiada.</span><span class="sxs-lookup"><span data-stu-id="620a7-111">Pointer to a source [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure to copy.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="620a7-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="620a7-112">Return value</span></span>

<span data-ttu-id="620a7-113">Retorna S \_ OK ou E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="620a7-113">Returns S\_OK or E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="620a7-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="620a7-114">Remarks</span></span>

<span data-ttu-id="620a7-115">Essa função aloca a memória para o bloco de formato.</span><span class="sxs-lookup"><span data-stu-id="620a7-115">This function allocates the memory for the format block.</span></span> <span data-ttu-id="620a7-116">Se o parâmetro *pmtTarget* já contiver um bloco de formato alocado, ocorrerá um vazamento de memória.</span><span class="sxs-lookup"><span data-stu-id="620a7-116">If the *pmtTarget* parameter already contains an allocated format block, a memory leak will occur.</span></span> <span data-ttu-id="620a7-117">Para evitar um vazamento de memória, chame [**FreeMediaType**](freemediatype.md) antes de chamar essa função.</span><span class="sxs-lookup"><span data-stu-id="620a7-117">To avoid a memory leak, call [**FreeMediaType**](freemediatype.md) before calling this function.</span></span>

<span data-ttu-id="620a7-118">Depois que o método retornar, chame [**FreeMediaType**](freemediatype.md) em *pmtTarget* para liberar o bloco de formato.</span><span class="sxs-lookup"><span data-stu-id="620a7-118">After the method returns, call [**FreeMediaType**](freemediatype.md) on *pmtTarget* to free the format block.</span></span>

## <a name="requirements"></a><span data-ttu-id="620a7-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="620a7-119">Requirements</span></span>



| <span data-ttu-id="620a7-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="620a7-120">Requirement</span></span> | <span data-ttu-id="620a7-121">Valor</span><span class="sxs-lookup"><span data-stu-id="620a7-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="620a7-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="620a7-122">Header</span></span><br/>  | <dl> <span data-ttu-id="620a7-123"><dt>Mtype. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="620a7-123"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="620a7-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="620a7-124">Library</span></span><br/> | <dl> <span data-ttu-id="620a7-125"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="620a7-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="620a7-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="620a7-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="620a7-127">**Funções de tipo de mídia**</span><span class="sxs-lookup"><span data-stu-id="620a7-127">**Media Type Functions**</span></span>](media-type-functions.md)
</dt> </dl>

 

 




