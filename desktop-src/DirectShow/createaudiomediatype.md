---
description: A função CreateAudioMediaType Inicializa um tipo de mídia de uma estrutura WAVEFORMATEX.
ms.assetid: 2571b7b4-86e9-443f-a99d-9ba48f469522
title: Função CreateAudioMediaType (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateAudioMediaType
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ef4e525762d4b6928e6a9095fad34f3f4f2e96fc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105812838"
---
# <a name="createaudiomediatype-function"></a><span data-ttu-id="36531-103">Função CreateAudioMediaType</span><span class="sxs-lookup"><span data-stu-id="36531-103">CreateAudioMediaType function</span></span>

<span data-ttu-id="36531-104">A função **CreateAudioMediaType** Inicializa um tipo de mídia de uma estrutura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="36531-104">The **CreateAudioMediaType** function initializes a media type from a [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="36531-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="36531-105">Syntax</span></span>


```C++
HRESULT STDAPI CreateAudioMediaType(
   const WAVEFORMATEX  *pwfx,
         AM_MEDIA_TYPE *pmt,
         BOOL          bSetFormat
);
```



## <a name="parameters"></a><span data-ttu-id="36531-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="36531-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36531-107">*pwfx*</span><span class="sxs-lookup"><span data-stu-id="36531-107">*pwfx*</span></span> 
</dt> <dd>

<span data-ttu-id="36531-108">Ponteiro para a estrutura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) fornecida.</span><span class="sxs-lookup"><span data-stu-id="36531-108">Pointer to the supplied [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure.</span></span>

</dd> <dt>

<span data-ttu-id="36531-109">*PMT*</span><span class="sxs-lookup"><span data-stu-id="36531-109">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="36531-110">Ponteiro para a estrutura do [**\_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) a ser inicializada.</span><span class="sxs-lookup"><span data-stu-id="36531-110">Pointer to the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure to initialize.</span></span>

</dd> <dt>

<span data-ttu-id="36531-111">*bSetFormat*</span><span class="sxs-lookup"><span data-stu-id="36531-111">*bSetFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="36531-112">Sinalizador que indica se o bloco de formato deve ser inicializado.</span><span class="sxs-lookup"><span data-stu-id="36531-112">Flag indicating whether to initialize the format block.</span></span> <span data-ttu-id="36531-113">Especifique **true** para inicializá-lo ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="36531-113">Specify **TRUE** to initialize it, or **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36531-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="36531-114">Return value</span></span>

<span data-ttu-id="36531-115">Retorna E \_ OUTOFMEMORY se não foi possível alocar a memória para os dados de formato; \_Caso contrário, ok.</span><span class="sxs-lookup"><span data-stu-id="36531-115">Returns E\_OUTOFMEMORY if memory could not be allocated for the format data; S\_OK otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="36531-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="36531-116">Remarks</span></span>

<span data-ttu-id="36531-117">Se o parâmetro *bSetFormat* for **true**, o método alocará a memória para o bloco de formato.</span><span class="sxs-lookup"><span data-stu-id="36531-117">If the *bSetFormat* parameter is **TRUE**, the method allocates the memory for the format block.</span></span> <span data-ttu-id="36531-118">Se o parâmetro *PGTO* já contiver um bloco de formato alocado, ocorrerá um vazamento de memória.</span><span class="sxs-lookup"><span data-stu-id="36531-118">If the *pmt* parameter already contains an allocated format block, a memory leak will occur.</span></span> <span data-ttu-id="36531-119">Para evitar um vazamento de memória, chame [**FreeMediaType**](freemediatype.md) antes de chamar essa função.</span><span class="sxs-lookup"><span data-stu-id="36531-119">To avoid a memory leak, call [**FreeMediaType**](freemediatype.md) before calling this function.</span></span> <span data-ttu-id="36531-120">Depois que o método retornar, chame **FreeMediaType** novamente para liberar o bloco de formato.</span><span class="sxs-lookup"><span data-stu-id="36531-120">After the method returns, call **FreeMediaType** again to free the format block.</span></span>

## <a name="requirements"></a><span data-ttu-id="36531-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="36531-121">Requirements</span></span>



| <span data-ttu-id="36531-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="36531-122">Requirement</span></span> | <span data-ttu-id="36531-123">Valor</span><span class="sxs-lookup"><span data-stu-id="36531-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36531-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="36531-124">Header</span></span><br/>  | <dl> <span data-ttu-id="36531-125"><dt>Mtype. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="36531-125"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="36531-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="36531-126">Library</span></span><br/> | <dl> <span data-ttu-id="36531-127"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="36531-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36531-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="36531-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36531-129">**Funções de tipo de mídia**</span><span class="sxs-lookup"><span data-stu-id="36531-129">**Media Type Functions**</span></span>](media-type-functions.md)
</dt> </dl>

 

