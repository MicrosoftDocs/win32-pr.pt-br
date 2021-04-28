---
description: 'Método CSourceSeeking. GetTimeFormat – o método GetTimeFormat recupera o formato de hora atual. Esse método implementa o método IMediaSeeking:: GetTimeFormat.'
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
ms.openlocfilehash: 4a56f9a490699d68d7a043e9385ad458562058f5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085214"
---
# <a name="csourceseekinggettimeformat-method"></a><span data-ttu-id="0726c-104">Método CSourceSeeking. GetTimeFormat</span><span class="sxs-lookup"><span data-stu-id="0726c-104">CSourceSeeking.GetTimeFormat method</span></span>

<span data-ttu-id="0726c-105">O `GetTimeFormat` método recupera o formato de hora atual.</span><span class="sxs-lookup"><span data-stu-id="0726c-105">The `GetTimeFormat` method retrieves the current time format.</span></span> <span data-ttu-id="0726c-106">Esse método implementa o método [**IMediaSeeking:: GetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-gettimeformat) .</span><span class="sxs-lookup"><span data-stu-id="0726c-106">This method implements the [**IMediaSeeking::GetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-gettimeformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="0726c-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0726c-107">Syntax</span></span>


```C++
HRESULT GetTimeFormat(
   const GUID *pFormat
);
```



## <a name="parameters"></a><span data-ttu-id="0726c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0726c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0726c-109">*pFormat*</span><span class="sxs-lookup"><span data-stu-id="0726c-109">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="0726c-110">Ponteiro para uma variável que recebe um GUID de formato de hora.</span><span class="sxs-lookup"><span data-stu-id="0726c-110">Pointer to a variable that receives a time format GUID.</span></span> <span data-ttu-id="0726c-111">Consulte [**GUIDs de formato de hora**](time-format-guids.md).</span><span class="sxs-lookup"><span data-stu-id="0726c-111">See [**Time Format GUIDs**](time-format-guids.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0726c-112">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="0726c-112">Return value</span></span>

<span data-ttu-id="0726c-113">Retorna um dos valores **HRESULT** listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="0726c-113">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="0726c-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="0726c-114">Return code</span></span>                                                                               | <span data-ttu-id="0726c-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="0726c-115">Description</span></span>                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <span data-ttu-id="0726c-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0726c-116"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="0726c-117">Êxito</span><span class="sxs-lookup"><span data-stu-id="0726c-117">Success</span></span><br/>                |
| <dl> <span data-ttu-id="0726c-118"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="0726c-118"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="0726c-119">Valor de ponteiro **nulo**</span><span class="sxs-lookup"><span data-stu-id="0726c-119">**NULL** pointer value</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0726c-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="0726c-120">Remarks</span></span>

<span data-ttu-id="0726c-121">O único formato de tempo com suporte da classe base é \_ o \_ tempo de mídia de formato de hora \_ (unidades de 100 nanossegundos).</span><span class="sxs-lookup"><span data-stu-id="0726c-121">The only time format supported by the base class is TIME\_FORMAT\_MEDIA\_TIME (100-nanosecond units).</span></span>

## <a name="requirements"></a><span data-ttu-id="0726c-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0726c-122">Requirements</span></span>



| <span data-ttu-id="0726c-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="0726c-123">Requirement</span></span> | <span data-ttu-id="0726c-124">Valor</span><span class="sxs-lookup"><span data-stu-id="0726c-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0726c-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0726c-125">Header</span></span><br/>  | <dl> <span data-ttu-id="0726c-126"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0726c-126"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0726c-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0726c-127">Library</span></span><br/> | <dl> <span data-ttu-id="0726c-128"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="0726c-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0726c-129">Consulte também</span><span class="sxs-lookup"><span data-stu-id="0726c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0726c-130">**Classe CSourceSeeking**</span><span class="sxs-lookup"><span data-stu-id="0726c-130">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




