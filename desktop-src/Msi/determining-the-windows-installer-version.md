---
description: 'você pode usar os seguintes métodos para determinar a versão do Windows Installer:'
ms.assetid: 6b39bb19-4360-4d0e-a797-980912a91275
title: determinando a versão de Windows Installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e13907790585356fa4a5bc8376fe87f30793e0e3af71e1b0c113f30cf04b8f9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764216"
---
# <a name="determining-the-windows-installer-version"></a>determinando a versão de Windows Installer

você pode usar os seguintes métodos para determinar a versão do Windows Installer:

-   Chame a função [**MsiGetFileVersion**](/windows/desktop/api/Msi/nf-msi-msigetfileversiona) com o parâmetro *szFilePath* definido como o caminho para o arquivo Msi.dll.

    Você pode chamar a função [**SHGetKnownFolderPath**](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) com a constante de **\_ sistema CSIDL** para obter o caminho para Msi.dll. a partir do Windows Vista, os aplicativos devem usar a função [**SHGetFolderPath**](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) e o **REFKNOWNFOLDERID** "System". Os aplicativos existentes que usam a função **SHGetFolderPath** e o tipo **CSIDL** continuarão funcionando.

-   o valor da propriedade [**installer. Version**](installer-version.md) do objeto do [**instalador**](installer-object.md) é equivalente às cadeias de quatro campos listadas nas [versões liberadas do tópico Windows Installer](released-versions-of-windows-installer.md) .
-   os aplicativos podem obter a versão Windows Installer usando o [**DllGetVersion**](/windows/win32/api/shlwapi/nc-shlwapi-dllgetversionproc).
-   o instalador define a propriedade [**VersionMsi**](versionmsi.md) para a versão do Windows Installer que é executada durante a instalação.

para obter mais informações, consulte [versões lançadas do Windows Installer](released-versions-of-windows-installer.md).

 

 
