---
description: Entenda as funções de sessão no gerenciamento de compartilhamento de rede. Essas funções controlam as sessões de rede estabelecidas entre estações de trabalho e servidores.
ms.assetid: 931455e3-1301-4a68-93c3-2674b3d4c491
title: Funções de sessão (gerenciamento de compartilhamento de rede)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cdde451eb2942171569b24c36aae5d5742208e5
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409719"
---
# <a name="session-functions-network-share-management"></a>Funções de sessão (gerenciamento de compartilhamento de rede)

As funções de sessão de gerenciamento de rede controlam as sessões de rede estabelecidas entre estações de trabalho e servidores. As funções exigem que o serviço do servidor seja iniciado no servidor.

As funções de sessão são listadas a seguir.



| Função                                       | Descrição                                                                                       |
|------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**NetSessionDel**](/windows/desktop/api/Lmshare/nf-lmshare-netsessiondel)         | Exclui as conexões atuais entre uma estação de trabalho e um servidor; encerra a sessão de rede. |
| [**NetSessionEnum**](/windows/desktop/api/Lmshare/nf-lmshare-netsessionenum)       | Retorna informações sobre todas as sessões atuais estabelecidas para um servidor.                          |
| [**NetSessionGetInfo**](/windows/desktop/api/Lmshare/nf-lmshare-netsessiongetinfo) | Retorna informações sobre uma sessão específica.                                                   |



 

Uma *sessão* é um link entre uma estação de trabalho e um servidor. Uma sessão é estabelecida na primeira vez em que uma estação de trabalho faz uma conexão com um recurso compartilhado no servidor. Até que a sessão termine, todas as conexões adicionais entre a estação de trabalho e o servidor fazem parte da mesma sessão. Para encerrar uma sessão, um aplicativo na extremidade do servidor de uma conexão chama a função [**NetSessionDel**](/windows/desktop/api/Lmshare/nf-lmshare-netsessiondel) .

As funções de sessão de gerenciamento de rede gerenciam informações em uma base por usuário com o parâmetro *username* . Como pode haver vários usuários por sessão, esse parâmetro é necessário para acessar as informações específicas do usuário para a sessão.

As funções de sessão estão disponíveis em cinco níveis de informações:

<dl>

[**Informações da sessão \_ \_ 0**](/windows/desktop/api/Lmshare/ns-lmshare-session_info_0)  
[**Informações da sessão \_ \_ 1**](/windows/desktop/api/Lmshare/ns-lmshare-session_info_1)  
[**Informações da sessão \_ \_ 2**](/windows/desktop/api/Lmshare/ns-lmshare-session_info_2)  
[**Informações da sessão \_ \_ 10**](/windows/desktop/api/Lmshare/ns-lmshare-session_info_10)  
[**Informações da sessão \_ \_ 502**](/windows/desktop/api/Lmshare/ns-lmshare-session_info_502)  
</dl>

Se você estiver programando para Active Directory, poderá chamar determinados métodos da interface de serviço Active Directory (ADSI) para obter a mesma funcionalidade que pode obter ao chamar as funções de sessão de gerenciamento de rede. Para obter mais informações, consulte [**IADsSession**](/windows/desktop/api/iads/nn-iads-iadssession) e [**IADsFileServiceOperations**](/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations).

 

 
