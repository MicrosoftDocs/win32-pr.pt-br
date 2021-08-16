---
title: Propriedades da fila de mensagens e mensagens
description: Uma mensagem tem propriedades, que especificam um rótulo, um corpo da mensagem e várias opções.
ms.assetid: d0c9126e-a2c6-4d70-b87a-154a570899fc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15c18b3a4751cd3be4473067dd9ca5aca17717672e6b67b559c10c502513fa2f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118928105"
---
# <a name="message-and-message-queue-properties"></a>Propriedades da fila de mensagens e mensagens

Uma mensagem tem propriedades, que especificam um rótulo, um corpo da mensagem e várias opções. As opções de propriedade de mensagem podem incluir qualidade de serviço, prioridade, diário, privacidade e níveis de autenticação e o tempo de vida da mensagem. Em aplicativos convencionais (não RPC), você especifica essas propriedades chamando as funções de API do MSMQ ou os métodos de objeto COM, que são descritos na documentação do SDK do MSMQ. Os aplicativos cliente RPC podem definir determinadas propriedades para chamadas de procedimento remoto chamando [**RpcBindingSetOption**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption) e [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo). Depois de definidas, as propriedades permanecem em vigor para cada mensagem até que o aplicativo cliente as redefine.

Uma fila de mensagens tem seu próprio conjunto de propriedades, além daquelas das mensagens. Essas propriedades identificam exclusivamente uma fila e definem a classe de serviço que a fila fornece, os níveis de privacidade e autenticação necessários para mensagens nessa fila e se as mensagens devem fazer parte de uma transação distribuída. Assim como com as propriedades da mensagem, você especifica as propriedades de uma fila de mensagens chamando as funções da API MSMQ ou métodos de objeto COM, que são descritos na documentação do MSMQ. No entanto, um aplicativo de servidor RPC pode especificar propriedades de sua própria fila de recebimento quando chama [**RpcServerUseProtseqEpEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex) para estabelecer a associação.

 

 




