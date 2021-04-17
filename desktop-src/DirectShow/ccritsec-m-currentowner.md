---
description: Identificador de thread do thread proprietário.
ms.assetid: 495598db-a0c9-473b-8184-121a1939b55a
title: 'Membro CCritSec:: m_currentOwner (Wxutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_currentOwner
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b6dcb8d968f1f437087a94c5b08db12d31952d92
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748206"
---
# <a name="ccritsecm_currentowner-member"></a><span data-ttu-id="a8522-103">Membro de CCritSec:: m \_ currentOwner</span><span class="sxs-lookup"><span data-stu-id="a8522-103">CCritSec::m\_currentOwner member</span></span>

<span data-ttu-id="a8522-104">Identificador de thread do thread proprietário.</span><span class="sxs-lookup"><span data-stu-id="a8522-104">Thread identifier of the owning thread.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8522-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a8522-105">Syntax</span></span>


```C++
DWORD m_currentOwner;
```



## <a name="remarks"></a><span data-ttu-id="a8522-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="a8522-106">Remarks</span></span>

<span data-ttu-id="a8522-107">Essa variável de membro é definida somente na versão de depuração da classe base.</span><span class="sxs-lookup"><span data-stu-id="a8522-107">This member variable is defined only in the debug version of the base class.</span></span> <span data-ttu-id="a8522-108">A [seção crítica Depurando funções](critical-section-debugging-functions.md) usa esse membro.</span><span class="sxs-lookup"><span data-stu-id="a8522-108">The [Critical Section Debugging Functions](critical-section-debugging-functions.md) use this member.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8522-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a8522-109">Requirements</span></span>



| <span data-ttu-id="a8522-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8522-110">Requirement</span></span> | <span data-ttu-id="a8522-111">Valor</span><span class="sxs-lookup"><span data-stu-id="a8522-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8522-112">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a8522-112">Header</span></span><br/>  | <dl> <span data-ttu-id="a8522-113"><dt>Wxutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a8522-113"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="a8522-114">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a8522-114">Library</span></span><br/> | <dl> <span data-ttu-id="a8522-115"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="a8522-115"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8522-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="a8522-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8522-117">**Classe CCritSec**</span><span class="sxs-lookup"><span data-stu-id="a8522-117">**CCritSec Class**</span></span>](ccritsec.md)
</dt> </dl>

 

 




