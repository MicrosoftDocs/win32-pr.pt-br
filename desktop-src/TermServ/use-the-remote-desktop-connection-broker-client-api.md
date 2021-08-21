---
title: Como usar a API de cliente do agente de Conexão de Área de Trabalho Remota
description: A API de cliente do agente de Conexão de Área de Trabalho Remota permite que fornecedores de protocolo de terceiros aproveitem o agente de conexão para agilizar a manipulação de conexões que usam seu protocolo para se conectar a máquinas virtuais ou servidores de Área de Trabalho Remota em um farm.
ms.assetid: 05C2D6CA-C9C5-4783-B196-6A02918046EF
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c7230a51915d0416a5c52ad8ce8fee2985f768b4466a8bcd28834744084c0a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118850884"
---
# <a name="how-to-use-the-remote-desktop-connection-broker-client-api"></a>Como usar a API de cliente do agente de Conexão de Área de Trabalho Remota

A API de cliente do agente de Conexão de Área de Trabalho Remota permite que fornecedores de protocolo de terceiros aproveitem o agente de conexão para agilizar a manipulação de conexões que usam seu protocolo para se conectar a máquinas virtuais ou servidores de Área de Trabalho Remota em um farm.

## <a name="instructions"></a>Instruções

### <a name="step-1-obtain-the-iconnectionbrokerclient-interface"></a>Etapa 1: obter a interface IConnectionBrokerClient

Quando seu aplicativo ou provedor de protocolo for inicializado, execute as etapas a seguir.

1.  Chame a função [**CBCreateClientInstance**](cbcreateclientinstance.md) para obter a interface [**IConnectionBrokerClient**](iconnectionbrokerclient.md) .
2.  Mantenha a interface [**IConnectionBrokerClient**](iconnectionbrokerclient.md) contanto que você precise dela.
3.  Quando a interface [**IConnectionBrokerClient**](iconnectionbrokerclient.md) não for mais necessária, chame o método [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) .

### <a name="step-2-request-the-target-information"></a>Etapa 2: solicitar as informações de destino

Quando o provedor de protocolo receber uma solicitação de conexão de entrada, execute as seguintes etapas para chamar o método [**IConnectionBrokerClient:: GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md) . Esse método obtém, do agente de conexão, o servidor apropriado para redirecionar a conexão.

1.  Crie um evento que possa ser sinalizado usando a função [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa), ou semelhante, a ser usada para o parâmetro *hStatusEvent* .
2.  Aloque memória para os parâmetros *pTargetInfo* e *pResult* . Esses blocos de memória devem permanecer no local até que toda a sequência seja concluída.
3.  Preencha uma estrutura [**de \_ \_ informações de conexão CB**](cb-connection-info.md) que contenha todas as informações sobre a conexão de entrada.
4.  Chame o método [**GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md) , passando todos os parâmetros necessários. Esse é um método assíncrono que retornará uma instância da interface [**IConnectionBrokerRequest**](iconnectionbrokerrequest.md) .
5.  Aguarde até que o evento *hStatusEvent* se torne definido.
6.  Sempre que o evento *hStatusEvent* for definido, chame o método [**IConnectionBrokerRequest:: CheckStatus**](iconnectionbrokerrequest-checkstatus.md) para determinar o status da solicitação.
7.  Quando [**CheckStatus**](iconnectionbrokerrequest-checkstatus.md) retornar **a \_ solicitação de status CB \_ \_ concluída**, os parâmetros *pTargetInfo* e *pResult* conterá suas informações. Você pode interromper o loop de espera porque o parâmetro *hStatusEvent* não será mais usado.
8.  Use as informações na estrutura [**de \_ \_ informações de destino CB**](cb-target-info.md) representada pelo parâmetro *pTargetInfo* para determinar para onde redirecionar a conexão de entrada.
9.  Libere a interface [**IConnectionBrokerRequest**](iconnectionbrokerrequest.md) .
10. Feche o identificador de evento *hStatusEvent* ou você pode reutilizá-lo para solicitações de conexão subsequentes.

 

 