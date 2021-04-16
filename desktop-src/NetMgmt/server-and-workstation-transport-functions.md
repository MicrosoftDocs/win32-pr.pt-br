---
title: Funções de transporte de servidor e estação de trabalho
description: O servidor de gerenciamento de rede e as funções de transporte de estação de trabalho lidam com a associação e desvinculação de protocolos de transporte de e para o servidor e o redirecionador.
ms.assetid: 64342e21-98f1-42d3-b541-46b826391fad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c1ab4a4ce5dcc3b887eb9eb9d5759db89dfed55
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105758298"
---
# <a name="server-and-workstation-transport-functions"></a>Funções de transporte de servidor e estação de trabalho

O servidor de gerenciamento de rede e as funções de transporte de estação de trabalho lidam com a associação e desvinculação de protocolos de transporte de e para o servidor e o redirecionador. As funções de transporte de servidor lidam com protocolos de transporte gerenciados pelo servidor; as funções de transporte de estação de trabalho lidam com protocolos de transporte gerenciados pelo redirecionador.

O compartilhamento de arquivos entre um dispositivo de transporte e um servidor tem dois componentes:

-   O computador servidor onde residem os arquivos
-   Um cliente de protocolo SMB que acessa os arquivos

O computador cliente se comunica com o computador do servidor em uma rede local usando um protocolo de transporte; por exemplo, TCP ou XNS. O cliente envia solicitações ao servidor para recuperar dados. O software no computador cliente que gera as solicitações de arquivo é chamado de *redirecionador* porque redireciona as solicitações de arquivo local para o computador servidor. O software no computador que recebe e atua nas solicitações de arquivo é chamado de *servidor* porque atende aos clientes. O formato específico para essas solicitações é chamado de protocolo SMB.

As funções de transporte de servidor são listadas a seguir.



| Função                                                     | Descrição                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NetServerComputerNameAdd**](/windows/desktop/api/Lmserver/nf-lmserver-netservercomputernameadd) | Associa um nome de servidor emulado a cada um dos protocolos de transporte nos quais um servidor está ativo. (Combina a funcionalidade da função [**NetServerTransportEnum**](/windows/desktop/api/Lmserver/nf-lmserver-netservertransportenum) e da função [**NetServerTransportAddEx**](/windows/desktop/api/Lmserver/nf-lmserver-netservertransportaddex) .)                                            |
| [**NetServerComputerNameDel**](/windows/desktop/api/Lmserver/nf-lmserver-netservercomputernamedel) | Desconecta cada protocolo de transporte de rede de um nome de servidor emulado definido por uma chamada anterior para a função **NetServerComputerNameAdd** .                                                                                                                                                                               |
| [**NetServerTransportAdd**](/windows/desktop/api/Lmserver/nf-lmserver-netservertransportadd)       | Associa o servidor especificado ao protocolo de transporte. (Essa função dá suporte apenas ao nível de informação [**\_ \_ \_ 0**](/windows/desktop/api/Lmserver/ns-lmserver-server_transport_info_0) de informações de transporte do servidor.)                                                                                                                                                |
| [**NetServerTransportAddEx**](/windows/desktop/api/Lmserver/nf-lmserver-netservertransportaddex)   | Associa o servidor especificado ao protocolo de transporte. (Essa função estendida dá suporte às informações de [**transporte do servidor \_ \_ info \_ 1**](/windows/desktop/api/Lmserver/ns-lmserver-server_transport_info_1), [**Server \_ Transport \_ info \_ 2**](/windows/desktop/api/Lmserver/ns-lmserver-server_transport_info_2)e [**Server \_ Transport \_ info \_ 3**](/windows/desktop/api/Lmserver/ns-lmserver-server_transport_info_3) .) |
| [**NetServerTransportDel**](/windows/desktop/api/Lmserver/nf-lmserver-netservertransportdel)       | Desconecta o protocolo de transporte do servidor.                                                                                                                                                                                                                                                                         |
| [**NetServerTransportEnum**](/windows/desktop/api/Lmserver/nf-lmserver-netservertransportenum)     | Enumera os protocolos de transporte gerenciados pelo servidor.                                                                                                                                                                                                                                                                   |



 

As funções de transporte de servidor estão disponíveis nos seguintes níveis de informações:

-   [**Informações de transporte do servidor \_ \_ \_ 0**](/windows/desktop/api/Lmserver/ns-lmserver-server_transport_info_0)
-   [**Informações de transporte do servidor \_ \_ \_ 1**](/windows/desktop/api/Lmserver/ns-lmserver-server_transport_info_1)
-   [**Informações de transporte do servidor \_ \_ \_ 2**](/windows/desktop/api/Lmserver/ns-lmserver-server_transport_info_2)
-   [**Informações de transporte do servidor \_ \_ \_ 3**](/windows/desktop/api/Lmserver/ns-lmserver-server_transport_info_3)

As funções de transporte de estação de trabalho executam operações equivalentes para a estação de trabalho.

**Windows Server 2003 e Windows XP/2000:** O redirecionador não dá suporte à função [**NetWkstaTransportAdd**](/windows/desktop/api/lmwksta/nf-lmwksta-netwkstatransportadd) ou à função [**NetWkstaTransportDel**](/windows/desktop/api/lmwksta/nf-lmwksta-netwkstatransportdel) . Você pode alterar as configurações padrão para protocolos de transporte manualmente por meio da caixa de diálogo **Propriedades de conexão de área local** na pasta **conexões de rede e dial-up** .

As funções de transporte da estação de trabalho são listadas a seguir.



| Função                                               | Descrição                                                       |
|--------------------------------------------------------|-------------------------------------------------------------------|
| [**NetWkstaTransportAdd**](/windows/desktop/api/lmwksta/nf-lmwksta-netwkstatransportadd)   | Conecta o redirecionador ao protocolo de transporte.                |
| [**NetWkstaTransportDel**](/windows/desktop/api/lmwksta/nf-lmwksta-netwkstatransportdel)   | Desconecta o protocolo de transporte do redirecionador.           |
| [**NetWkstaTransportEnum**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstatransportenum) | Lista os protocolos de transporte que são gerenciados pelo redirecionador. |



 

As funções de transporte de estação de trabalho estão disponíveis em um nível de informação:

-   [**\_Informações de transporte WKSTA \_ \_ 0**](/windows/desktop/api/Lmwksta/ns-lmwksta-wksta_transport_info_0)

 

 




