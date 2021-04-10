---
description: Computadores pessoais que executam o Microsoft Windows geralmente têm várias conexões de rede, como várias placas de interface de rede (NIC) conectadas a redes diferentes, ou uma conexão de rede física e uma conexão dial-up.
ms.assetid: 73a1999d-0c19-4f9d-8e47-07f819874535
title: Provedor de serviços de reconhecimento de local de rede (NLA)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91d3b5882b63539ce0299c9d4a2d93dc17ef2576
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090368"
---
# <a name="network-location-awareness-service-provider-nla"></a><span data-ttu-id="981b4-103">Provedor de serviços de reconhecimento de local de rede (NLA)</span><span class="sxs-lookup"><span data-stu-id="981b4-103">Network Location Awareness Service Provider (NLA)</span></span>

<span data-ttu-id="981b4-104">Computadores pessoais que executam o Microsoft Windows geralmente têm várias conexões de rede, como várias placas de interface de rede (NIC) conectadas a redes diferentes, ou uma conexão de rede física e uma conexão dial-up.</span><span class="sxs-lookup"><span data-stu-id="981b4-104">Personal computers running Microsoft Windows often have numerous network connections, such as multiple network interface cards (NIC) connected to different networks, or a physical network connection and a dial-up connection.</span></span> <span data-ttu-id="981b4-105">O Windows Sockets foi capaz de enumerar as interfaces de rede disponíveis por algum tempo, mas algumas informações críticas sobre as conexões de rede estavam indisponíveis anteriormente.</span><span class="sxs-lookup"><span data-stu-id="981b4-105">Windows Sockets has been capable of enumerating available network interfaces for some time, but certain critical information about network connections was previously unavailable.</span></span> <span data-ttu-id="981b4-106">Isso inclui informações como a rede lógica à qual um computador Windows está conectado ou se várias interfaces estão conectadas à mesma rede.</span><span class="sxs-lookup"><span data-stu-id="981b4-106">This includes information such as the logical network to which a Windows computer is attached or whether multiple interfaces are connected to the same network.</span></span>

<span data-ttu-id="981b4-107">O provedor de serviços de reconhecimento de local de rede, conhecido como NLA, permite que aplicativos Windows Sockets 2 identifiquem a rede lógica à qual um computador Windows está conectado.</span><span class="sxs-lookup"><span data-stu-id="981b4-107">The Network Location Awareness service provider, commonly referred to as NLA, enables Windows Sockets 2 applications to identify the logical network to which a Windows computer is attached.</span></span> <span data-ttu-id="981b4-108">Além disso, o NLA permite que os aplicativos Windows Sockets identifiquem em qual interface de rede física um determinado aplicativo salvou informações específicas.</span><span class="sxs-lookup"><span data-stu-id="981b4-108">In addition, NLA enables Windows Sockets applications to identify to which physical network interface a given application has saved specific information.</span></span> <span data-ttu-id="981b4-109">O NLA é implementado como um provedor de serviço de resolução de nomes do Windows Sockets 2 genérico.</span><span class="sxs-lookup"><span data-stu-id="981b4-109">NLA is implemented as a generic Windows Sockets 2 Name Resolution service provider.</span></span>

 

 



