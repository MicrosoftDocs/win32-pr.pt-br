---
description: 'O método QueryPreferredFormat recupera o formato de hora preferencial para o fluxo. Esse método implementa o método IMediaSeeking:: QueryPreferredFormat.'
ms.assetid: 8637448f-6b53-4ec9-9671-43bc8b713668
title: Método CPosPassThru. QueryPreferredFormat (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.QueryPreferredFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c22348a10e8b9e5f241e06252c025e2ec9593486
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758688"
---
# <a name="cpospassthruquerypreferredformat-method"></a><span data-ttu-id="6c860-104">Método CPosPassThru. QueryPreferredFormat</span><span class="sxs-lookup"><span data-stu-id="6c860-104">CPosPassThru.QueryPreferredFormat method</span></span>

<span data-ttu-id="6c860-105">O `QueryPreferredFormat` método recupera o formato de hora preferencial para o fluxo.</span><span class="sxs-lookup"><span data-stu-id="6c860-105">The `QueryPreferredFormat` method retrieves the preferred time format for the stream.</span></span> <span data-ttu-id="6c860-106">Esse método implementa o método [**IMediaSeeking:: QueryPreferredFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-querypreferredformat) .</span><span class="sxs-lookup"><span data-stu-id="6c860-106">This method implements the [**IMediaSeeking::QueryPreferredFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-querypreferredformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c860-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6c860-107">Syntax</span></span>


```C++
HRESULT QueryPreferredFormat(
   GUID *pFormat
);
```



## <a name="parameters"></a><span data-ttu-id="6c860-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6c860-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c860-109">*pFormat*</span><span class="sxs-lookup"><span data-stu-id="6c860-109">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="6c860-110">Ponteiro para uma variável que recebe um GUID de formato de hora.</span><span class="sxs-lookup"><span data-stu-id="6c860-110">Pointer to a variable that receives a time format GUID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c860-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6c860-111">Return value</span></span>

<span data-ttu-id="6c860-112">Retorna o valor **HRESULT** do PIN conectado.</span><span class="sxs-lookup"><span data-stu-id="6c860-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c860-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6c860-113">Requirements</span></span>



| <span data-ttu-id="6c860-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c860-114">Requirement</span></span> | <span data-ttu-id="6c860-115">Valor</span><span class="sxs-lookup"><span data-stu-id="6c860-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c860-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6c860-116">Header</span></span><br/>  | <dl> <span data-ttu-id="6c860-117"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6c860-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="6c860-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6c860-118">Library</span></span><br/> | <dl> <span data-ttu-id="6c860-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="6c860-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c860-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="6c860-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c860-121">**Classe CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="6c860-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> <dt>

[<span data-ttu-id="6c860-122">**GUIDs de formato de hora**</span><span class="sxs-lookup"><span data-stu-id="6c860-122">**Time Format GUIDs**</span></span>](time-format-guids.md)
</dt> </dl>

 

 




