---
title: Habilitando o sistema de arquivos projetado pelo Windows
description: Descreve como habilitar o ProjFS no Windows
ms.assetid: <GUID-GOES-HERE>
ms.date: 09/17/2018
ms.topic: article
ms.openlocfilehash: f903192190877631084e366bcaeafd8b5b0e7e72
ms.sourcegitcommit: 42cdae4d2eca84713ab3f7a5c88f583a352991a8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/23/2019
ms.locfileid: "105759178"
---
# <a name="enabling-windows-projected-file-system"></a>Habilitando o sistema de arquivos projetado pelo Windows

O ProjFS é fornecido com o Windows como um componente opcional.  Antes que um provedor possa usá-lo, ele deve ser habilitado.  É possível usar o <!--the GUI or--> PowerShell para habilitar ProjFS.

<!--
## How to enable ProjFS in the GUI

Open the Start menu and type "Control Panel".  Click "Programs", then "Turn Windows features on or off".  In the Windows Features dialog box select the check box next to "Windows Projected File System":

![Windows features dialog](images/WindowsFeaturesDialog.png)
-->

## <a name="how-to-enable-projfs-using-powershell"></a>Como habilitar o ProjFS usando o PowerShell

Para usar o PowerShell para habilitar o ProjFS, use o `Enable-WindowsOptionalFeature` cmdlet em uma janela do PowerShell com privilégios elevados:

```PowerShell
Enable-WindowsOptionalFeature -Online -FeatureName Client-ProjFS -NoRestart
```

Reinicialize o computador se o Enable-WindowsOptionalFeature relatórios `RestartNeeded: True` .
