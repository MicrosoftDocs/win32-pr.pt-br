---
description: Evento sinalizado quando o PIN é bloqueado com êxito ou o usuário cancela um bloco pendente.
ms.assetid: 699bb7f7-e4f7-47c3-bbb1-0bc6556651ae
title: 'Membro CDynamicOutputPin:: m_hNotifyCallerPinBlockedEvent (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_hNotifyCallerPinBlockedEvent
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3e28aa890e15602376b9500243a89e8f0e3d3bb6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750484"
---
# <a name="cdynamicoutputpinm_hnotifycallerpinblockedevent-member"></a><span data-ttu-id="25f97-103">Membro de CDynamicOutputPin:: m \_ hNotifyCallerPinBlockedEvent</span><span class="sxs-lookup"><span data-stu-id="25f97-103">CDynamicOutputPin::m\_hNotifyCallerPinBlockedEvent member</span></span>

<span data-ttu-id="25f97-104">Evento sinalizado quando o PIN é bloqueado com êxito ou o usuário cancela um bloco pendente.</span><span class="sxs-lookup"><span data-stu-id="25f97-104">Event that is signaled when the pin successfully blocks, or the user cancels a pending block.</span></span>

## <a name="syntax"></a><span data-ttu-id="25f97-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="25f97-105">Syntax</span></span>


```C++
HANDLE m_hNotifyCallerPinBlockedEvent;
```



## <a name="remarks"></a><span data-ttu-id="25f97-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="25f97-106">Remarks</span></span>

<span data-ttu-id="25f97-107">Antes de acessar essa variável, mantenha a seção crítica [**CDynamicOutputPin:: m \_ BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) .</span><span class="sxs-lookup"><span data-stu-id="25f97-107">Before accessing this variable, hold the [**CDynamicOutputPin::m\_BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) critical section.</span></span>

## <a name="requirements"></a><span data-ttu-id="25f97-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="25f97-108">Requirements</span></span>



| <span data-ttu-id="25f97-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="25f97-109">Requirement</span></span> | <span data-ttu-id="25f97-110">Valor</span><span class="sxs-lookup"><span data-stu-id="25f97-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25f97-111">parâmetro</span><span class="sxs-lookup"><span data-stu-id="25f97-111">Header</span></span><br/>  | <dl> <span data-ttu-id="25f97-112"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="25f97-112"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="25f97-113">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="25f97-113">Library</span></span><br/> | <dl> <span data-ttu-id="25f97-114"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="25f97-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25f97-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="25f97-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25f97-116">**Classe CDynamicOutputPin**</span><span class="sxs-lookup"><span data-stu-id="25f97-116">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




