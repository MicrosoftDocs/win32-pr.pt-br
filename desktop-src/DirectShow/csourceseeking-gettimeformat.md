---
description: 'O método GetTimeFormat recupera o formato de hora atual. Esse método implementa o método IMediaSeeking:: GetTimeFormat.'
ms.assetid: c90804f7-9a0a-423c-8b26-87abf15eddc5
title: Método CSourceSeeking. GetTimeFormat (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ce53f4a6cabcc5face6c332666701dc208c3f8bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747814"
---
# <a name="csourceseekinggettimeformat-method"></a><span data-ttu-id="3f144-104">Método CSourceSeeking. GetTimeFormat</span><span class="sxs-lookup"><span data-stu-id="3f144-104">CSourceSeeking.GetTimeFormat method</span></span>

<span data-ttu-id="3f144-105">O `GetTimeFormat` método recupera o formato de hora atual.</span><span class="sxs-lookup"><span data-stu-id="3f144-105">The `GetTimeFormat` method retrieves the current time format.</span></span> <span data-ttu-id="3f144-106">Esse método implementa o método [**IMediaSeeking:: GetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-gettimeformat) .</span><span class="sxs-lookup"><span data-stu-id="3f144-106">This method implements the [**IMediaSeeking::GetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-gettimeformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f144-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3f144-107">Syntax</span></span>


```C++
HRESULT GetTimeFormat(
   const GUID *pFormat
);
```



## <a name="parameters"></a><span data-ttu-id="3f144-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3f144-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f144-109">*pFormat*</span><span class="sxs-lookup"><span data-stu-id="3f144-109">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="3f144-110">Ponteiro para uma variável que recebe um GUID de formato de hora.</span><span class="sxs-lookup"><span data-stu-id="3f144-110">Pointer to a variable that receives a time format GUID.</span></span> <span data-ttu-id="3f144-111">Consulte [**GUIDs de formato de hora**](time-format-guids.md).</span><span class="sxs-lookup"><span data-stu-id="3f144-111">See [**Time Format GUIDs**](time-format-guids.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f144-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3f144-112">Return value</span></span>

<span data-ttu-id="3f144-113">Retorna um dos valores **HRESULT** listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="3f144-113">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="3f144-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="3f144-114">Return code</span></span>                                                                               | <span data-ttu-id="3f144-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="3f144-115">Description</span></span>                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <span data-ttu-id="3f144-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3f144-116"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="3f144-117">Sucesso</span><span class="sxs-lookup"><span data-stu-id="3f144-117">Success</span></span><br/>                |
| <dl> <span data-ttu-id="3f144-118"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="3f144-118"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="3f144-119">Valor de ponteiro **nulo**</span><span class="sxs-lookup"><span data-stu-id="3f144-119">**NULL** pointer value</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3f144-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="3f144-120">Remarks</span></span>

<span data-ttu-id="3f144-121">O único formato de tempo com suporte da classe base é \_ o \_ tempo de mídia de formato de hora \_ (unidades de 100 nanossegundos).</span><span class="sxs-lookup"><span data-stu-id="3f144-121">The only time format supported by the base class is TIME\_FORMAT\_MEDIA\_TIME (100-nanosecond units).</span></span>

## <a name="requirements"></a><span data-ttu-id="3f144-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3f144-122">Requirements</span></span>



| <span data-ttu-id="3f144-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f144-123">Requirement</span></span> | <span data-ttu-id="3f144-124">Valor</span><span class="sxs-lookup"><span data-stu-id="3f144-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f144-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3f144-125">Header</span></span><br/>  | <dl> <span data-ttu-id="3f144-126"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3f144-126"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3f144-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3f144-127">Library</span></span><br/> | <dl> <span data-ttu-id="3f144-128"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="3f144-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f144-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="3f144-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f144-130">**Classe CSourceSeeking**</span><span class="sxs-lookup"><span data-stu-id="3f144-130">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




