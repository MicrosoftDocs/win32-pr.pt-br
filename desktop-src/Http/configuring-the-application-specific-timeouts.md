---
title: Configurando os tempos limite específicos do aplicativo
description: Configurando os tempos limite específicos do aplicativo
ms.assetid: 24526320-4174-4fc7-b45a-c1ec605e1666
keywords:
- Configurando o tempo limite de HTTP específico do aplicativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aca1cbcdb0b0796820282673c41507f6bfcc0ebd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109734"
---
# <a name="configuring-the-application-specific-timeouts"></a>Configurando os tempos limite específicos do aplicativo

As configurações de toda a API do servidor HTTP se aplicam a todas as sessões de servidor e a grupos de URLs no computador. Essas configurações podem ser substituídas pelo aplicativo definindo os valores de tempo limite específicos do aplicativo. Os tempos limite da sessão do servidor substituem os tempos limite de toda a API do servidor HTTP e se aplicam a todos os grupos de URLs criados sob eles. Configurar a propriedade timeouts em um grupo de URLs substitui os tempos limite de sessão de servidor para todas as URLs no grupo.

A especificação de zero para qualquer um dos temporizadores na estrutura de [**\_ informações de \_ limite \_ de tempo limite http**](/windows/desktop/api/Http/ns-http-http_timeout_limit_info) para um grupo de URLs faz com que a API do servidor http reverta para os tempos limite da sessão do servidor, se existirem, ou as configurações padrão da API do servidor http se os tempos limite da sessão do servidor não existirem. Por exemplo, quando a Propriedade Timeout do servidor está presente em um grupo de URLs e o temporizador **EntityBody** é zero, o tempo limite da sessão do servidor é usado. Se a propriedade timeouts não estiver definida em uma sessão de servidor, a configuração padrão da API do servidor HTTP será usada. Para desabilitar um temporizador, defina o valor como **MAXUSHORT**, exceto para o temporizador **MinSendRate** que está definido como **MAXULONG**.

A API do servidor HTTP só pode configurar o **HeaderWait** específico do aplicativo e os temporizadores **IdleConnection** são efetivos somente depois que a primeira solicitação é recebida. Antes que a primeira solicitação seja recebida, os valores de tempo limite de toda a API do servidor HTTP são aplicados. Depois que a primeira solicitação chega e é associada a uma fila de solicitações, os temporizadores **HeaderWait** e **IdleConnection** específicos do aplicativo podem ser aplicados. Os temporizadores específicos do aplicativo são aplicados a todas as solicitações subsequentes que chegam na fila de solicitações para uma conexão Keep-Alive.

Para obter mais informações sobre como configurar temporizadores, consulte os tópicos [Configurando o grupo de URLs](configuring-the-url-group.md) e [Configurando a sessão de servidor](configuring-the-server-session.md) .

 

 




