---
description: O \_ método Get AvgTimePerFrame recupera o tempo médio por quadro.
ms.assetid: bcfdb241-9ec1-49f4-b2b5-0869c27da953
title: Método de CBaseControlVideo.get_AvgTimePerFrame (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_AvgTimePerFrame
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ae69140348be6e2fdfc120ee7fb40096d663f720
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105785500"
---
# <a name="cbasecontrolvideoget_avgtimeperframe-method"></a><span data-ttu-id="eb10d-103">CBaseControlVideo. obter \_ método AvgTimePerFrame</span><span class="sxs-lookup"><span data-stu-id="eb10d-103">CBaseControlVideo.get\_AvgTimePerFrame method</span></span>

<span data-ttu-id="eb10d-104">O `get_AvgTimePerFrame` método recupera o tempo médio por quadro.</span><span class="sxs-lookup"><span data-stu-id="eb10d-104">The `get_AvgTimePerFrame` method retrieves the average time per frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb10d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="eb10d-105">Syntax</span></span>


```C++
HRESULT get_AvgTimePerFrame(
   REFTIME *pAvgTimePerFrame
);
```



## <a name="parameters"></a><span data-ttu-id="eb10d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="eb10d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb10d-107">*pAvgTimePerFrame*</span><span class="sxs-lookup"><span data-stu-id="eb10d-107">*pAvgTimePerFrame*</span></span> 
</dt> <dd>

<span data-ttu-id="eb10d-108">Ponteiro para o tempo médio por quadro.</span><span class="sxs-lookup"><span data-stu-id="eb10d-108">Pointer to the average time per frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb10d-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="eb10d-109">Return value</span></span>

<span data-ttu-id="eb10d-110">Retornará NOERROR se for bem-sucedido ou E \_ OUTOFMEMORY se não houver memória suficiente disponível.</span><span class="sxs-lookup"><span data-stu-id="eb10d-110">Returns NOERROR if successful or E\_OUTOFMEMORY if there is not enough memory available.</span></span>

## <a name="remarks"></a><span data-ttu-id="eb10d-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="eb10d-111">Remarks</span></span>

<span data-ttu-id="eb10d-112">Essa função de membro implementa o método [**IBasicVideo:: get \_ AvgTimePerFrame**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_avgtimeperframe) .</span><span class="sxs-lookup"><span data-stu-id="eb10d-112">This member function implements the [**IBasicVideo::get\_AvgTimePerFrame**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_avgtimeperframe) method.</span></span> <span data-ttu-id="eb10d-113">Ele chama a função de membro puramente virtual [**CBaseControlVideo:: GetVideoFormat**](cbasecontrolvideo-getvideoformat.md) para recuperar a estrutura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) da classe derivada.</span><span class="sxs-lookup"><span data-stu-id="eb10d-113">It calls the pure virtual [**CBaseControlVideo::GetVideoFormat**](cbasecontrolvideo-getvideoformat.md) member function to retrieve the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure from the derived class.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb10d-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eb10d-114">Requirements</span></span>



| <span data-ttu-id="eb10d-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="eb10d-115">Requirement</span></span> | <span data-ttu-id="eb10d-116">Valor</span><span class="sxs-lookup"><span data-stu-id="eb10d-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb10d-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="eb10d-117">Header</span></span><br/>  | <dl> <span data-ttu-id="eb10d-118"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="eb10d-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="eb10d-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="eb10d-119">Library</span></span><br/> | <dl> <span data-ttu-id="eb10d-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="eb10d-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb10d-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="eb10d-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb10d-122">**Classe CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="eb10d-122">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




