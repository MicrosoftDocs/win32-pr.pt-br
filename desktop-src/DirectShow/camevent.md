---
description: A classe CAMEvent é um wrapper para eventos de redefinição manual e redefinição automática.
ms.assetid: 228b4e51-afc5-4cb6-b225-309013713983
title: Classe CAMEvent (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bde2db8adf2bb713df665e06eb2cc5f8d2a9a00f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750715"
---
# <a name="camevent-class"></a><span data-ttu-id="a7ba9-103">Classe CAMEvent</span><span class="sxs-lookup"><span data-stu-id="a7ba9-103">CAMEvent class</span></span>

![hierarquia de classe CAMEvent](images/util06.png)

<span data-ttu-id="a7ba9-105">A classe **CAMEvent** é um wrapper para eventos de redefinição manual e redefinição automática.</span><span class="sxs-lookup"><span data-stu-id="a7ba9-105">The **CAMEvent** class is a wrapper for manual-reset and auto-reset events.</span></span>

<span data-ttu-id="a7ba9-106">Essa classe fornece uma maneira conveniente de gerenciar eventos, em vez de chamar funções como, por exemplo, [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa), [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject)e [**ResetEvent**](/windows/desktop/api/synchapi/nf-synchapi-resetevent).</span><span class="sxs-lookup"><span data-stu-id="a7ba9-106">This class provides a convenient way to manage events, rather than calling functions such as [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa), [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject), and [**ResetEvent**](/windows/desktop/api/synchapi/nf-synchapi-resetevent).</span></span>



| <span data-ttu-id="a7ba9-107">Variáveis de membro protegido</span><span class="sxs-lookup"><span data-stu-id="a7ba9-107">Protected Member Variables</span></span>                          | <span data-ttu-id="a7ba9-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="a7ba9-108">Description</span></span>                                                     |
|-----------------------------------------------------|-----------------------------------------------------------------|
| [<span data-ttu-id="a7ba9-109">**\_hEvent m**</span><span class="sxs-lookup"><span data-stu-id="a7ba9-109">**m\_hEvent**</span></span>](camevent-m-hevent.md)              | <span data-ttu-id="a7ba9-110">Identificador de evento.</span><span class="sxs-lookup"><span data-stu-id="a7ba9-110">Event handle.</span></span>                                                   |
| <span data-ttu-id="a7ba9-111">Métodos públicos</span><span class="sxs-lookup"><span data-stu-id="a7ba9-111">Public Methods</span></span>                                      | <span data-ttu-id="a7ba9-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="a7ba9-112">Description</span></span>                                                     |
| [<span data-ttu-id="a7ba9-113">**CAMEvent**</span><span class="sxs-lookup"><span data-stu-id="a7ba9-113">**CAMEvent**</span></span>](camevent-camevent.md)               | <span data-ttu-id="a7ba9-114">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="a7ba9-114">Constructor method.</span></span>                                             |
| [<span data-ttu-id="a7ba9-115">**~ CAMEvent**</span><span class="sxs-lookup"><span data-stu-id="a7ba9-115">**~CAMEvent**</span></span>](camevent--camevent.md)             | <span data-ttu-id="a7ba9-116">Método destruidor.</span><span class="sxs-lookup"><span data-stu-id="a7ba9-116">Destructor method.</span></span>                                              |
| [<span data-ttu-id="a7ba9-117">**Verificação**</span><span class="sxs-lookup"><span data-stu-id="a7ba9-117">**Check**</span></span>](camevent-check.md)                     | <span data-ttu-id="a7ba9-118">Verifica se o evento está definido, sem bloqueio.</span><span class="sxs-lookup"><span data-stu-id="a7ba9-118">Checks whether the event is set, without blocking.</span></span>              |
| [<span data-ttu-id="a7ba9-119">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="a7ba9-119">**Reset**</span></span>](camevent-reset.md)                     | <span data-ttu-id="a7ba9-120">Define o estado do evento como não sinalizado.</span><span class="sxs-lookup"><span data-stu-id="a7ba9-120">Sets the state of the event to nonsignaled.</span></span>                     |
| [<span data-ttu-id="a7ba9-121">**Definir**</span><span class="sxs-lookup"><span data-stu-id="a7ba9-121">**Set**</span></span>](camevent-set.md)                         | <span data-ttu-id="a7ba9-122">Sinaliza o evento.</span><span class="sxs-lookup"><span data-stu-id="a7ba9-122">Signals the event.</span></span>                                              |
| [<span data-ttu-id="a7ba9-123">**Aguarde**</span><span class="sxs-lookup"><span data-stu-id="a7ba9-123">**Wait**</span></span>](camevent-wait.md)                       | <span data-ttu-id="a7ba9-124">Bloqueia até que o evento seja sinalizado ou até que ocorra um tempo limite.</span><span class="sxs-lookup"><span data-stu-id="a7ba9-124">Blocks until the event is signaled, or until a time-out occurs.</span></span> |
| <span data-ttu-id="a7ba9-125">Operadores</span><span class="sxs-lookup"><span data-stu-id="a7ba9-125">Operators</span></span>                                           | <span data-ttu-id="a7ba9-126">Descrição</span><span class="sxs-lookup"><span data-stu-id="a7ba9-126">Description</span></span>                                                     |
| [<span data-ttu-id="a7ba9-127">**IDENTIFICADOR do operador**</span><span class="sxs-lookup"><span data-stu-id="a7ba9-127">**operator HANDLE**</span></span>](camevent-operator-handle.md) | <span data-ttu-id="a7ba9-128">Recupera o identificador de evento.</span><span class="sxs-lookup"><span data-stu-id="a7ba9-128">Retrieves the event handle.</span></span>                                     |



 

## <a name="requirements"></a><span data-ttu-id="a7ba9-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a7ba9-129">Requirements</span></span>



| <span data-ttu-id="a7ba9-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="a7ba9-130">Requirement</span></span> | <span data-ttu-id="a7ba9-131">Valor</span><span class="sxs-lookup"><span data-stu-id="a7ba9-131">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7ba9-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a7ba9-132">Header</span></span><br/>  | <dl> <span data-ttu-id="a7ba9-133"><dt>Wxutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a7ba9-133"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="a7ba9-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a7ba9-134">Library</span></span><br/> | <dl> <span data-ttu-id="a7ba9-135"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="a7ba9-135"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

