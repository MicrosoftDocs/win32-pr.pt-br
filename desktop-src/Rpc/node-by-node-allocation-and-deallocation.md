---
title: Alocação e desalocação de nó por nó
description: Alocação de nó por nó e desalocação de estruturas de dados pelos stubs é o método padrão de gerenciamento de memória para todos os parâmetros no cliente e no servidor.
ms.assetid: 04752fd9-438c-4b52-830b-ce136f83b3b8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52aea7c2e95615af8549c1f66476e1a105b91abd68dd31089db9cf23d8ec2af3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118927835"
---
# <a name="node-by-node-allocation-and-deallocation"></a>Alocação e desalocação de nó por nó

Alocação de nó por nó e desalocação de estruturas de dados pelos stubs é o método padrão de gerenciamento de memória para todos os parâmetros no cliente e no servidor. No lado do cliente, o stub aloca cada nó com uma chamada separada para [o \_ usuário médio \_ alocar](/windows/desktop/Midl/midl-user-allocate-1). No lado do servidor, em vez de chamar **o usuário médio \_ \_ alocar**, a memória privada é usada sempre que possível. Se **a \_ alocação de usuário \_ médio** for chamada, os stubs de servidor chamarão o usuário **midl \_ \_ gratuitamente** para liberar os dados. Na maioria dos casos, o uso da alocação e da desalocação nó a nó em vez de usar **\[ alocar (todos os \_ nós) \]** resultará em um maior desempenho dos stubs do lado do servidor.

 

 