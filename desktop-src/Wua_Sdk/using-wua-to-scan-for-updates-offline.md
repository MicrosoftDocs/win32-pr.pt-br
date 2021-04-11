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
# <a name="using-wua-to-scan-for-updates-offline"></a><span data-ttu-id="31cf4-104">Usando o WUA para verificar se há atualizações offline</span><span class="sxs-lookup"><span data-stu-id="31cf4-104">Using WUA to Scan for Updates Offline</span></span>

<span data-ttu-id="31cf4-105">O WUA (Windows Update Agent) pode ser usado para verificar se há atualizações de segurança nos computadores sem se conectar ao Windows Update ou a um servidor Windows Server Update Services (WSUS), que permite que os computadores que não estão conectados à Internet sejam verificados quanto a atualizações de segurança.</span><span class="sxs-lookup"><span data-stu-id="31cf4-105">Windows Update Agent (WUA) can be used to scan computers for security updates without connecting to Windows Update or to a Windows Server Update Services (WSUS) server, which enables computers that are not connected to the Internet to be scanned for security updates.</span></span>

<span data-ttu-id="31cf4-106">A verificação offline de atualizações requer o download de um arquivo assinado, Wsusscn2.cab, da Windows Update.</span><span class="sxs-lookup"><span data-stu-id="31cf4-106">Offline scanning for updates requires the download of a signed file, Wsusscn2.cab, from Windows Update.</span></span>

<span data-ttu-id="31cf4-107">O arquivo de Wsusscn2.cab é um arquivo de gabinete assinado pela Microsoft.</span><span class="sxs-lookup"><span data-stu-id="31cf4-107">The Wsusscn2.cab file is a cabinet file that is signed by Microsoft.</span></span> <span data-ttu-id="31cf4-108">Este arquivo contém informações sobre atualizações relacionadas à segurança que são publicadas pela Microsoft.</span><span class="sxs-lookup"><span data-stu-id="31cf4-108">This file contains info about security-related updates that are published by Microsoft.</span></span> <span data-ttu-id="31cf4-109">Os computadores que não estão conectados à Internet podem ser verificados para ver se essas atualizações relacionadas à segurança estão presentes ou obrigatórias.</span><span class="sxs-lookup"><span data-stu-id="31cf4-109">Computers that aren't connected to the Internet can be scanned to see whether these security-related updates are present or required.</span></span> <span data-ttu-id="31cf4-110">O arquivo de Wsusscn2.cab não contém as atualizações de segurança em si, portanto você deve obter e instalar todas as atualizações necessárias relacionadas à segurança por meio de outros meios.</span><span class="sxs-lookup"><span data-stu-id="31cf4-110">The Wsusscn2.cab file doesn't contain the security updates themselves so you must obtain and install any needed security-related updates through other means.</span></span> <span data-ttu-id="31cf4-111">As novas versões do arquivo de Wsusscn2.cab são liberadas periodicamente, pois as atualizações relacionadas à segurança são liberadas, removidas ou revisadas no site do Windows Update.</span><span class="sxs-lookup"><span data-stu-id="31cf4-111">New versions of the Wsusscn2.cab file are released periodically as security-related updates are released, removed, or revised on the Windows Update site.</span></span> <span data-ttu-id="31cf4-112">O arquivo de Wsusscn2.cab mais recente está disponível para download no seguinte local: [baixar Wsusscn2.cab](http://download.windowsupdate.com/microsoftupdate/v6/wsusscan/wsusscn2.cab)</span><span class="sxs-lookup"><span data-stu-id="31cf4-112">The latest Wsusscn2.cab file is available for download at the following location: [Download Wsusscn2.cab](http://download.windowsupdate.com/microsoftupdate/v6/wsusscan/wsusscn2.cab)</span></span>

<span data-ttu-id="31cf4-113">Depois de baixar a Wsusscn2.cab mais recente, o arquivo pode ser fornecido para o método [**AddScanPackageService**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-addscanpackageservice) e a API do WUA pode ser usada para Pesquisar atualizações de segurança no computador offline.</span><span class="sxs-lookup"><span data-stu-id="31cf4-113">After you download the latest Wsusscn2.cab, the file can be provided to the [**AddScanPackageService**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-addscanpackageservice) method, and the WUA API can be used to search the offline computer for security updates.</span></span> <span data-ttu-id="31cf4-114">O WUA valida que a Wsusscn2.cab é assinada por um certificado da Microsoft válido antes de executar uma verificação offline.</span><span class="sxs-lookup"><span data-stu-id="31cf4-114">WUA validates that the Wsusscn2.cab is signed by a valid Microsoft certificate before running an offline scan.</span></span>

> [!NOTE]
> <span data-ttu-id="31cf4-115">De acordo com nossa [iniciativa de substituição SHA-1](https://aka.ms/sha1deprecation), o arquivo de Wsusscn2.cab não é mais assinado duplo usando o SHA-1 e o pacote SHA-2 de algoritmos de hash (especificamente SHA-256).</span><span class="sxs-lookup"><span data-stu-id="31cf4-115">In accordance with our [SHA-1 deprecation initiative](https://aka.ms/sha1deprecation), the Wsusscn2.cab file is no longer dual-signed using both SHA-1 and the SHA-2 suite of hash algorithms (specifically SHA-256).</span></span> <span data-ttu-id="31cf4-116">Este arquivo agora está assinado usando somente SHA-256.</span><span class="sxs-lookup"><span data-stu-id="31cf4-116">This file is now signed using only SHA-256.</span></span> <span data-ttu-id="31cf4-117">Os administradores que verificam assinaturas digitais neste arquivo agora devem esperar apenas assinaturas do SHA-256.</span><span class="sxs-lookup"><span data-stu-id="31cf4-117">Administrators who verify digital signatures on this file should now expect only single SHA-256 signatures.</span></span>

## <a name="example"></a><span data-ttu-id="31cf4-118">Exemplo</span><span class="sxs-lookup"><span data-stu-id="31cf4-118">Example</span></span>

<span data-ttu-id="31cf4-119">O exemplo a seguir usa o arquivo Wsusscn2.cab para verificar um computador e exibe as atualizações que estão faltando.</span><span class="sxs-lookup"><span data-stu-id="31cf4-119">The following example uses the Wsusscn2.cab file to scan a computer and displays updates that are missing.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="31cf4-120">Esse script destina-se a demonstrar o uso das APIs do agente de Windows Update e fornece um exemplo de como os desenvolvedores podem usar essas APIs para resolver problemas.</span><span class="sxs-lookup"><span data-stu-id="31cf4-120">This script is intended to demonstrate the use of the Windows Update Agent APIs, and provide an example of how developers can use these APIs to solve problems.</span></span> <span data-ttu-id="31cf4-121">Esse script não se destina como código de produção e o próprio script não tem suporte da Microsoft (embora haja suporte para as APIs de agente de Windows Update subjacentes).</span><span class="sxs-lookup"><span data-stu-id="31cf4-121">This script is not intended as production code, and the script itself is not supported by Microsoft (though the underlying Windows Update Agent APIs are supported).</span></span>

 


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



 

 



