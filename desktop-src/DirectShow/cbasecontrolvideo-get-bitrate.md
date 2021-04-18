---
description: O método Get taxa de bits \_ recupera uma taxa aproximada do vídeo.
ms.assetid: e12e4677-a038-479f-8b64-937ad521c4be
title: Método de CBaseControlVideo.get_BitRate (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_BitRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 62f1feaed786b397801bbd17d2d2d41c0ccb813d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810951"
---
# <a name="cbasecontrolvideoget_bitrate-method"></a><span data-ttu-id="4a708-103">Método de taxa de bits CBaseControlVideo. get \_</span><span class="sxs-lookup"><span data-stu-id="4a708-103">CBaseControlVideo.get\_BitRate method</span></span>

<span data-ttu-id="4a708-104">O `get_BitRate` método recupera uma taxa de bits aproximada para o vídeo.</span><span class="sxs-lookup"><span data-stu-id="4a708-104">The `get_BitRate` method retrieves an approximate bit rate for the video.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a708-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4a708-105">Syntax</span></span>


```C++
HRESULT get_BitRate(
   long *pBitRate
);
```



## <a name="parameters"></a><span data-ttu-id="4a708-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4a708-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a708-107">*pBitRate*</span><span class="sxs-lookup"><span data-stu-id="4a708-107">*pBitRate*</span></span> 
</dt> <dd>

<span data-ttu-id="4a708-108">Ponteiro para a taxa de bits, em bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="4a708-108">Pointer to the bit rate, in bits per second.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a708-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4a708-109">Return value</span></span>

<span data-ttu-id="4a708-110">Retorna NOERROR se for successful ou E \_ OUTOFMEMORY se não houver memória suficiente disponível.</span><span class="sxs-lookup"><span data-stu-id="4a708-110">Returns NOERROR if successful or E\_OUTOFMEMORY if not enough memory is available.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a708-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="4a708-111">Remarks</span></span>

<span data-ttu-id="4a708-112">Essa função de membro implementa o método [**IBasicVideo:: get \_ taxa de bits**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_bitrate) .</span><span class="sxs-lookup"><span data-stu-id="4a708-112">This member function implements the [**IBasicVideo::get\_BitRate**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_bitrate) method.</span></span> <span data-ttu-id="4a708-113">Ele chama o CBaseControlVideo virtual puro [**:: GetVideoFormat**](cbasecontrolvideo-getvideoformat.md) para recuperar a estrutura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) da classe derivada.</span><span class="sxs-lookup"><span data-stu-id="4a708-113">It calls the pure virtual [**CBaseControlVideo::GetVideoFormat**](cbasecontrolvideo-getvideoformat.md) to retrieve the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure from the derived class.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a708-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4a708-114">Requirements</span></span>



| <span data-ttu-id="4a708-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a708-115">Requirement</span></span> | <span data-ttu-id="4a708-116">Valor</span><span class="sxs-lookup"><span data-stu-id="4a708-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a708-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4a708-117">Header</span></span><br/>  | <dl> <span data-ttu-id="4a708-118"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4a708-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4a708-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4a708-119">Library</span></span><br/> | <dl> <span data-ttu-id="4a708-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="4a708-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a708-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="4a708-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a708-122">**Classe CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="4a708-122">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




