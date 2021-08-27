---
description: o exemplo de script neste tópico mostra como usar o WUA (agente de Windows Update) para verificar, baixar e instalar uma atualização específica. A atualização pode ser especificada por seu título.
ms.assetid: 4a5bb920-fc51-48a0-8f66-bb2fcc72589f
title: Pesquisando, baixando e instalando atualizações específicas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70c2da9569ed6fe34b18264ee59e91965877d63e422ae20e25fc27fbc025e812
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071276"
---
# <a name="searching-downloading-and-installing-specific-updates"></a>Pesquisando, baixando e instalando atualizações específicas

o exemplo de script neste tópico mostra como usar o WUA (agente de Windows Update) para verificar, baixar e instalar uma atualização específica. A atualização pode ser especificada por seu título.

O exemplo pesquisa uma atualização de software específica, baixa a atualização e instala a atualização. Por exemplo, um usuário pode usar esse método para determinar se uma atualização de segurança crítica está instalada em um computador. Se a atualização não estiver instalada, o usuário poderá garantir que a atualização seja baixada e instalada. O usuário também pode garantir que eles sejam notificados sobre o status da instalação.

A atualização de exemplo é identificada pelo título de atualização na [**Propriedade Title de IUpdate**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_title). o título da atualização sugerido neste exemplo é "update for Windows Rights Management client 1,0".

> [!Note]  
> Para obter informações sobre como Pesquisar, baixar e instalar todas as atualizações que se aplicam a um aplicativo específico, consulte [pesquisando, baixando e instalando atualizações](searching--downloading--and-installing-updates.md).

 

Antes de tentar executar este exemplo, observe o seguinte:

-   O WUA deve estar instalado no computador. Para obter mais informações sobre como determinar a versão do WUA que está instalada, consulte [determinando a versão atual do WUA](determining-the-current-version-of-wua.md).
-   O exemplo não fornece sua própria interface do usuário. O WUA solicita que o usuário reinicie o computador se uma atualização exigir uma reinicialização.
-   O exemplo pode baixar atualizações somente do WUA. Ele não pode baixar atualizações de um servidor SUS (Software Update Services) 1,0.
-   a execução deste exemplo requer o Host de Script do Windows (WSH). Para obter mais informações sobre o WSH, consulte a seção WSH do kit de desenvolvimento de software de plataforma (SDK). Se o exemplo for copiado para um arquivo chamado WUA \_SpecificUpdate.vbs, você poderá executá-lo abrindo uma janela de prompt de comando e digitando este comando: **cscript WUA \_SpecificUpdate.vbs**  
    

## <a name="example"></a>Exemplo

> [!IMPORTANT]
> esse script destina-se a demonstrar o uso das apis do agente de Windows Update e fornece um exemplo de como os desenvolvedores podem usar essas apis para resolver problemas. esse script não se destina como código de produção e o próprio script não tem suporte da Microsoft (embora haja suporte para as APIs de agente de Windows Update subjacentes).

 


```VB
Set updateSession = CreateObject("Microsoft.Update.Session")
updateSession.ClientApplicationID = "MSDN Sample Script"

'Get update title to search for
WScript.Echo "Enter the title of the update: " & _
"(for example, Update for Windows Rights Management client 1.0)"
updateTitle = WScript.StdIn.Readline

WScript.Echo vbCRLF & "Searching for: " & updateTitle & "..."

Set updateSearcher = updateSession.CreateupdateSearcher()

'Search for all software updates, already installed and not installed
Set searchResult = _
updateSearcher.Search("Type='Software'")

Set updateToInstall = CreateObject("Microsoft.Update.UpdateColl")

updateIsApplicable = False

'Cycle through search results to look for the update title
For i = 0 To searchResult.Updates.Count-1
   Set update = searchResult.Updates.Item(i)
   If UCase(update.Title) = UCase(updateTitle) Then
   'Update in list of applicable updates 
   'Determine if it is already installed or not
      If update.IsInstalled = False Then
         WScript.Echo vbCRLF & _
         "Result: Update applicable, not installed."
         updateIsApplicable = True
         updateToInstall.Add(update)
      Else 
         'Update is installed so notify user and quit
         WScript.Echo vbCRLF & _
         "Result: Update applicable, already installed."
         updateIsApplicable = True
         WScript.Quit 
      End If
   End If 
Next

If updateIsApplicable = False Then
   WScript.Echo "Result: Update is not applicable to this machine."
   WScript.Quit
End If

WScript.Echo vbCRLF & "Would you like to install now? (Y/N)"
stdInput = WScript.StdIn.Readline
 
If (strInput = "N" or strInput = "n") Then 
   WScript.Quit
ElseIf  (stdInput = "Y" OR stdInput = "y") Then
   'Download update
   Set downloader = updateSession.CreateUpdateDownloader() 
   downloader.Updates = updateToInstall
   WScript.Echo vbCRLF & "Downloading..."
   Set downloadResult = downloader.Download()
   WScript.Echo "Download Result: " & downloadResult.ResultCode
  
   'Install Update
   Set installer = updateSession.CreateUpdateInstaller()
   WScript.Echo vbCRLF & "Installing..."
   installer.Updates = updateToInstall
   Set installationResult = installer.Install()
  
   'Output the result of the installation
   WScript.Echo "Installation Result: " & _
   installationResult.ResultCode
   WScript.Echo "Reboot Required: " & _
   installationResult.RebootRequired 
End If
```



 

 



