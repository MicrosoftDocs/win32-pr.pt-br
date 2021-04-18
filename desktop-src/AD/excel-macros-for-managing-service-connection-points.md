---
title: Macros do Excel para gerenciar pontos de conexão de serviço
description: Os pontos de conexão de serviço podem ser gerenciados usando macros simples do Excel.
ms.assetid: da8a7363-6814-4c26-b259-53e6f6ba98cd
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 69bc3561962b063c9128d46934d3cb87b84e0a24
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105753042"
---
# <a name="excel-macros-for-managing-service-connection-points"></a><span data-ttu-id="0b5e9-103">Macros do Excel para gerenciar pontos de conexão de serviço</span><span class="sxs-lookup"><span data-stu-id="0b5e9-103">Excel Macros for Managing Service Connection Points</span></span>

<span data-ttu-id="0b5e9-104">Os pontos de conexão de serviço podem ser gerenciados usando macros simples do Excel.</span><span class="sxs-lookup"><span data-stu-id="0b5e9-104">Service Connection Points can be managed using simple Excel Macros.</span></span>

<span data-ttu-id="0b5e9-105">A macro do Excel a seguir mostra os requisitos mínimos para a criação de um novo ponto de conexão de serviço.</span><span class="sxs-lookup"><span data-stu-id="0b5e9-105">The following Excel Macro shows the minimum requirements for creating a new Service Connection Point.</span></span>


```VB
Option Explicit

Private Sub p_CreateExampleSCP()

    Dim oAdSysInfo As ADSystemInfo
    Set oAdSysInfo = CreateObject("ADSystemInfo")
    
    Dim objComputer As ActiveDs.IADsContainer
    Set objComputer = GetObject("LDAP://" + oAdSysInfo.ComputerName)
    
    Dim IADsSCP As ActiveDs.IADs
    Set IADsSCP = objComputer.Create("ServiceConnectionPoint", _
                                "CN=Example SCP")
    
    IADsSCP.PutEx 2, "serviceBindingInformation", _
                    Array( _
                        " - UNC connection to Service", _
                        " - WS-Man connection to service" _
                    )
                    
    IADsSCP.PutEx 2, "Keywords", _
                    Array( _
                        "KW1=A kewyrowd value" _
                    )
                    
    IADsSCP.SetInfo

End Sub
```



<span data-ttu-id="0b5e9-106">A macro do Excel a seguir mostra como excluir o ponto de conexão de serviço de exemplo.</span><span class="sxs-lookup"><span data-stu-id="0b5e9-106">The following Excel Macro shows how to delete the sample Service Connection Point.</span></span>


```VB
Option Explicit

Private Sub p_DeleteExampleScp()
    Dim oAdSysInfo As ADSystemInfo
    Set oAdSysInfo = CreateObject("ADSystemInfo")
    
    Dim objComputer As ActiveDs.IADsContainer
    Set objComputer = GetObject("LDAP://" + oAdSysInfo.ComputerName)

    objComputer.Delete "ServiceConnectionPoint", _
                        "CN=Example SCP"

End Sub
```



 

 




