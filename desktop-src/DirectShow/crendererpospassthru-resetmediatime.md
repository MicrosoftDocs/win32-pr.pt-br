---
description: O método ResetMediaTime redefine os carimbos de data/hora em cache como zero.
ms.assetid: 80dd2ae3-0a83-4017-8860-a089bef9a919
title: Método CRendererPosPassThru. ResetMediaTime (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererPosPassThru.ResetMediaTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 667b060258864290b64c5ffd780488ccb5d442ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752285"
---
# <a name="crendererpospassthruresetmediatime-method"></a><span data-ttu-id="f581c-103">Método CRendererPosPassThru. ResetMediaTime</span><span class="sxs-lookup"><span data-stu-id="f581c-103">CRendererPosPassThru.ResetMediaTime method</span></span>

<span data-ttu-id="f581c-104">O `ResetMediaTime` método redefine os carimbos de data/hora em cache como zero.</span><span class="sxs-lookup"><span data-stu-id="f581c-104">The `ResetMediaTime` method resets the cached time stamps to zero.</span></span>

## <a name="syntax"></a><span data-ttu-id="f581c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f581c-105">Syntax</span></span>


```C++
HRESULT ResetMediaTime();
```



## <a name="parameters"></a><span data-ttu-id="f581c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f581c-106">Parameters</span></span>

<span data-ttu-id="f581c-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="f581c-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f581c-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f581c-108">Return value</span></span>

<span data-ttu-id="f581c-109">Retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f581c-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="f581c-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="f581c-110">Remarks</span></span>

<span data-ttu-id="f581c-111">O filtro deve chamar esse método sempre que os carimbos de data/hora armazenados em cache pelo método [**CRendererPosPassThru:: RegisterMediaTime**](crendererpospassthru-registermediatime.md) se tornarem inválidos.</span><span class="sxs-lookup"><span data-stu-id="f581c-111">The filter should call this method whenever the time stamps cached by the [**CRendererPosPassThru::RegisterMediaTime**](crendererpospassthru-registermediatime.md) method become invalid.</span></span> <span data-ttu-id="f581c-112">Especificamente, ele deve chamar esse método em resposta aos métodos [**IPin:: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) e [**IMediaFilter:: Stop**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop) .</span><span class="sxs-lookup"><span data-stu-id="f581c-112">Specifically, it should call this method in response to the [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) and [**IMediaFilter::Stop**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop) methods.</span></span>

<span data-ttu-id="f581c-113">Depois que esse método é chamado, o método [**CRendererPosPassThru:: GetMediaTime**](crendererpospassthru-getmediatime.md) retorna zero para os horários de início e término.</span><span class="sxs-lookup"><span data-stu-id="f581c-113">After this method is called, the [**CRendererPosPassThru::GetMediaTime**](crendererpospassthru-getmediatime.md) method returns zero for the start and end times.</span></span>

## <a name="requirements"></a><span data-ttu-id="f581c-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f581c-114">Requirements</span></span>



| <span data-ttu-id="f581c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="f581c-115">Requirement</span></span> | <span data-ttu-id="f581c-116">Valor</span><span class="sxs-lookup"><span data-stu-id="f581c-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f581c-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f581c-117">Header</span></span><br/>  | <dl> <span data-ttu-id="f581c-118"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f581c-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f581c-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f581c-119">Library</span></span><br/> | <dl> <span data-ttu-id="f581c-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="f581c-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




