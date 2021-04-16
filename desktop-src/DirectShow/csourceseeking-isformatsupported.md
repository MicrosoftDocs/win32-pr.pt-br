---
description: 'O método IsFormatSupported determina se há suporte para um formato de hora especificado. Esse método implementa o método IMediaSeeking:: IsFormatSupported.'
ms.assetid: 79b6dfd4-7f03-479b-b855-8f389bf6cbc7
title: Método CSourceSeeking. IsFormatSupported (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.IsFormatSupported
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7d027a2ee6e94e4ccf4944c27e77f02d1d1c5edb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758071"
---
# <a name="csourceseekingisformatsupported-method"></a><span data-ttu-id="290f3-104">Método CSourceSeeking. IsFormatSupported</span><span class="sxs-lookup"><span data-stu-id="290f3-104">CSourceSeeking.IsFormatSupported method</span></span>

<span data-ttu-id="290f3-105">O `IsFormatSupported` método determina se há suporte para um formato de hora especificado.</span><span class="sxs-lookup"><span data-stu-id="290f3-105">The `IsFormatSupported` method determines whether a specified time format is supported.</span></span> <span data-ttu-id="290f3-106">Esse método implementa o método [**IMediaSeeking:: IsFormatSupported**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isformatsupported) .</span><span class="sxs-lookup"><span data-stu-id="290f3-106">This method implements the [**IMediaSeeking::IsFormatSupported**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isformatsupported) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="290f3-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="290f3-107">Syntax</span></span>


```C++
HRESULT IsFormatSupported(
   const GUID *pFormat
);
```



## <a name="parameters"></a><span data-ttu-id="290f3-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="290f3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="290f3-109">*pFormat*</span><span class="sxs-lookup"><span data-stu-id="290f3-109">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="290f3-110">Ponteiro para um GUID de formato de hora.</span><span class="sxs-lookup"><span data-stu-id="290f3-110">Pointer to a time format GUID.</span></span> <span data-ttu-id="290f3-111">Consulte [**GUIDs de formato de hora**](time-format-guids.md).</span><span class="sxs-lookup"><span data-stu-id="290f3-111">See [**Time Format GUIDs**](time-format-guids.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="290f3-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="290f3-112">Return value</span></span>

<span data-ttu-id="290f3-113">Retorna um dos valores **HRESULT** listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="290f3-113">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="290f3-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="290f3-114">Return code</span></span>                                                                               | <span data-ttu-id="290f3-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="290f3-115">Description</span></span>                             |
|-------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="290f3-116"><dt>**\_falso**</dt></span><span class="sxs-lookup"><span data-stu-id="290f3-116"><dt>**S\_FALSE**</dt></span></span> </dl>   | <span data-ttu-id="290f3-117">Não há suporte para o formato.</span><span class="sxs-lookup"><span data-stu-id="290f3-117">The format is not supported.</span></span><br/> |
| <dl> <span data-ttu-id="290f3-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="290f3-118"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="290f3-119">Há suporte para o formato.</span><span class="sxs-lookup"><span data-stu-id="290f3-119">The format is supported.</span></span><br/>     |
| <dl> <span data-ttu-id="290f3-120"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="290f3-120"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="290f3-121">Argumento de ponteiro **nulo** .</span><span class="sxs-lookup"><span data-stu-id="290f3-121">**NULL** pointer argument.</span></span><br/>   |



 

## <a name="remarks"></a><span data-ttu-id="290f3-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="290f3-122">Remarks</span></span>

<span data-ttu-id="290f3-123">O único formato de tempo com suporte da classe base é \_ o \_ tempo de mídia de formato de hora \_ (unidades de 100 nanossegundos).</span><span class="sxs-lookup"><span data-stu-id="290f3-123">The only time format supported by the base class is TIME\_FORMAT\_MEDIA\_TIME (100-nanosecond units).</span></span>

## <a name="requirements"></a><span data-ttu-id="290f3-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="290f3-124">Requirements</span></span>



| <span data-ttu-id="290f3-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="290f3-125">Requirement</span></span> | <span data-ttu-id="290f3-126">Valor</span><span class="sxs-lookup"><span data-stu-id="290f3-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="290f3-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="290f3-127">Header</span></span><br/>  | <dl> <span data-ttu-id="290f3-128"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="290f3-128"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="290f3-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="290f3-129">Library</span></span><br/> | <dl> <span data-ttu-id="290f3-130"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="290f3-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="290f3-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="290f3-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="290f3-132">**Classe CSourceSeeking**</span><span class="sxs-lookup"><span data-stu-id="290f3-132">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




