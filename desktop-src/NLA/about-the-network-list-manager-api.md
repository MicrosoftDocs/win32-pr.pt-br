---
title: Sobre a API do Gerenciador de lista de rede
description: Sobre a API do Gerenciador de lista de rede
ms.assetid: 675cf7ed-9f57-4d62-8091-1f4e8812f2ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6230251e627671b7fd33adbf50b3904703bc9847
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636931"
---
# <a name="about-the-network-list-manager-api"></a>Sobre a API do Gerenciador de lista de rede

O ambiente de rede do Microsoft Windows permite que computadores de hospedagem múltipla se conectem a várias redes simultaneamente. Pode haver várias redes sem fio disponíveis juntamente com conexões de LAN e dial-up. O Gerenciador de lista de rede identifica as redes disponíveis e retorna os dados de atributo de rede para o aplicativo.

A API do Gerenciador de lista de rede interage com o serviço Gerenciador de listas de rede para identificar e recuperar as propriedades de cada rede à qual o PC se conecta. Cada rede é identificada exclusivamente com uma assinatura de rede com base nas propriedades exclusivamente identificáveis da rede. Quando um aplicativo é registrado para notificações do Gerenciador de lista de rede, o aplicativo recebe notificações sobre a disponibilidade de novas conexões de rede ou alterações em conexões de rede existentes. Os aplicativos podem ajustar sua lógica dependendo de: a rede à qual estão conectados; a qual conexão de rede eles estão conectados; ou quais são as propriedades de rede. Com essas informações, os aplicativos podem ajustar suas ações com base nas condições de rede atuais

O Windows Vista apresenta novas interfaces que podem ser usadas para obter informações detalhadas sobre essas características de rede e muito mais. Com a interface [**INetworkListManager**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworklistmanager) , é fácil enumerar todas as redes (a [**inet**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork)) que um computador já viu ou apenas as redes conectadas ou apenas as redes desconectadas. A interface **INetworkListManager** também torna mais fácil enumerar as interfaces de rede em um computador.

A interface da [**inet**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork) é usada para determinar as propriedades de uma conexão de rede: nome, descrição, ID, gerenciado/autenticado, conectado/desconectado e muito mais. É possível que uma única rede esteja conectada a várias interfaces, por isso, por meio de uma interface da **inet** , você também pode enumerar as instâncias da interface de rede da **inet** que está sendo usada.

A interface da [**inet**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork) informa as propriedades relevantes de uma interface: ID, GUID, tipo (gerenciado, autenticado) e estado (conectado, desconectado, V4 local, IPv4 da Internet, V6 local, Internet V6). V4 local significa acesso local do protocolo IP versão 4 (IPv4). A Internet v4 significa IPv4 com acesso à Internet. A Internet V6 local e V6 significam IPv6.

A raiz da árvore de objetos para o local de rede é a interface [**INetworkListManager**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworklistmanager) . Essa interface é implementada na coclasse **CLSID \_ NetworkListManager** . Para usar essa interface, é necessário criar o objeto com NetworkListManager do **CLSID \_** , conforme demonstrado:


```C++
#include <windows.h>
#include <netlistmgr.h>

#pragma comment(lib, "ole32.lib")

void main()
{
    INetworkListManager *pNetworkListManager = NULL; 
    HRESULT hr = CoCreateInstance(CLSID_NetworkListManager, NULL,
            CLSCTX_ALL, IID_INetworkListManager,
            (LPVOID *)&pNetworkListManager);
}
```



 

 




