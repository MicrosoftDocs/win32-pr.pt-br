---
title: A teoria do versioning para RPC e COM
description: Teoria de controle de versão para RPC (Chamada de Procedimento Remoto) e COM.
ms.assetid: c4df0a7b-e1be-481d-9149-317ffc9179b9
keywords:
- RPC de Chamada de Procedimento Remoto , práticas recomendadas, controle de versão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac3681ce1290b7653c28b12c09c93d21de3052e0e6137ed5c6f906afd42f8d07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120016376"
---
# <a name="the-versioning-theory-for-rpc-and-com"></a>A teoria do versioning para RPC e COM

Apenas dois métodos completamente à prova de falhas são compatíveis com novas funcionalidades sem risco de problemas de compatibilidade de transmissão:

-   Altere a versão da interface de acordo com as regras; Isso impede que novos clientes se comuniquem com um servidor antigo e podem ou não impedir que um cliente antigo se comunique com o novo servidor. Isso será esclarecida posteriormente nesta seção.
-   Introduza uma interface diferente que lida com a nova funcionalidade.

Uma interface RPC padrão é identificada por uma combinação de guid e número de versão; uma interface COM é identificada por seu GUID. A versão consiste em partes principais e secundárias. Para interfaces padrão com o mesmo GUID e números de versão diferentes, uma conexão só é possível quando a versão principal é a mesma e o cliente não é maior que a versão secundária do servidor.

Uma consequência é que alterar o GUID da interface RPC interrompe a compatibilidade do fio, enquanto alterar o nome da interface não interrompe.

No RPC padrão, um caminho para atualizações e extensões é bem definido e, basicamente, requer que novos métodos sejam adicionados somente no final da interface e novos tipos sejam usados somente nos novos métodos. Se essas adições são necessárias, a versão secundária deve ser aumentada. Qualquer outra alteração requer uma alteração na versão principal, porque o software cliente e servidor seria incompatível na transmissão. A aderindo a essas regras garante sempre que houver uma conexão entre um novo cliente e um servidor antigo ou vice-versa, ambos os lados são totalmente compatíveis.

Para uma interface COM, o atributo de versão não pode ser usado. Criar novas interfaces e herdar das interfaces antigas é um equivalente à manipulação da versão no RPC. Normalmente, a melhor abordagem em COM é criar uma nova interface para a funcionalidade expandida. Um equivalente à versão secundária é a nova interface herdada da antiga. Alterar métodos antigos ou tipos de dados antigos requer uma interface COM totalmente nova, uma interface que não herda da antiga.

Para COM, a [**função QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) é um método estabelecido para verificar se um servidor dá suporte a uma interface; portanto, as situações em que um cliente pode se falar com uma versão antiga ou nova de uma interface podem ser facilmente resolvidas.

 

 