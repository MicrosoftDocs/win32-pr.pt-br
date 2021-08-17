---
title: Funções de compartilhamento
description: As funções de compartilhamento de gerenciamento de rede controlam recursos compartilhados. Um recurso compartilhado é um recurso local em um servidor (por exemplo, um diretório de disco, um dispositivo de impressão ou um pipe nomeado) que pode ser acessado por usuários e aplicativos na rede.
ms.assetid: 3764c667-2290-48e6-ba3a-c74eee2c27f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e97dc4570c3ef1300322bdf9bd4c9616176e31661319ac77378c61a71667523f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119064286"
---
# <a name="share-functions"></a>Funções de compartilhamento

As funções de compartilhamento de gerenciamento de rede controlam recursos compartilhados. Um recurso compartilhado é um recurso local em um servidor (por exemplo, um diretório de disco, um dispositivo de impressão ou um pipe nomeado) que pode ser acessado por usuários e aplicativos na rede.

As funções de compartilhamento são listadas a seguir.



| Função                                  | Descrição                                                          |
|-------------------------------------------|----------------------------------------------------------------------|
| [**NetShareAdd**](/windows/desktop/api/lmshare/nf-lmshare-netshareadd)         | Compartilha um recurso em um servidor.                                       |
| [**NetShareCheck**](/windows/desktop/api/lmshare/nf-lmshare-netsharecheck)     | Consulta se um servidor está compartilhando um dispositivo.                        |
| [**NetShareDel**](/windows/desktop/api/lmshare/nf-lmshare-netsharedel)         | Exclui um nome de compartilhamento da lista de recursos compartilhados de um servidor.       |
| [**NetShareEnum**](/windows/desktop/api/lmshare/nf-lmshare-netshareenum)       | Recupera informações de compartilhamento sobre cada recurso compartilhado em um servidor.  |
| [**NetShareGetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netsharegetinfo) | Recupera informações sobre um recurso compartilhado especificado em um servidor. |
| [**Netsharesetinfo**](/windows/desktop/api/lmshare/nf-lmshare-netsharesetinfo) | Define os parâmetros de um recurso compartilhado.                                 |



 

Essa função de compartilhamento se aplica somente a compartilhamentos em um servidor do LAN Manager (Server Message Block). Essas funções de compartilhamento não são suportadas Sistema de Arquivos Distribuído compartilhamentos dfs (compartilhamentos). Por exemplo, a [**função NetShareGetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netsharegetinfo) só pode recuperar informações para um recurso de compartilhamento especificado em um servidor SMB. Para recuperar informações de um compartilhamento usando um provedor de rede diferente (WebDAV ou um compartilhamento DFS, por exemplo), use a [**função WNetGetConnection.**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetgetconnectiona)

A [**função NetShareAdd**](/windows/desktop/api/lmshare/nf-lmshare-netshareadd) permite que um usuário ou aplicativo compartilhe um recurso de um tipo específico usando o nome de compartilhamento especificado. A **função NetShareAdd** requer o nome do compartilhamento e o nome do dispositivo local para compartilhar o recurso. Um usuário ou aplicativo deve ter uma conta no servidor para acessar o recurso.

Você também pode especificar um descritor de segurança a ser associado a um compartilhamento. Os descritores de segurança especificam quais usuários têm permissão para acessar arquivos por meio do compartilhamento e com que tipo de acesso. [**Especifique \_ um DESCRITOR DE SEGURANÇA**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) com o nível de informações DO SHARE INFO [**\_ \_ 502**](/windows/desktop/api/lmshare/ns-lmshare-share_info_502) ao chamar **NetShareAdd** ou [**NetShareSetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netsharesetinfo). **NetShareSetInfo dá** suporte ao nível de informações [**SHARE INFO \_ \_ 1501.**](/windows/desktop/api/lmshare/ns-lmshare-share_info_1501) Para obter mais informações sobre descritores de segurança, consulte [Controle de acesso](/windows/desktop/SecAuthZ/access-control).

As funções de gerenciamento de rede usam os seguintes nomes de compartilhamento especiais para comunicação entre processos (IPC) e administração remota do servidor:

-   IPC$, reservado para comunicação entre processos
-   ADMIN$, reservado para administração remota
-   A$, B$, C$ (e outros nomes de disco local seguidos por um cifrão), atribuídos a dispositivos de disco local

Para listar todas as conexões feitas com um recurso compartilhado em um servidor ou listar todas as conexões estabelecidas de um computador específico, chame a [**função NetConnectionEnum.**](/windows/desktop/api/lmshare/nf-lmshare-netconnectionenum) Você pode chamar **NetConnectionEnum nos** níveis de informações [**INFORMAÇÕES DE CONEXÃO \_ \_ 0**](/windows/desktop/api/lmshare/ns-lmshare-connection_info_0) e [**INFORMAÇÕES DE CONEXÃO \_ \_ 1.**](/windows/desktop/api/lmshare/ns-lmshare-connection_info_1)

As funções de compartilhamento estão disponíveis nos seguintes níveis de informações, embora alguns níveis de compartilhamento sejam aplicáveis apenas a algumas das funções de compartilhamento:

-   [**COMPARTILHAR \_ INFORMAÇÕES \_ 0**](/windows/desktop/api/lmshare/ns-lmshare-share_info_0)
-   [**COMPARTILHAR \_ INFORMAÇÕES \_ 1**](/windows/desktop/api/lmshare/ns-lmshare-share_info_1)
-   [**COMPARTILHAR \_ INFORMAÇÕES \_ 2**](/windows/desktop/api/lmshare/ns-lmshare-share_info_2)
-   [**INFORMAÇÕES \_ DE \_ COMPARTILHAMENTO 501**](/windows/desktop/api/lmshare/ns-lmshare-share_info_501)
-   [**INFORMAÇÕES \_ DE \_ COMPARTILHAMENTO 502**](/windows/desktop/api/lmshare/ns-lmshare-share_info_502)
-   [**INFORMAÇÕES \_ DE \_ COMPARTILHAMENTO 503**](/windows/desktop/api/lmshare/ns-lmshare-share_info_503)
-   [**INFORMAÇÕES \_ DE \_ COMPARTILHAMENTO 1004**](/windows/desktop/api/lmshare/ns-lmshare-share_info_1004)
-   [**INFORMAÇÕES \_ DE \_ COMPARTILHAMENTO 1005**](/windows/desktop/api/lmshare/ns-lmshare-share_info_1005)
-   [**INFORMAÇÕES \_ DE \_ COMPARTILHAMENTO 1006**](/windows/desktop/api/lmshare/ns-lmshare-share_info_1006)
-   [**INFORMAÇÕES \_ DE \_ COMPARTILHAMENTO 1501**](/windows/desktop/api/lmshare/ns-lmshare-share_info_1501)

Consulte a documentação de uma função de compartilhamento específica para obter detalhes.

Se você estiver programando para o Active Directory, poderá chamar determinados métodos ADSI (Interface de Serviço do Active Directory) para obter a mesma funcionalidade que você pode obter chamando as funções de compartilhamento de gerenciamento de rede. Para obter mais informações, [**consulte IADsFileShare**](/windows/desktop/api/iads/nn-iads-iadsfileshare).

 

 