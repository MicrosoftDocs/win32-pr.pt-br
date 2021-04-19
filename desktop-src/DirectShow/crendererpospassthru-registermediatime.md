---
description: O método RegisterMediaTime armazena em cache os carimbos de data/hora do exemplo atual.
ms.assetid: 9ff8e4ec-3401-4272-894d-643f0fc029de
title: Método CRendererPosPassThru. RegisterMediaTime (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererPosPassThru.RegisterMediaTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3c829690572d55ea700d51124b99370f23e755a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755588"
---
# <a name="crendererpospassthruregistermediatime-method-ctlutilh"></a><span data-ttu-id="0023c-103">Método CRendererPosPassThru. RegisterMediaTime (Ctlutil. h)</span><span class="sxs-lookup"><span data-stu-id="0023c-103">CRendererPosPassThru.RegisterMediaTime method (Ctlutil.h)</span></span>

<span data-ttu-id="0023c-104">O método **RegisterMediaTime** armazena em cache os carimbos de data/hora do exemplo atual.</span><span class="sxs-lookup"><span data-stu-id="0023c-104">The **RegisterMediaTime** method caches the time stamps from the current sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="0023c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0023c-105">Syntax</span></span>


```C++
HRESULT RegisterMediaTime(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="0023c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0023c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0023c-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="0023c-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="0023c-108">Ponteiro para a interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) do exemplo.</span><span class="sxs-lookup"><span data-stu-id="0023c-108">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface of the sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0023c-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0023c-109">Return value</span></span>

<span data-ttu-id="0023c-110">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0023c-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="0023c-111">Os valores possíveis incluem os listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="0023c-111">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="0023c-112">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="0023c-112">Return code</span></span>                                                                                                  | <span data-ttu-id="0023c-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="0023c-113">Description</span></span>                                |
|--------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <dl> <span data-ttu-id="0023c-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0023c-114"><dt>**S\_OK**</dt></span></span> </dl>                         | <span data-ttu-id="0023c-115">Êxito.</span><span class="sxs-lookup"><span data-stu-id="0023c-115">Success.</span></span><br/>                        |
| <dl> <span data-ttu-id="0023c-116"><dt>**VFW \_ E \_ hora de mídia \_ \_ não \_ definida**</dt></span><span class="sxs-lookup"><span data-stu-id="0023c-116"><dt>**VFW\_E\_MEDIA\_TIME\_NOT\_SET**</dt></span></span> </dl> | <span data-ttu-id="0023c-117">O exemplo não está com carimbo de data/hora.</span><span class="sxs-lookup"><span data-stu-id="0023c-117">The sample is not time-stamped.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0023c-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="0023c-118">Remarks</span></span>

<span data-ttu-id="0023c-119">Esse método armazena os carimbos de data/hora do exemplo atual.</span><span class="sxs-lookup"><span data-stu-id="0023c-119">This method stores the time stamps from the current sample.</span></span> <span data-ttu-id="0023c-120">O método [**CRendererPosPassThru:: GetMediaTime**](crendererpospassthru-getmediatime.md) recupera os mesmos valores.</span><span class="sxs-lookup"><span data-stu-id="0023c-120">The [**CRendererPosPassThru::GetMediaTime**](crendererpospassthru-getmediatime.md) method retrieves the same values.</span></span>

<span data-ttu-id="0023c-121">O filtro deve chamar esse método para cada amostra que receber.</span><span class="sxs-lookup"><span data-stu-id="0023c-121">The filter should call this method for each sample that it receives.</span></span> <span data-ttu-id="0023c-122">O método é sobrecarregado para aceitar um ponteiro para a amostra ou os próprios valores de carimbo de data/hora.</span><span class="sxs-lookup"><span data-stu-id="0023c-122">The method is overloaded to accept either a pointer to the sample, or the time stamp values themselves.</span></span>

## <a name="requirements"></a><span data-ttu-id="0023c-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0023c-123">Requirements</span></span>



| <span data-ttu-id="0023c-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="0023c-124">Requirement</span></span> | <span data-ttu-id="0023c-125">Valor</span><span class="sxs-lookup"><span data-stu-id="0023c-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0023c-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0023c-126">Header</span></span><br/>  | <dl> <span data-ttu-id="0023c-127"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0023c-127"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0023c-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0023c-128">Library</span></span><br/> | <dl> <span data-ttu-id="0023c-129"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="0023c-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




