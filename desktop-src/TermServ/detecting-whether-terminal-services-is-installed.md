---
title: Detectando se a função de Serviços de Área de Trabalho Remota está instalada
description: C \ código de exemplo que mostra um método que retorna true se a função de servidor Serviços de Área de Trabalho Remota estiver instalada e em execução ou false caso contrário, começando com o Windows Server 2008.
ms.assetid: 53ef8d43-2141-4df7-b9e6-baf0677924ba
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49f7d094f88271346c97f8d0467b48a266c865d5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366486"
---
# <a name="detecting-whether-the-remote-desktop-services-role-is-installed"></a><span data-ttu-id="07a27-103">Detectando se a função de Serviços de Área de Trabalho Remota está instalada</span><span class="sxs-lookup"><span data-stu-id="07a27-103">Detecting Whether the Remote Desktop Services Role Is Installed</span></span>

<span data-ttu-id="07a27-104">Você pode usar a classe WMI [**\_ ServerFeature do Win32**](/windows/desktop/WmiSdk/win32-serverfeature) para detectar se a função de servidor serviços de área de trabalho remota está instalada.</span><span class="sxs-lookup"><span data-stu-id="07a27-104">You can use the [**Win32\_ServerFeature**](/windows/desktop/WmiSdk/win32-serverfeature) WMI class to detect whether the Remote Desktop Services server role is installed.</span></span>

<span data-ttu-id="07a27-105">O exemplo de C# a seguir mostra um método que retorna **true** se a função de servidor serviços de área de trabalho remota estiver instalada e em execução ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="07a27-105">The following C# example shows a method that returns **True** if the Remote Desktop Services server role is installed and running or **false** otherwise.</span></span> <span data-ttu-id="07a27-106">Como a classe WMI [**\_ ServerFeature do Win32**](/windows/desktop/WmiSdk/win32-serverfeature) só está disponível a partir do Windows Server 2008, esse código não é compatível com versões anteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="07a27-106">Because the [**Win32\_ServerFeature**](/windows/desktop/WmiSdk/win32-serverfeature) WMI class is only available beginning with Windows Server 2008, this code is not compatible with earlier versions of Windows.</span></span>


```CSharp
static void Main(string[] args)
{
    // 14 is the identifier of the Remote Desktop Services role.
    HasServerFeatureById(14);
}

static bool HasServerFeatureById(UInt32 roleId)
{
    try
    {
        ManagementClass serviceClass = new ManagementClass("Win32_ServerFeature");
        foreach (ManagementObject feature in serviceClass.GetInstances())
        {
            if ((UInt32)feature["ID"] == roleId)
            {
                return true;
            }
        }

        return false;
    }
    catch (ManagementException)
    {
        // The most likely cause of this is that this is being called from an 
        // operating system that is not a server operating system.
    }

    return false;
}

```



 

 