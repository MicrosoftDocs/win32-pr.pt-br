---
description: 'O método QueryPreferredFormat recupera o formato de hora preferencial do objeto. Esse método implementa o método IMediaSeeking:: QueryPreferredFormat.'
ms.assetid: 3b73b7cf-1ba7-47c5-8442-5f138b74f335
title: Método CSourceSeeking. QueryPreferredFormat (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.QueryPreferredFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8916e23756279dd30eaf177ef839944a4c68d61a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782851"
---
# <a name="csourceseekingquerypreferredformat-method"></a><span data-ttu-id="42cc9-104">Método CSourceSeeking. QueryPreferredFormat</span><span class="sxs-lookup"><span data-stu-id="42cc9-104">CSourceSeeking.QueryPreferredFormat method</span></span>

<span data-ttu-id="42cc9-105">O `QueryPreferredFormat` método recupera o formato de hora preferencial do objeto.</span><span class="sxs-lookup"><span data-stu-id="42cc9-105">The `QueryPreferredFormat` method retrieves the object's preferred time format.</span></span> <span data-ttu-id="42cc9-106">Esse método implementa o método [**IMediaSeeking:: QueryPreferredFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-querypreferredformat) .</span><span class="sxs-lookup"><span data-stu-id="42cc9-106">This method implements the [**IMediaSeeking::QueryPreferredFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-querypreferredformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="42cc9-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="42cc9-107">Syntax</span></span>


```C++
HRESULT QueryPreferredFormat(
   GUID *pFormat
);
```



## <a name="parameters"></a><span data-ttu-id="42cc9-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="42cc9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42cc9-109">*pFormat*</span><span class="sxs-lookup"><span data-stu-id="42cc9-109">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="42cc9-110">Ponteiro para uma variável que recebe um GUID de formato de hora.</span><span class="sxs-lookup"><span data-stu-id="42cc9-110">Pointer to a variable that receives a time format GUID.</span></span> <span data-ttu-id="42cc9-111">Consulte [**GUIDs de formato de hora**](time-format-guids.md).</span><span class="sxs-lookup"><span data-stu-id="42cc9-111">See [**Time Format GUIDs**](time-format-guids.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42cc9-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="42cc9-112">Return value</span></span>

<span data-ttu-id="42cc9-113">Retorna um dos valores **HRESULT** listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="42cc9-113">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="42cc9-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="42cc9-114">Return code</span></span>                                                                               | <span data-ttu-id="42cc9-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="42cc9-115">Description</span></span>                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <span data-ttu-id="42cc9-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="42cc9-116"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="42cc9-117">Sucesso</span><span class="sxs-lookup"><span data-stu-id="42cc9-117">Success</span></span><br/>                |
| <dl> <span data-ttu-id="42cc9-118"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="42cc9-118"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="42cc9-119">Valor de ponteiro **nulo**</span><span class="sxs-lookup"><span data-stu-id="42cc9-119">**NULL** pointer value</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="42cc9-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="42cc9-120">Remarks</span></span>

<span data-ttu-id="42cc9-121">O único formato de tempo com suporte da classe base é \_ o \_ tempo de mídia de formato de hora \_ (unidades de 100 nanossegundos).</span><span class="sxs-lookup"><span data-stu-id="42cc9-121">The only time format supported by the base class is TIME\_FORMAT\_MEDIA\_TIME (100-nanosecond units).</span></span>

## <a name="requirements"></a><span data-ttu-id="42cc9-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="42cc9-122">Requirements</span></span>



| <span data-ttu-id="42cc9-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="42cc9-123">Requirement</span></span> | <span data-ttu-id="42cc9-124">Valor</span><span class="sxs-lookup"><span data-stu-id="42cc9-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42cc9-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="42cc9-125">Header</span></span><br/>  | <dl> <span data-ttu-id="42cc9-126"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="42cc9-126"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="42cc9-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="42cc9-127">Library</span></span><br/> | <dl> <span data-ttu-id="42cc9-128"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="42cc9-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42cc9-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="42cc9-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42cc9-130">**Classe CSourceSeeking**</span><span class="sxs-lookup"><span data-stu-id="42cc9-130">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




