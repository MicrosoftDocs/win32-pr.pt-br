---
title: Modos de acesso de armazenamento estruturado
description: Os mecanismos para controlar o acesso simultâneo a um objeto, por vários processos e usuários, são essenciais.
ms.assetid: 2d524c2b-f2b4-49f2-9be8-2037846eb9e9
keywords:
- Armazenamento estruturado Strctd STG, conceitos básicos, funções de API, sinalizadores de acesso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2e46a231cb5168d15564f0b86b064c8bfd19e38
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105755299"
---
# <a name="structured-storage-access-modes"></a><span data-ttu-id="8462d-104">Modos de acesso de armazenamento estruturado</span><span class="sxs-lookup"><span data-stu-id="8462d-104">Structured Storage Access Modes</span></span>

<span data-ttu-id="8462d-105">Os mecanismos para controlar o acesso simultâneo a um objeto, por vários processos e usuários, são essenciais.</span><span class="sxs-lookup"><span data-stu-id="8462d-105">Mechanisms for controlling simultaneous access to an object, by multiple processes and users, are essential.</span></span> <span data-ttu-id="8462d-106">O COM fornece esses mecanismos definindo modos de acesso para objetos de armazenamento e de fluxo.</span><span class="sxs-lookup"><span data-stu-id="8462d-106">COM provides these mechanisms by defining access modes for both storage and stream objects.</span></span> <span data-ttu-id="8462d-107">O modo de acesso especificado para um objeto de armazenamento pai é herdado por seus filhos, embora você possa inserir restrições adicionais no armazenamento ou fluxo filho.</span><span class="sxs-lookup"><span data-stu-id="8462d-107">The access mode specified for a parent storage object is inherited by its children, though you can place additional restrictions on the child storage or stream.</span></span> <span data-ttu-id="8462d-108">Um objeto de armazenamento ou fluxo aninhado pode ser aberto no mesmo modo ou em um modo mais restrito do que o de seu pai, mas não pode ser aberto em um modo menos restrito do que o de seu pai.</span><span class="sxs-lookup"><span data-stu-id="8462d-108">A nested storage or stream object can be opened in the same mode or in a more restricted mode than that of its parent, but it cannot be opened in a less restricted mode than that of its parent.</span></span>

<span data-ttu-id="8462d-109">Você especifica modos de acesso usando os valores listados em [**constantes STGM**](stgm-constants.md).</span><span class="sxs-lookup"><span data-stu-id="8462d-109">You specify access modes by using the values listed in [**STGM Constants**](stgm-constants.md).</span></span> <span data-ttu-id="8462d-110">Esses valores servem como sinalizadores a serem passados como argumentos para métodos na interface [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) e funções de API associadas.</span><span class="sxs-lookup"><span data-stu-id="8462d-110">These values serve as flags to be passed as arguments to methods in the [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) interface and associated API functions.</span></span> <span data-ttu-id="8462d-111">Normalmente, vários sinalizadores são combinados no parâmetro *grfMode*, usando um booliano **ou** uma operação.</span><span class="sxs-lookup"><span data-stu-id="8462d-111">Typically, several flags are combined in the parameter *grfMode*, using a Boolean **OR** operation.</span></span>

<span data-ttu-id="8462d-112">Os sinalizadores se enquadram em seis grupos.</span><span class="sxs-lookup"><span data-stu-id="8462d-112">The flags fall into six groups.</span></span> <span data-ttu-id="8462d-113">Somente um sinalizador de cada grupo pode ser especificado por vez:</span><span class="sxs-lookup"><span data-stu-id="8462d-113">Only one flag from each group can be specified at a time:</span></span>

-   [<span data-ttu-id="8462d-114">Sinalizadores de transação</span><span class="sxs-lookup"><span data-stu-id="8462d-114">Transaction Flags</span></span>](transaction-flags.md)
-   [<span data-ttu-id="8462d-115">Sinalizadores de criação de armazenamento</span><span class="sxs-lookup"><span data-stu-id="8462d-115">Storage Creation Flags</span></span>](storage-creation-flags.md)
-   [<span data-ttu-id="8462d-116">Sinalizadores de criação temporários</span><span class="sxs-lookup"><span data-stu-id="8462d-116">Temporary Creation Flags</span></span>](temporary-creation-flags.md)
-   [<span data-ttu-id="8462d-117">Sinalizadores de prioridade</span><span class="sxs-lookup"><span data-stu-id="8462d-117">Priority Flags</span></span>](priority-flags.md)
-   [<span data-ttu-id="8462d-118">Sinalizadores de permissão de acesso</span><span class="sxs-lookup"><span data-stu-id="8462d-118">Access Permission Flags</span></span>](access-permission-flags.md)
-   [<span data-ttu-id="8462d-119">Sinalizadores de acesso compartilhado</span><span class="sxs-lookup"><span data-stu-id="8462d-119">Shared Access Flags</span></span>](shared-access-flags.md)

 

 




