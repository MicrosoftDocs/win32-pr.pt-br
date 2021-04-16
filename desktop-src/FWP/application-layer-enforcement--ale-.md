---
title: Aplicação da camada de aplicativo (EPA)
description: A EPA é um conjunto de camadas de modo de kernel da WFP (plataforma de filtragem do Windows) que são usadas para filtragem com monitoração de estado.
ms.assetid: ffebd312-9220-476c-a4ba-28e2e8ac8879
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f4cab1b2583d221c59d83c513c451077c806129
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104365966"
---
# <a name="application-layer-enforcement-ale"></a><span data-ttu-id="fa5cb-103">Aplicação da camada de aplicativo (EPA)</span><span class="sxs-lookup"><span data-stu-id="fa5cb-103">Application Layer Enforcement (ALE)</span></span>

<span data-ttu-id="fa5cb-104">A EPA é um conjunto de camadas de modo de kernel da WFP (plataforma de filtragem do Windows) que são usadas para filtragem com monitoração de estado.</span><span class="sxs-lookup"><span data-stu-id="fa5cb-104">ALE is a set of Windows Filtering Platform (WFP) kernel-mode layers that are used for stateful filtering.</span></span>

<span data-ttu-id="fa5cb-105">A filtragem com monitoração de estado controla o estado das conexões de rede e permite apenas os pacotes que correspondem a um estado de conexão conhecido.</span><span class="sxs-lookup"><span data-stu-id="fa5cb-105">Stateful filtering keeps track of the state of network connections and allows only packets that match a known connection state.</span></span> <span data-ttu-id="fa5cb-106">Por exemplo, a filtragem com monitoração de estado para uma conexão TCP iniciada por trás de um firewall pode permitir apenas pacotes de entrada que correspondam aos pacotes de saída anteriores enviados pela parte protegida.</span><span class="sxs-lookup"><span data-stu-id="fa5cb-106">For example, stateful filtering for a TCP connection initiated from behind a firewall can allow only incoming packets that match previous outgoing packets sent by the party protected.</span></span>

<span data-ttu-id="fa5cb-107">Filtros nas camadas de ALE autorizam a criação de conexão de entrada e saída, atribuições de porta, operações de soquete como [**escuta ()**](/windows/desktop/api/winsock2/nf-winsock2-listen), criação de soquete bruto e modo promíscuo recebendo.</span><span class="sxs-lookup"><span data-stu-id="fa5cb-107">Filters in the ALE layers authorize inbound and outbound connection creation, port assignments, socket operations such as [**listen()**](/windows/desktop/api/winsock2/nf-winsock2-listen), raw socket creation, and promiscuous mode receiving.</span></span>

<span data-ttu-id="fa5cb-108">O tráfego nas camadas ALE é classificado por conexão ou operação por soquete.</span><span class="sxs-lookup"><span data-stu-id="fa5cb-108">Traffic at the ALE layers is classified either per-connection or per-socket operation.</span></span> <span data-ttu-id="fa5cb-109">Em camadas não ALE, os filtros só podem classificar o tráfego em uma base por pacote.</span><span class="sxs-lookup"><span data-stu-id="fa5cb-109">At non-ALE layers, filters can only classify traffic on a per-packet basis.</span></span>

<span data-ttu-id="fa5cb-110">As camadas de ALE são as únicas camadas de WFP em que o tráfego de rede pode ser filtrado com base na identidade do aplicativo — usando um nome de arquivo normalizado — e com base na identidade do usuário — usando um descritor de segurança.</span><span class="sxs-lookup"><span data-stu-id="fa5cb-110">ALE layers are the only WFP layers where network traffic can be filtered based on the application identity—using a normalized file name—and based on the user identity—using a security descriptor.</span></span> <span data-ttu-id="fa5cb-111">(Consulte FLT \_ Informações de nome de arquivo \_ \_ na documentação do Windows Driver Kit (WDK), para obter mais informações sobre nomes de arquivo normalizados.)</span><span class="sxs-lookup"><span data-stu-id="fa5cb-111">(See FLT\_FILE\_NAME\_INFORMATION in the Windows Driver Kit (WDK) documentation, for more information on normalized file names.)</span></span>

