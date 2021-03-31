---
title: A MIB (base de informações de gerenciamento) SNMP
description: Uma MIB (base de informações de gerenciamento) descreve um conjunto de objetos gerenciados. Um aplicativo de console de gerenciamento SNMP pode manipular os objetos em um computador específico se o serviço SNMP tiver uma DLL de agente de extensão que dá suporte à MIB.
ms.assetid: 684200b6-a5e4-42bb-8a01-fcb6100967c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ba4612c026aa5a3a1a1574556f58207bad08e06
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635344"
---
# <a name="the-snmp-management-information-base-mib"></a><span data-ttu-id="dc56c-104">A MIB (base de informações de gerenciamento) SNMP</span><span class="sxs-lookup"><span data-stu-id="dc56c-104">The SNMP Management Information Base (MIB)</span></span>

<span data-ttu-id="dc56c-105">Uma MIB (base de informações de gerenciamento) descreve um conjunto de objetos gerenciados.</span><span class="sxs-lookup"><span data-stu-id="dc56c-105">A Management Information Base (MIB) describes a set of managed objects.</span></span> <span data-ttu-id="dc56c-106">Um aplicativo de console de gerenciamento SNMP pode manipular os objetos em um computador específico se o serviço SNMP tiver uma DLL de agente de extensão que dá suporte à MIB.</span><span class="sxs-lookup"><span data-stu-id="dc56c-106">An SNMP management console application can manipulate the objects on a specific computer if the SNMP service has an extension agent DLL that supports the MIB.</span></span>

<span data-ttu-id="dc56c-107">Cada objeto gerenciado em uma MIB tem um identificador exclusivo.</span><span class="sxs-lookup"><span data-stu-id="dc56c-107">Each managed object in a MIB has a unique identifier.</span></span> <span data-ttu-id="dc56c-108">O identificador inclui o tipo do objeto (como contador, Cadeia de caracteres, medidor ou endereço), o nível de acesso do objeto (como leitura ou leitura/gravação), restrições de tamanho e informações de intervalo.</span><span class="sxs-lookup"><span data-stu-id="dc56c-108">The identifier includes the object's type (such as counter, string, gauge, or address), the object's access level (such as read or read/write), size restrictions, and range information.</span></span>

<span data-ttu-id="dc56c-109">A tabela a seguir contém uma lista parcial das MIBs que acompanham o sistema.</span><span class="sxs-lookup"><span data-stu-id="dc56c-109">The following table contains a partial list of the MIBs that ship with the system.</span></span> <span data-ttu-id="dc56c-110">Eles são instalados com o serviço SNMP no diretório% systemroot% \\ System32.</span><span class="sxs-lookup"><span data-stu-id="dc56c-110">They are installed with the SNMP service in the %systemroot%\\system32 directory.</span></span> <span data-ttu-id="dc56c-111">Para obter uma lista completa de MIBs, consulte o Windows Resource Kit.</span><span class="sxs-lookup"><span data-stu-id="dc56c-111">For a complete listing of MIBs, refer to the Windows Resource Kit.</span></span>



