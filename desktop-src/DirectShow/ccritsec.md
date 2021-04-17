---
description: A classe CCritSec fornece um bloqueio de thread.
ms.assetid: ecc60afe-15d0-4780-8133-1dfc558c6325
title: Classe CCritSec (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCritSec
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8db0243ecfecd47655f547d40390e602c04d5b88
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757327"
---
# <a name="ccritsec-class"></a><span data-ttu-id="f3545-103">Classe CCritSec</span><span class="sxs-lookup"><span data-stu-id="f3545-103">CCritSec class</span></span>

<span data-ttu-id="f3545-104">A classe **CCritSec** fornece um bloqueio de thread.</span><span class="sxs-lookup"><span data-stu-id="f3545-104">The **CCritSec** class provides a thread lock.</span></span>

<span data-ttu-id="f3545-105">Essa classe é um wrapper fino para um objeto **de \_ seção crítica** do Windows.</span><span class="sxs-lookup"><span data-stu-id="f3545-105">This class is a thin wrapper for a Windows **CRITICAL\_SECTION** object.</span></span> <span data-ttu-id="f3545-106">Você pode bloquear e desbloquear o thread chamando os métodos [**CCritSec:: Lock**](ccritsec-lock.md) e [**CCritSec:: Unlock**](ccritsec-unlock.md) .</span><span class="sxs-lookup"><span data-stu-id="f3545-106">You can lock and unlock the thread by calling the [**CCritSec::Lock**](ccritsec-lock.md) and [**CCritSec::Unlock**](ccritsec-unlock.md) methods.</span></span> <span data-ttu-id="f3545-107">No entanto, é mais seguro usar essa classe em conjunto com a classe [**CAutoLock**](cautolock.md) .</span><span class="sxs-lookup"><span data-stu-id="f3545-107">However, it is safer to use this class in conjunction with the [**CAutoLock**](cautolock.md) class.</span></span> <span data-ttu-id="f3545-108">Quando a classe **CAutoLock** sai do escopo, ela automaticamente desbloqueia o objeto **CCritSec** .</span><span class="sxs-lookup"><span data-stu-id="f3545-108">When the **CAutoLock** class goes out of scope, it automatically unlocks the **CCritSec** object.</span></span> <span data-ttu-id="f3545-109">Além disso, ele é compilado para um código embutido eficiente.</span><span class="sxs-lookup"><span data-stu-id="f3545-109">Moreover, it compiles to efficient inline code.</span></span>



| <span data-ttu-id="f3545-110">Variáveis de membro público</span><span class="sxs-lookup"><span data-stu-id="f3545-110">Public Member Variables</span></span>                            | <span data-ttu-id="f3545-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="f3545-111">Description</span></span>                                              |
|----------------------------------------------------|----------------------------------------------------------|
| [<span data-ttu-id="f3545-112">**\_currentOwner m**</span><span class="sxs-lookup"><span data-stu-id="f3545-112">**m\_currentOwner**</span></span>](ccritsec-m-currentowner.md) | <span data-ttu-id="f3545-113">Identificador de thread do thread proprietário.</span><span class="sxs-lookup"><span data-stu-id="f3545-113">Thread identifier of the owning thread.</span></span>                  |
| [<span data-ttu-id="f3545-114">**\_lockCount m**</span><span class="sxs-lookup"><span data-stu-id="f3545-114">**m\_lockCount**</span></span>](ccritsec-m-lockcount.md)       | <span data-ttu-id="f3545-115">Número de bloqueios pendentes neste objeto.</span><span class="sxs-lookup"><span data-stu-id="f3545-115">Number of outstanding locks on this object.</span></span>              |
| [<span data-ttu-id="f3545-116">**\_fTrace m**</span><span class="sxs-lookup"><span data-stu-id="f3545-116">**m\_fTrace**</span></span>](ccritsec-m-ftrace.md)             | <span data-ttu-id="f3545-117">Valor booliano que especifica se o bloqueio deve ser rastreado.</span><span class="sxs-lookup"><span data-stu-id="f3545-117">Boolean value that specifies whether to trace this lock.</span></span> |
| <span data-ttu-id="f3545-118">Métodos públicos</span><span class="sxs-lookup"><span data-stu-id="f3545-118">Public Methods</span></span>                                     | <span data-ttu-id="f3545-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="f3545-119">Description</span></span>                                              |
| [<span data-ttu-id="f3545-120">**CCritSec**</span><span class="sxs-lookup"><span data-stu-id="f3545-120">**CCritSec**</span></span>](ccritsec-ccritsec.md)              | <span data-ttu-id="f3545-121">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="f3545-121">Constructor method.</span></span>                                      |
| [<span data-ttu-id="f3545-122">**~ CCritSec**</span><span class="sxs-lookup"><span data-stu-id="f3545-122">**~CCritSec**</span></span>](ccritsec--ccritsec.md)            | <span data-ttu-id="f3545-123">Método destruidor.</span><span class="sxs-lookup"><span data-stu-id="f3545-123">Destructor method.</span></span>                                       |
| [<span data-ttu-id="f3545-124">**Bloquear**</span><span class="sxs-lookup"><span data-stu-id="f3545-124">**Lock**</span></span>](ccritsec-lock.md)                      | <span data-ttu-id="f3545-125">Bloqueia o objeto de seção crítica.</span><span class="sxs-lookup"><span data-stu-id="f3545-125">Locks the critical section object.</span></span>                       |
| [<span data-ttu-id="f3545-126">**Unlock**</span><span class="sxs-lookup"><span data-stu-id="f3545-126">**Unlock**</span></span>](ccritsec-unlock.md)                  | <span data-ttu-id="f3545-127">Desbloqueia o objeto da seção crítica.</span><span class="sxs-lookup"><span data-stu-id="f3545-127">Unlocks the critical section object.</span></span>                     |



 

## <a name="requirements"></a><span data-ttu-id="f3545-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f3545-128">Requirements</span></span>



| <span data-ttu-id="f3545-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3545-129">Requirement</span></span> | <span data-ttu-id="f3545-130">Valor</span><span class="sxs-lookup"><span data-stu-id="f3545-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3545-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f3545-131">Header</span></span><br/>  | <dl> <span data-ttu-id="f3545-132"><dt>Wxutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f3545-132"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="f3545-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f3545-133">Library</span></span><br/> | <dl> <span data-ttu-id="f3545-134"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="f3545-134"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3545-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="f3545-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3545-136">Objetos de seção crítica</span><span class="sxs-lookup"><span data-stu-id="f3545-136">Critical Section Objects</span></span>](/windows/desktop/Sync/critical-section-objects)
</dt> <dt>

[<span data-ttu-id="f3545-137">Referência de classe base do DirectShow</span><span class="sxs-lookup"><span data-stu-id="f3545-137">DirectShow Base Class Reference</span></span>](base-class-reference.md)
</dt> </dl>

 

