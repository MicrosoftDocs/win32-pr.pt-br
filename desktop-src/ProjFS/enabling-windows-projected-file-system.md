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
# <a name="enabling-windows-projected-file-system"></a><span data-ttu-id="200e7-103">Habilitando o sistema de arquivos projetado pelo Windows</span><span class="sxs-lookup"><span data-stu-id="200e7-103">Enabling Windows Projected File System</span></span>

<span data-ttu-id="200e7-104">O ProjFS é fornecido com o Windows como um componente opcional.</span><span class="sxs-lookup"><span data-stu-id="200e7-104">ProjFS ships with Windows as an Optional Component.</span></span>  <span data-ttu-id="200e7-105">Antes que um provedor possa usá-lo, ele deve ser habilitado.</span><span class="sxs-lookup"><span data-stu-id="200e7-105">Before a provider can use it, it must be enabled.</span></span>  <span data-ttu-id="200e7-106">É possível usar o</span><span class="sxs-lookup"><span data-stu-id="200e7-106">You can use</span></span> <!--the GUI or--> <span data-ttu-id="200e7-107">PowerShell para habilitar ProjFS.</span><span class="sxs-lookup"><span data-stu-id="200e7-107">PowerShell to enable ProjFS.</span></span>

<!--
## How to enable ProjFS in the GUI

Open the Start menu and type "Control Panel".  Click "Programs", then "Turn Windows features on or off".  In the Windows Features dialog box select the check box next to "Windows Projected File System":

![Windows features dialog](images/WindowsFeaturesDialog.png)
-->

## <a name="how-to-enable-projfs-using-powershell"></a><span data-ttu-id="200e7-108">Como habilitar o ProjFS usando o PowerShell</span><span class="sxs-lookup"><span data-stu-id="200e7-108">How to enable ProjFS using PowerShell</span></span>

<span data-ttu-id="200e7-109">Para usar o PowerShell para habilitar o ProjFS, use o `Enable-WindowsOptionalFeature` cmdlet em uma janela do PowerShell com privilégios elevados:</span><span class="sxs-lookup"><span data-stu-id="200e7-109">To use PowerShell to enable ProjFS use the `Enable-WindowsOptionalFeature` cmdlet in an elevated PowerShell window:</span></span>

```PowerShell
Enable-WindowsOptionalFeature -Online -FeatureName Client-ProjFS -NoRestart
```

<span data-ttu-id="200e7-110">Reinicialize o computador se o Enable-WindowsOptionalFeature relatórios `RestartNeeded: True` .</span><span class="sxs-lookup"><span data-stu-id="200e7-110">Reboot the computer if the Enable-WindowsOptionalFeature reports `RestartNeeded: True`.</span></span>
