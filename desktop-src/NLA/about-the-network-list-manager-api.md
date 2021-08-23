---
title: Sobre a API do Gerenciador de Lista de Rede
description: Sobre a API do Gerenciador de Lista de Rede
ms.assetid: 675cf7ed-9f57-4d62-8091-1f4e8812f2ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 704bedb3a1029c2be3c123c65a896b1765f191b886af9b354d747abd5e1698e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065166"
---
# <a name="about-the-network-list-manager-api"></a>Sobre a API do Gerenciador de Lista de Rede

O ambiente de rede Windows Microsoft permite que computadores multihomed se conectem a várias redes simultaneamente. Pode haver várias redes sem fio disponíveis junto com LAN e conexões discadas. O Gerenciador de Lista de Rede identifica redes disponíveis e retorna dados de atributo de rede para o aplicativo.

A API do Gerenciador de Lista de Rede interage com o serviço Gerenciador de Lista de Rede para identificar e recuperar as propriedades de cada rede à qual o computador se conecta. Cada rede é identificada exclusivamente com uma assinatura de rede com base nas propriedades de identificação exclusiva dessa rede. Quando um aplicativo se registra para notificações do Gerenciador de Lista de Rede, o aplicativo recebe notificações sobre a disponibilidade de novas conexões de rede ou alterações em conexões de rede existentes. Os aplicativos podem ajustar sua lógica dependendo de: a qual rede eles estão conectados; a qual conexão de rede eles estão conectados; ou quais são as propriedades de rede. Com essas informações, os aplicativos podem ajustar suas ações com base nas condições de rede atuais

Windows O Vista introduz novas interfaces que podem ser usadas para obter informações detalhadas sobre essas características de rede e muito mais. Com a interface [**INetworkListManager,**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworklistmanager) é fácil enumerar todas as redes ([**INetwork**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork)) que um computador já viu ou apenas as redes conectadas ou apenas as redes desconectadas. A interface **INetworkListManager** também facilita a enumeração dos interfaces de rede em um computador.

A interface [**INetwork**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork) é usada para determinar as propriedades de uma conexão de rede: nome, descrição, ID, gerenciado/autenticado, conectado/desconectado e muito mais. É possível que uma única rede esteja conectada a várias interfaces, portanto, por meio de uma interface **INetwork,** você também pode enumerar as instâncias da interface **INetwork** que está sendo usada.

A interface [**INetwork**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork) informa as propriedades relevantes de uma interface: ID, GUID, Tipo (gerenciado, autenticado) e Estado (conectado, desconectado, V4 Local, V4 Internet, V6 Local, V6 Internet). V4 Local significa protocolo IP versão 4 (IPv4) acesso local. Internet V4 significa IPv4 com acesso à Internet. V6 Local e V6 Internet significam IPv6.

A raiz da árvore de objetos para Local de Rede é a interface [**INetworkListManager.**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworklistmanager) Essa interface é implementada na **coclasse \_ NetworkListManager clSID.** Para usar essa interface, é necessário criar o objeto **COM \_ NetworkListManager clSID,** conforme demonstrado:


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



 

 




