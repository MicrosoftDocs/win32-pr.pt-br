---
description: A função FreeMediaType exclui o bloco de formato em uma \_ estrutura de tipo de mídia am \_ .
ms.assetid: b7ec335e-518d-4aa6-8cde-8cb92184d0b0
title: Função FreeMediaType (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FreeMediaType
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9f332ccc9a60473a9d814481b759221dc6468d5c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758523"
---
# <a name="freemediatype-function"></a><span data-ttu-id="5dac9-103">Função FreeMediaType</span><span class="sxs-lookup"><span data-stu-id="5dac9-103">FreeMediaType function</span></span>

<span data-ttu-id="5dac9-104">A função **FreeMediaType** exclui o bloco de formato em uma estrutura de [**\_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="5dac9-104">The **FreeMediaType** function deletes the format block in an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="5dac9-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5dac9-105">Syntax</span></span>


```C++
void FreeMediaType(
   AM_MEDIA_TYPE &mt
);
```



## <a name="parameters"></a><span data-ttu-id="5dac9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5dac9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5dac9-107">*MT* \[ referência\]</span><span class="sxs-lookup"><span data-stu-id="5dac9-107">*mt* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="5dac9-108">Uma referência a uma estrutura de [**\_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="5dac9-108">A reference to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5dac9-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5dac9-109">Return value</span></span>

<span data-ttu-id="5dac9-110">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="5dac9-110">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5dac9-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="5dac9-111">Remarks</span></span>

<span data-ttu-id="5dac9-112">O bloco de formato é alocado no heap.</span><span class="sxs-lookup"><span data-stu-id="5dac9-112">The format block is allocated on the heap.</span></span> <span data-ttu-id="5dac9-113">O membro **pbFormat** do [**\_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) aponta para o bloco de formato.</span><span class="sxs-lookup"><span data-stu-id="5dac9-113">The **pbFormat** member of the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) points to the format block.</span></span> <span data-ttu-id="5dac9-114">Use essa função para liberar apenas o bloco de formato.</span><span class="sxs-lookup"><span data-stu-id="5dac9-114">Use this function to free just the format block.</span></span> <span data-ttu-id="5dac9-115">Para excluir uma estrutura **de \_ \_ tipo de mídia am** alocada, chame [**DeleteMediaType**](deletemediatype.md).</span><span class="sxs-lookup"><span data-stu-id="5dac9-115">To delete an allocated **AM\_MEDIA\_TYPE** structure, call [**DeleteMediaType**](deletemediatype.md).</span></span>

<span data-ttu-id="5dac9-116">Essa função é definida na biblioteca de [classes base do DirectShow](directshow-base-classes.md) .</span><span class="sxs-lookup"><span data-stu-id="5dac9-116">This function is defined in the [DirectShow Base Classes](directshow-base-classes.md) library.</span></span> <span data-ttu-id="5dac9-117">Se preferir não vincular à biblioteca de classes base, você pode usar o seguinte código:</span><span class="sxs-lookup"><span data-stu-id="5dac9-117">If you prefer not to link to the base class library, you can use the following code:</span></span>


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
```



## <a name="requirements"></a><span data-ttu-id="5dac9-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5dac9-118">Requirements</span></span>



| <span data-ttu-id="5dac9-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="5dac9-119">Requirement</span></span> | <span data-ttu-id="5dac9-120">Valor</span><span class="sxs-lookup"><span data-stu-id="5dac9-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5dac9-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5dac9-121">Header</span></span><br/>  | <dl> <span data-ttu-id="5dac9-122"><dt>Mtype. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5dac9-122"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="5dac9-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5dac9-123">Library</span></span><br/> | <dl> <span data-ttu-id="5dac9-124"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="5dac9-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5dac9-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="5dac9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5dac9-126">**DeleteMediaType**</span><span class="sxs-lookup"><span data-stu-id="5dac9-126">**DeleteMediaType**</span></span>](deletemediatype.md)
</dt> <dt>

[<span data-ttu-id="5dac9-127">**Funções de tipo de mídia**</span><span class="sxs-lookup"><span data-stu-id="5dac9-127">**Media Type Functions**</span></span>](media-type-functions.md)
</dt> </dl>

 

 




