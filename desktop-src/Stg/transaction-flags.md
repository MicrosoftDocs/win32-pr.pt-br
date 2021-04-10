---
title: Sinalizadores de transação
description: Um objeto pode ser aberto no modo direto ou transacionado.
ms.assetid: f3be52b9-957c-4ab9-8fc1-e765faae2489
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 581d21db07921fe6d635aac44ceed256fee4ad85
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159982"
---
# <a name="transaction-flags"></a><span data-ttu-id="058f4-103">Sinalizadores de transação</span><span class="sxs-lookup"><span data-stu-id="058f4-103">Transaction Flags</span></span>

<span data-ttu-id="058f4-104">Um objeto pode ser aberto no modo direto ou transacionado.</span><span class="sxs-lookup"><span data-stu-id="058f4-104">An object can be opened in either direct or transacted mode.</span></span> <span data-ttu-id="058f4-105">Quando um objeto é aberto no modo direto, as alterações são feitas imediatamente e permanentemente.</span><span class="sxs-lookup"><span data-stu-id="058f4-105">When an object is opened in direct mode, changes are made immediately and permanently.</span></span> <span data-ttu-id="058f4-106">Quando um objeto é aberto no modo transacionado, as alterações são armazenadas em buffer para que possam ser explicitamente confirmadas ou revertidas quando a edição for concluída.</span><span class="sxs-lookup"><span data-stu-id="058f4-106">When an object is opened in transacted mode, changes are buffered so they can be explicitly committed or reverted once editing is complete.</span></span> <span data-ttu-id="058f4-107">As alterações confirmadas são salvas no objeto enquanto as alterações revertidas são descartadas.</span><span class="sxs-lookup"><span data-stu-id="058f4-107">Committed changes are saved to the object while reverted changes are discarded.</span></span> <span data-ttu-id="058f4-108">O modo direto é o modo de acesso padrão.</span><span class="sxs-lookup"><span data-stu-id="058f4-108">Direct mode is the default access mode.</span></span>

<span data-ttu-id="058f4-109">O modo transacionado não é necessário em um objeto de armazenamento pai para usá-lo em um elemento aninhado.</span><span class="sxs-lookup"><span data-stu-id="058f4-109">Transacted mode is not required on a parent storage object in order to use it on a nested element.</span></span> <span data-ttu-id="058f4-110">Uma transação para um elemento aninhado, no entanto, é aninhada dentro da transação para seu objeto de armazenamento pai.</span><span class="sxs-lookup"><span data-stu-id="058f4-110">A transaction for a nested element, however, is nested within the transaction for its parent storage object.</span></span> <span data-ttu-id="058f4-111">Portanto, as alterações feitas em um objeto filho não podem ser confirmadas até que as feitas no pai sejam confirmadas e ambas permaneçam não confirmadas até que o objeto de armazenamento raiz (o pai de nível superior) seja realmente gravado no disco.</span><span class="sxs-lookup"><span data-stu-id="058f4-111">Therefore, changes made to a child object cannot be committed until those made to the parent are committed, and both remain uncommitted until the root storage object (the top-level parent) is actually written to disk.</span></span> <span data-ttu-id="058f4-112">Em outras palavras, as alterações se movem para fora: os objetos internos publicam alterações nas transações de seus contêineres imediatos.</span><span class="sxs-lookup"><span data-stu-id="058f4-112">In other words, the changes move outward: inner objects publish changes to the transactions of their immediate containers.</span></span>

 

 