| <span data-ttu-id="dc56c-112">MIB</span><span class="sxs-lookup"><span data-stu-id="dc56c-112">MIB</span></span>         | <span data-ttu-id="dc56c-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="dc56c-113">Description</span></span>                                                                                                                                      |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc56c-114">DHCP. MIB</span><span class="sxs-lookup"><span data-stu-id="dc56c-114">DHCP.MIB</span></span>    | <span data-ttu-id="dc56c-115">MIB definida pela Microsoft que contém tipos de objeto para monitorar o tráfego de rede entre hosts remotos e servidores DHCP</span><span class="sxs-lookup"><span data-stu-id="dc56c-115">Microsoft-defined MIB that contains object types for monitoring the network traffic between remote hosts and DHCP servers</span></span>                        |
| <span data-ttu-id="dc56c-116">HOSTMIB. MIB</span><span class="sxs-lookup"><span data-stu-id="dc56c-116">HOSTMIB.MIB</span></span> | <span data-ttu-id="dc56c-117">Contém tipos de objeto para monitorar e gerenciar recursos de host</span><span class="sxs-lookup"><span data-stu-id="dc56c-117">Contains object types for monitoring and managing host resources</span></span>                                                                                 |
| <span data-ttu-id="dc56c-118">LMMIB2. MIB</span><span class="sxs-lookup"><span data-stu-id="dc56c-118">LMMIB2.MIB</span></span>  | <span data-ttu-id="dc56c-119">Abrange serviços de estação de trabalho e servidor</span><span class="sxs-lookup"><span data-stu-id="dc56c-119">Covers workstation and server services</span></span>                                                                                                           |
| <span data-ttu-id="dc56c-120">MIB \_ II. MIB</span><span class="sxs-lookup"><span data-stu-id="dc56c-120">MIB\_II.MIB</span></span> | <span data-ttu-id="dc56c-121">Contém a MIB-II (base de informações de gerenciamento), que fornece uma arquitetura e um sistema simples e viável para o gerenciamento de Internets baseadas em TCP/IP</span><span class="sxs-lookup"><span data-stu-id="dc56c-121">Contains the Management Information Base (MIB-II), which provides a simple, workable architecture and system for managing TCP/IP-based internets</span></span> |
| <span data-ttu-id="dc56c-122">WINS. MIB</span><span class="sxs-lookup"><span data-stu-id="dc56c-122">WINS.MIB</span></span>    | <span data-ttu-id="dc56c-123">MIB definida pela Microsoft para o serviço de cadastramento na Internet do Windows (WINS)</span><span class="sxs-lookup"><span data-stu-id="dc56c-123">Microsoft-defined MIB for the Windows Internet Name Service (WINS)</span></span>                                                                               |



 

<span data-ttu-id="dc56c-124">**Windows NT:** Normalmente, você pode copiar uma MIB do agente de extensão SNMP que dá suporte à MIB específica.</span><span class="sxs-lookup"><span data-stu-id="dc56c-124">**Windows NT:** Typically, you can copy a MIB from the SNMP extension agent that supports the particular MIB.</span></span> <span data-ttu-id="dc56c-125">Alguns MIBs adicionais estão disponíveis com o Windows NT 4,0 Resource Kit.</span><span class="sxs-lookup"><span data-stu-id="dc56c-125">Some additional MIBs are available with the Windows NT 4.0 Resource Kit.</span></span>

<span data-ttu-id="dc56c-126">As DLLs do agente de extensão para MIB-II, LAN Manager MIB-II e os recursos de host MIB são instalados com o serviço SNMP.</span><span class="sxs-lookup"><span data-stu-id="dc56c-126">The extension agent DLLs for MIB-II, LAN Manager MIB-II, and the Host Resources MIB are installed with the SNMP service.</span></span> <span data-ttu-id="dc56c-127">As DLLs do agente de extensão para os outros MIBs são instaladas quando seus respectivos serviços são instalados.</span><span class="sxs-lookup"><span data-stu-id="dc56c-127">The extension agent DLLs for the other MIBs are installed when their respective services are installed.</span></span> <span data-ttu-id="dc56c-128">No momento da inicialização do serviço, o serviço SNMP carrega todas as DLLs do agente de extensão listadas no registro.</span><span class="sxs-lookup"><span data-stu-id="dc56c-128">At service startup time, the SNMP service loads all of the extension agent DLLs that are listed in the registry.</span></span>

<span data-ttu-id="dc56c-129">Os usuários podem adicionar outras DLLs de agente de extensão que implementam MIBs adicionais.</span><span class="sxs-lookup"><span data-stu-id="dc56c-129">Users can add other extension agent DLLs that implement additional MIBs.</span></span> <span data-ttu-id="dc56c-130">Para fazer isso, eles devem adicionar uma entrada de registro para a nova DLL no serviço SNMP.</span><span class="sxs-lookup"><span data-stu-id="dc56c-130">To do this, they must add a registry entry for the new DLL under the SNMP service.</span></span> <span data-ttu-id="dc56c-131">Eles também devem registrar a nova MIB com o aplicativo de console de gerenciamento SNMP.</span><span class="sxs-lookup"><span data-stu-id="dc56c-131">They must also register the new MIB with the SNMP management console application.</span></span> <span data-ttu-id="dc56c-132">Para obter mais informações, consulte a documentação incluída no seu aplicativo de console de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="dc56c-132">For more information, see the documentation included with your management console application.</span></span>

<span data-ttu-id="dc56c-133">Para obter mais informações, consulte [MIB Name Tree](mib-name-tree.md).</span><span class="sxs-lookup"><span data-stu-id="dc56c-133">For more information, see [MIB Name Tree](mib-name-tree.md).</span></span>

 

 




