---
description: A classe CAutoLock mantém uma seção crítica para o escopo de um bloco de código.
ms.assetid: 8013b3a7-297b-4cf8-8107-4cee1fc12b56
title: Classe CAutoLock (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAutoLock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 866ca7164fdaef5a93679da000779c51fb4ddb24
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750714"
---
# <a name="cautolock-class"></a><span data-ttu-id="3b41c-103">Classe CAutoLock</span><span class="sxs-lookup"><span data-stu-id="3b41c-103">CAutoLock class</span></span>

<span data-ttu-id="3b41c-104">A `CAutoLock` classe mantém uma seção crítica para o escopo de um bloco de código.</span><span class="sxs-lookup"><span data-stu-id="3b41c-104">The `CAutoLock` class holds a critical section for the scope of a code block.</span></span>

<span data-ttu-id="3b41c-105">Essa classe funciona em conjunto com a classe [**CCritSec**](ccritsec.md) , que é um wrapper para objetos de seção críticos.</span><span class="sxs-lookup"><span data-stu-id="3b41c-105">This class works in conjunction with the [**CCritSec**](ccritsec.md) class, which is a wrapper for critical section objects.</span></span> <span data-ttu-id="3b41c-106">O `CAutoLock` Construtor bloqueia a seção crítica e o destruidor a desbloqueia.</span><span class="sxs-lookup"><span data-stu-id="3b41c-106">The `CAutoLock` constructor locks the critical section, and the destructor unlocks it.</span></span> <span data-ttu-id="3b41c-107">Usando um `CAutoLock` objeto como uma variável local, você pode bloquear uma seção crítica com a garantia de que todos os caminhos de código desbloquearão a seção crítica.</span><span class="sxs-lookup"><span data-stu-id="3b41c-107">By using a `CAutoLock` object as a local variable, you can lock a critical section with the guarantee that all code paths will unlock the critical section.</span></span>

<span data-ttu-id="3b41c-108">O exemplo de código a seguir mostra como usar essa classe:</span><span class="sxs-lookup"><span data-stu-id="3b41c-108">The following code example shows how to use this class:</span></span>


```
CCritSec csMyLock;  // Critical section is not locked yet.
{
    CAutoLock cObjectLock(&csMyLock);  // Lock the critical section.

    // Protected section of code.     

} // Lock goes out of scope here.

```



<span data-ttu-id="3b41c-109">Os métodos nesta classe não foram projetados para serem substituídos.</span><span class="sxs-lookup"><span data-stu-id="3b41c-109">The methods in this class are not designed to be overridden.</span></span>



| <span data-ttu-id="3b41c-110">Variáveis de membro protegido</span><span class="sxs-lookup"><span data-stu-id="3b41c-110">Protected Member Variables</span></span>                 | <span data-ttu-id="3b41c-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="3b41c-111">Description</span></span>                                                      |
|--------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="3b41c-112">**\_pLock m**</span><span class="sxs-lookup"><span data-stu-id="3b41c-112">**m\_pLock**</span></span>](cautolock-m-plock.md)      | <span data-ttu-id="3b41c-113">Seção crítica para este bloqueio.</span><span class="sxs-lookup"><span data-stu-id="3b41c-113">Critical section for this lock.</span></span>                                  |
| <span data-ttu-id="3b41c-114">Métodos públicos</span><span class="sxs-lookup"><span data-stu-id="3b41c-114">Public Methods</span></span>                             | <span data-ttu-id="3b41c-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="3b41c-115">Description</span></span>                                                      |
| [<span data-ttu-id="3b41c-116">**CAutoLock**</span><span class="sxs-lookup"><span data-stu-id="3b41c-116">**CAutoLock**</span></span>](cautolock-cautolock.md)   | <span data-ttu-id="3b41c-117">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="3b41c-117">Constructor method.</span></span> <span data-ttu-id="3b41c-118">Bloqueia o objeto de seção crítica especificado.</span><span class="sxs-lookup"><span data-stu-id="3b41c-118">Locks the specified critical section object.</span></span> |
| [<span data-ttu-id="3b41c-119">**~ CAutoLock**</span><span class="sxs-lookup"><span data-stu-id="3b41c-119">**~CAutoLock**</span></span>](cautolock--cautolock.md) | <span data-ttu-id="3b41c-120">Método destruidor.</span><span class="sxs-lookup"><span data-stu-id="3b41c-120">Destructor method.</span></span> <span data-ttu-id="3b41c-121">Desbloqueia o objeto da seção crítica.</span><span class="sxs-lookup"><span data-stu-id="3b41c-121">Unlocks the critical section object.</span></span>          |



 

## <a name="requirements"></a><span data-ttu-id="3b41c-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b41c-122">Requirements</span></span>



| <span data-ttu-id="3b41c-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b41c-123">Requirement</span></span> | <span data-ttu-id="3b41c-124">Valor</span><span class="sxs-lookup"><span data-stu-id="3b41c-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b41c-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3b41c-125">Header</span></span><br/>  | <dl> <span data-ttu-id="3b41c-126"><dt>Wxutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3b41c-126"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="3b41c-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3b41c-127">Library</span></span><br/> | <dl> <span data-ttu-id="3b41c-128"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="3b41c-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




