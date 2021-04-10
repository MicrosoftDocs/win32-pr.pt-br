---
description: O provedor de serviços NLA (reconhecimento de local de rede) é vital para computadores ou dispositivos que podem ser movidos entre redes diferentes e para a seleção de configurações ideais quando há mais de uma disponível.
ms.assetid: 307f384d-e59a-4fc5-8f6a-ed81a102df60
title: A função de NLA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28034d0d08353b3e794b5a30a6900e24d214e977
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165340"
---
# <a name="the-role-of-nla"></a><span data-ttu-id="ea296-103">A função de NLA</span><span class="sxs-lookup"><span data-stu-id="ea296-103">The Role of NLA</span></span>

<span data-ttu-id="ea296-104">O provedor de serviços NLA (reconhecimento de local de rede) é vital para computadores ou dispositivos que podem ser movidos entre redes diferentes e para a seleção de configurações ideais quando há mais de uma disponível.</span><span class="sxs-lookup"><span data-stu-id="ea296-104">The Network Location Awareness (NLA) service provider is vital for computers or devices that might move between different networks, and for selecting optimal configurations when more than one is available.</span></span> <span data-ttu-id="ea296-105">Por exemplo, um roaming de computador sem fio entre redes físicas pode usar NLA para determinar a configuração adequada com base nas informações sobre sua conexão de rede disponível.</span><span class="sxs-lookup"><span data-stu-id="ea296-105">For example, a wireless computer roaming between physical networks can use NLA to determine the proper configuration based on information about its available network connection.</span></span> <span data-ttu-id="ea296-106">A NLA também comprova valioso quando um computador com hospedagem múltipla tem uma conexão física com uma rede, enquanto também está conectado a outra rede por meio de uma conexão discada ou de um túnel.</span><span class="sxs-lookup"><span data-stu-id="ea296-106">NLA also proves valuable when a multihomed computer has a physical connection to one network while also connected to another network through a dial-up connection or a tunnel.</span></span>

<span data-ttu-id="ea296-107">No passado, os desenvolvedores tinham que obter informações sobre uma interface de rede lógica e, portanto, tomar decisões sobre a conectividade de rede, com base em uma infinidade de informações de rede diferentes.</span><span class="sxs-lookup"><span data-stu-id="ea296-107">In the past, developers had to obtain information about a logical network interface, and therefore make decisions about network connectivity, based on a multitude of disparate network information.</span></span> <span data-ttu-id="ea296-108">Nessas circunstâncias, os desenvolvedores tinham que escolher a interface de rede apropriada com base no endereço IP, a sub-rede da interface, o nome DNS (sistema de nomes de domínio) associado à interface, o endereço MAC de uma NIC, um nome de rede sem fio ou outras informações de rede.</span><span class="sxs-lookup"><span data-stu-id="ea296-108">In those circumstances, developers had to choose the appropriate network interface based on the IP address, the subnet of the interface, the Domain Name System (DNS) name associated with the interface, the MAC address of a NIC, a wireless network name, or other network information.</span></span> <span data-ttu-id="ea296-109">O NLA alivia esse problema fornecendo uma interface padrão para enumerar informações de anexo de rede lógica, correlacioná-las com informações de interface de rede física e, em seguida, fornecer notificação quando as informações retornadas anteriormente forem invalidadas.</span><span class="sxs-lookup"><span data-stu-id="ea296-109">NLA alleviates this problem by supplying a standard interface for enumerating logical network attachment information, correlating it with physical network interface information, and then providing notification when previously returned information gets invalidated.</span></span>

<span data-ttu-id="ea296-110">O NLA fornece as seguintes informações de local de rede:</span><span class="sxs-lookup"><span data-stu-id="ea296-110">NLA provides the following network location information:</span></span>

<dl> <dt>

<span data-ttu-id="ea296-111"><span id="Logical_Network_Identity"></span><span id="logical_network_identity"></span><span id="LOGICAL_NETWORK_IDENTITY"></span>Identidade de rede lógica</span><span class="sxs-lookup"><span data-stu-id="ea296-111"><span id="Logical_Network_Identity"></span><span id="logical_network_identity"></span><span id="LOGICAL_NETWORK_IDENTITY"></span>Logical Network Identity</span></span>
</dt> <dd>

<span data-ttu-id="ea296-112">A NLA tenta primeiro identificar uma rede lógica por seu nome de domínio DNS.</span><span class="sxs-lookup"><span data-stu-id="ea296-112">NLA first attempts to identify a logical network by its DNS domain name.</span></span> <span data-ttu-id="ea296-113">Se uma rede lógica não tiver um nome de domínio, a NLA identificará a rede de informações estáticas personalizadas armazenadas no registro e, por fim, do seu endereço de sub-rede.</span><span class="sxs-lookup"><span data-stu-id="ea296-113">If a logical network does not have a domain name, NLA identifies the network from custom static information stored in the registry, and finally from its subnet address.</span></span>

</dd> <dt>

<span data-ttu-id="ea296-114"><span id="Logical_Network_Interfaces"></span><span id="logical_network_interfaces"></span><span id="LOGICAL_NETWORK_INTERFACES"></span>Interfaces de rede lógica</span><span class="sxs-lookup"><span data-stu-id="ea296-114"><span id="Logical_Network_Interfaces"></span><span id="logical_network_interfaces"></span><span id="LOGICAL_NETWORK_INTERFACES"></span>Logical Network Interfaces</span></span>
</dt> <dd>

<span data-ttu-id="ea296-115">Para cada rede à qual um computador está conectado, a NLA fornece um *adaptadorname* que identifica exclusivamente uma interface física, como uma NIC, ou uma interface lógica, como uma conexão RAS.</span><span class="sxs-lookup"><span data-stu-id="ea296-115">For each network to which a computer is attached, NLA supplies an *AdapterName* that uniquely identifies a physical interface such as a NIC, or a logical interface such as a RAS connection.</span></span> <span data-ttu-id="ea296-116">O Adaptadorname pode ser usado com funções disponíveis na API do auxiliar de IP para obter características de interface adicionais.</span><span class="sxs-lookup"><span data-stu-id="ea296-116">The AdapterName can then be used with functions available in the IP Helper API to obtain further interface characteristics.</span></span>

</dd> </dl>

<span data-ttu-id="ea296-117">A NLA implementa a rede lógica como uma classe de serviço, com uma GUID de classe e propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="ea296-117">NLA implements the logical network as a service class, with an associated class GUID and properties.</span></span> <span data-ttu-id="ea296-118">Cada rede lógica para a qual a NLA retorna informações é uma instância dessa classe de serviço.</span><span class="sxs-lookup"><span data-stu-id="ea296-118">Each logical network for which NLA returns information is an instance of that service class.</span></span>

 

 



