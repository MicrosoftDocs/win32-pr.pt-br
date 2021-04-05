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
# <a name="overview-of-using-the-dns-wmi-provider"></a>Visão geral do uso do provedor WMI de DNS

As etapas gerais a seguir o ajudarão a criar seu próprio script ou programa que usa o provedor WMI de DNS.

**Para criar um script ou programa usando o provedor WMI de DNS**

1.  Conecte-se ao provedor WMI de DNS.
    ```VB
    Set objLocator = CreateObject("WbemScripting.SWbemLocator")

    'Connect to the namespace which is either local or remote
    Set objService = objLocator.ConnectServer (strServer, strNameSpace, _
                                                                                                                                                                                strUserName, strPassword)
    ```

    

    > [!Note]  
    > O espaço de nome para o provedor WMI de DNS será sempre "root \\ MicrosoftDNS".

     

2.  Obtenha uma instância do servidor DNS.
    ```VB
    set objServer = objService.Get("MicrosoftDNS_Server.name="".""")
    ```

    

3.  Dependendo da ação de tipo que você deseja executar, obtenha uma zona DNS ou uma instância de registro.
    ```VB
    Set objDNSSet = objService.Get("MicrosoftDNS_ZONE")
    Set objDNSset = objService.Get("MicrosoftDNS_Zone.ContainerName=""" _
                                                                    & strZoneArray(0) & """,DnsServerName=""" & _ 
                    objServer.Name & """,Name=""" & _
                    strZoneArray(0) & """")
    ```

    

4.  Execute as ações desejadas:
    -   Executar um método
    -   Exibir uma propriedade
    -   Modificar uma propriedade (deve ter acesso de leitura/gravação)

 

 




