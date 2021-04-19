---
description: Esse operador sobrecarrega o operador de atribuição para copiar um tipo de mídia.
ms.assetid: 5b94191d-b5e4-42b2-b0c5-8c2da2483c54
title: 'CMediaType. CMediaType:: Operator = Method (mtype. h)-parâmetro mtype'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.CMediaType::operator=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dfa577c8c8cfcdbcb0b62287a80cd998ab8775c6
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/05/2021
ms.locfileid: "106389035"
---
# <a name="cmediatypecmediatypeoperator-method-mtypeh"></a><span data-ttu-id="43421-103">CMediaType. CMediaType:: Operator = método (mtype. h)</span><span class="sxs-lookup"><span data-stu-id="43421-103">CMediaType.CMediaType::operator= method (Mtype.h)</span></span>

<span data-ttu-id="43421-104">Esse operador sobrecarrega o operador de atribuição para copiar um tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="43421-104">This operator overloads the assignment operator to copy a media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="43421-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="43421-105">Syntax</span></span>


```C++
CMediaType& CMediaType::operator=(
  [ref] const AM_MEDIA_TYPE &mtype
);
```



## <a name="parameters"></a><span data-ttu-id="43421-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="43421-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43421-107">*mtype* \[ referência\]</span><span class="sxs-lookup"><span data-stu-id="43421-107">*mtype* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="43421-108">Referência a uma estrutura de [**\_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="43421-108">Reference to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43421-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="43421-109">Return value</span></span>

<span data-ttu-id="43421-110">Retorna uma referência ao objeto.</span><span class="sxs-lookup"><span data-stu-id="43421-110">Returns a reference to the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="43421-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="43421-111">Requirements</span></span>



| <span data-ttu-id="43421-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="43421-112">Requirement</span></span> | <span data-ttu-id="43421-113">Valor</span><span class="sxs-lookup"><span data-stu-id="43421-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43421-114">parâmetro</span><span class="sxs-lookup"><span data-stu-id="43421-114">Header</span></span><br/>  | <dl> <span data-ttu-id="43421-115"><dt>Mtype. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="43421-115"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="43421-116">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="43421-116">Library</span></span><br/> | <dl> <span data-ttu-id="43421-117"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="43421-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43421-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="43421-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43421-119">**Classe CMediaType**</span><span class="sxs-lookup"><span data-stu-id="43421-119">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




