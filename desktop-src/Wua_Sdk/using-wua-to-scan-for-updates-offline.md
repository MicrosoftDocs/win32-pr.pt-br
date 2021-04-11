---
description: O WUA (Windows Update Agent) pode ser usado para verificar se há atualizações de segurança nos computadores sem se conectar ao Windows Update ou a um servidor Windows Server Update Services (WSUS), que permite que os computadores que não estão conectados à Internet sejam verificados quanto a atualizações de segurança. A verificação offline de atualizações requer o download de um arquivo assinado, Wsusscn2.cab, da Windows Update.
ms.assetid: 452b53af-0f7b-435e-bf12-dd9d84cbd564
title: Usando o WUA para verificar se há atualizações offline
ms.topic: article
ms.date: 07/23/2020
ms.openlocfilehash: 242ff3655f4ab469d8d768a94f8dc8e529e0da74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296193"
---
# <a name="using-wua-to-scan-for-updates-offline"></a>Usando o WUA para verificar se há atualizações offline

O WUA (Windows Update Agent) pode ser usado para verificar se há atualizações de segurança nos computadores sem se conectar ao Windows Update ou a um servidor Windows Server Update Services (WSUS), que permite que os computadores que não estão conectados à Internet sejam verificados quanto a atualizações de segurança.

A verificação offline de atualizações requer o download de um arquivo assinado, Wsusscn2.cab, da Windows Update.

O arquivo de Wsusscn2.cab é um arquivo de gabinete assinado pela Microsoft. Este arquivo contém informações sobre atualizações relacionadas à segurança que são publicadas pela Microsoft. Os computadores que não estão conectados à Internet podem ser verificados para ver se essas atualizações relacionadas à segurança estão presentes ou obrigatórias. O arquivo de Wsusscn2.cab não contém as atualizações de segurança em si, portanto você deve obter e instalar todas as atualizações necessárias relacionadas à segurança por meio de outros meios. As novas versões do arquivo de Wsusscn2.cab são liberadas periodicamente, pois as atualizações relacionadas à segurança são liberadas, removidas ou revisadas no site do Windows Update. O arquivo de Wsusscn2.cab mais recente está disponível para download no seguinte local: [baixar Wsusscn2.cab](http://download.windowsupdate.com/microsoftupdate/v6/wsusscan/wsusscn2.cab)

Depois de baixar a Wsusscn2.cab mais recente, o arquivo pode ser fornecido para o método [**AddScanPackageService**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-addscanpackageservice) e a API do WUA pode ser usada para Pesquisar atualizações de segurança no computador offline. O WUA valida que a Wsusscn2.cab é assinada por um certificado da Microsoft válido antes de executar uma verificação offline.

> [!NOTE]
> De acordo com nossa [iniciativa de substituição SHA-1](https://aka.ms/sha1deprecation), o arquivo de Wsusscn2.cab não é mais assinado duplo usando o SHA-1 e o pacote SHA-2 de algoritmos de hash (especificamente SHA-256). Este arquivo agora está assinado usando somente SHA-256. Os administradores que verificam assinaturas digitais neste arquivo agora devem esperar apenas assinaturas do SHA-256.

## <a name="example"></a>Exemplo

O exemplo a seguir usa o arquivo Wsusscn2.cab para verificar um computador e exibe as atualizações que estão faltando.

> [!IMPORTANT]
> Esse script destina-se a demonstrar o uso das APIs do agente de Windows Update e fornece um exemplo de como os desenvolvedores podem usar essas APIs para resolver problemas. Esse script não se destina como código de produção e o próprio script não tem suporte da Microsoft (embora haja suporte para as APIs de agente de Windows Update subjacentes).

 


```VB
Set UpdateSession = CreateObject("Microsoft.Update.Session")
Set UpdateServiceManager = CreateObject("Microsoft.Update.ServiceManager")
Set UpdateService = UpdateServiceManager.AddScanPackageService("Offline Sync Service", "c:\wsusscn2.cab", 1)
Set UpdateSearcher = UpdateSession.CreateUpdateSearcher()

WScript.Echo "Searching for updates..." & vbCRLF

UpdateSearcher.ServerSelection = 3 ' ssOthers

UpdateSearcher.ServiceID = UpdateService.ServiceID

Set SearchResult = UpdateSearcher.Search("IsInstalled=0")

Set Updates = SearchResult.Updates

If searchResult.Updates.Count = 0 Then
    WScript.Echo "There are no applicable updates."
    WScript.Quit
End If

WScript.Echo "List of applicable items on the machine when using wssuscan.cab:" & vbCRLF

For I = 0 to searchResult.Updates.Count-1
    Set update = searchResult.Updates.Item(I)
    WScript.Echo I + 1 & "> " & update.Title
Next

WScript.Quit
```



 

 



