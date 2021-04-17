---
description: Ponteiro para uma seção crítica.
ms.assetid: 7d949b7f-a6a7-4ab5-b651-f85b70d55065
title: 'Membro CBaseMediaFilter:: m_pLock (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pLock
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 126aa213004dd032eea43b28198b6f8b49fe7f3e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752906"
---
# <a name="cbasemediafilterm_plock-member"></a><span data-ttu-id="67597-103">Membro de CBaseMediaFilter:: m \_ pLock</span><span class="sxs-lookup"><span data-stu-id="67597-103">CBaseMediaFilter::m\_pLock member</span></span>

<span data-ttu-id="67597-104">Ponteiro para uma seção crítica.</span><span class="sxs-lookup"><span data-stu-id="67597-104">Pointer to a critical section.</span></span>

## <a name="syntax"></a><span data-ttu-id="67597-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="67597-105">Syntax</span></span>


```C++
CCritSec *m_pLock;
```



## <a name="remarks"></a><span data-ttu-id="67597-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="67597-106">Remarks</span></span>

<span data-ttu-id="67597-107">A seção crítica é mantida durante as transições de estado ([**CBaseMediaFilter:: Run**](cbasemediafilter-run.md), [**CBaseMediaFilter::P ause**](cbasemediafilter-pause.md), [**CBaseMediaFilter:: Stop**](cbasemediafilter-stop.md)), ao acessar o relógio de referência ([**CBaseMediaFilter:: setsyncname**](cbasemediafilter-setsyncsource.md), [**CBaseMediaFilter:: getsyncname**](cbasemediafilter-getsyncsource.md)) e no método [**CBaseMediaFilter:: IsActive**](cbasemediafilter-isactive.md) .</span><span class="sxs-lookup"><span data-stu-id="67597-107">The critical section is held during state transitions ([**CBaseMediaFilter::Run**](cbasemediafilter-run.md), [**CBaseMediaFilter::Pause**](cbasemediafilter-pause.md), [**CBaseMediaFilter::Stop**](cbasemediafilter-stop.md)), when accessing the reference clock ([**CBaseMediaFilter::SetSyncSource**](cbasemediafilter-setsyncsource.md), [**CBaseMediaFilter::GetSyncSource**](cbasemediafilter-getsyncsource.md)), and in the [**CBaseMediaFilter::IsActive**](cbasemediafilter-isactive.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="67597-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="67597-108">Requirements</span></span>



| <span data-ttu-id="67597-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="67597-109">Requirement</span></span> | <span data-ttu-id="67597-110">Valor</span><span class="sxs-lookup"><span data-stu-id="67597-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67597-111">parâmetro</span><span class="sxs-lookup"><span data-stu-id="67597-111">Header</span></span><br/>  | <dl> <span data-ttu-id="67597-112"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="67597-112"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="67597-113">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="67597-113">Library</span></span><br/> | <dl> <span data-ttu-id="67597-114"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="67597-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67597-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="67597-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67597-116">**Classe CBaseMediaFilter**</span><span class="sxs-lookup"><span data-stu-id="67597-116">**CBaseMediaFilter Class**</span></span>](cbasemediafilter.md)
</dt> </dl>

 

 




