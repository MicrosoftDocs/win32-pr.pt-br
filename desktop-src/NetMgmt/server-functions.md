---
title: Funções de servidor (gerenciamento de rede)
description: As funções do servidor de gerenciamento de rede executam tarefas administrativas em um servidor local ou remoto. As funções de servidor são listadas a seguir.
ms.assetid: 43e1285b-8c86-4af4-9834-fcd5ee8aceb8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43758fa822ce60d484418431941a386681bb77d1
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104008768"
---
# <a name="server-functions-network-management"></a>Funções de servidor (gerenciamento de rede)

As funções do servidor de gerenciamento de rede executam tarefas administrativas em um servidor local ou remoto. As funções de servidor são listadas a seguir.



| Função                                       | Descrição                                                                        |
|------------------------------------------------|------------------------------------------------------------------------------------|
| [**NetServerDiskEnum**](/windows/desktop/api/Lmserver/nf-lmserver-netserverdiskenum) | Retorna uma lista de unidades de disco locais em um servidor.                                   |
| [**NetServerEnum**](/windows/desktop/api/Lmserver/nf-lmserver-netserverenum)         | Lista todos os servidores visíveis de um tipo específico (ou tipos) no domínio especificado. |
| [**NetServerGetInfo**](/windows/desktop/api/Lmserver/nf-lmserver-netservergetinfo)   | Retorna informações de configuração sobre um servidor especificado.                        |
| [**NetServerSetInfo**](/windows/desktop/api/Lmserver/nf-lmserver-netserversetinfo)   | Define os parâmetros operacionais de um servidor.                                        |



 

Somente um usuário ou aplicativo com associação de grupo de administrador em um servidor local ou remoto pode executar tarefas administrativas nesse servidor para controlar a operação, o acesso do usuário e o compartilhamento de recursos do servidor. Os parâmetros de nível baixo que afetam a operação de um servidor podem ser examinados e modificados chamando as funções [**NetServerGetInfo**](/windows/desktop/api/Lmserver/nf-lmserver-netservergetinfo) e [**NetServerSetInfo**](/windows/desktop/api/Lmserver/nf-lmserver-netserversetinfo) . Esses parâmetros são definidos no arquivo de LANMAN.INI do servidor.

A maioria das funções do servidor de gerenciamento de rede é executada somente em um servidor remoto. A função [**NetServerEnum**](/windows/desktop/api/Lmserver/nf-lmserver-netserverenum) é executada em uma estação de trabalho local ou em um servidor remoto. Se você tentar executar outras funções de servidor em uma estação de trabalho local, as funções retornarão o erro NERR \_ RemoteOnly.

As informações específicas do servidor estão disponíveis nos seguintes níveis:

-   [**Informações do servidor \_ \_ 100**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_100)
-   [**Informações do servidor \_ \_ 101**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_101)
-   [**Informações do servidor \_ \_ 102**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_102)
-   [**Informações do servidor \_ \_ 402**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_402)
-   [**Informações do servidor \_ \_ 403**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_403)
-   [**Informações do servidor \_ \_ 1501**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1501)
-   [**Informações do servidor \_ \_ 1502**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1502)
-   [**Informações do servidor \_ \_ 1503**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1503)
-   [**Informações do servidor \_ \_ 1506**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1506)
-   [**Informações do servidor \_ \_ 1509**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1509)
-   [**Informações do servidor \_ \_ 1510**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1510)
-   [**Informações do servidor \_ \_ 1511**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1511)
-   [**Informações do servidor \_ \_ 1512**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1512)
-   [**Informações do servidor \_ \_ 1513**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1513)
-   [**Informações do servidor \_ \_ 1515**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1515)
-   [**Informações do servidor \_ \_ 1516**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1516)
-   [**Informações do servidor \_ \_ 1518**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1518)
-   [**Informações do servidor \_ \_ 1523**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1523)
-   [**Informações do servidor \_ \_ 1528**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1528)
-   [**Informações do servidor \_ \_ 1529**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1529)
-   [**Informações do servidor \_ \_ 1530**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1530)
-   [**Informações do servidor \_ \_ 1533**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1533)
-   [**Informações do servidor \_ \_ 1536**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1536)
-   [**Informações do servidor \_ \_ 1538**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1538)
-   [**Informações do servidor \_ \_ 1539**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1539)
-   [**Informações do servidor \_ \_ 1540**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1540)
-   [**Informações do servidor \_ \_ 1541**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1541)
-   [**Informações do servidor \_ \_ 1542**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1542)
-   [**Informações do servidor \_ \_ 1544**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1544)
-   [**Informações do servidor \_ \_ 1550**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1550)
-   [**Informações do servidor \_ \_ 1552**](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1552)

Se estiver programando para Active Directory, você poderá chamar determinados métodos ADSI (interface do serviço de Active Directory) para obter a mesma funcionalidade que pode obter ao chamar as funções do servidor de gerenciamento de rede. Para obter mais informações, consulte [**IADsComputer**](/windows/desktop/api/iads/nn-iads-iadscomputer).

Para obter mais informações, consulte as [funções de transporte de servidor e estação de trabalho](server-and-workstation-transport-functions.md).

 

 
