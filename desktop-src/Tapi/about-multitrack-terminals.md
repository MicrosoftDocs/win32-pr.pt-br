---
description: Um terminal multitrack pode ser considerado como um terminal que é uma coleção de outros terminais. Cada terminal filho (um &\# 0034; track&\# 0034;) pode ser um terminal multitrack ou um terminal de controle único.
ms.assetid: bf23bc26-5763-45a3-a63d-e43ce2480956
title: Sobre terminais multitrack
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58042236c737f6ab0b933699d75e19358f6e6b81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105760688"
---
# <a name="about-multitrack-terminals"></a><span data-ttu-id="22f89-104">Sobre terminais multitrack</span><span class="sxs-lookup"><span data-stu-id="22f89-104">About Multitrack Terminals</span></span>

<span data-ttu-id="22f89-105">Um terminal multitrack pode ser considerado como um terminal que é uma coleção de outros terminais.</span><span class="sxs-lookup"><span data-stu-id="22f89-105">A multitrack terminal can be thought of as a terminal that is a collection of other terminals.</span></span> <span data-ttu-id="22f89-106">Cada terminal filho (uma "faixa") pode ser um terminal multitrack ou um terminal de controle único.</span><span class="sxs-lookup"><span data-stu-id="22f89-106">Each child terminal (a "track") can be a multitrack terminal or a single-track terminal.</span></span>

<span data-ttu-id="22f89-107">Todos os terminais multitrack expõem a interface [**ITMultiTrackTerminal**](/windows/desktop/api/tapi3if/nn-tapi3if-itmultitrackterminal) , que inclui métodos genéricos para enumerar, criar e remover terminais de faixa de um terminal multitrack.</span><span class="sxs-lookup"><span data-stu-id="22f89-107">All multitrack terminals expose the [**ITMultiTrackTerminal**](/windows/desktop/api/tapi3if/nn-tapi3if-itmultitrackterminal) interface, which includes generic methods for enumerating, creating, and removing track terminals from a multitrack terminal.</span></span> <span data-ttu-id="22f89-108">Todos os terminais, controle único e multitrack, expõem a interface [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) .</span><span class="sxs-lookup"><span data-stu-id="22f89-108">All terminals, single-track and multitrack, expose the [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) interface.</span></span>

<span data-ttu-id="22f89-109">Um cliente que tem um ponteiro para uma interface [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) pode descobrir se o terminal é multitrack ou de controle único consultando o terminal para a interface [**ITMultiTrackTerminal**](/windows/desktop/api/tapi3if/nn-tapi3if-itmultitrackterminal) , que é exposta apenas em terminais multitrack.</span><span class="sxs-lookup"><span data-stu-id="22f89-109">A client that has a pointer to an [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) interface can discover whether the terminal is multitrack or single-track by querying the terminal for the [**ITMultiTrackTerminal**](/windows/desktop/api/tapi3if/nn-tapi3if-itmultitrackterminal) interface, which is exposed only on multitrack terminals.</span></span>

<span data-ttu-id="22f89-110">O terminal pai pode usar a interface [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) de seus terminais de faixa ou pode exigir que os terminais de faixa exponham interfaces privadas.</span><span class="sxs-lookup"><span data-stu-id="22f89-110">The parent terminal may use the [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) interface of its track terminals, or it may require track terminals to expose private interfaces.</span></span>

<span data-ttu-id="22f89-111">Para obter mais informações, consulte [Track Terminals](track-terminals.md).</span><span class="sxs-lookup"><span data-stu-id="22f89-111">For more information, see [Track Terminals](track-terminals.md).</span></span>

 

 
