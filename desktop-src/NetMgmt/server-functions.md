---
title: Funções de servidor (gerenciamento de rede)
description: As funções do servidor de gerenciamento de rede executam tarefas administrativas em um servidor local ou remoto. As funções de servidor são listadas a seguir.
ms.assetid: 43e1285b-8c86-4af4-9834-fcd5ee8aceb8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 086abbd23682c17bb1bbfee6180067ca0947a848a4a8dfadb36ba1b87ef13c11
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117983130"
---
# <a name="server-functions-network-management"></a>Funções de servidor (gerenciamento de rede)

As funções do servidor de gerenciamento de rede executam tarefas administrativas em um servidor local ou remoto. As funções de servidor são listadas a seguir.



| Função                                       | Descrição                                                                        |
|------------------------------------------------|------------------------------------------------------------------------------------|
| [**NetServerDiskEnum**](/windows/desktop/api/Lmserver/nf-lmserver-netserverdiskenum) | Retorna uma lista de unidades de disco local em um servidor.                                   |
| [**NetServerEnum**](/windows/desktop/api/Lmserver/nf-lmserver-netserverenum)         | Lista todos os servidores visíveis de um tipo específico (ou tipos) no domínio especificado. |
| [**NetServerGetInfo**](/windows/desktop/api/Lmserver/nf-lmserver-netservergetinfo)   | Retorna informações de configuração sobre um servidor especificado.                        |
| [**NetServerSetInfo**](/windows/desktop/api/Lmserver/nf-lmserver-netserversetinfo)   | Define os parâmetros operacionais de um servidor.                                        |



 

Somente um usuário ou aplicativo com associação de grupo de administração em um servidor local ou remoto pode executar tarefas administrativas nesse servidor para controlar a operação do servidor, o acesso do usuário e o compartilhamento de recursos. Os parâmetros de baixo nível que afetam a operação de um servidor podem ser examinados e modificados chamando as funções [**NetServerGetInfo**](/windows/desktop/api/Lmserver/nf-lmserver-netservergetinfo) e [**NetServerSetInfo.**](/windows/desktop/api/Lmserver/nf-lmserver-netserversetinfo) Esses parâmetros são definidos no arquivo de LANMAN.INI servidor.

A maioria das funções de servidor de gerenciamento de rede é executada somente em um servidor remoto. A [**função NetServerEnum**](/windows/desktop/api/Lmserver/nf-lmserver-netserverenum) é executada em uma estação de trabalho local ou em um servidor remoto. Se você tentar executar outras funções de servidor em uma estação de trabalho local, as funções retornarão o erro NERR \_ RemoteOnly.

Informações específicas do servidor estão disponíveis nos seguintes níveis:

-   [**INFORMAÇÕES \_ DO \_ SERVIDOR 100**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_100)
-   [**INFORMAÇÕES \_ DO SERVIDOR \_ 101**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_101)
-   [**INFORMAÇÕES \_ DO SERVIDOR \_ 102**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_102)
-   [**INFORMAÇÕES \_ DO SERVIDOR \_ 402**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_402)
-   [**INFORMAÇÕES \_ DO SERVIDOR \_ 403**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_403)
-   [**INFORMAÇÕES \_ DO \_ SERVIDOR 1501**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1501)
-   [**INFORMAÇÕES \_ DO SERVIDOR \_ 1502**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1502)
-   [**INFORMAÇÕES \_ DO \_ SERVIDOR 1503**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1503)
-   [**INFORMAÇÕES \_ DO \_ SERVIDOR 1506**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1506)
-   [**INFORMAÇÕES \_ DO \_ SERVIDOR 1509**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1509)
-   [**INFORMAÇÕES \_ DO \_ SERVIDOR 1510**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1510)
-   [**INFORMAÇÕES \_ DO \_ SERVIDOR 1511**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1511)
-   [**INFORMAÇÕES \_ DO \_ SERVIDOR 1512**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1512)
-   [**INFORMAÇÕES \_ DO \_ SERVIDOR 1513**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1513)
-   [**INFORMAÇÕES \_ DO \_ SERVIDOR 1515**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1515)
-   [**INFORMAÇÕES \_ DO \_ SERVIDOR 1516**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1516)
-   [**INFORMAÇÕES \_ DO \_ SERVIDOR 1518**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1518)
-   [**INFORMAÇÕES \_ DO \_ SERVIDOR 1523**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1523)
-   [**INFORMAÇÕES \_ DO \_ SERVIDOR 1528**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1528)
-   [**INFORMAÇÕES \_ DO \_ SERVIDOR 1529**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1529)
-   [**INFORMAÇÕES \_ DO \_ SERVIDOR 1530**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1530)
-   [**INFORMAÇÕES \_ DO \_ SERVIDOR 1533**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1533)
-   [**INFORMAÇÕES \_ DO \_ SERVIDOR 1536**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1536)
-   [**INFORMAÇÕES \_ DO \_ SERVIDOR 1538**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1538)
-   [**INFORMAÇÕES \_ DO \_ SERVIDOR 1539**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1539)
-   [**INFORMAÇÕES \_ DO \_ SERVIDOR 1540**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1540)
-   [**INFORMAÇÕES \_ DO \_ SERVIDOR 1541**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1541)
-   [**INFORMAÇÕES \_ DO \_ SERVIDOR 1542**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1542)
-   [**INFORMAÇÕES \_ DO \_ SERVIDOR 1544**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1544)
-   [**INFORMAÇÕES \_ DO \_ SERVIDOR 1550**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1550)
-   [**INFORMAÇÕES \_ DO \_ SERVIDOR 1552**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1552)

Se você estiver programando para o Active Directory, poderá chamar determinados métodos ADSI (Interface de Serviço do Active Directory) para obter a mesma funcionalidade que você pode obter chamando as funções do servidor de gerenciamento de rede. Para obter mais informações, [**consulte IADsComputer**](/windows/desktop/api/iads/nn-iads-iadscomputer).

Para obter mais informações, consulte [Funções de transporte de servidor e estação de trabalho](server-and-workstation-transport-functions.md).

 

 
