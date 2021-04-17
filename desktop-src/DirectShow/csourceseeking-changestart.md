---
description: O método altere é chamado quando a posição inicial é alterada.
ms.assetid: d0a5497e-43e9-4d1f-9106-1f4cd8fcb372
title: Método CSourceSeeking. Altere (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.ChangeStart
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d0a2751cf0ad1ecc6fddeeffd97b97c32b4a31b1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747815"
---
# <a name="csourceseekingchangestart-method"></a><span data-ttu-id="fb6b8-103">Método CSourceSeeking. Altere</span><span class="sxs-lookup"><span data-stu-id="fb6b8-103">CSourceSeeking.ChangeStart method</span></span>

<span data-ttu-id="fb6b8-104">O `ChangeStart` método é chamado quando a posição inicial é alterada.</span><span class="sxs-lookup"><span data-stu-id="fb6b8-104">The `ChangeStart` method is called when the start position changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb6b8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fb6b8-105">Syntax</span></span>


```C++
virtual HRESULT ChangeStart() = 0;
```



## <a name="parameters"></a><span data-ttu-id="fb6b8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fb6b8-106">Parameters</span></span>

<span data-ttu-id="fb6b8-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="fb6b8-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fb6b8-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fb6b8-108">Return value</span></span>

<span data-ttu-id="fb6b8-109">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="fb6b8-109">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fb6b8-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="fb6b8-110">Remarks</span></span>

<span data-ttu-id="fb6b8-111">O método [**CSourceSeeking:: Setposicionations**](csourceseeking-setpositions.md) chamará esse método se a posição inicial for alterada.</span><span class="sxs-lookup"><span data-stu-id="fb6b8-111">The [**CSourceSeeking::SetPositions**](csourceseeking-setpositions.md) method calls this method if the start position changes.</span></span> <span data-ttu-id="fb6b8-112">Este método é virtual puro; a classe derivada deve implementá-la.</span><span class="sxs-lookup"><span data-stu-id="fb6b8-112">This method is pure virtual; the derived class must implement it.</span></span> <span data-ttu-id="fb6b8-113">Após uma operação de busca, os carimbos de data/hora devem reiniciar de zero.</span><span class="sxs-lookup"><span data-stu-id="fb6b8-113">After a seek operation, time stamps should restart from zero.</span></span> <span data-ttu-id="fb6b8-114">Os horários de mídia devem refletir a nova hora de início.</span><span class="sxs-lookup"><span data-stu-id="fb6b8-114">Media times should reflect the new start time.</span></span> <span data-ttu-id="fb6b8-115">O exemplo a seguir mostra uma possível implementação:</span><span class="sxs-lookup"><span data-stu-id="fb6b8-115">The following example shows a possible implementation:</span></span>


```C++
HRESULT CMyStream::ChangeStart( )
{
    m_rtSampleTime = 0;          // Reset the time stamps.
    m_rtMediaTime = m_rtStart;   // Reset the media times.
    UpdateFromSeek();
    return S_OK;
}
```



## <a name="requirements"></a><span data-ttu-id="fb6b8-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fb6b8-116">Requirements</span></span>



| <span data-ttu-id="fb6b8-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb6b8-117">Requirement</span></span> | <span data-ttu-id="fb6b8-118">Valor</span><span class="sxs-lookup"><span data-stu-id="fb6b8-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb6b8-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fb6b8-119">Header</span></span><br/>  | <dl> <span data-ttu-id="fb6b8-120"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fb6b8-120"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="fb6b8-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fb6b8-121">Library</span></span><br/> | <dl> <span data-ttu-id="fb6b8-122"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="fb6b8-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb6b8-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="fb6b8-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb6b8-124">**Classe CSourceSeeking**</span><span class="sxs-lookup"><span data-stu-id="fb6b8-124">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




