---
description: As funções de compartilhamento de rede controlam recursos compartilhados. Um recurso compartilhado é um recurso local em um servidor (por exemplo, um diretório de disco, um dispositivo de impressão ou um pipe nomeado) que pode ser acessado por usuários e aplicativos na rede.
ms.assetid: 14886bb0-e597-4728-a64f-bc16e82874da
title: Funções de compartilhamento de rede
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 640dc877c9b482cb8ebdcef0d36e6dff562fcd8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105761410"
---
# <a name="network-share-functions"></a>Funções de compartilhamento de rede

As funções de compartilhamento de rede controlam recursos compartilhados. Um recurso compartilhado é um recurso local em um servidor (por exemplo, um diretório de disco, um dispositivo de impressão ou um pipe nomeado) que pode ser acessado por usuários e aplicativos na rede.

As funções de compartilhamento são listadas a seguir.



| Função                                   | Descrição                                                          |
|--------------------------------------------|----------------------------------------------------------------------|
| [**NetShareAdd**](/windows/desktop/api/Lmshare/nf-lmshare-netshareadd)         | Compartilha um recurso em um servidor.                                       |
| [**NetShareCheck**](/windows/desktop/api/Lmshare/nf-lmshare-netsharecheck)     | Consulta se um servidor está compartilhando um dispositivo.                        |
| [**NetShareDel**](/windows/desktop/api/Lmshare/nf-lmshare-netsharedel)         | Exclui um nome de compartilhamento da lista de recursos compartilhados de um servidor.       |
| [**NetShareEnum**](/windows/desktop/api/Lmshare/nf-lmshare-netshareenum)       | Recupera informações de compartilhamento sobre cada recurso compartilhado em um servidor.  |
| [**NetShareGetInfo**](/windows/desktop/api/Lmshare/nf-lmshare-netsharegetinfo) | Recupera informações sobre um recurso compartilhado especificado em um servidor. |
| [**NetShareSetInfo**](/windows/desktop/api/Lmshare/nf-lmshare-netsharesetinfo) | Define os parâmetros de um recurso compartilhado.                                 |



 

A função [**NetShareAdd**](/windows/desktop/api/Lmshare/nf-lmshare-netshareadd) permite que um usuário ou aplicativo Compartilhe um recurso de um tipo específico usando o nome de compartilhamento especificado. A função **NetShareAdd** requer o nome do compartilhamento e o nome do dispositivo local para compartilhar o recurso. Um usuário ou aplicativo deve ter uma conta no servidor para acessar o recurso.

Você também pode especificar um descritor de segurança a ser associado a um compartilhamento. Descritores de segurança especificam quais usuários têm permissão para acessar arquivos por meio do compartilhamento e com que tipo de acesso. Especifique um [**\_ descritor de segurança**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) com o nível de informações do [**share \_ info \_ 502**](/windows/desktop/api/Lmshare/ns-lmshare-share_info_502) ao chamar [**NetShareAdd**](/windows/desktop/api/Lmshare/nf-lmshare-netshareadd) ou [**NetShareSetInfo**](/windows/desktop/api/Lmshare/nf-lmshare-netsharesetinfo). O **NetShareSetInfo** dá suporte ao nível de informação [**\_ \_ 1501**](/windows/desktop/api/Lmshare/ns-lmshare-share_info_1501) de informações de compartilhamento. Para obter mais informações sobre descritores de segurança, consulte [controle de acesso](/windows/desktop/SecAuthZ/access-control).

As funções de gerenciamento de rede usam os seguintes nomes de compartilhamento especiais para IPC (comunicação entre processos) e administração remota do servidor:

-   IPC $, reservado para comunicação entre processos
-   ADMIN $, reservado para administração remota
-   R $, B $, C $ (e outros nomes de disco locais seguidos de um cifrão), atribuídos aos dispositivos de disco locais

Para listar todas as conexões feitas a um recurso compartilhado em um servidor ou para listar todas as conexões estabelecidas de um determinado computador, chame a função [**NetConnectionEnum**](/windows/desktop/api/Lmshare/nf-lmshare-netconnectionenum) . Você pode chamar **NetConnectionEnum** nas informações [**de \_ conexão \_ 0**](/windows/desktop/api/Lmshare/ns-lmshare-connection_info_0) e informações de [**conexão \_ \_ 1**](/windows/desktop/api/Lmshare/ns-lmshare-connection_info_1) níveis de informação.

As funções de compartilhamento estão disponíveis nos seguintes níveis de informações:

<dl>

[**Informações de compartilhamento \_ \_ 0**](/windows/desktop/api/Lmshare/ns-lmshare-share_info_0)  
[**Informações de compartilhamento \_ \_ 1**](/windows/desktop/api/Lmshare/ns-lmshare-share_info_1)  
[**Informações de compartilhamento \_ \_ 2**](/windows/desktop/api/Lmshare/ns-lmshare-share_info_2)  
[**Informações de compartilhamento \_ \_ 501**](/windows/desktop/api/Lmshare/ns-lmshare-share_info_501)  
[**Informações de compartilhamento \_ \_ 502**](/windows/desktop/api/Lmshare/ns-lmshare-share_info_502)  
[**Informações de compartilhamento \_ \_ 1005**](/windows/desktop/api/Lmshare/ns-lmshare-share_info_1005)  
</dl>

Os seguintes níveis de informações são válidos somente para [**NetShareSetInfo**](/windows/desktop/api/Lmshare/nf-lmshare-netsharesetinfo):

<dl>

[**Informações de compartilhamento \_ \_ 1004**](/windows/desktop/api/Lmshare/ns-lmshare-share_info_1004)  
[**Informações de compartilhamento \_ \_ 1006**](/windows/desktop/api/Lmshare/ns-lmshare-share_info_1006)  
[**Informações de compartilhamento \_ \_ 1501**](/windows/desktop/api/Lmshare/ns-lmshare-share_info_1501)  
</dl>

Se estiver programando para Active Directory, você poderá chamar determinados métodos ADSI (interface do serviço de Active Directory) para obter a mesma funcionalidade que pode obter ao chamar as funções de compartilhamento de gerenciamento de rede. Para obter mais informações, consulte [**IADsFileShare**](/windows/desktop/api/iads/nn-iads-iadsfileshare).

 

 
