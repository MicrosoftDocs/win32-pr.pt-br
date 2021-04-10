---
title: Propriedades da mensagem e da fila de mensagens
description: Uma mensagem tem propriedades, que especificam um rótulo, um corpo de mensagem e várias opções.
ms.assetid: d0c9126e-a2c6-4d70-b87a-154a570899fc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0139a588b52f1de1de43d8ec50aebdaf57b995ea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292427"
---
# <a name="message-and-message-queue-properties"></a>Propriedades da mensagem e da fila de mensagens

Uma mensagem tem propriedades, que especificam um rótulo, um corpo de mensagem e várias opções. As opções de propriedade de mensagem podem incluir qualidade de serviço, prioridade, registro no diário, privacidade e níveis de autenticação e o tempo de vida da mensagem. Em aplicativos convencionais de enfileiramento de mensagens (não RPC), você especifica essas propriedades chamando as funções da API MSMQ ou os métodos de objeto COM, que são descritos na documentação do SDK do MSMQ. Os aplicativos cliente RPC podem definir certas propriedades para chamadas de procedimento remoto chamando [**RpcBindingSetOption**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption) e [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo). Uma vez definido, as propriedades permanecem em vigor para cada mensagem até que o aplicativo cliente as redefina.

Uma fila de mensagens tem seu próprio conjunto de propriedades, além das mensagens. Essas propriedades identificam exclusivamente uma fila e definem a classe de serviço que a fila fornece, os níveis de privacidade e autenticação necessários para as mensagens nessa fila e se as mensagens devem fazer parte de uma transação distribuída. Assim como acontece com as propriedades de mensagem, você especifica as propriedades de uma fila de mensagens chamando as funções da API MSMQ ou os métodos de objeto COM, que são descritos na documentação do MSMQ. No entanto, um aplicativo de servidor RPC pode especificar propriedades de sua própria fila de recebimento quando chama [**RpcServerUseProtseqEpEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex) para estabelecer a associação.

 

 




