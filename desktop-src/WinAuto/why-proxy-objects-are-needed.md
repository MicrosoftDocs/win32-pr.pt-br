---
title: Por que os objetos proxy são necessários
description: Com objetos acessíveis, quando um cliente define uma função de gancho no contexto, a DLL na qual a função de gancho do cliente é implementada é carregada no espaço de endereço do servidor.
ms.assetid: e8e93271-1da6-42cd-9200-23a3e08b490b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28d672f48e9c41f23599a8a64585062a126dafb8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292168"
---
# <a name="why-proxy-objects-are-needed"></a><span data-ttu-id="24fd6-103">Por que os objetos proxy são necessários</span><span class="sxs-lookup"><span data-stu-id="24fd6-103">Why Proxy Objects Are Needed</span></span>

<span data-ttu-id="24fd6-104">Com objetos acessíveis, quando um cliente define uma [função de gancho no contexto](in-context-and-out-of-context-hook-functions.md), a dll na qual a função de gancho do cliente é implementada é carregada no espaço de endereço do servidor.</span><span class="sxs-lookup"><span data-stu-id="24fd6-104">With accessible objects, when a client sets an [in-context hook function](in-context-and-out-of-context-hook-functions.md), the DLL in which the client's hook function is implemented is loaded into the server's address space.</span></span> <span data-ttu-id="24fd6-105">Nesse caso, quando o cliente chama [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) de dentro da função Hook, o ponteiro de interface que é retornado aponta diretamente para o código no espaço de endereço do servidor.</span><span class="sxs-lookup"><span data-stu-id="24fd6-105">In this case, when the client calls [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) from within the hook function, the interface pointer that is returned points directly to code in the server's address space.</span></span> <span data-ttu-id="24fd6-106">Quando o cliente chama uma propriedade de interface usando esse ponteiro, a biblioteca de Component Object Model (COM) não está envolvida no marshaling ou no desempacotamento e não pode detectar se um objeto é destruído.</span><span class="sxs-lookup"><span data-stu-id="24fd6-106">When the client calls an interface property using this pointer, the Component Object Model (COM) library is not involved with marshaling or unmarshaling and cannot detect if an object is destroyed.</span></span> <span data-ttu-id="24fd6-107">Portanto, o servidor deve detectar essa situação e retornar um código de erro para o cliente.</span><span class="sxs-lookup"><span data-stu-id="24fd6-107">Therefore, the server must detect this situation and return an error code to the client.</span></span>

 

 