<span data-ttu-id="fa5cb-112">Além disso, quando o IPsec é usado para proteger a conexão, a filtragem em camadas ALE também pode ser executada na identidade do computador remoto e na identidade do usuário remoto.</span><span class="sxs-lookup"><span data-stu-id="fa5cb-112">In addition, when IPsec is used to secure the connection, filtering at ALE layers can also be performed on the remote machine identity and on the remote user identity.</span></span> <span data-ttu-id="fa5cb-113">As identidades do computador remoto e do usuário são obtidas das credenciais usadas na criação de uma sessão IPsec.</span><span class="sxs-lookup"><span data-stu-id="fa5cb-113">The remote machine and user identities are obtained from the credentials used in the creation of an IPsec session.</span></span>

<span data-ttu-id="fa5cb-114">Por esse motivo, as políticas que impõem quem (por exemplo, "administrador") e/ou qual aplicativo (por exemplo, "Internet Explorer") têm permissão para executar as operações de rede mencionadas acima são criadas nas camadas da ALE.</span><span class="sxs-lookup"><span data-stu-id="fa5cb-114">For this reason, policies that enforce who (for example, "administrator") and/or which application (for example, "Internet Explorer") are allowed to perform the network operations mentioned above are authored at the ALE layers.</span></span>

<span data-ttu-id="fa5cb-115">A EPA fornece imposição para políticas como "permitir que o Windows Messenger todo o acesso à rede ao bloquear todos os outros aplicativos".</span><span class="sxs-lookup"><span data-stu-id="fa5cb-115">ALE provides enforcement for policies such as "allow Windows Messenger all access to the network while blocking all other applications."</span></span> <span data-ttu-id="fa5cb-116">Nesse exemplo, quando o aplicativo "Messenger" se conecta pela rede, a EPA intercepta o evento, determina que ele foi iniciado pelo Messenger e consulta o mecanismo de filtro de WFP para determinar se o soquete deve ter permissão para continuar.</span><span class="sxs-lookup"><span data-stu-id="fa5cb-116">In such an example, when the application "Messenger" connects across the network, ALE traps the event, determines that it was initiated by Messenger and queries the WFP filter engine to determine whether the socket should be allowed to proceed.</span></span>

> [!Note]  
> <span data-ttu-id="fa5cb-117">Devido à natureza dos soquetes de IP duplo, as classificações na camada ALE de IPv4 podem não ocorrer.</span><span class="sxs-lookup"><span data-stu-id="fa5cb-117">Due to the nature of true dual-IP sockets, classifications at the IPv4 ALE layer may not occur.</span></span> <span data-ttu-id="fa5cb-118">Isso é por design, porque para todas as intenções e finalidades, o soquete é um soquete IPv6.</span><span class="sxs-lookup"><span data-stu-id="fa5cb-118">This is by design, because for all intents and purposes, the socket is an IPv6 socket.</span></span> <span data-ttu-id="fa5cb-119">Para ver o tráfego v4 para esse soquete, crie filtros na camada V6 usando o endereço mapeado para IPv6.</span><span class="sxs-lookup"><span data-stu-id="fa5cb-119">To see the V4 traffic for such a socket, create filters at the V6 layer using the IPv6-mapped address.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="fa5cb-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fa5cb-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fa5cb-121">Camadas ALE</span><span class="sxs-lookup"><span data-stu-id="fa5cb-121">ALE Layers</span></span>](ale-layers.md)
</dt> <dt>

[<span data-ttu-id="fa5cb-122">Filtragem de estado de ALE</span><span class="sxs-lookup"><span data-stu-id="fa5cb-122">ALE Stateful Filtering</span></span>](ale-stateful-filtering.md)
</dt> <dt>

[<span data-ttu-id="fa5cb-123">Tráfego de difusão/multicast ALE</span><span class="sxs-lookup"><span data-stu-id="fa5cb-123">ALE Multicast/Broadcast Traffic</span></span>](ale-multicast-broadcast-traffic.md)
</dt> <dt>

[<span data-ttu-id="fa5cb-124">Reautorização de ALE</span><span class="sxs-lookup"><span data-stu-id="fa5cb-124">ALE Reauthorization</span></span>](ale-re-authorization.md)
</dt> <dt>

[<span data-ttu-id="fa5cb-125">Personalização de fluxo ALE</span><span class="sxs-lookup"><span data-stu-id="fa5cb-125">ALE Flow Customization</span></span>](ale-flow-customization.md)
</dt> </dl>

 

 