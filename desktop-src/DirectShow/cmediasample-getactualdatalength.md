---
description: 'O método GetActualDataLength recupera o comprimento dos dados válidos no buffer. Esse método implementa o método IMediaSample:: GetActualDataLength.'
ms.assetid: bdb8c2b9-7be4-494b-bb96-34a9936d4a2f
title: Método CMediaSample. GetActualDataLength (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.GetActualDataLength
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2e65b72c1e0b6db85a271c10f76e5630b0799b78
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811737"
---
# <a name="cmediasamplegetactualdatalength-method"></a><span data-ttu-id="ca074-104">Método CMediaSample. GetActualDataLength</span><span class="sxs-lookup"><span data-stu-id="ca074-104">CMediaSample.GetActualDataLength method</span></span>

<span data-ttu-id="ca074-105">O `GetActualDataLength` método recupera o comprimento dos dados válidos no buffer.</span><span class="sxs-lookup"><span data-stu-id="ca074-105">The `GetActualDataLength` method retrieves the length of the valid data in the buffer.</span></span> <span data-ttu-id="ca074-106">Esse método implementa o método [**IMediaSample:: GetActualDataLength**](/windows/win32/api/strmif/nf-strmif-imediasample-getactualdatalength) .</span><span class="sxs-lookup"><span data-stu-id="ca074-106">This method implements the [**IMediaSample::GetActualDataLength**](/windows/win32/api/strmif/nf-strmif-imediasample-getactualdatalength) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca074-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ca074-107">Syntax</span></span>


```C++
LONG GetActualDataLength();
```



## <a name="parameters"></a><span data-ttu-id="ca074-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ca074-108">Parameters</span></span>

<span data-ttu-id="ca074-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="ca074-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ca074-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ca074-110">Return value</span></span>

<span data-ttu-id="ca074-111">Retorna o comprimento dos dados válidos, em bytes.</span><span class="sxs-lookup"><span data-stu-id="ca074-111">Returns the length of the valid data, in bytes.</span></span>

## <a name="remarks"></a><span data-ttu-id="ca074-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="ca074-112">Remarks</span></span>

<span data-ttu-id="ca074-113">A variável de membro [**CMediaSample:: m \_ lActual**](cmediasample-m-lactual.md) especifica essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="ca074-113">The [**CMediaSample::m\_lActual**](cmediasample-m-lactual.md) member variable specifies this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca074-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ca074-114">Requirements</span></span>



| <span data-ttu-id="ca074-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca074-115">Requirement</span></span> | <span data-ttu-id="ca074-116">Valor</span><span class="sxs-lookup"><span data-stu-id="ca074-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca074-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ca074-117">Header</span></span><br/>  | <dl> <span data-ttu-id="ca074-118"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ca074-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="ca074-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ca074-119">Library</span></span><br/> | <dl> <span data-ttu-id="ca074-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="ca074-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca074-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="ca074-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca074-122">**Classe CMediaSample**</span><span class="sxs-lookup"><span data-stu-id="ca074-122">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

