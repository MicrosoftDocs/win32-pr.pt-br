---
description: O \_ método Get VideoWidth recupera a largura do vídeo nativo.
ms.assetid: dfd897f0-f580-44c0-9445-ba61ae267187
title: Método de CBaseControlVideo.get_VideoWidth (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_VideoWidth
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: faeeed7ea8af58103e74d9b8c3690523c893282f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749050"
---
# <a name="cbasecontrolvideoget_videowidth-method"></a><span data-ttu-id="4d421-103">CBaseControlVideo. obter \_ método VideoWidth</span><span class="sxs-lookup"><span data-stu-id="4d421-103">CBaseControlVideo.get\_VideoWidth method</span></span>

<span data-ttu-id="4d421-104">O `get_VideoWidth` método recupera a largura do vídeo nativo.</span><span class="sxs-lookup"><span data-stu-id="4d421-104">The `get_VideoWidth` method retrieves the width of the native video.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d421-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4d421-105">Syntax</span></span>


```C++
HRESULT get_VideoWidth(
   long *pVideoWidth
);
```



## <a name="parameters"></a><span data-ttu-id="4d421-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4d421-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d421-107">*pVideoWidth*</span><span class="sxs-lookup"><span data-stu-id="4d421-107">*pVideoWidth*</span></span> 
</dt> <dd>

<span data-ttu-id="4d421-108">Ponteiro para a largura do vídeo nativo, em pixels.</span><span class="sxs-lookup"><span data-stu-id="4d421-108">Pointer to the width of the native video, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d421-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4d421-109">Return value</span></span>

<span data-ttu-id="4d421-110">Retornará NOERROR se for bem-sucedido ou E \_ OUTOFMEMORY se não houver memória suficiente disponível.</span><span class="sxs-lookup"><span data-stu-id="4d421-110">Returns NOERROR if successful or E\_OUTOFMEMORY if there is not enough memory available.</span></span>

## <a name="remarks"></a><span data-ttu-id="4d421-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="4d421-111">Remarks</span></span>

<span data-ttu-id="4d421-112">Essa função de membro implementa o método [**IBasicVideo:: get \_ VideoWidth**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_videowidth) .</span><span class="sxs-lookup"><span data-stu-id="4d421-112">This member function implements the [**IBasicVideo::get\_VideoWidth**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_videowidth) method.</span></span> <span data-ttu-id="4d421-113">Ele chama o CBaseControlVideo virtual puro [**:: GetVideoFormat**](cbasecontrolvideo-getvideoformat.md) para recuperar a estrutura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) da classe derivada.</span><span class="sxs-lookup"><span data-stu-id="4d421-113">It calls the pure virtual [**CBaseControlVideo::GetVideoFormat**](cbasecontrolvideo-getvideoformat.md) to retrieve the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure from the derived class.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d421-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4d421-114">Requirements</span></span>



| <span data-ttu-id="4d421-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d421-115">Requirement</span></span> | <span data-ttu-id="4d421-116">Valor</span><span class="sxs-lookup"><span data-stu-id="4d421-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d421-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4d421-117">Header</span></span><br/>  | <dl> <span data-ttu-id="4d421-118"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4d421-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4d421-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4d421-119">Library</span></span><br/> | <dl> <span data-ttu-id="4d421-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="4d421-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d421-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="4d421-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d421-122">**Classe CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="4d421-122">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




