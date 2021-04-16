---
description: O método DisplayTypeInfo exibe informações de tipo de mídia durante a depuração.
ms.assetid: fd10d37b-57f5-4246-8ca3-f4bc59911445
title: Método CBasePin. DisplayTypeInfo (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.DisplayTypeInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 681e424505bb2ff840ac5beaa48431f17a5d177b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750066"
---
# <a name="cbasepindisplaytypeinfo-method"></a><span data-ttu-id="aa18c-103">Método CBasePin. DisplayTypeInfo</span><span class="sxs-lookup"><span data-stu-id="aa18c-103">CBasePin.DisplayTypeInfo method</span></span>

<span data-ttu-id="aa18c-104">O `DisplayTypeInfo` método exibe informações de tipo de mídia durante a depuração.</span><span class="sxs-lookup"><span data-stu-id="aa18c-104">The `DisplayTypeInfo` method displays media type information during debugging.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa18c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="aa18c-105">Syntax</span></span>


```C++
void DisplayTypeInfo(
         IPin       *pPin,
   const CMediaType *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="aa18c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="aa18c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa18c-107">*pPin*</span><span class="sxs-lookup"><span data-stu-id="aa18c-107">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="aa18c-108">Ignorado.</span><span class="sxs-lookup"><span data-stu-id="aa18c-108">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="aa18c-109">*PMT*</span><span class="sxs-lookup"><span data-stu-id="aa18c-109">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="aa18c-110">Ponteiro para um objeto [**CMediaType**](cmediatype.md) que especifica o tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="aa18c-110">Pointer to a [**CMediaType**](cmediatype.md) object that specifies the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa18c-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="aa18c-111">Return value</span></span>

<span data-ttu-id="aa18c-112">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="aa18c-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="aa18c-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="aa18c-113">Remarks</span></span>

<span data-ttu-id="aa18c-114">Em compilações de depuração, esse método chama a função [**DbgLog**](dbglog.md) para exibir o tipo de mídia especificado.</span><span class="sxs-lookup"><span data-stu-id="aa18c-114">In debug builds, this method calls the [**DbgLog**](dbglog.md) function to display the specified media type.</span></span> <span data-ttu-id="aa18c-115">Em compilações de varejo, esse método não faz nada.</span><span class="sxs-lookup"><span data-stu-id="aa18c-115">In retail builds, this method does nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa18c-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aa18c-116">Requirements</span></span>



| <span data-ttu-id="aa18c-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa18c-117">Requirement</span></span> | <span data-ttu-id="aa18c-118">Valor</span><span class="sxs-lookup"><span data-stu-id="aa18c-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa18c-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="aa18c-119">Header</span></span><br/>  | <dl> <span data-ttu-id="aa18c-120"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="aa18c-120"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="aa18c-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="aa18c-121">Library</span></span><br/> | <dl> <span data-ttu-id="aa18c-122"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="aa18c-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa18c-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="aa18c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa18c-124">**Classe CBasePin**</span><span class="sxs-lookup"><span data-stu-id="aa18c-124">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




