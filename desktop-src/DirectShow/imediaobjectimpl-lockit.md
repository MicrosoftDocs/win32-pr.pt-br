---
description: A classe LockIt é uma classe interna que bloqueia e desbloqueia o DMO.
ms.assetid: f516ce22-17ad-488e-a768-3f3849c56087
title: 'Classe IMediaObjectImpl:: LockIt (Dmoimpl. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24fe896ea293ec5e60b038f908cab794274d26e7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810219"
---
# <a name="imediaobjectimpllockit-class"></a><span data-ttu-id="77944-103">Classe IMediaObjectImpl:: LockIt</span><span class="sxs-lookup"><span data-stu-id="77944-103">IMediaObjectImpl::LockIt Class</span></span>

<span data-ttu-id="77944-104">A `LockIt` classe é uma classe interna que bloqueia e desbloqueia o DMO.</span><span class="sxs-lookup"><span data-stu-id="77944-104">The `LockIt` class is an internal class that locks and unlocks the DMO.</span></span>

``` syntax
LockIt(
    _DERIVED_ *p
);
```

## <a name="parameters"></a><span data-ttu-id="77944-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="77944-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77944-106"><span id="p"></span><span id="P"></span>*DTI*</span><span class="sxs-lookup"><span data-stu-id="77944-106"><span id="p"></span><span id="P"></span>*p*</span></span>
</dt> <dd>

<span data-ttu-id="77944-107">Ponteiro para o objeto derivado.</span><span class="sxs-lookup"><span data-stu-id="77944-107">Pointer to the derived object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="77944-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="77944-108">Remarks</span></span>

<span data-ttu-id="77944-109">O `LockIt` Construtor bloqueia o DMO e o destruidor desbloqueia o DMO.</span><span class="sxs-lookup"><span data-stu-id="77944-109">The `LockIt` constructor locks the DMO, and the destructor unlocks the DMO.</span></span> <span data-ttu-id="77944-110">Para bloquear o objeto de dentro de sua classe derivada, declare uma variável local do tipo `LockIt` .</span><span class="sxs-lookup"><span data-stu-id="77944-110">To lock the object from inside your derived class, declare a local variable of type `LockIt`.</span></span> <span data-ttu-id="77944-111">O DMO é bloqueado enquanto o `LockIt` objeto permanece no escopo:</span><span class="sxs-lookup"><span data-stu-id="77944-111">The DMO is locked while the `LockIt` object remains in scope:</span></span>


```C++
void SomeMethod()
{
    // The DMO is not locked.
    {
        LockIt dmoLock(this); // Locks the DMO.
        /* ... */
    } 
    // dmoLock goes out of scope, DMO is unlocked.
}
```



<span data-ttu-id="77944-112">Os métodos no **IMediaObjectImpl** bloqueiam automaticamente o DMO.</span><span class="sxs-lookup"><span data-stu-id="77944-112">The methods in **IMediaObjectImpl** automatically lock the DMO.</span></span>

## <a name="requirements"></a><span data-ttu-id="77944-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="77944-113">Requirements</span></span>



| <span data-ttu-id="77944-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="77944-114">Requirement</span></span> | <span data-ttu-id="77944-115">Valor</span><span class="sxs-lookup"><span data-stu-id="77944-115">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77944-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="77944-116">Header</span></span><br/>  | <dl> <span data-ttu-id="77944-117"><dt>Dmoimpl. h</dt></span><span class="sxs-lookup"><span data-stu-id="77944-117"><dt>Dmoimpl.h</dt></span></span> </dl>                                                                     |
| <span data-ttu-id="77944-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="77944-118">Library</span></span><br/> | <dl> <span data-ttu-id="77944-119"><dt>Dmoguids. lib; </dt> <dt>Msdmo. lib</dt></span><span class="sxs-lookup"><span data-stu-id="77944-119"><dt>Dmoguids.lib; </dt> <dt>Msdmo.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77944-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="77944-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77944-121">**Modelo de classe IMediaObjectImpl**</span><span class="sxs-lookup"><span data-stu-id="77944-121">**IMediaObjectImpl Class Template**</span></span>](imediaobjectimpl-class-template.md)
</dt> </dl>

 

 




