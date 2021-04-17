---
description: O \_ método Get VideoHeight recupera a altura do vídeo nativo.
ms.assetid: f33ba789-f9c6-47f1-879b-241bfdc72010
title: Método de CBaseControlVideo.get_VideoHeight (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_VideoHeight
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4e738636cecd8031962ae31ebf54ac258d868013
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105784034"
---
# <a name="cbasecontrolvideoget_videoheight-method"></a><span data-ttu-id="ab13b-103">CBaseControlVideo. obter \_ método VideoHeight</span><span class="sxs-lookup"><span data-stu-id="ab13b-103">CBaseControlVideo.get\_VideoHeight method</span></span>

<span data-ttu-id="ab13b-104">O `get_VideoHeight` método recupera a altura do vídeo nativo.</span><span class="sxs-lookup"><span data-stu-id="ab13b-104">The `get_VideoHeight` method retrieves the height of the native video.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab13b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ab13b-105">Syntax</span></span>


```C++
HRESULT get_VideoHeight(
   long *pVideoHeight
);
```



## <a name="parameters"></a><span data-ttu-id="ab13b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ab13b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab13b-107">*pVideoHeight*</span><span class="sxs-lookup"><span data-stu-id="ab13b-107">*pVideoHeight*</span></span> 
</dt> <dd>

<span data-ttu-id="ab13b-108">Ponteiro para a altura do vídeo nativo, em pixels.</span><span class="sxs-lookup"><span data-stu-id="ab13b-108">Pointer to the height of the native video, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab13b-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ab13b-109">Return value</span></span>

<span data-ttu-id="ab13b-110">Retornará NOERROR se for bem-sucedido ou E \_ OUTOFMEMORY se não houver memória suficiente disponível.</span><span class="sxs-lookup"><span data-stu-id="ab13b-110">Returns NOERROR if successful or E\_OUTOFMEMORY if there is not enough memory available.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab13b-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="ab13b-111">Remarks</span></span>

<span data-ttu-id="ab13b-112">Essa função de membro implementa o método [**IBasicVideo:: get \_ VideoHeight**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_videoheight) .</span><span class="sxs-lookup"><span data-stu-id="ab13b-112">This member function implements the [**IBasicVideo::get\_VideoHeight**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_videoheight) method.</span></span> <span data-ttu-id="ab13b-113">Ele chama o CBaseControlVideo virtual puro [**:: GetVideoFormat**](cbasecontrolvideo-getvideoformat.md) para recuperar a estrutura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) da classe derivada.</span><span class="sxs-lookup"><span data-stu-id="ab13b-113">It calls the pure virtual [**CBaseControlVideo::GetVideoFormat**](cbasecontrolvideo-getvideoformat.md) to retrieve the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure from the derived class.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab13b-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ab13b-114">Requirements</span></span>



| <span data-ttu-id="ab13b-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab13b-115">Requirement</span></span> | <span data-ttu-id="ab13b-116">Valor</span><span class="sxs-lookup"><span data-stu-id="ab13b-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab13b-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ab13b-117">Header</span></span><br/>  | <dl> <span data-ttu-id="ab13b-118"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ab13b-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ab13b-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ab13b-119">Library</span></span><br/> | <dl> <span data-ttu-id="ab13b-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="ab13b-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab13b-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="ab13b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab13b-122">**Classe CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="ab13b-122">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




