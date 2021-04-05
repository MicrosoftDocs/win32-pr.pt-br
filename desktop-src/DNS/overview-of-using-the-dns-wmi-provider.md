---
title: Visão geral do uso do provedor WMI de DNS
description: As etapas gerais a seguir o ajudarão a criar seu próprio script ou programa que usa o provedor WMI de DNS.
ms.assetid: d9d64bda-0564-4074-9f0a-a249c7315042
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9188e14e0a0b1f73380434be0d4298b0748da12f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005802"
---
# <a name="overview-of-using-the-dns-wmi-provider"></a><span data-ttu-id="1abf9-103">Visão geral do uso do provedor WMI de DNS</span><span class="sxs-lookup"><span data-stu-id="1abf9-103">Overview of Using the DNS WMI Provider</span></span>

<span data-ttu-id="1abf9-104">As etapas gerais a seguir o ajudarão a criar seu próprio script ou programa que usa o provedor WMI de DNS.</span><span class="sxs-lookup"><span data-stu-id="1abf9-104">The following general steps get you started in creating your own script or program that makes use of the DNS WMI Provider.</span></span>

<span data-ttu-id="1abf9-105">**Para criar um script ou programa usando o provedor WMI de DNS**</span><span class="sxs-lookup"><span data-stu-id="1abf9-105">**To create a script or program using the DNS WMI Provider**</span></span>

1.  <span data-ttu-id="1abf9-106">Conecte-se ao provedor WMI de DNS.</span><span class="sxs-lookup"><span data-stu-id="1abf9-106">Connect to the DNS WMI Provider.</span></span>
    ```VB
    Set objLocator = CreateObject("WbemScripting.SWbemLocator")

    'Connect to the namespace which is either local or remote
    Set objService = objLocator.ConnectServer (strServer, strNameSpace, _
                                                                                                                                                                                strUserName, strPassword)
    ```

    

    > [!Note]  
    > <span data-ttu-id="1abf9-107">O espaço de nome para o provedor WMI de DNS será sempre "root \\ MicrosoftDNS".</span><span class="sxs-lookup"><span data-stu-id="1abf9-107">The name space for the DNS WMI Provider will always be "root\\microsoftdns".</span></span>

     

2.  <span data-ttu-id="1abf9-108">Obtenha uma instância do servidor DNS.</span><span class="sxs-lookup"><span data-stu-id="1abf9-108">Get a DNS Server instance.</span></span>
    ```VB
    set objServer = objService.Get("MicrosoftDNS_Server.name="".""")
    ```

    

3.  <span data-ttu-id="1abf9-109">Dependendo da ação de tipo que você deseja executar, obtenha uma zona DNS ou uma instância de registro.</span><span class="sxs-lookup"><span data-stu-id="1abf9-109">Depending on the type action you want to perform, get a DNS zone or record instance.</span></span>
    ```VB
    Set objDNSSet = objService.Get("MicrosoftDNS_ZONE")
    Set objDNSset = objService.Get("MicrosoftDNS_Zone.ContainerName=""" _
                                                                    & strZoneArray(0) & """,DnsServerName=""" & _ 
                    objServer.Name & """,Name=""" & _
                    strZoneArray(0) & """")
    ```

    

4.  <span data-ttu-id="1abf9-110">Execute as ações desejadas:</span><span class="sxs-lookup"><span data-stu-id="1abf9-110">Perform the desired actions:</span></span>
    -   <span data-ttu-id="1abf9-111">Executar um método</span><span class="sxs-lookup"><span data-stu-id="1abf9-111">Execute a method</span></span>
    -   <span data-ttu-id="1abf9-112">Exibir uma propriedade</span><span class="sxs-lookup"><span data-stu-id="1abf9-112">Display a property</span></span>
    -   <span data-ttu-id="1abf9-113">Modificar uma propriedade (deve ter acesso de leitura/gravação)</span><span class="sxs-lookup"><span data-stu-id="1abf9-113">Modify a property (must have Read/Write access)</span></span>

 

 




