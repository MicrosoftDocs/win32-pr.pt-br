---
description: O exemplo de script neste tópico mostra como usar o WUA (agente de Windows Update) para verificar, baixar e instalar uma atualização específica. A atualização pode ser especificada por seu título.
ms.assetid: 4a5bb920-fc51-48a0-8f66-bb2fcc72589f
title: Pesquisando, baixando e instalando atualizações específicas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aadd7903303356c3937f41e44aa7a47e71192409
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296410"
---
# <a name="searching-downloading-and-installing-specific-updates"></a><span data-ttu-id="7d601-104">Pesquisando, baixando e instalando atualizações específicas</span><span class="sxs-lookup"><span data-stu-id="7d601-104">Searching, Downloading, and Installing Specific Updates</span></span>

<span data-ttu-id="7d601-105">O exemplo de script neste tópico mostra como usar o WUA (agente de Windows Update) para verificar, baixar e instalar uma atualização específica.</span><span class="sxs-lookup"><span data-stu-id="7d601-105">The scripting sample in this topic shows you how to use the Windows Update Agent (WUA) to scan, download, and install a specific update.</span></span> <span data-ttu-id="7d601-106">A atualização pode ser especificada por seu título.</span><span class="sxs-lookup"><span data-stu-id="7d601-106">The update can be specified by its title.</span></span>

<span data-ttu-id="7d601-107">O exemplo pesquisa uma atualização de software específica, baixa a atualização e instala a atualização.</span><span class="sxs-lookup"><span data-stu-id="7d601-107">The sample searches for a specific software update, downloads the update, and then installs the update.</span></span> <span data-ttu-id="7d601-108">Por exemplo, um usuário pode usar esse método para determinar se uma atualização de segurança crítica está instalada em um computador.</span><span class="sxs-lookup"><span data-stu-id="7d601-108">For example, a user can use this method to determine if a critical security update is installed on a computer.</span></span> <span data-ttu-id="7d601-109">Se a atualização não estiver instalada, o usuário poderá garantir que a atualização seja baixada e instalada.</span><span class="sxs-lookup"><span data-stu-id="7d601-109">If the update isn't installed, the user can ensure that the update is downloaded and installed.</span></span> <span data-ttu-id="7d601-110">O usuário também pode garantir que eles sejam notificados sobre o status da instalação.</span><span class="sxs-lookup"><span data-stu-id="7d601-110">The user can also ensure that they are notified about the status of the installation.</span></span>

<span data-ttu-id="7d601-111">A atualização de exemplo é identificada pelo título de atualização na [**Propriedade Title de IUpdate**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_title).</span><span class="sxs-lookup"><span data-stu-id="7d601-111">The sample update is identified by the update title in [**Title Property of IUpdate**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_title).</span></span> <span data-ttu-id="7d601-112">O título da atualização sugerido neste exemplo é "atualização para o Windows Rights Management Client 1,0".</span><span class="sxs-lookup"><span data-stu-id="7d601-112">The title of the update that is suggested in this sample is "Update for Windows Rights Management client 1.0."</span></span>

> [!Note]  
> <span data-ttu-id="7d601-113">Para obter informações sobre como Pesquisar, baixar e instalar todas as atualizações que se aplicam a um aplicativo específico, consulte [pesquisando, baixando e instalando atualizações](searching--downloading--and-installing-updates.md).</span><span class="sxs-lookup"><span data-stu-id="7d601-113">For info about how to search, download, and install all the updates that apply to a specific application, see [Searching, Downloading, and Installing Updates](searching--downloading--and-installing-updates.md).</span></span>

 

<span data-ttu-id="7d601-114">Antes de tentar executar este exemplo, observe o seguinte:</span><span class="sxs-lookup"><span data-stu-id="7d601-114">Before you attempt to run this sample, note the following:</span></span>

-   <span data-ttu-id="7d601-115">O WUA deve estar instalado no computador.</span><span class="sxs-lookup"><span data-stu-id="7d601-115">WUA must be installed on the computer.</span></span> <span data-ttu-id="7d601-116">Para obter mais informações sobre como determinar a versão do WUA que está instalada, consulte [determinando a versão atual do WUA](determining-the-current-version-of-wua.md).</span><span class="sxs-lookup"><span data-stu-id="7d601-116">For more info about how to determine the version of WUA that is installed, see [Determining the Current Version of WUA](determining-the-current-version-of-wua.md).</span></span>
-   <span data-ttu-id="7d601-117">O exemplo não fornece sua própria interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="7d601-117">The sample doesn't provide its own user interface.</span></span> <span data-ttu-id="7d601-118">O WUA solicita que o usuário reinicie o computador se uma atualização exigir uma reinicialização.</span><span class="sxs-lookup"><span data-stu-id="7d601-118">WUA prompts the user to restart the computer if an update requires a restart.</span></span>
-   <span data-ttu-id="7d601-119">O exemplo pode baixar atualizações somente do WUA.</span><span class="sxs-lookup"><span data-stu-id="7d601-119">The sample can download updates only from WUA.</span></span> <span data-ttu-id="7d601-120">Ele não pode baixar atualizações de um servidor SUS (Software Update Services) 1,0.</span><span class="sxs-lookup"><span data-stu-id="7d601-120">It can't download updates from a Software Update Services (SUS) 1.0 server.</span></span>
-   <span data-ttu-id="7d601-121">A execução deste exemplo requer o WSH (Windows Script Host).</span><span class="sxs-lookup"><span data-stu-id="7d601-121">Running this sample requires Windows Script Host (WSH).</span></span> <span data-ttu-id="7d601-122">Para obter mais informações sobre o WSH, consulte a seção WSH do kit de desenvolvimento de software de plataforma (SDK).</span><span class="sxs-lookup"><span data-stu-id="7d601-122">For more info about WSH, see the WSH section of the Platform Software Development Kit (SDK).</span></span> <span data-ttu-id="7d601-123">Se o exemplo for copiado para um arquivo chamado WUA \_SpecificUpdate.vbs, você poderá executá-lo abrindo uma janela de prompt de comando e digitando este comando: **cscript WUA \_SpecificUpdate.vbs**</span><span class="sxs-lookup"><span data-stu-id="7d601-123">If the sample is copied to a file named WUA\_SpecificUpdate.vbs, you can run it by opening a Command Prompt window and by typing this command: **cscript WUA\_SpecificUpdate.vbs**</span></span>  
    

## <a name="example"></a><span data-ttu-id="7d601-124">Exemplo</span><span class="sxs-lookup"><span data-stu-id="7d601-124">Example</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7d601-125">Esse script destina-se a demonstrar o uso das APIs do agente de Windows Update e fornece um exemplo de como os desenvolvedores podem usar essas APIs para resolver problemas.</span><span class="sxs-lookup"><span data-stu-id="7d601-125">This script is intended to demonstrate the use of the Windows Update Agent APIs, and provide an example of how developers can use these APIs to solve problems.</span></span> <span data-ttu-id="7d601-126">Esse script não se destina como código de produção e o próprio script não tem suporte da Microsoft (embora haja suporte para as APIs de agente de Windows Update subjacentes).</span><span class="sxs-lookup"><span data-stu-id="7d601-126">This script is not intended as production code, and the script itself is not supported by Microsoft (though the underlying Windows Update Agent APIs are supported).</span></span>

 


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



 

 



