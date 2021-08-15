---
description: Windows O WUA (Agente de Atualização) pode ser usado para verificar os computadores em busca de atualizações de segurança sem se conectar ao Windows Update ou a um servidor do WSUS (Windows Server Update Services), o que permite que computadores que não estão conectados à Internet sejam verificados quanto a atualizações de segurança. A verificação offline de atualizações requer o download de um arquivo assinado, Wsusscn2.cab, do Windows Update.
ms.assetid: 452b53af-0f7b-435e-bf12-dd9d84cbd564
title: Usando WUA para verificar se há atualizações offline
ms.topic: article
ms.date: 07/23/2020
ms.openlocfilehash: 54da554eca4e2320ecb8644ffb7ae274ed929d897f6e17e28b271a682f9fdc59
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119410756"
---
# <a name="using-wua-to-scan-for-updates-offline"></a>Usando WUA para verificar se há atualizações offline

Windows O WUA (Agente de Atualização) pode ser usado para verificar os computadores em busca de atualizações de segurança sem se conectar ao Windows Update ou a um servidor do WSUS (Windows Server Update Services), o que permite que computadores que não estão conectados à Internet sejam verificados quanto a atualizações de segurança.

A verificação offline de atualizações requer o download de um arquivo assinado, Wsusscn2.cab, do Windows Update.

O Wsusscn2.cab arquivo é um arquivo de gabinete assinado pela Microsoft. Esse arquivo contém informações sobre atualizações relacionadas à segurança publicadas pela Microsoft. Computadores que não estão conectados à Internet podem ser verificados para ver se essas atualizações relacionadas à segurança estão presentes ou necessárias. O Wsusscn2.cab arquivo não contém as atualizações de segurança em si, portanto, você deve obter e instalar as atualizações necessárias relacionadas à segurança por outros meios. Novas versões do arquivo Wsusscn2.cab são lançadas periodicamente à medida que as atualizações relacionadas à segurança são liberadas, removidas ou revisadas no site Windows Update. O arquivo Wsusscn2.cab mais recente está disponível para download no seguinte local: [Baixar Wsusscn2.cab](http://download.windowsupdate.com/microsoftupdate/v6/wsusscan/wsusscn2.cab)

Depois de baixar a versão Wsusscn2.cab, o arquivo pode ser fornecido para o método [**AddScanPackageService**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-addscanpackageservice) e a API WUA pode ser usada para pesquisar atualizações de segurança no computador offline. O WUA valida que o Wsusscn2.cab é assinado por um certificado válido da Microsoft antes de executar uma verificação offline.

> [!NOTE]
> De acordo com nossa iniciativa de preterição [SHA-1,](https://aka.ms/sha1deprecation)o arquivo Wsusscn2.cab não é mais assinado duas vezes usando SHA-1 e o pacote SHA-2 de algoritmos de hash (especificamente SHA-256). Esse arquivo agora é assinado usando apenas SHA-256. Os administradores que verificam assinaturas digitais nesse arquivo agora devem esperar apenas assinaturas SHA-256 únicas.

## <a name="example"></a>Exemplo

O exemplo a seguir usa o arquivo Wsusscn2.cab para verificar um computador e exibe as atualizações ausentes.

> [!IMPORTANT]
> Esse script destina-se a demonstrar o uso das APIs Windows Update Agent e fornecer um exemplo de como os desenvolvedores podem usar essas APIs para resolver problemas. Esse script não se destina ao código de produção e o próprio script não tem suporte da Microsoft (embora as APIs do Agente de Atualização Windows subjacentes sejam suportadas).

 


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



 

 



