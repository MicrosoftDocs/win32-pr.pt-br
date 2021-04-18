---
description: 'Você pode usar os seguintes métodos para determinar a versão do Windows Installer:'
ms.assetid: 6b39bb19-4360-4d0e-a797-980912a91275
title: Determinando a versão de Windows Installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a48434fe415084a93158fb3445a36906d8b8993
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105757125"
---
# <a name="determining-the-windows-installer-version"></a><span data-ttu-id="360c2-103">Determinando a versão de Windows Installer</span><span class="sxs-lookup"><span data-stu-id="360c2-103">Determining the Windows Installer Version</span></span>

<span data-ttu-id="360c2-104">Você pode usar os seguintes métodos para determinar a versão do Windows Installer:</span><span class="sxs-lookup"><span data-stu-id="360c2-104">You can use the following methods to determine the Windows Installer version:</span></span>

-   <span data-ttu-id="360c2-105">Chame a função [**MsiGetFileVersion**](/windows/desktop/api/Msi/nf-msi-msigetfileversiona) com o parâmetro *szFilePath* definido como o caminho para o arquivo Msi.dll.</span><span class="sxs-lookup"><span data-stu-id="360c2-105">Call the [**MsiGetFileVersion**](/windows/desktop/api/Msi/nf-msi-msigetfileversiona) function with the *szFilePath* parameter set to the path to the file Msi.dll.</span></span>

    <span data-ttu-id="360c2-106">Você pode chamar a função [**SHGetKnownFolderPath**](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) com a constante de **\_ sistema CSIDL** para obter o caminho para Msi.dll.</span><span class="sxs-lookup"><span data-stu-id="360c2-106">You can call the [**SHGetKnownFolderPath**](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) function with the **CSIDL\_SYSTEM** constant to get the path to Msi.dll.</span></span> <span data-ttu-id="360c2-107">A partir do Windows Vista, os aplicativos devem usar a função [**SHGetFolderPath**](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) e o **REFKNOWNFOLDERID** "System".</span><span class="sxs-lookup"><span data-stu-id="360c2-107">Beginning with Windows Vista, applications should use the [**SHGetFolderPath**](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) function and the **REFKNOWNFOLDERID** "System."</span></span> <span data-ttu-id="360c2-108">Os aplicativos existentes que usam a função **SHGetFolderPath** e o tipo **CSIDL** continuarão funcionando.</span><span class="sxs-lookup"><span data-stu-id="360c2-108">Existing applications that use the **SHGetFolderPath** function and the **CSIDL** type will continue to work.</span></span>

-   <span data-ttu-id="360c2-109">O valor da propriedade [**Installer. Version**](installer-version.md) do objeto do [**instalador**](installer-object.md) é equivalente às cadeias de quatro campos listadas nas [versões liberadas do tópico Windows Installer](released-versions-of-windows-installer.md) .</span><span class="sxs-lookup"><span data-stu-id="360c2-109">The value of the [**Installer.Version**](installer-version.md) property of the [**Installer Object**](installer-object.md) is equivalent to the four-field strings listed in the [Released Versions of Windows Installer](released-versions-of-windows-installer.md) topic.</span></span>
-   <span data-ttu-id="360c2-110">Os aplicativos podem obter a versão Windows Installer usando o [**DllGetVersion**](/windows/win32/api/shlwapi/nc-shlwapi-dllgetversionproc).</span><span class="sxs-lookup"><span data-stu-id="360c2-110">Applications can get the Windows Installer version by using [**DllGetVersion**](/windows/win32/api/shlwapi/nc-shlwapi-dllgetversionproc).</span></span>
-   <span data-ttu-id="360c2-111">O instalador define a propriedade [**VersionMsi**](versionmsi.md) para a versão do Windows Installer que é executada durante a instalação.</span><span class="sxs-lookup"><span data-stu-id="360c2-111">The installer sets the [**VersionMsi**](versionmsi.md) property to the version of Windows Installer that is run during the installation.</span></span>

<span data-ttu-id="360c2-112">Para obter mais informações, consulte [versões lançadas do Windows Installer](released-versions-of-windows-installer.md).</span><span class="sxs-lookup"><span data-stu-id="360c2-112">For more information, see [Released Versions of Windows Installer](released-versions-of-windows-installer.md).</span></span>

 

 
