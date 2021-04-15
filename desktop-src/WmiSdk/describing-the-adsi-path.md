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
# <a name="describing-the-adsi-path"></a>Descrevendo o caminho ADSI

O Lightweight Directory Access Protocol (LDAP) exige que você escape alguns caracteres com uma barra invertida ( \) caractere ao usá-los em um caminho ADSI (interfaces do serviço de Active Directory LDAP).

, = +<>\# ; \\ "

O caractere de escape só é necessário para o valor da propriedade **ADSIPath** .

O exemplo a seguir mostra como definir a propriedade **ADSIPath** . Observe que o \# caractere no valor da propriedade **CN** de ABC \# é de escape.


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
> Para obter mais informações sobre o suporte e a instalação desse componente em um sistema operacional específico, consulte [disponibilidade do sistema operacional de componentes WMI](operating-system-availability-of-wmi-components.md).

 

 

 



