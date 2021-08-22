---
description: Entender as funções de sessão no gerenciamento de compartilhamento de rede. Essas funções controlam as sessões de rede estabelecidas entre estações de trabalho e servidores.
ms.assetid: 931455e3-1301-4a68-93c3-2674b3d4c491
title: Funções de sessão (Gerenciamento de Compartilhamento de Rede)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa914bd747f8b47e4bc4086245f425ba2d290fb9b0a6de256781a9fbca7e1516
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119580336"
---
# <a name="session-functions-network-share-management"></a>Funções de sessão (Gerenciamento de Compartilhamento de Rede)

As funções de sessão de gerenciamento de rede controlam as sessões de rede estabelecidas entre estações de trabalho e servidores. As funções exigem que o serviço de servidor seja iniciado no servidor.

As funções de sessão são listadas a seguir.



| Função                                       | Descrição                                                                                       |
|------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**NetSessionDel**](/windows/desktop/api/Lmshare/nf-lmshare-netsessiondel)         | Exclui as conexões atuais entre uma estação de trabalho e um servidor; encerra a sessão de rede. |
| [**NetSessionEnum**](/windows/desktop/api/Lmshare/nf-lmshare-netsessionenum)       | Retorna informações sobre todas as sessões atuais estabelecidas para um servidor.                          |
| [**NetSessionGetInfo**](/windows/desktop/api/Lmshare/nf-lmshare-netsessiongetinfo) | Retorna informações sobre uma sessão específica.                                                   |



 

Uma *sessão* é um link entre uma estação de trabalho e um servidor. Uma sessão é estabelecida na primeira vez que uma estação de trabalho faz uma conexão com um recurso compartilhado no servidor. Até que a sessão termine, todas as conexões entre a estação de trabalho e o servidor fazem parte da mesma sessão. Para encerrar uma sessão, um aplicativo na extremidade do servidor de uma conexão chama a [**função NetSessionDel.**](/windows/desktop/api/Lmshare/nf-lmshare-netsessiondel)

As funções de sessão de gerenciamento de rede gerenciam informações por usuário com o parâmetro *username.* Como pode haver vários usuários por sessão, esse parâmetro é necessário para acessar as informações específicas do usuário para a sessão.

As funções de sessão estão disponíveis em cinco níveis de informações:

<dl>

[**INFORMAÇÕES \_ DA \_ SESSÃO 0**](/windows/desktop/api/Lmshare/ns-lmshare-session_info_0)  
[**INFORMAÇÕES \_ DA SESSÃO \_ 1**](/windows/desktop/api/Lmshare/ns-lmshare-session_info_1)  
[**INFORMAÇÕES \_ DA \_ SESSÃO 2**](/windows/desktop/api/Lmshare/ns-lmshare-session_info_2)  
[**INFORMAÇÕES \_ DA SESSÃO \_ 10**](/windows/desktop/api/Lmshare/ns-lmshare-session_info_10)  
[**INFORMAÇÕES \_ DA \_ SESSÃO 502**](/windows/desktop/api/Lmshare/ns-lmshare-session_info_502)  
</dl>

Se você estiver programando para o Active Directory, poderá chamar determinados métodos ADSI (Interface de Serviço do Active Directory) para obter a mesma funcionalidade que você pode obter chamando as funções de sessão de gerenciamento de rede. Para obter mais informações, [**consulte IADsSession**](/windows/desktop/api/iads/nn-iads-iadssession) e [**IADsFileServiceOperations**](/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations).

 

 
