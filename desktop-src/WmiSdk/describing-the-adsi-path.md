---
description: O Lightweight Directory Access Protocol (LDAP) exige que você escape alguns caracteres com uma barra invertida ( \) caractere ao usá-los em um caminho ADSI (interfaces do serviço de Active Directory LDAP).
ms.assetid: bc04359c-4eda-4574-a9c2-f005a1d92dea
ms.tgt_platform: multiple
title: Descrevendo o caminho ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51a6f3f28ffa5faa80dbd9f3d7906bba542e47e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104505713"
---
# <a name="describing-the-adsi-path"></a><span data-ttu-id="8d4cd-103">Descrevendo o caminho ADSI</span><span class="sxs-lookup"><span data-stu-id="8d4cd-103">Describing the ADSI Path</span></span>

<span data-ttu-id="8d4cd-104">O Lightweight Directory Access Protocol (LDAP) exige que você escape alguns caracteres com uma barra invertida ( \) caractere ao usá-los em um caminho ADSI (interfaces do serviço de Active Directory LDAP).</span><span class="sxs-lookup"><span data-stu-id="8d4cd-104">The Lightweight Directory Access Protocol (LDAP) requires that you escape some characters with a backslash (\) character when you use them in an LDAP Active Directory Service Interfaces (ADSI) path.</span></span>

<span data-ttu-id="8d4cd-105">, = +<>\# ; \\ "</span><span class="sxs-lookup"><span data-stu-id="8d4cd-105">,=+<>\#;\\"</span></span>

<span data-ttu-id="8d4cd-106">O caractere de escape só é necessário para o valor da propriedade **ADSIPath** .</span><span class="sxs-lookup"><span data-stu-id="8d4cd-106">The escape character is only required for the **ADSIPath** property value.</span></span>

<span data-ttu-id="8d4cd-107">O exemplo a seguir mostra como definir a propriedade **ADSIPath** .</span><span class="sxs-lookup"><span data-stu-id="8d4cd-107">The following example shows how to define the **ADSIPath** property.</span></span> <span data-ttu-id="8d4cd-108">Observe que o \# caractere no valor da propriedade **CN** de ABC \# é de escape.</span><span class="sxs-lookup"><span data-stu-id="8d4cd-108">Note that the \# character in the **CN** property value of abc\# is escaped.</span></span>


```C++
// #include <windows.h> for this code to compile

BSTR strObjPath = 
    SysAllocString(L"ds_user.ADSIPath=\"LDAP://CN=abc\#,"
                   L"CN=Users,DC=dsprovider,DC=nttest,"
                   L"DC=microsoft,DC=com\"");

// Use strObjectPath here.

SysFreeString(strObjPath); // Free memory resources.
```



> [!Note]  
> <span data-ttu-id="8d4cd-109">Para obter mais informações sobre o suporte e a instalação desse componente em um sistema operacional específico, consulte [disponibilidade do sistema operacional de componentes WMI](operating-system-availability-of-wmi-components.md).</span><span class="sxs-lookup"><span data-stu-id="8d4cd-109">For more information about support and installation of this component on a specific operating system, see [Operating System Availability of WMI Components](operating-system-availability-of-wmi-components.md).</span></span>

 

 

 



