---
description: O método Notify recebe uma notificação de que uma alteração de qualidade é solicitada.
ms.assetid: bb9aa1c3-caef-42fb-87d2-75cc3691f64f
title: Método CBaseVideoRenderer. Notify (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.Notify
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cd2b894bf78163a7b2d2387e43ecb5cec76ffdf4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750058"
---
# <a name="cbasevideorenderernotify-method"></a><span data-ttu-id="638d7-103">Método CBaseVideoRenderer. Notify</span><span class="sxs-lookup"><span data-stu-id="638d7-103">CBaseVideoRenderer.Notify method</span></span>

<span data-ttu-id="638d7-104">O `Notify` método recebe uma notificação de que uma alteração de qualidade é solicitada.</span><span class="sxs-lookup"><span data-stu-id="638d7-104">The `Notify` method receives a notification that a quality change is requested.</span></span>

## <a name="syntax"></a><span data-ttu-id="638d7-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="638d7-105">Syntax</span></span>


```C++
HRESULT Notify(
  [in] IBaseFilter *pSelf,
  [in] Quality     q
);
```



## <a name="parameters"></a><span data-ttu-id="638d7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="638d7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="638d7-107">*pSelf* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="638d7-107">*pSelf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="638d7-108">Ponteiro para o filtro que está enviando a notificação de qualidade.</span><span class="sxs-lookup"><span data-stu-id="638d7-108">Pointer to the filter that is sending the quality notification.</span></span>

</dd> <dt>

<span data-ttu-id="638d7-109">*q* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="638d7-109">*q* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="638d7-110">Estrutura de notificação de qualidade.</span><span class="sxs-lookup"><span data-stu-id="638d7-110">Quality notification structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="638d7-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="638d7-111">Return value</span></span>

<span data-ttu-id="638d7-112">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="638d7-112">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="638d7-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="638d7-113">Remarks</span></span>

<span data-ttu-id="638d7-114">Essa função de membro implementa o método [**IQualityControl:: Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) no processador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="638d7-114">This member function implements the [**IQualityControl::Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) method on the video renderer.</span></span> <span data-ttu-id="638d7-115">Isso é chamado, normalmente pelo Gerenciador de gráfico de filtro, quando a qualidade deve ser recortada.</span><span class="sxs-lookup"><span data-stu-id="638d7-115">This is called, typically by the filter graph manager, when the quality must be cut back.</span></span> <span data-ttu-id="638d7-116">Isso pode ocorrer quando a qualidade da reprodução de áudio foi aumentada para o ponto em que a qualidade da reprodução do vídeo deve ser diminuída.</span><span class="sxs-lookup"><span data-stu-id="638d7-116">This might occur when the quality of audio playback has been increased to the point that the video playback quality must be decreased.</span></span>

<span data-ttu-id="638d7-117">`Notify` define o membro de dados **m \_ trThrottle** como um valor de atraso a ser inserido entre os quadros por [**ThrottleWait**](cbasevideorenderer-throttlewait.md).</span><span class="sxs-lookup"><span data-stu-id="638d7-117">`Notify` sets the **m\_trThrottle** data member to a delay value to be inserted between frames by [**ThrottleWait**](cbasevideorenderer-throttlewait.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="638d7-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="638d7-118">Requirements</span></span>



| <span data-ttu-id="638d7-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="638d7-119">Requirement</span></span> | <span data-ttu-id="638d7-120">Valor</span><span class="sxs-lookup"><span data-stu-id="638d7-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="638d7-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="638d7-121">Header</span></span><br/>  | <dl> <span data-ttu-id="638d7-122"><dt>Renbase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="638d7-122"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="638d7-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="638d7-123">Library</span></span><br/> | <dl> <span data-ttu-id="638d7-124"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="638d7-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="638d7-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="638d7-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="638d7-126">**Classe CBaseVideoRenderer**</span><span class="sxs-lookup"><span data-stu-id="638d7-126">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




