---
description: Número de bloqueios pendentes neste objeto.
ms.assetid: 27506c1d-6a9a-4410-80fb-6d4f2fd2f824
title: 'Membro CCritSec:: m_lockCount (Wxutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_lockCount
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 88098a8ded025a899e2092a96308bd6c54750758
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105787413"
---
# <a name="ccritsecm_lockcount-member"></a><span data-ttu-id="a2acb-103">Membro de CCritSec:: m \_ lockCount</span><span class="sxs-lookup"><span data-stu-id="a2acb-103">CCritSec::m\_lockCount member</span></span>

<span data-ttu-id="a2acb-104">Número de bloqueios pendentes neste objeto.</span><span class="sxs-lookup"><span data-stu-id="a2acb-104">Number of outstanding locks on this object.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2acb-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a2acb-105">Syntax</span></span>


```C++
DWORD m_lockCount;
```



## <a name="remarks"></a><span data-ttu-id="a2acb-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="a2acb-106">Remarks</span></span>

<span data-ttu-id="a2acb-107">Essa variável de membro é definida somente na versão de depuração da classe base.</span><span class="sxs-lookup"><span data-stu-id="a2acb-107">This member variable is defined only in the debug version of the base class.</span></span> <span data-ttu-id="a2acb-108">A [seção crítica Depurando funções funções](critical-section-debugging-functions.md) usam esse membro.</span><span class="sxs-lookup"><span data-stu-id="a2acb-108">The [Critical Section Debugging Functions](critical-section-debugging-functions.md) functions use this member.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2acb-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a2acb-109">Requirements</span></span>



| <span data-ttu-id="a2acb-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2acb-110">Requirement</span></span> | <span data-ttu-id="a2acb-111">Valor</span><span class="sxs-lookup"><span data-stu-id="a2acb-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2acb-112">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a2acb-112">Header</span></span><br/>  | <dl> <span data-ttu-id="a2acb-113"><dt>Wxutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a2acb-113"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="a2acb-114">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a2acb-114">Library</span></span><br/> | <dl> <span data-ttu-id="a2acb-115"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="a2acb-115"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2acb-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="a2acb-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2acb-117">**Classe CCritSec**</span><span class="sxs-lookup"><span data-stu-id="a2acb-117">**CCritSec Class**</span></span>](ccritsec.md)
</dt> </dl>

 

 




