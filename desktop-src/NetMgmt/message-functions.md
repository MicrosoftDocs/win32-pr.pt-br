---
title: Funções de mensagem (gerenciamento de rede)
description: As funções de mensagem de gerenciamento de rede enviam mensagens e mantêm aliases de mensagens. As funções de mensagem são listadas a seguir.
ms.assetid: 9face737-3472-4a53-97b6-e861a60ee96a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3629a281637fe4ecd0c937ce0c7504beac8e11d2
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104369140"
---
# <a name="message-functions-network-management"></a>Funções de mensagem (gerenciamento de rede)

\[As funções de mensagem não têm suporte no Windows Vista porque não há suporte para os serviços alerta e mensageiro.\]

As funções de mensagem de gerenciamento de rede enviam mensagens e mantêm aliases de mensagens. As funções de mensagem são listadas a seguir.

**Windows Server 2003:** Os serviços alerta e mensageiro estão desabilitados por padrão. Você deve reabilitar os serviços antes de chamar as funções de [alerta](alert-functions.md) de gerenciamento de rede ou as funções de mensagem de gerenciamento de rede.



| Função                                               | Descrição                                                                     |
|--------------------------------------------------------|---------------------------------------------------------------------------------|
| [**NetMessageBufferSend**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagebuffersend)   | Envia uma mensagem para um alias de mensagem registrado.                                  |
| [**NetMessageNameAdd**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagenameadd)         | Registra um alias de mensagem na tabela de nome da mensagem.                            |
| [**NetMessageNameDel**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagenamedel)         | Exclui um alias de mensagem da tabela de nome da mensagem.                            |
| [**NetMessageNameEnum**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagenameenum)       | Lista todos os aliases de mensagens armazenados na tabela nome da mensagem.                 |
| [**NetMessageNameGetInfo**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagenamegetinfo) | Retorna informações sobre um alias de mensagem específico na tabela de nomes de mensagem. |



 

Uma *mensagem* é um buffer de dados de texto enviados a um usuário ou aplicativo na rede. Para receber uma mensagem, um usuário ou aplicativo deve registrar um alias de mensagem na tabela de nomes de mensagem de um computador. Os aliases a seguir são registrados por padrão: "usuário", "máquina", "domínio" ou " \* " (o domínio atual do computador). O alias "domínio" especifica o conjunto de computadores que têm o mesmo nome de domínio definido como seu domínio ou como seu grupo de trabalho e escutam difusões na mesma sub-rede. Para NetBIOS sobre TCP/IP, a especificação do alias "domínio" também poderá ser realizada em sub-redes se o nome de domínio for resolvido por um servidor de nomes ou se as difusões de datagrama NetBIOS forem encaminhadas entre roteadores. Portanto, as mensagens enviadas a um domínio não têm a entrega garantida para todos os membros do domínio. Também é possível que alguns membros do domínio recebam a mensagem várias vezes se tiverem vários transportes instalados que dão suporte ao NetBIOS.

Você também pode registrar um alias de mensagem chamando a função [**NetMessageNameAdd**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagenameadd) . Uma *tabela de nome de mensagem* contém uma lista de aliases de mensagens registradas (usuários e aplicativos) com permissão para receber mensagens. Os aliases registrados na tabela de nome de mensagem não diferenciam maiúsculas de minúsculas.

O serviço de mensageiro deve estar em execução no computador receptor para exibir uma mensagem pop-up quando a mensagem é recebida. Além disso, o serviço de estação de trabalho deve estar em execução no computador local. NetBIOS é o mecanismo de transporte usado entre o remetente e o destinatário.

As funções de mensagem estão disponíveis em dois níveis de informação:

-   [**Informação de MSG \_ \_ 0**](/windows/desktop/api/Lmmsg/ns-lmmsg-msg_info_0)
-   [**Informações da mensagem \_ \_ 1**](/windows/desktop/api/Lmmsg/ns-lmmsg-msg_info_1)

O nível de informação **msg \_ info \_ 1** existe apenas para compatibilidade. O serviço mensageiro não encaminha nomes nem permite que os nomes sejam encaminhados a ele.

 

 




