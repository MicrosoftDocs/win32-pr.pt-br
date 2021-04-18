---
description: O método getvideoclipize recupera a largura e a altura do vídeo nativo.
ms.assetid: b3461a56-705b-465a-9cfc-e86fd52a07c5
title: Método CBaseControlVideo. (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetVideoSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4b1df6fe781f036043728050354519dfa6e28d00
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749049"
---
# <a name="cbasecontrolvideogetvideosize-method"></a><span data-ttu-id="d610b-103">Método CBaseControlVideo.</span><span class="sxs-lookup"><span data-stu-id="d610b-103">CBaseControlVideo.GetVideoSize method</span></span>

<span data-ttu-id="d610b-104">O `GetVideoSize` método recupera a largura e a altura do vídeo nativo.</span><span class="sxs-lookup"><span data-stu-id="d610b-104">The `GetVideoSize` method retrieves the native video's width and height.</span></span>

## <a name="syntax"></a><span data-ttu-id="d610b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d610b-105">Syntax</span></span>


```C++
HRESULT GetVideoSize(
   long *pWidth,
   long *pHeight
);
```



## <a name="parameters"></a><span data-ttu-id="d610b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d610b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d610b-107">*pWidth*</span><span class="sxs-lookup"><span data-stu-id="d610b-107">*pWidth*</span></span> 
</dt> <dd>

<span data-ttu-id="d610b-108">Ponteiro para a largura do vídeo.</span><span class="sxs-lookup"><span data-stu-id="d610b-108">Pointer to the video width.</span></span>

</dd> <dt>

<span data-ttu-id="d610b-109">*pHeight*</span><span class="sxs-lookup"><span data-stu-id="d610b-109">*pHeight*</span></span> 
</dt> <dd>

<span data-ttu-id="d610b-110">Ponteiro para a altura do vídeo.</span><span class="sxs-lookup"><span data-stu-id="d610b-110">Pointer to the video height.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d610b-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d610b-111">Return value</span></span>

<span data-ttu-id="d610b-112">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d610b-112">Returns an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="d610b-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d610b-113">Requirements</span></span>



| <span data-ttu-id="d610b-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="d610b-114">Requirement</span></span> | <span data-ttu-id="d610b-115">Valor</span><span class="sxs-lookup"><span data-stu-id="d610b-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d610b-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d610b-116">Header</span></span><br/>  | <dl> <span data-ttu-id="d610b-117"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d610b-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d610b-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d610b-118">Library</span></span><br/> | <dl> <span data-ttu-id="d610b-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="d610b-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d610b-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="d610b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d610b-121">**Classe CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="d610b-121">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




