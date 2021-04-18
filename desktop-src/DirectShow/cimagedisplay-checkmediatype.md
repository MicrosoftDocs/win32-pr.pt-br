---
description: O método CheckMediaType determina se um tipo de mídia proposto é compatível com o formato de exibição.
ms.assetid: 567663cf-c79f-4549-9fa9-b16da957d2b1
title: Método CImageDisplay. CheckMediaType (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a8ebcdbe6bbfe6538a2ea166be0816f31954c7d2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749620"
---
# <a name="cimagedisplaycheckmediatype-method"></a><span data-ttu-id="30f4a-103">Método CImageDisplay. CheckMediaType</span><span class="sxs-lookup"><span data-stu-id="30f4a-103">CImageDisplay.CheckMediaType method</span></span>

<span data-ttu-id="30f4a-104">O `CheckMediaType` método determina se um tipo de mídia proposto é compatível com o formato de exibição.</span><span class="sxs-lookup"><span data-stu-id="30f4a-104">The `CheckMediaType` method determines whether a proposed media type is compatible with the display format.</span></span>

## <a name="syntax"></a><span data-ttu-id="30f4a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="30f4a-105">Syntax</span></span>


```C++
HRESULT CheckMediaType(
   const CMediaType *pmtIn
);
```



## <a name="parameters"></a><span data-ttu-id="30f4a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="30f4a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30f4a-107">*pmtIn*</span><span class="sxs-lookup"><span data-stu-id="30f4a-107">*pmtIn*</span></span> 
</dt> <dd>

<span data-ttu-id="30f4a-108">Ponteiro para um objeto [**CMediaType**](cmediatype.md) que contém o tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="30f4a-108">Pointer to a [**CMediaType**](cmediatype.md) object that contains the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30f4a-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="30f4a-109">Return value</span></span>

<span data-ttu-id="30f4a-110">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="30f4a-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="30f4a-111">Os possíveis valores incluem os seguintes.</span><span class="sxs-lookup"><span data-stu-id="30f4a-111">Possible values include the following.</span></span>



| <span data-ttu-id="30f4a-112">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="30f4a-112">Return code</span></span>                                                                                  | <span data-ttu-id="30f4a-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="30f4a-113">Description</span></span>                              |
|----------------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <span data-ttu-id="30f4a-114"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="30f4a-114"><dt>**E\_FAIL**</dt></span></span> </dl>       | <span data-ttu-id="30f4a-115">Tipo de mídia inválido.</span><span class="sxs-lookup"><span data-stu-id="30f4a-115">Invalid media type.</span></span><br/>           |
| <dl> <span data-ttu-id="30f4a-116"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="30f4a-116"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="30f4a-117">Tipo de mídia inválido.</span><span class="sxs-lookup"><span data-stu-id="30f4a-117">Invalid media type.</span></span><br/>           |
| <dl> <span data-ttu-id="30f4a-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="30f4a-118"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="30f4a-119">O tipo de mídia é compatível.</span><span class="sxs-lookup"><span data-stu-id="30f4a-119">The media type is compatible.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="30f4a-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="30f4a-120">Requirements</span></span>



| <span data-ttu-id="30f4a-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="30f4a-121">Requirement</span></span> | <span data-ttu-id="30f4a-122">Valor</span><span class="sxs-lookup"><span data-stu-id="30f4a-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30f4a-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="30f4a-123">Header</span></span><br/>  | <dl> <span data-ttu-id="30f4a-124"><dt>Winutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="30f4a-124"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="30f4a-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="30f4a-125">Library</span></span><br/> | <dl> <span data-ttu-id="30f4a-126"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="30f4a-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30f4a-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="30f4a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30f4a-128">**Classe CImageDisplay**</span><span class="sxs-lookup"><span data-stu-id="30f4a-128">**CImageDisplay Class**</span></span>](cimagedisplay.md)
</dt> </dl>

 

 




