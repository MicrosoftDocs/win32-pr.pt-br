---
description: Esse operador sobrecarrega o operador de atribuição para copiar um tipo de mídia.
ms.assetid: 5b94191d-b5e4-42b2-b0c5-8c2da2483c54
title: 'CMediaType. CMediaType:: Operator = método (mtype. h)'
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
ms.openlocfilehash: 748ad2efae39fc6a7b26c39d10351c44a5cee8a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759916"
---
# <a name="cmediatypecmediatypeoperator-method-mtypeh"></a><span data-ttu-id="79502-103">CMediaType. CMediaType:: Operator = método (mtype. h)</span><span class="sxs-lookup"><span data-stu-id="79502-103">CMediaType.CMediaType::operator= method (Mtype.h)</span></span>

<span data-ttu-id="79502-104">Esse operador sobrecarrega o operador de atribuição para copiar um tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="79502-104">This operator overloads the assignment operator to copy a media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="79502-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="79502-105">Syntax</span></span>


```C++
CMediaType& CMediaType::operator=(
  [ref] const AM_MEDIA_TYPE &mtype
);
```



## <a name="parameters"></a><span data-ttu-id="79502-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="79502-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79502-107">*mtype* \[ referência\]</span><span class="sxs-lookup"><span data-stu-id="79502-107">*mtype* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="79502-108">Referência a uma estrutura de [**\_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="79502-108">Reference to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79502-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="79502-109">Return value</span></span>

<span data-ttu-id="79502-110">Retorna uma referência ao objeto.</span><span class="sxs-lookup"><span data-stu-id="79502-110">Returns a reference to the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="79502-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="79502-111">Requirements</span></span>



| <span data-ttu-id="79502-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="79502-112">Requirement</span></span> | <span data-ttu-id="79502-113">Valor</span><span class="sxs-lookup"><span data-stu-id="79502-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79502-114">parâmetro</span><span class="sxs-lookup"><span data-stu-id="79502-114">Header</span></span><br/>  | <dl> <span data-ttu-id="79502-115"><dt>Mtype. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="79502-115"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="79502-116">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="79502-116">Library</span></span><br/> | <dl> <span data-ttu-id="79502-117"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="79502-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79502-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="79502-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79502-119">**Classe CMediaType**</span><span class="sxs-lookup"><span data-stu-id="79502-119">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




