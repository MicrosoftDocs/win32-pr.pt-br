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
# <a name="determining-the-windows-installer-version"></a>Determinando a versão de Windows Installer

Você pode usar os seguintes métodos para determinar a versão do Windows Installer:

-   Chame a função [**MsiGetFileVersion**](/windows/desktop/api/Msi/nf-msi-msigetfileversiona) com o parâmetro *szFilePath* definido como o caminho para o arquivo Msi.dll.

    Você pode chamar a função [**SHGetKnownFolderPath**](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) com a constante de **\_ sistema CSIDL** para obter o caminho para Msi.dll. A partir do Windows Vista, os aplicativos devem usar a função [**SHGetFolderPath**](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) e o **REFKNOWNFOLDERID** "System". Os aplicativos existentes que usam a função **SHGetFolderPath** e o tipo **CSIDL** continuarão funcionando.

-   O valor da propriedade [**Installer. Version**](installer-version.md) do objeto do [**instalador**](installer-object.md) é equivalente às cadeias de quatro campos listadas nas [versões liberadas do tópico Windows Installer](released-versions-of-windows-installer.md) .
-   Os aplicativos podem obter a versão Windows Installer usando o [**DllGetVersion**](/windows/win32/api/shlwapi/nc-shlwapi-dllgetversionproc).
-   O instalador define a propriedade [**VersionMsi**](versionmsi.md) para a versão do Windows Installer que é executada durante a instalação.

Para obter mais informações, consulte [versões lançadas do Windows Installer](released-versions-of-windows-installer.md).

 

 
