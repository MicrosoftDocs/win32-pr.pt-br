---
title: Funções de mensagem (gerenciamento de rede)
description: As funções de mensagem de gerenciamento de rede enviam mensagens e mantêm aliases de mensagem. As funções de mensagem são listadas a seguir.
ms.assetid: 9face737-3472-4a53-97b6-e861a60ee96a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0b30f88b3cbe0742b3bd06f2200475aaeb0d96d0c37bff9189efd1127ddc7d4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912036"
---
# <a name="message-functions-network-management"></a>Funções de mensagem (gerenciamento de rede)

\[As funções de mensagem não têm suporte a partir do Windows Vista porque não há suporte para os serviços do alerter e do messenger.\]

As funções de mensagem de gerenciamento de rede enviam mensagens e mantêm aliases de mensagem. As funções de mensagem são listadas a seguir.

**Windows Server 2003:** Os serviços de alerta e de mensagens são desabilitados por padrão. Você deve reabilitar os serviços antes de chamar as funções de Alerta de gerenciamento de [rede](alert-functions.md) ou as funções de mensagem de gerenciamento de rede.



| Função                                               | Descrição                                                                     |
|--------------------------------------------------------|---------------------------------------------------------------------------------|
| [**NetMessageBufferSend**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagebuffersend)   | Envia uma mensagem para um alias de mensagem registrado.                                  |
| [**NetMessageNameAdd**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagenameadd)         | Registra um alias de mensagem na tabela de nome da mensagem.                            |
| [**NetMessageNameDel**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagenamedel)         | Exclui um alias de mensagem da tabela de nome da mensagem.                            |
| [**NetMessageNameEnum**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagenameenum)       | Lista todos os aliases de mensagem armazenados na tabela de nomes de mensagem.                 |
| [**NetMessageNameGetInfo**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagenamegetinfo) | Retorna informações sobre um alias de mensagem específico na tabela de nome da mensagem. |



 

Uma *mensagem* é um buffer de dados de texto enviados a um usuário ou aplicativo na rede. Para receber uma mensagem, um usuário ou aplicativo deve registrar um alias de mensagem na tabela de nomes de mensagens de um computador. Os aliases a seguir são registrados por padrão: "user", "machine", "domain" ou \* " ( o domínio atual do computador). O alias "domínio" especifica o conjunto de computadores que têm o mesmo nome de domínio definido como seu domínio ou como seu grupo de trabalho e escuta difusões na mesma sub-rede. Para NetBIOS sobre TCP/IP, especificar o alias "domínio" também poderá ser bem-sucedido entre sub-redes se o nome de domínio for resolvido por um servidor de nomes ou se as difusões de datagrama NetBIOS são encaminhadas entre roteadores. Portanto, as mensagens enviadas para um domínio não têm entrega garantida para todos os membros do domínio. Também é possível que alguns membros do domínio recebam a mensagem várias vezes se eles têm vários transporte instalados que suportam NetBIOS.

Você também pode registrar um alias de mensagem chamando a [**função NetMessageNameAdd.**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagenameadd) Uma *tabela de nomes de mensagem* contém uma lista de aliases de mensagens registrados (usuários e aplicativos) permitidos para receber mensagens. Os aliases registrados na tabela de nomes de mensagem não são sensíveis a maiúsculas e minúsculas.

O serviço messenger deve estar em execução no computador receptor para exibir uma mensagem pop-up quando a mensagem for recebida. Além disso, o serviço estação de trabalho deve estar em execução no computador local. NetBIOS é o mecanismo de transporte usado entre o remetente e o receptor.

As funções de mensagem estão disponíveis em dois níveis de informações:

-   [**INFORMAÇÕES DO MSG \_ \_ 0**](/windows/desktop/api/Lmmsg/ns-lmmsg-msg_info_0)
-   [**INFORMAÇÕES DO MSG \_ \_ 1**](/windows/desktop/api/Lmmsg/ns-lmmsg-msg_info_1)

O **nível de informações do MSG INFO \_ \_ 1** existe apenas para compatibilidade. O serviço messenger não encaminha nomes nem permite que os nomes sejam encaminhados a ele.

 

 




