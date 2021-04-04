---
title: Exemplo de valores de registro
description: O exemplo a seguir mostra possíveis dados para alguns dos valores de registro do protocolo de autenticação.
ms.assetid: 07772af0-db56-4cc6-ad72-cf79d3813883
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bcbc3d4ca10a3e9298177a5eea240d0d34ade04
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2019
ms.locfileid: "104006956"
---
# <a name="registry-values-example"></a>Exemplo de valores de registro

O exemplo a seguir mostra possíveis dados para alguns dos valores de registro do protocolo de autenticação.

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            Rasman
               PPP
                  EAP
                     40
                        Path
                        FriendlyName
                        ConfigUIPath
                        IdentityPath
                        InteractiveUIPath
                        RequireConfigUI
                        ConfigCLSID
                        StandaloneSupported
```



| Nome da Chave            | Datatype        | Valor                                  |
|---------------------|-----------------|----------------------------------------|
| Caminho                | REG \_ expande \_ sz | % SystemRoot% \\ system32 \\sample.dll     |
| FriendlyName        | REG \_ sz         | Protocolo EAP de exemplo                    |
| ConfigUIPath        | REG \_ expande \_ sz | % SystemRoot% \\ system32 \\sample.dll     |
| IdentityPath        | REG \_ expande \_ sz | % SystemRoot% \\ system32 \\sample.dll     |
| InteractiveUIPath   | REG \_ expande \_ sz | % SystemRoot% \\ system32 \\sample.dll     |
| RequireConfigUI     | REG \_ DWORD      | 1                                      |
| ConfigCLSID         | REG \_ sz         | {0000031A-0000-0000-C000-000000000046} |
| StandaloneSupported | REG \_ DWORD      | 1                                      |



 

 

 




