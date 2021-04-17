---
description: O método ForceRefresh é obsoleto.
ms.assetid: 9895f72b-abf8-46a8-aa75-2a30901a4c41
title: Método CPosPassThru. ForceRefresh (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.ForceRefresh
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1955afe069dc419b710978eecf662758916e4cb1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789702"
---
# <a name="cpospassthruforcerefresh-method"></a><span data-ttu-id="67ee9-103">Método CPosPassThru. ForceRefresh</span><span class="sxs-lookup"><span data-stu-id="67ee9-103">CPosPassThru.ForceRefresh method</span></span>

<span data-ttu-id="67ee9-104">O `ForceRefresh` método está obsoleto.</span><span class="sxs-lookup"><span data-stu-id="67ee9-104">The `ForceRefresh` method is obsolete.</span></span>

## <a name="syntax"></a><span data-ttu-id="67ee9-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="67ee9-105">Syntax</span></span>


```C++
HRESULT ForceRefresh();
```



## <a name="parameters"></a><span data-ttu-id="67ee9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="67ee9-106">Parameters</span></span>

<span data-ttu-id="67ee9-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="67ee9-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="67ee9-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="67ee9-108">Return value</span></span>

<span data-ttu-id="67ee9-109">Retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="67ee9-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="67ee9-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="67ee9-110">Remarks</span></span>

<span data-ttu-id="67ee9-111">Originalmente, essa classe foi projetada para armazenar em cache ponteiros para as interfaces [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) e [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) do PIN conectado.</span><span class="sxs-lookup"><span data-stu-id="67ee9-111">Originally this class was designed to cache pointers to the connected pin's [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) and [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interfaces.</span></span> <span data-ttu-id="67ee9-112">O `ForceRefresh` método liberou essas interfaces.</span><span class="sxs-lookup"><span data-stu-id="67ee9-112">The `ForceRefresh` method released those interfaces.</span></span>

<span data-ttu-id="67ee9-113">Como implementado atualmente, essa classe não armazena em cache essas interfaces.</span><span class="sxs-lookup"><span data-stu-id="67ee9-113">As currently implemented, this class does not cache those interfaces.</span></span> <span data-ttu-id="67ee9-114">Para compatibilidade, o `ForceRefresh` método ainda é incluído, mas ele retorna S \_ OK sem fazer nada.</span><span class="sxs-lookup"><span data-stu-id="67ee9-114">For compatibility, the `ForceRefresh` method is still included, but it returns S\_OK without doing anything.</span></span>

## <a name="requirements"></a><span data-ttu-id="67ee9-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="67ee9-115">Requirements</span></span>



| <span data-ttu-id="67ee9-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="67ee9-116">Requirement</span></span> | <span data-ttu-id="67ee9-117">Valor</span><span class="sxs-lookup"><span data-stu-id="67ee9-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67ee9-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="67ee9-118">Header</span></span><br/>  | <dl> <span data-ttu-id="67ee9-119"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="67ee9-119"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="67ee9-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="67ee9-120">Library</span></span><br/> | <dl> <span data-ttu-id="67ee9-121"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="67ee9-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67ee9-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="67ee9-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67ee9-123">**Classe CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="67ee9-123">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




