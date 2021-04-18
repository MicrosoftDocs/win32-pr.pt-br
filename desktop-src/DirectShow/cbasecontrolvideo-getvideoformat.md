---
description: O método GetVideoFormat recupera um exemplo de vídeo que representa o formato de vídeo atual.
ms.assetid: f7457c5b-037c-4a63-963e-0fc6086609a4
title: Método CBaseControlVideo. GetVideoFormat (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetVideoFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d84b64818a02a60073fc21411e4a99bde07a6e00
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754772"
---
# <a name="cbasecontrolvideogetvideoformat-method"></a><span data-ttu-id="33e1f-103">Método CBaseControlVideo. GetVideoFormat</span><span class="sxs-lookup"><span data-stu-id="33e1f-103">CBaseControlVideo.GetVideoFormat method</span></span>

<span data-ttu-id="33e1f-104">O `GetVideoFormat` método recupera um exemplo de vídeo que representa o formato de vídeo atual.</span><span class="sxs-lookup"><span data-stu-id="33e1f-104">The `GetVideoFormat` method retrieves a video sample that represents the current video format.</span></span>

## <a name="syntax"></a><span data-ttu-id="33e1f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="33e1f-105">Syntax</span></span>


```C++
virtual VIDEOINFOHEADER* GetVideoFormat() = 0;
```



## <a name="parameters"></a><span data-ttu-id="33e1f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="33e1f-106">Parameters</span></span>

<span data-ttu-id="33e1f-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="33e1f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="33e1f-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="33e1f-108">Return value</span></span>

<span data-ttu-id="33e1f-109">Retorna um ponteiro para uma estrutura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) que contém o formato de vídeo atual.</span><span class="sxs-lookup"><span data-stu-id="33e1f-109">Returns a pointer to a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure that contains the current video format.</span></span>

## <a name="remarks"></a><span data-ttu-id="33e1f-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="33e1f-110">Remarks</span></span>

<span data-ttu-id="33e1f-111">Para retornar e verificar determinadas informações por meio de [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo), o objeto deve saber o formato de vídeo atual.</span><span class="sxs-lookup"><span data-stu-id="33e1f-111">To return and check certain information through [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo), the object must know the current video format.</span></span> <span data-ttu-id="33e1f-112">Ele obtém essas informações chamando esse método virtual puro que as classes derivadas devem substituir.</span><span class="sxs-lookup"><span data-stu-id="33e1f-112">It gets this information by calling this pure virtual method that derived classes must override.</span></span> <span data-ttu-id="33e1f-113">Essa função de membro é chamada pelas seguintes funções de membro [**CBaseControlVideo**](cbasecontrolvideo.md) .</span><span class="sxs-lookup"><span data-stu-id="33e1f-113">This member function is called by the following [**CBaseControlVideo**](cbasecontrolvideo.md) member functions.</span></span>

-   [<span data-ttu-id="33e1f-114">**CBaseControlVideo::OnVideoSizeChange**</span><span class="sxs-lookup"><span data-stu-id="33e1f-114">**CBaseControlVideo::OnVideoSizeChange**</span></span>](cbasecontrolvideo-onvideosizechange.md)
-   [<span data-ttu-id="33e1f-115">**CBaseControlVideo:: obter \_ AvgTimePerFrame**</span><span class="sxs-lookup"><span data-stu-id="33e1f-115">**CBaseControlVideo::get\_AvgTimePerFrame**</span></span>](cbasecontrolvideo-get-avgtimeperframe.md)
-   [<span data-ttu-id="33e1f-116">**CBaseControlVideo:: obter \_ taxa de bits**</span><span class="sxs-lookup"><span data-stu-id="33e1f-116">**CBaseControlVideo::get\_BitRate**</span></span>](cbasecontrolvideo-get-bitrate.md)
-   [<span data-ttu-id="33e1f-117">**CBaseControlVideo:: obter \_ BitErrorRate**</span><span class="sxs-lookup"><span data-stu-id="33e1f-117">**CBaseControlVideo::get\_BitErrorRate**</span></span>](cbasecontrolvideo-get-biterrorrate.md)
-   [<span data-ttu-id="33e1f-118">**CBaseControlVideo:: obter \_ VideoWidth**</span><span class="sxs-lookup"><span data-stu-id="33e1f-118">**CBaseControlVideo::get\_VideoWidth**</span></span>](cbasecontrolvideo-get-videowidth.md)
-   [<span data-ttu-id="33e1f-119">**CBaseControlVideo:: obter \_ VideoHeight**</span><span class="sxs-lookup"><span data-stu-id="33e1f-119">**CBaseControlVideo::get\_VideoHeight**</span></span>](cbasecontrolvideo-get-videoheight.md)
-   [<span data-ttu-id="33e1f-120">**CBaseControlVideo::GetVideoPaletteEntries**</span><span class="sxs-lookup"><span data-stu-id="33e1f-120">**CBaseControlVideo::GetVideoPaletteEntries**</span></span>](cbasecontrolvideo-getvideopaletteentries.md)
-   [<span data-ttu-id="33e1f-121">**CBaseControlVideo::**</span><span class="sxs-lookup"><span data-stu-id="33e1f-121">**CBaseControlVideo::GetVideoSize**</span></span>](cbasecontrolvideo-getvideosize.md)

## <a name="requirements"></a><span data-ttu-id="33e1f-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="33e1f-122">Requirements</span></span>



| <span data-ttu-id="33e1f-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="33e1f-123">Requirement</span></span> | <span data-ttu-id="33e1f-124">Valor</span><span class="sxs-lookup"><span data-stu-id="33e1f-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33e1f-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="33e1f-125">Header</span></span><br/>  | <dl> <span data-ttu-id="33e1f-126"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="33e1f-126"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="33e1f-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="33e1f-127">Library</span></span><br/> | <dl> <span data-ttu-id="33e1f-128"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="33e1f-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33e1f-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="33e1f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33e1f-130">**Classe CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="33e1f-130">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




