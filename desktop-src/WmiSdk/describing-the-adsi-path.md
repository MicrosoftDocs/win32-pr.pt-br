---
description: O LDAP (Lightweight Directory Access Protocol) requer que você escape de alguns caracteres com uma faixa invertida ( caractere ao usá-los em um caminho ADSI (Interfaces de Serviço \) do Active Directory) LDAP.
ms.assetid: bc04359c-4eda-4574-a9c2-f005a1d92dea
ms.tgt_platform: multiple
title: Descrevendo o caminho ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e0ba1dafac273ab3564549a5caca44180161643
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387105"
---
# <a name="describing-the-adsi-path"></a><span data-ttu-id="91d63-103">Descrevendo o caminho ADSI</span><span class="sxs-lookup"><span data-stu-id="91d63-103">Describing the ADSI Path</span></span>

<span data-ttu-id="91d63-104">O LDAP (Lightweight Directory Access Protocol) requer que você escape de alguns caracteres com um caractere de invertida ( ) ao usá-los em um caminho ADSI (Interfaces de Serviço \\ do Active Directory) LDAP.</span><span class="sxs-lookup"><span data-stu-id="91d63-104">The Lightweight Directory Access Protocol (LDAP) requires that you escape some characters with a backslash (\\) character when you use them in an LDAP Active Directory Service Interfaces (ADSI) path.</span></span>

<span data-ttu-id="91d63-105">,=+<>\# ; \\ "</span><span class="sxs-lookup"><span data-stu-id="91d63-105">,=+<>\#;\\"</span></span>

<span data-ttu-id="91d63-106">O caractere de escape só é necessário para o valor da propriedade **ADSIPath.**</span><span class="sxs-lookup"><span data-stu-id="91d63-106">The escape character is only required for the **ADSIPath** property value.</span></span>

<span data-ttu-id="91d63-107">O exemplo a seguir mostra como definir a **propriedade ADSIPath.**</span><span class="sxs-lookup"><span data-stu-id="91d63-107">The following example shows how to define the **ADSIPath** property.</span></span> <span data-ttu-id="91d63-108">Observe que o \# caractere no valor da propriedade **CN** de abc \# é escapado.</span><span class="sxs-lookup"><span data-stu-id="91d63-108">Note that the \# character in the **CN** property value of abc\# is escaped.</span></span>


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
> <span data-ttu-id="91d63-109">Para obter mais informações sobre o suporte e a instalação desse componente em um sistema operacional específico, consulte Disponibilidade do sistema operacional [de componentes WMI](operating-system-availability-of-wmi-components.md).</span><span class="sxs-lookup"><span data-stu-id="91d63-109">For more information about support and installation of this component on a specific operating system, see [Operating System Availability of WMI Components](operating-system-availability-of-wmi-components.md).</span></span>

 

 

 



