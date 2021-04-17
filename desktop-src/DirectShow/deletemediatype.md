---
description: A função DeleteMediaType exclui uma estrutura de \_ tipo de mídia am alocada \_ , incluindo o bloco de formato.
ms.assetid: 970f6b2b-2bf5-418d-b4ae-637561cd6765
title: Função DeleteMediaType (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeleteMediaType
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: db0de399ab1be7808370a6d0da57c4c3ca7b8de1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752278"
---
# <a name="deletemediatype-function"></a><span data-ttu-id="b098a-103">Função DeleteMediaType</span><span class="sxs-lookup"><span data-stu-id="b098a-103">DeleteMediaType function</span></span>

<span data-ttu-id="b098a-104">A função **DeleteMediaType** exclui uma estrutura [**de \_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) alocada, incluindo o bloco de formato.</span><span class="sxs-lookup"><span data-stu-id="b098a-104">The **DeleteMediaType** function deletes an allocated [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure, including the format block.</span></span>

## <a name="syntax"></a><span data-ttu-id="b098a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b098a-105">Syntax</span></span>


```C++
void WINAPI DeleteMediaType(
   AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="b098a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b098a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b098a-107">*PMT*</span><span class="sxs-lookup"><span data-stu-id="b098a-107">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="b098a-108">Um ponteiro para uma estrutura de [**\_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="b098a-108">A pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b098a-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b098a-109">Return value</span></span>

<span data-ttu-id="b098a-110">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="b098a-110">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b098a-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="b098a-111">Remarks</span></span>

<span data-ttu-id="b098a-112">Use essa função para liberar qualquer estrutura de tipo de mídia que foi alocada usando [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) ou [**CreateMediaType**](createmediatype.md).</span><span class="sxs-lookup"><span data-stu-id="b098a-112">Use this function to release any media type structure that was allocated using either [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) or [**CreateMediaType**](createmediatype.md).</span></span>

<span data-ttu-id="b098a-113">Essa função é definida na biblioteca de [classes base do DirectShow](directshow-base-classes.md) .</span><span class="sxs-lookup"><span data-stu-id="b098a-113">This function is defined in the [DirectShow Base Classes](directshow-base-classes.md) library.</span></span> <span data-ttu-id="b098a-114">Se preferir não vincular à biblioteca de classes base, você pode usar o seguinte código:</span><span class="sxs-lookup"><span data-stu-id="b098a-114">If you prefer not to link to the base class library, you can use the following code:</span></span>


```C++
// Release the format block for a media type.

void _FreeMediaType(AM_MEDIA_TYPE& mt)
{
    if (mt.cbFormat != 0)
    {
        CoTaskMemFree((PVOID)mt.pbFormat);
        mt.cbFormat = 0;
        mt.pbFormat = NULL;
    }
    if (mt.pUnk != NULL)
    {
        // pUnk should not be used.
        mt.pUnk->Release();
        mt.pUnk = NULL;
    }
}


// Delete a media type structure that was allocated on the heap.
void _DeleteMediaType(AM_MEDIA_TYPE *pmt)
{
    if (pmt != NULL)
    {
        _FreeMediaType(*pmt); 
        CoTaskMemFree(pmt);
    }
}
```





## <a name="requirements"></a><span data-ttu-id="b098a-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b098a-115">Requirements</span></span>



| <span data-ttu-id="b098a-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="b098a-116">Requirement</span></span> | <span data-ttu-id="b098a-117">Valor</span><span class="sxs-lookup"><span data-stu-id="b098a-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b098a-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b098a-118">Header</span></span><br/>  | <dl> <span data-ttu-id="b098a-119"><dt>Mtype. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b098a-119"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="b098a-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b098a-120">Library</span></span><br/> | <dl> <span data-ttu-id="b098a-121"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="b098a-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b098a-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="b098a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b098a-123">**FreeMediaType**</span><span class="sxs-lookup"><span data-stu-id="b098a-123">**FreeMediaType**</span></span>](freemediatype.md)
</dt> <dt>

[<span data-ttu-id="b098a-124">**Funções de tipo de mídia**</span><span class="sxs-lookup"><span data-stu-id="b098a-124">**Media Type Functions**</span></span>](media-type-functions.md)
</dt> </dl>

 

