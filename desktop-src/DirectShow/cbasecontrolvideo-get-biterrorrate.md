---
description: O \_ método Get BitErrorRate recupera uma taxa aproximada de erros de bits para o vídeo.
ms.assetid: 4078611c-6e09-47c8-8e1c-f33bc6ddca79
title: Método de CBaseControlVideo.get_BitErrorRate (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_BitErrorRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9ae15a882f6dcd8840519f9067223dde3e925f6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755794"
---
# <a name="cbasecontrolvideoget_biterrorrate-method"></a><span data-ttu-id="feb6c-103">CBaseControlVideo. obter \_ método BitErrorRate</span><span class="sxs-lookup"><span data-stu-id="feb6c-103">CBaseControlVideo.get\_BitErrorRate method</span></span>

<span data-ttu-id="feb6c-104">O `get_BitErrorRate` método recupera uma taxa aproximada de erros de bits para o vídeo.</span><span class="sxs-lookup"><span data-stu-id="feb6c-104">The `get_BitErrorRate` method retrieves an approximate bit error rate for the video.</span></span>

## <a name="syntax"></a><span data-ttu-id="feb6c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="feb6c-105">Syntax</span></span>


```C++
HRESULT get_BitErrorRate(
   long *pBitErrorRate
);
```



## <a name="parameters"></a><span data-ttu-id="feb6c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="feb6c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="feb6c-107">*pBitErrorRate*</span><span class="sxs-lookup"><span data-stu-id="feb6c-107">*pBitErrorRate*</span></span> 
</dt> <dd>

<span data-ttu-id="feb6c-108">Ponteiro para a taxa de erros de bits (um erro para aproximadamente este número de bits).</span><span class="sxs-lookup"><span data-stu-id="feb6c-108">Pointer to the bit error rate (one error for approximately this many bits).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="feb6c-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="feb6c-109">Return value</span></span>

<span data-ttu-id="feb6c-110">Retornará NOERROR se for bem-sucedido ou E \_ OUTOFMEMORY se não houver memória suficiente disponível.</span><span class="sxs-lookup"><span data-stu-id="feb6c-110">Returns NOERROR if successful or E\_OUTOFMEMORY if there is not enough memory available.</span></span>

## <a name="remarks"></a><span data-ttu-id="feb6c-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="feb6c-111">Remarks</span></span>

<span data-ttu-id="feb6c-112">Essa função de membro implementa o método [**IBasicVideo:: get \_ BitErrorRate**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_biterrorrate) .</span><span class="sxs-lookup"><span data-stu-id="feb6c-112">This member function implements the [**IBasicVideo::get\_BitErrorRate**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_biterrorrate) method.</span></span> <span data-ttu-id="feb6c-113">Ele chama o método puro virtual [**CBaseControlVideo:: GetVideoFormat**](cbasecontrolvideo-getvideoformat.md) para recuperar a estrutura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) da classe derivada.</span><span class="sxs-lookup"><span data-stu-id="feb6c-113">It calls the pure virtual [**CBaseControlVideo::GetVideoFormat**](cbasecontrolvideo-getvideoformat.md) method to retrieve the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure from the derived class.</span></span>

## <a name="requirements"></a><span data-ttu-id="feb6c-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="feb6c-114">Requirements</span></span>



| <span data-ttu-id="feb6c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="feb6c-115">Requirement</span></span> | <span data-ttu-id="feb6c-116">Valor</span><span class="sxs-lookup"><span data-stu-id="feb6c-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="feb6c-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="feb6c-117">Header</span></span><br/>  | <dl> <span data-ttu-id="feb6c-118"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="feb6c-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="feb6c-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="feb6c-119">Library</span></span><br/> | <dl> <span data-ttu-id="feb6c-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="feb6c-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="feb6c-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="feb6c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="feb6c-122">**Classe CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="feb6c-122">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




