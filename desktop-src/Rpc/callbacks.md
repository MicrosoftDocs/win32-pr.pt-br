---
title: Retornos de chamada (RPC)
description: Geralmente, o modelo de programação exige um retorno de chamada de servidor para um cliente por meio de uma RPC (chamada de procedimento remoto) ou chamadas de cliente para um servidor não confiável. Isso introduz muitas armadilhas potenciais.
ms.assetid: a4f3ea26-ac4b-41e5-abde-96b4baedf2ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6260e2cff2cbaff86f210764e89d55859c4d33af
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104008773"
---
# <a name="callbacks-rpc"></a>Retornos de chamada (RPC)

Geralmente, o modelo de programação exige um retorno de chamada de servidor para um cliente por meio de uma RPC (chamada de procedimento remoto) ou chamadas de cliente para um servidor não confiável. Isso introduz muitas armadilhas potenciais.

Primeiro, o retorno de chamada para o cliente deve ser feito com um nível de representação suficientemente baixo. Se o servidor for um serviço de sistema altamente privilegiado, chamar novamente um cliente local com um nível de representação de IMPERSONATE ou superior pode fornecer ao cliente privilégios suficientes para assumir o sistema. Chamar novamente um cliente remoto com um nível de representação mais alto do que o necessário também pode levar a consequências indesejáveis.

Em segundo lugar, se um invasor induzir seu serviço a executar um retorno de chamada, ele poderá iniciar o que é chamado de *buraco negro*— ataque de negação de serviço. Tais ataques não são específicos do RPC; nesses ataques, um computador o induzi a enviar tráfego para ele, mas não responde às suas solicitações. Você coleta cada vez mais recursos para chamar o buraco negro, mas eles nunca retornam. Um exemplo genérico desse tipo de ataque é um ataque de nível de TCP chamado ataque de inundação SYN TCP/IP.

No nível de RPC, um ataque de buraco negro simples ocorre quando um invasor chama uma interface e solicita que o servidor chame a interface de volta. A interface está em conformidade, mas o invasor nunca retorna a chamada: um thread no servidor está ligado. O invasor faz isso 100 vezes, vinculando 100 threads no servidor. Eventualmente, o servidor fica sem memória. A depuração do servidor pode potencialmente revelar a identidade do chamador de buraco negro, mas, muitas vezes, o servidor será reiniciado sem suspeitar de fracasso Play, ou pode não haver conhecimento suficiente disponível para determinar o invasor.

A terceira armadilha está no cliente. Geralmente, um cliente faz uma chamada para o servidor informando ao servidor como chamá-lo de volta (geralmente uma associação de cadeia de caracteres) e aguarda uma chamada do servidor para chegar, aceitando indistinta qualquer chamada nesse ponto de extremidade que alega ser proveniente do servidor. O protocolo de retorno de chamada do servidor para o cliente deve incluir algum mecanismo de verificação para garantir que quando o retorno de chamada chega ao cliente, ele realmente se originou no servidor.

 

 




