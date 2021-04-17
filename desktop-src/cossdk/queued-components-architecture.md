---
description: O serviço de componentes em fila do COM+ aprimora o modelo de programação COM, fornecendo um ambiente no qual um componente pode ser invocado de forma síncrona (em tempo real) ou assincronamente (na fila).
ms.assetid: fd455679-b2b3-487f-8494-9ea296ce2c89
title: Arquitetura de componentes na fila
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8a2f6e1012bd3c11a27a44214ee28e84d5bd404
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/05/2021
ms.locfileid: "104569987"
---
# <a name="queued-components-architecture"></a>Arquitetura de componentes na fila

O serviço de componentes em fila do COM+ aprimora o modelo de programação COM, fornecendo um ambiente no qual um componente pode ser invocado de forma síncrona (em tempo real) ou assincronamente (na fila). Um componente não precisa estar ciente se ele é empregado em um contexto em tempo real ou em fila.

Os aplicativos de mensagens são como transações de email entre programas. O solicitante envia uma mensagem para o servidor; Quando o servidor chega a ele, a mensagem é processada. Como o email, um sistema de mensagens deve lidar com os detalhes da rede e garantir que a mensagem se mova do cliente para o servidor. Na estrutura de componentes em fila, o enfileiramento de mensagens é responsável por isso.

O serviço de componentes em fila COM+ consiste nas seguintes partes:

-   Gravador (para o cliente ou para o lado de envio)
-   Ouvinte (para o servidor ou lado de recebimento)
-   Player (para o servidor ou lado de recebimento)

![Diagrama que mostra o caminho do cliente para o servidor: cliente, gravador, fila, ouvinte, Player, servidor.](images/d732774b-1ca6-45ad-bce0-a95b0bfc3edb.png)

## <a name="the-recorder"></a>O gravador

Em um cenário típico de componentes enfileirados, o cliente chama um componente enfileirado. A chamada é feita ao gravador de componentes em fila, que o empacota como parte de uma mensagem para o servidor e o coloca em uma fila. O gravador realiza marshaling do contexto de segurança do cliente na mensagem e registra todas as chamadas de método do cliente. Em sua função como proxy para o componente de servidor, o gravador seleciona interfaces das interfaces queuable no catálogo COM+.

Uma representação da gravação é enviada ao serviço de enfileiramento de mensagens como uma mensagem a ser enviada a um servidor. Quando o componente em fila tiver a configuração de atributo de transação necessária ou com suporte, o enfileiramento de mensagens aceitará a entrega da mensagem somente se a transação do lado do cliente for confirmada e a fila de enfileiramento de mensagens for transacional, que é o padrão normalmente estabelecido. Quando a configuração do atributo de transação é necessária, o serviço de enfileiramento de mensagens pode aceitar a mensagem mesmo que a transação do lado do cliente seja anulada. Para obter mais informações sobre transações, consulte [enfileiramento de mensagens transacionais](transactional-message-queuing.md).

## <a name="the-listener"></a>O ouvinte

O ouvinte de componentes na fila recupera a mensagem da fila e a transmite para o player de componentes na fila.

## <a name="the-player"></a>O Player

O Player desempacota o contexto de segurança do cliente no lado do servidor e, em seguida, invoca o componente do servidor e faz as mesmas chamadas de método. As chamadas de método não são reproduzidas pelo Player até que o componente cliente seja concluído e a transação que registrou o método chame confirmações.

## <a name="the-message-mover"></a>O movimentador de mensagens

O movimentador de mensagens de componentes em fila é um utilitário que move todas as mensagens de enfileiramento de mensagens com falha de uma fila para outra para que elas possam ser repetidas. O utilitário de movimentação de mensagens é um objeto de automação que pode ser invocado com um VBScript; para obter mais informações, consulte [Manipulando erros](handling-errors-in-queued-components.md).

 

 



