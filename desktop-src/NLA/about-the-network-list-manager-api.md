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
# <a name="about-the-network-list-manager-api"></a><span data-ttu-id="5c390-103">Sobre a API do Gerenciador de lista de rede</span><span class="sxs-lookup"><span data-stu-id="5c390-103">About the Network List Manager API</span></span>

<span data-ttu-id="5c390-104">O ambiente de rede do Microsoft Windows permite que computadores de hospedagem múltipla se conectem a várias redes simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="5c390-104">The Microsoft Windows networking environment allows multihomed computers to connect to several networks simultaneously.</span></span> <span data-ttu-id="5c390-105">Pode haver várias redes sem fio disponíveis juntamente com conexões de LAN e dial-up.</span><span class="sxs-lookup"><span data-stu-id="5c390-105">There may be multiple wireless networks available along with LAN and dial-up connections.</span></span> <span data-ttu-id="5c390-106">O Gerenciador de lista de rede identifica as redes disponíveis e retorna os dados de atributo de rede para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5c390-106">Network List Manager identifies available networks and returns network attribute data to the application.</span></span>

<span data-ttu-id="5c390-107">A API do Gerenciador de lista de rede interage com o serviço Gerenciador de listas de rede para identificar e recuperar as propriedades de cada rede à qual o PC se conecta.</span><span class="sxs-lookup"><span data-stu-id="5c390-107">The Network List Manager API interacts with the Network List Manager service to identify and retrieve properties of each network that the PC connects to.</span></span> <span data-ttu-id="5c390-108">Cada rede é identificada exclusivamente com uma assinatura de rede com base nas propriedades exclusivamente identificáveis da rede.</span><span class="sxs-lookup"><span data-stu-id="5c390-108">Each network is uniquely identified with a network signature based on the uniquely identifiable properties of that network.</span></span> <span data-ttu-id="5c390-109">Quando um aplicativo é registrado para notificações do Gerenciador de lista de rede, o aplicativo recebe notificações sobre a disponibilidade de novas conexões de rede ou alterações em conexões de rede existentes.</span><span class="sxs-lookup"><span data-stu-id="5c390-109">When an application registers for Network List Manager notifications, the application receives notifications about the availability of new network connections or changes to existing network connections.</span></span> <span data-ttu-id="5c390-110">Os aplicativos podem ajustar sua lógica dependendo de: a rede à qual estão conectados; a qual conexão de rede eles estão conectados; ou quais são as propriedades de rede.</span><span class="sxs-lookup"><span data-stu-id="5c390-110">Applications can adjust their logic depending on: which network they are connected to; which network connection they are connected to; or what the network properties are.</span></span> <span data-ttu-id="5c390-111">Com essas informações, os aplicativos podem ajustar suas ações com base nas condições de rede atuais</span><span class="sxs-lookup"><span data-stu-id="5c390-111">With this information applications can fine tune their actions based on current network conditions</span></span>

<span data-ttu-id="5c390-112">O Windows Vista apresenta novas interfaces que podem ser usadas para obter informações detalhadas sobre essas características de rede e muito mais.</span><span class="sxs-lookup"><span data-stu-id="5c390-112">Windows Vista introduces new interfaces that can be used to obtain detailed information about these network characteristics and more.</span></span> <span data-ttu-id="5c390-113">Com a interface [**INetworkListManager**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworklistmanager) , é fácil enumerar todas as redes (a [**inet**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork)) que um computador já viu ou apenas as redes conectadas ou apenas as redes desconectadas.</span><span class="sxs-lookup"><span data-stu-id="5c390-113">With the [**INetworkListManager**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworklistmanager) interface it is easy to enumerate all networks ([**INetwork**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork)) a computer has ever seen, or just the connected networks, or just the disconnected networks.</span></span> <span data-ttu-id="5c390-114">A interface **INetworkListManager** também torna mais fácil enumerar as interfaces de rede em um computador.</span><span class="sxs-lookup"><span data-stu-id="5c390-114">The **INetworkListManager** interface also makes it easy to enumerate the network interfaces on a computer.</span></span>

<span data-ttu-id="5c390-115">A interface da [**inet**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork) é usada para determinar as propriedades de uma conexão de rede: nome, descrição, ID, gerenciado/autenticado, conectado/desconectado e muito mais.</span><span class="sxs-lookup"><span data-stu-id="5c390-115">The [**INetwork**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork) interface is used to determine the properties of a network connection: name, description, ID, managed/authenticated, connected/disconnected, and more.</span></span> <span data-ttu-id="5c390-116">É possível que uma única rede esteja conectada a várias interfaces, por isso, por meio de uma interface da **inet** , você também pode enumerar as instâncias da interface de rede da **inet** que está sendo usada.</span><span class="sxs-lookup"><span data-stu-id="5c390-116">It is possible that a single network is connected to several interfaces, so through an **INetwork** interface you can also enumerate the instances of the **INetwork** interface being used.</span></span>

<span data-ttu-id="5c390-117">A interface da [**inet**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork) informa as propriedades relevantes de uma interface: ID, GUID, tipo (gerenciado, autenticado) e estado (conectado, desconectado, V4 local, IPv4 da Internet, V6 local, Internet V6).</span><span class="sxs-lookup"><span data-stu-id="5c390-117">The [**INetwork**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork) interface tells you the relevant properties of an interface: ID, GUID, Type (managed, authenticated), and State (connected, disconnected, V4 Local, V4 Internet, V6 Local, V6 Internet).</span></span> <span data-ttu-id="5c390-118">V4 local significa acesso local do protocolo IP versão 4 (IPv4).</span><span class="sxs-lookup"><span data-stu-id="5c390-118">V4 Local means Internet Protocol version 4 (IPv4) local access.</span></span> <span data-ttu-id="5c390-119">A Internet v4 significa IPv4 com acesso à Internet.</span><span class="sxs-lookup"><span data-stu-id="5c390-119">V4 Internet means IPv4 with internet access.</span></span> <span data-ttu-id="5c390-120">A Internet V6 local e V6 significam IPv6.</span><span class="sxs-lookup"><span data-stu-id="5c390-120">V6 Local and V6 Internet mean IPv6.</span></span>

<span data-ttu-id="5c390-121">A raiz da árvore de objetos para o local de rede é a interface [**INetworkListManager**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworklistmanager) .</span><span class="sxs-lookup"><span data-stu-id="5c390-121">The root of the object tree for Network Location is the [**INetworkListManager**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworklistmanager) interface.</span></span> <span data-ttu-id="5c390-122">Essa interface é implementada na coclasse **CLSID \_ NetworkListManager** .</span><span class="sxs-lookup"><span data-stu-id="5c390-122">This interface is implemented on the **CLSID\_NetworkListManager** coclass.</span></span> <span data-ttu-id="5c390-123">Para usar essa interface, é necessário criar o objeto com NetworkListManager do **CLSID \_** , conforme demonstrado:</span><span class="sxs-lookup"><span data-stu-id="5c390-123">In order to use this interface, it is necessary to create the **CLSID\_NetworkListManager** COM object as demonstrated:</span></span>


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



 

 




