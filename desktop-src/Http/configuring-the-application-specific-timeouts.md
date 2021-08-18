---
title: Configurando os temposouts específicos do aplicativo
description: Configurando os temposouts específicos do aplicativo
ms.assetid: 24526320-4174-4fc7-b45a-c1ec605e1666
keywords:
- Configurando o HTTP de temposouts específicos do aplicativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 722d44c1377a3bee22a88fe92f0f5aed272c08f0b0a6645361c4e03816f408fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950875"
---
# <a name="configuring-the-application-specific-timeouts"></a>Configurando os temposouts específicos do aplicativo

As configurações de TODA a API do servidor HTTP se aplicam a todas as sessões de servidor e grupos de URL no computador. Essas configurações podem ser substituídos pelo aplicativo definindo os valores de tempoout específicos do aplicativo. Os temposouts de sessão do servidor substituem os temposouts de toda a API do servidor HTTP e se aplicam a todos os grupos de URL criados neles. Configurar a propriedade timeouts em um grupo de URL substitui os tempos de sessão do servidor para todas as URLs no grupo.

Especificar zero para qualquer um dos temporizadores na estrutura [**HTTP \_ TIMEOUT \_ LIMIT \_ INFO**](/windows/desktop/api/Http/ns-http-http_timeout_limit_info) para um grupo de URL faz com que a API do Servidor HTTP seja revertida para os tempos limite da sessão do servidor, se eles existirem, ou as configurações padrão da API do servidor HTTP se os tempos limite da sessão do servidor não existirem. Por exemplo, quando a propriedade de tempoout do servidor está presente em um grupo de URL e o temporizador **EntityBody** é zero, o tempo de sessão do servidor é usado. Se a propriedade timeouts não estiver definida em uma sessão de servidor, a configuração padrão da API do servidor HTTP será usada. Para desabilitar um temporizador, defina o valor como **MAXUSHORT**, exceto pelo temporizador **MinSendRate,** que está definido como **MAXULONG.**

A API do Servidor HTTP só pode configurar o **HeaderWait** específico do aplicativo e os temporizadores **IdleConnection** só são eficazes depois que a primeira solicitação é recebida. Antes que a primeira solicitação seja recebida, os valores de tempo-tempo de todo o SERVIDOR HTTP são aplicados. Depois que a primeira solicitação chegar e for associada a uma fila de solicitação, os temporizadores **HeaderWait** e **IdleConnection** específicos do aplicativo poderão ser aplicados. Os temporizadores específicos do aplicativo são aplicados a todas as solicitações subsequentes que chegam na fila de solicitação para uma conexão keep alive.

Para obter mais informações sobre como configurar temporizadores, consulte os tópicos [Configuring the URL Group](configuring-the-url-group.md) [and Configuring the Server Session](configuring-the-server-session.md) .

 

 




