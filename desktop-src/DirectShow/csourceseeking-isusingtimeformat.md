---
description: O método IsUsingTimeFormat determina se um formato de hora especificado é o formato em uso no momento.
ms.assetid: 86965bfc-fc9f-42d3-bcaa-2049195b98bd
title: Método CSourceSeeking. IsUsingTimeFormat (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.IsUsingTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8229387364a061febc7bd825e7bc76ee5d9b4a2d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748194"
---
# <a name="csourceseekingisusingtimeformat-method"></a><span data-ttu-id="99950-103">Método CSourceSeeking. IsUsingTimeFormat</span><span class="sxs-lookup"><span data-stu-id="99950-103">CSourceSeeking.IsUsingTimeFormat method</span></span>

<span data-ttu-id="99950-104">O `IsUsingTimeFormat` método determina se um formato de hora especificado é o formato em uso no momento.</span><span class="sxs-lookup"><span data-stu-id="99950-104">The `IsUsingTimeFormat` method determines whether a specified time format is the format currently in use.</span></span>

## <a name="syntax"></a><span data-ttu-id="99950-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="99950-105">Syntax</span></span>


```C++
HRESULT IsUsingTimeFormat(
   const GUID *pFormat
);
```



## <a name="parameters"></a><span data-ttu-id="99950-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="99950-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99950-107">*pFormat*</span><span class="sxs-lookup"><span data-stu-id="99950-107">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="99950-108">Ponteiro para um GUID de formato de hora.</span><span class="sxs-lookup"><span data-stu-id="99950-108">Pointer to a time format GUID.</span></span> <span data-ttu-id="99950-109">Consulte [**GUIDs de formato de hora**](time-format-guids.md).</span><span class="sxs-lookup"><span data-stu-id="99950-109">See [**Time Format GUIDs**](time-format-guids.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99950-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="99950-110">Return value</span></span>

<span data-ttu-id="99950-111">Retorna um dos valores **HRESULT** listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="99950-111">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="99950-112">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="99950-112">Return code</span></span>                                                                               | <span data-ttu-id="99950-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="99950-113">Description</span></span>                                                |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <span data-ttu-id="99950-114"><dt>**\_falso**</dt></span><span class="sxs-lookup"><span data-stu-id="99950-114"><dt>**S\_FALSE**</dt></span></span> </dl>   | <span data-ttu-id="99950-115">O formato especificado não é o formato atual.</span><span class="sxs-lookup"><span data-stu-id="99950-115">The specified format is not the current format.</span></span><br/> |
| <dl> <span data-ttu-id="99950-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="99950-116"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="99950-117">O formato especificado é o formato atual.</span><span class="sxs-lookup"><span data-stu-id="99950-117">The specified format is the current format.</span></span><br/>     |
| <dl> <span data-ttu-id="99950-118"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="99950-118"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="99950-119">Argumento de ponteiro **nulo** .</span><span class="sxs-lookup"><span data-stu-id="99950-119">**NULL** pointer argument.</span></span><br/>                      |



 

## <a name="remarks"></a><span data-ttu-id="99950-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="99950-120">Remarks</span></span>

<span data-ttu-id="99950-121">O único formato de tempo com suporte da classe base é \_ o \_ tempo de mídia de formato de hora \_ (unidades de 100 nanossegundos).</span><span class="sxs-lookup"><span data-stu-id="99950-121">The only time format supported by the base class is TIME\_FORMAT\_MEDIA\_TIME (100-nanosecond units).</span></span>

## <a name="requirements"></a><span data-ttu-id="99950-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="99950-122">Requirements</span></span>



| <span data-ttu-id="99950-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="99950-123">Requirement</span></span> | <span data-ttu-id="99950-124">Valor</span><span class="sxs-lookup"><span data-stu-id="99950-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99950-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="99950-125">Header</span></span><br/>  | <dl> <span data-ttu-id="99950-126"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="99950-126"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="99950-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="99950-127">Library</span></span><br/> | <dl> <span data-ttu-id="99950-128"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="99950-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99950-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="99950-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99950-130">**Classe CSourceSeeking**</span><span class="sxs-lookup"><span data-stu-id="99950-130">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




