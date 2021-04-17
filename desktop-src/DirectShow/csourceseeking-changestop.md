---
description: O método ChangeStop é chamado quando a posição de parada é alterada.
ms.assetid: 3d4a73a4-68e6-449c-9637-62cad937c4b4
title: Método CSourceSeeking. ChangeStop (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.ChangeStop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: eefcc64b4692363c8caa8f39a3a0db9beb0d08b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760886"
---
# <a name="csourceseekingchangestop-method"></a><span data-ttu-id="879c4-103">Método CSourceSeeking. ChangeStop</span><span class="sxs-lookup"><span data-stu-id="879c4-103">CSourceSeeking.ChangeStop method</span></span>

<span data-ttu-id="879c4-104">O `ChangeStop` método é chamado quando a posição de parada é alterada.</span><span class="sxs-lookup"><span data-stu-id="879c4-104">The `ChangeStop` method is called when the stop position changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="879c4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="879c4-105">Syntax</span></span>


```C++
virtual HRESULT ChangeStop() = 0;
```



## <a name="parameters"></a><span data-ttu-id="879c4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="879c4-106">Parameters</span></span>

<span data-ttu-id="879c4-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="879c4-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="879c4-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="879c4-108">Return value</span></span>

<span data-ttu-id="879c4-109">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="879c4-109">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="879c4-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="879c4-110">Remarks</span></span>

<span data-ttu-id="879c4-111">O método [**CSourceSeeking:: Setposicionations**](csourceseeking-setpositions.md) chamará esse método se a posição de parada for alterada.</span><span class="sxs-lookup"><span data-stu-id="879c4-111">The [**CSourceSeeking::SetPositions**](csourceseeking-setpositions.md) method calls this method if the stop position changes.</span></span> <span data-ttu-id="879c4-112">Este método é virtual puro; a classe derivada deve implementá-la.</span><span class="sxs-lookup"><span data-stu-id="879c4-112">This method is pure virtual; the derived class must implement it.</span></span> <span data-ttu-id="879c4-113">O exemplo a seguir mostra uma possível implementação:</span><span class="sxs-lookup"><span data-stu-id="879c4-113">The following example shows a possible implementation:</span></span>


```C++
HRESULT CMyStream::ChangeStop( )
{
    UpdateFromSeek();
    return S_OK;
}
```



## <a name="requirements"></a><span data-ttu-id="879c4-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="879c4-114">Requirements</span></span>



| <span data-ttu-id="879c4-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="879c4-115">Requirement</span></span> | <span data-ttu-id="879c4-116">Valor</span><span class="sxs-lookup"><span data-stu-id="879c4-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="879c4-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="879c4-117">Header</span></span><br/>  | <dl> <span data-ttu-id="879c4-118"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="879c4-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="879c4-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="879c4-119">Library</span></span><br/> | <dl> <span data-ttu-id="879c4-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="879c4-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="879c4-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="879c4-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="879c4-122">**Classe CSourceSeeking**</span><span class="sxs-lookup"><span data-stu-id="879c4-122">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




