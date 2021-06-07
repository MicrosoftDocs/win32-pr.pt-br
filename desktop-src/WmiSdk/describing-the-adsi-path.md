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
# <a name="describing-the-adsi-path"></a>Descrevendo o caminho ADSI

O LDAP (Lightweight Directory Access Protocol) requer que você escape de alguns caracteres com um caractere de invertida ( ) ao usá-los em um caminho ADSI (Interfaces de Serviço \\ do Active Directory) LDAP.

,=+<>\# ; \\ "

O caractere de escape só é necessário para o valor da propriedade **ADSIPath.**

O exemplo a seguir mostra como definir a **propriedade ADSIPath.** Observe que o \# caractere no valor da propriedade **CN** de abc \# é escapado.


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
> Para obter mais informações sobre o suporte e a instalação desse componente em um sistema operacional específico, consulte Disponibilidade do sistema operacional [de componentes WMI](operating-system-availability-of-wmi-components.md).

 

 

 



