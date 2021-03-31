---
title: A função do Gerenciador de lista de rede
description: A função do Gerenciador de lista de rede
ms.assetid: 056d7b0f-5ff7-4b87-8bfe-d4e2018ee638
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3976cdee7a8fa93a7c0dc883f25d65c2e4ae6e6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103823030"
---
# <a name="the-role-of-network-list-manager"></a><span data-ttu-id="f44f8-103">A função do Gerenciador de lista de rede</span><span class="sxs-lookup"><span data-stu-id="f44f8-103">The Role of Network List Manager</span></span>

<span data-ttu-id="f44f8-104">Antes do Windows XP e do Windows Server 2003, os aplicativos eram obrigados a chamar várias APIs não relacionadas para obter dados sobre atributos de rede, como o endereço IP, o controlador de domínio ou o DNS (sistema de nomes de domínio).</span><span class="sxs-lookup"><span data-stu-id="f44f8-104">Prior to Windows XP and Windows Server 2003, applications were required to call a number of unrelated APIs to obtain data about network attributes such as the IP address, the domain controller, or the Domain Name System (DNS).</span></span> <span data-ttu-id="f44f8-105">A partir do Windows XP e do Windows Server 2003, a API Winsock de reconhecimento de local de rede apresentou um conjunto limitado de funcionalidades de local de rede.</span><span class="sxs-lookup"><span data-stu-id="f44f8-105">Starting with Windows XP and Windows Server 2003, the Network Location Awareness Winsock API featured a limited set of network location functionality.</span></span> <span data-ttu-id="f44f8-106">No Windows Server 2008 e no Windows Vista, o serviço de reconhecimento de rede captura os atributos de rede em um local e permite que os aplicativos consultem e recuperem redes e atributos específicos.</span><span class="sxs-lookup"><span data-stu-id="f44f8-106">In Windows Server 2008 and Windows Vista, the Network Awareness service captures the network attributes in one location and allows applications to query and retrieve specific networks and attributes.</span></span> <span data-ttu-id="f44f8-107">O Gerenciador de lista de rede substitui a funcionalidade da API do Winsock anterior (disponível como um provedor de espaço para nome do Winsock) enquanto mantém a compatibilidade com aplicativos mais antigos usando a API do Winsock.</span><span class="sxs-lookup"><span data-stu-id="f44f8-107">Network List Manager replaces the functionality of the previous Winsock API (available as a Winsock Name Space Provider) while maintaining compatibility with older applications using the Winsock API.</span></span>

 

 




