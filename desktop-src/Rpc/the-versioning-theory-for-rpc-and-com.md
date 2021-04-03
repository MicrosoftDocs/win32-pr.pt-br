---
title: A teoria do controle de versão para RPC e COM
description: Teoria de controle de versão para RPC (chamada de procedimento remoto) e COM.
ms.assetid: c4df0a7b-e1be-481d-9149-317ffc9179b9
keywords:
- RPC de chamada de procedimento remoto, práticas recomendadas, controle de versão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e03b23c91bf69fbc3c4f72366b80812fd54330d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084782"
---
# <a name="the-versioning-theory-for-rpc-and-com"></a>A teoria do controle de versão para RPC e COM

Somente dois métodos totalmente infalívels dão suporte à nova funcionalidade sem risco de problemas de compatibilidade de conexão:

-   Alterar a versão da interface de acordo com as regras; Isso impede que novos clientes se comuniquem com um servidor antigo e pode ou não impeçam que um cliente antigo se comunique com o novo servidor. Isso é esclarecido mais adiante nesta seção.
-   Introduza uma interface diferente lidando com a nova funcionalidade.

Uma interface RPC padrão é identificada por uma combinação de GUID e número de versão; uma interface COM é identificada por seu GUID. A versão consiste em partes principais e secundárias. Para interfaces padrão com o mesmo GUID e números de versão diferentes, uma conexão só é possível quando a versão principal é a mesma, e o cliente não é maior que a versão secundária do servidor.

Uma consequência é que a alteração da GUID da interface RPC interrompe a compatibilidade de conexão, ao passo que a alteração do nome da interface não.

No RPC padrão, um caminho para atualizações e extensões é bem definido e basicamente requer que novos métodos sejam adicionados ao final da interface e os novos tipos sejam usados apenas nos novos métodos. Se essas adições forem necessárias, a versão secundária deverá ser aumentada. Qualquer outra alteração requer uma alteração na versão principal, pois o software do cliente e do servidor seria incompatível na conexão. Obedecer a essas regras garante que sempre que houver uma conexão entre um novo cliente e um servidor antigo, ou vice-versa, ambos os lados sejam totalmente compatíveis.

Para uma interface COM, o atributo Version não pode ser usado. A criação de novas interfaces e a herança das interfaces antigas é equivalente à manipulação da versão no RPC. Normalmente, a melhor abordagem em COM é criar uma nova interface para a funcionalidade expandida. Um equivalente da versão secundária é a nova interface herdada da antiga. A alteração de métodos antigos ou de tipos de dados antigos requer uma interface COM totalmente nova – uma interface que não herda da antiga.

Para COM, a função [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) é um método estabelecido para verificar se um servidor dá suporte a uma interface; Portanto, as situações em que um cliente pode se comunicar com uma versão antiga ou nova de uma interface podem ser facilmente resolvidas.

 

 