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
# <a name="why-proxy-objects-are-needed"></a>Por que os objetos proxy são necessários

Com objetos acessíveis, quando um cliente define uma [função de gancho no contexto](in-context-and-out-of-context-hook-functions.md), a dll na qual a função de gancho do cliente é implementada é carregada no espaço de endereço do servidor. Nesse caso, quando o cliente chama [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) de dentro da função Hook, o ponteiro de interface que é retornado aponta diretamente para o código no espaço de endereço do servidor. Quando o cliente chama uma propriedade de interface usando esse ponteiro, a biblioteca de Component Object Model (COM) não está envolvida no marshaling ou no desempacotamento e não pode detectar se um objeto é destruído. Portanto, o servidor deve detectar essa situação e retornar um código de erro para o cliente.

 

 




