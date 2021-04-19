---
description: 'O método GetCurrentPosition recupera a posição atual, em relação à duração total do fluxo. Esse método implementa o método IMediaSeeking:: GetCurrentPosition.'
ms.assetid: 07020182-2199-4153-9bab-f30d112bc09f
title: Método CPosPassThru. GetCurrentPosition (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetCurrentPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5cdbd93edf7630499f6585fbbf6e34a70bed68c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105768652"
---
# <a name="cpospassthrugetcurrentposition-method"></a><span data-ttu-id="93069-104">Método CPosPassThru. GetCurrentPosition</span><span class="sxs-lookup"><span data-stu-id="93069-104">CPosPassThru.GetCurrentPosition method</span></span>

<span data-ttu-id="93069-105">O `GetCurrentPosition` método recupera a posição atual, em relação à duração total do fluxo.</span><span class="sxs-lookup"><span data-stu-id="93069-105">The `GetCurrentPosition` method retrieves the current position, relative to the total duration of the stream.</span></span> <span data-ttu-id="93069-106">Esse método implementa o método [**IMediaSeeking:: getCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) .</span><span class="sxs-lookup"><span data-stu-id="93069-106">This method implements the [**IMediaSeeking::GetCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="93069-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="93069-107">Syntax</span></span>


```C++
HRESULT GetCurrentPosition(
   LONGLONG *pCurrent
);
```



## <a name="parameters"></a><span data-ttu-id="93069-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="93069-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93069-109">*pCurrent*</span><span class="sxs-lookup"><span data-stu-id="93069-109">*pCurrent*</span></span> 
</dt> <dd>

<span data-ttu-id="93069-110">Ponteiro para uma variável que recebe a posição atual, em unidades do formato de hora atual.</span><span class="sxs-lookup"><span data-stu-id="93069-110">Pointer to a variable that receives the current position, in units of the current time format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93069-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="93069-111">Return value</span></span>

<span data-ttu-id="93069-112">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="93069-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="93069-113">Os valores possíveis incluem os mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="93069-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="93069-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="93069-114">Return code</span></span>                                                                               | <span data-ttu-id="93069-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="93069-115">Description</span></span>                           |
|-------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="93069-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="93069-116"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="93069-117">Êxito.</span><span class="sxs-lookup"><span data-stu-id="93069-117">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="93069-118"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="93069-118"><dt>**E\_NOTIMPL**</dt></span></span> </dl> | <span data-ttu-id="93069-119">Não há suporte para o método.</span><span class="sxs-lookup"><span data-stu-id="93069-119">Method is not supported.</span></span><br/>   |
| <dl> <span data-ttu-id="93069-120"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="93069-120"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="93069-121">Argumento de ponteiro **nulo** .</span><span class="sxs-lookup"><span data-stu-id="93069-121">**NULL** pointer argument.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="93069-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="93069-122">Remarks</span></span>

<span data-ttu-id="93069-123">Esse método chama o método [**CPosPassThru:: GetMediaTime**](cpospassthru-getmediatime.md) para recuperar a posição mais recente.</span><span class="sxs-lookup"><span data-stu-id="93069-123">This method calls the [**CPosPassThru::GetMediaTime**](cpospassthru-getmediatime.md) method to retrieve the most recent position.</span></span> <span data-ttu-id="93069-124">Se **GetMediaTime** falhar, o método chamará **IMediaSeeking:: getCurrentPosition** no PIN conectado.</span><span class="sxs-lookup"><span data-stu-id="93069-124">If **GetMediaTime** fails, the method calls **IMediaSeeking::GetCurrentPosition** on the connected pin.</span></span>

<span data-ttu-id="93069-125">O método **GetMediaTime** falha, por padrão, na classe base.</span><span class="sxs-lookup"><span data-stu-id="93069-125">The **GetMediaTime** method fails by default in the base class.</span></span> <span data-ttu-id="93069-126">Se o filtro armazenar a posição atual em cache, substitua **GetMediaTime** para retornar o valor armazenado em cache.</span><span class="sxs-lookup"><span data-stu-id="93069-126">If your filter caches the current position, override **GetMediaTime** to return the cached value.</span></span>

## <a name="requirements"></a><span data-ttu-id="93069-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="93069-127">Requirements</span></span>



| <span data-ttu-id="93069-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="93069-128">Requirement</span></span> | <span data-ttu-id="93069-129">Valor</span><span class="sxs-lookup"><span data-stu-id="93069-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93069-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="93069-130">Header</span></span><br/>  | <dl> <span data-ttu-id="93069-131"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="93069-131"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="93069-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="93069-132">Library</span></span><br/> | <dl> <span data-ttu-id="93069-133"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="93069-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93069-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="93069-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93069-135">**Classe CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="93069-135">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




