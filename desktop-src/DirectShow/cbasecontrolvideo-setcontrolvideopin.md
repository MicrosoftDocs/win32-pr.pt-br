---
description: O método SetControlVideoPin define o PIN usado pelo filtro.
ms.assetid: 4346f828-4380-4150-9ecb-74eb690bdcdf
title: Método CBaseControlVideo. SetControlVideoPin (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.SetControlVideoPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a4cf47469800a4d1ecd8abe373d6f3c1fd53ece5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755396"
---
# <a name="cbasecontrolvideosetcontrolvideopin-method"></a><span data-ttu-id="d24b7-103">Método CBaseControlVideo. SetControlVideoPin</span><span class="sxs-lookup"><span data-stu-id="d24b7-103">CBaseControlVideo.SetControlVideoPin method</span></span>

<span data-ttu-id="d24b7-104">O `SetControlVideoPin` método define o PIN usado pelo filtro.</span><span class="sxs-lookup"><span data-stu-id="d24b7-104">The `SetControlVideoPin` method sets the pin used by the filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="d24b7-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d24b7-105">Syntax</span></span>


```C++
void SetControlVideoPin(
   CBasePin *pPin
);
```



## <a name="parameters"></a><span data-ttu-id="d24b7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d24b7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d24b7-107">*pPin*</span><span class="sxs-lookup"><span data-stu-id="d24b7-107">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="d24b7-108">Ponteiro para o PIN com o qual a interface é sincronizada.</span><span class="sxs-lookup"><span data-stu-id="d24b7-108">Pointer to the pin with which the interface is synchronized.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d24b7-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d24b7-109">Return value</span></span>

<span data-ttu-id="d24b7-110">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="d24b7-110">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d24b7-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="d24b7-111">Remarks</span></span>

<span data-ttu-id="d24b7-112">A interface pode ser chamada somente quando o filtro tiver sido conectado com êxito.</span><span class="sxs-lookup"><span data-stu-id="d24b7-112">The interface can be called only when the filter has been connected successfully.</span></span> <span data-ttu-id="d24b7-113">O objeto é passado por esse método para o PIN com o qual ele é sincronizado; na maioria dos casos, ele determinará se o PIN está conectado quando tiver um método de interface chamado e retornará VFW \_ e \_ não \_ conectado se falhar.</span><span class="sxs-lookup"><span data-stu-id="d24b7-113">The object is passed through this method to the pin with which it is synchronized; in most cases it will determine if the pin is connected when it has an interface method called and will return VFW\_E\_NOT\_CONNECTED if it fails.</span></span>

## <a name="requirements"></a><span data-ttu-id="d24b7-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d24b7-114">Requirements</span></span>



| <span data-ttu-id="d24b7-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d24b7-115">Requirement</span></span> | <span data-ttu-id="d24b7-116">Valor</span><span class="sxs-lookup"><span data-stu-id="d24b7-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d24b7-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d24b7-117">Header</span></span><br/>  | <dl> <span data-ttu-id="d24b7-118"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d24b7-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d24b7-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d24b7-119">Library</span></span><br/> | <dl> <span data-ttu-id="d24b7-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="d24b7-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d24b7-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="d24b7-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d24b7-122">**Classe CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="d24b7-122">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




