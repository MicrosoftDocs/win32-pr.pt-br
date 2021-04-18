---
description: O \_ método Get AvgSyncOffset recupera a média do tempo em milissegundos entre quando cada quadro esteve devido e quando foi realmente renderizado para todos os quadros desde o início do streaming.
ms.assetid: b41741e9-e0b5-4c49-93ef-cb8c0cf2ddeb
title: Método de CBaseVideoRenderer.get_AvgSyncOffset (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.get_AvgSyncOffset
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 35c682b8f4bb60ec629db5489e879d1ca7968b77
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759324"
---
# <a name="cbasevideorendererget_avgsyncoffset-method"></a><span data-ttu-id="c366c-103">CBaseVideoRenderer. obter \_ método AvgSyncOffset</span><span class="sxs-lookup"><span data-stu-id="c366c-103">CBaseVideoRenderer.get\_AvgSyncOffset method</span></span>

<span data-ttu-id="c366c-104">O `get_AvgSyncOffset` método recupera a média do tempo em milissegundos entre quando cada quadro esteve devido e quando ele foi realmente renderizado para todos os quadros desde o início do streaming.</span><span class="sxs-lookup"><span data-stu-id="c366c-104">The `get_AvgSyncOffset` method retrieves the average of the time in milliseconds between when each frame was due and when it was actually rendered for all frames since streaming started.</span></span>

## <a name="syntax"></a><span data-ttu-id="c366c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c366c-105">Syntax</span></span>


```C++
HRESULT get_AvgSyncOffset(
   int *piAvg
);
```



## <a name="parameters"></a><span data-ttu-id="c366c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c366c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c366c-107">*piAvg*</span><span class="sxs-lookup"><span data-stu-id="c366c-107">*piAvg*</span></span> 
</dt> <dd>

<span data-ttu-id="c366c-108">Ponteiro para a média do tempo conforme descrito anteriormente.</span><span class="sxs-lookup"><span data-stu-id="c366c-108">Pointer to the average of the time as previously described.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c366c-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c366c-109">Return value</span></span>

<span data-ttu-id="c366c-110">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c366c-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c366c-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="c366c-111">Remarks</span></span>

<span data-ttu-id="c366c-112">Essa função de membro implementa o método [**IQualProp:: get \_ AvgSyncOffset**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_avgsyncoffset) .</span><span class="sxs-lookup"><span data-stu-id="c366c-112">This member function implements the [**IQualProp::get\_AvgSyncOffset**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_avgsyncoffset) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="c366c-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c366c-113">Requirements</span></span>



| <span data-ttu-id="c366c-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="c366c-114">Requirement</span></span> | <span data-ttu-id="c366c-115">Valor</span><span class="sxs-lookup"><span data-stu-id="c366c-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c366c-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c366c-116">Header</span></span><br/>  | <dl> <span data-ttu-id="c366c-117"><dt>Renbase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c366c-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c366c-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c366c-118">Library</span></span><br/> | <dl> <span data-ttu-id="c366c-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="c366c-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c366c-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="c366c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c366c-121">**Classe CBaseVideoRenderer**</span><span class="sxs-lookup"><span data-stu-id="c366c-121">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




