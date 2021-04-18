---
description: O método SetSink define o objeto IQualityControl que receberá mensagens de qualidade.
ms.assetid: f5789781-1871-4fea-9d1f-bd1a21b70439
title: Método CBaseVideoRenderer. SetSink (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.SetSink
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9658ab4a1099e7baaef0a3e1a0ae3c0d495e89e6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105766328"
---
# <a name="cbasevideorenderersetsink-method"></a><span data-ttu-id="b6d9a-103">Método CBaseVideoRenderer. SetSink</span><span class="sxs-lookup"><span data-stu-id="b6d9a-103">CBaseVideoRenderer.SetSink method</span></span>

<span data-ttu-id="b6d9a-104">O `SetSink` método define o objeto [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) que receberá mensagens de qualidade.</span><span class="sxs-lookup"><span data-stu-id="b6d9a-104">The `SetSink` method sets the [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) object that will receive quality messages.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6d9a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b6d9a-105">Syntax</span></span>


```C++
HRESULT SetSink(
   IQualityControl *piqc
);
```



## <a name="parameters"></a><span data-ttu-id="b6d9a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b6d9a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6d9a-107">*piqc*</span><span class="sxs-lookup"><span data-stu-id="b6d9a-107">*piqc*</span></span> 
</dt> <dd>

<span data-ttu-id="b6d9a-108">Ponteiro para o objeto [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) para o qual as notificações devem ser enviadas.</span><span class="sxs-lookup"><span data-stu-id="b6d9a-108">Pointer to the [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) object to which the notifications should be sent.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6d9a-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b6d9a-109">Return value</span></span>

<span data-ttu-id="b6d9a-110">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b6d9a-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b6d9a-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="b6d9a-111">Remarks</span></span>

<span data-ttu-id="b6d9a-112">Essa função de membro implementa o método [**IQualityControl:: SetSink**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink) no processador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="b6d9a-112">This member function implements the [**IQualityControl::SetSink**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink) method on the video renderer.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6d9a-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b6d9a-113">Requirements</span></span>



| <span data-ttu-id="b6d9a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6d9a-114">Requirement</span></span> | <span data-ttu-id="b6d9a-115">Valor</span><span class="sxs-lookup"><span data-stu-id="b6d9a-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6d9a-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b6d9a-116">Header</span></span><br/>  | <dl> <span data-ttu-id="b6d9a-117"><dt>Renbase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b6d9a-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b6d9a-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b6d9a-118">Library</span></span><br/> | <dl> <span data-ttu-id="b6d9a-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="b6d9a-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6d9a-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="b6d9a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6d9a-121">**Classe CBaseVideoRenderer**</span><span class="sxs-lookup"><span data-stu-id="b6d9a-121">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




