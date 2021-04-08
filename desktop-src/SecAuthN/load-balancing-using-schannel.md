---
description: Cada servidor pode definir um valor de chave de registro de MachineID no registro que é definido como uma parte fixa da ID de sessão.
ms.assetid: 1B373496-1C1B-4D4B-8CAC-B572C58E43A2
title: Balanceamento de carga usando Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dce190d665f4cc41eb0615a2ddc83e0ee54798d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828694"
---
# <a name="load-balancing-using-schannel"></a>Balanceamento de carga usando Schannel

Cada servidor pode definir um valor de chave de registro de MachineID no registro que é definido como uma parte fixa da ID de sessão. A chave do registro MachineID é um tipo de valor **reg \_ DWORD** . O balanceador de carga pode usar essa parte da ID de sessão para determinar qual servidor gerou a sessão SSL e pode manter o mapa para esse servidor. A ID de sessão faz parte do handshake SSL/TLS que é enviado pela conexão. O código do balanceador de carga deve usar o segundo **DWORD** na ID da sessão ao retomar ou reconectar-se ao cliente. A segunda **DWORD** da ID de sessão aleatória gerada por um servidor Schannel é substituída pelo **DWORD** armazenado no registro. O valor do registro para o **DWORD** não pode ser 0xFFFFFFFF.

O valor da chave do registro é o seguinte.

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Control
            SecurityProviders
               SCHANNEL
                  MachineID<dl>
<dt>

                  Data type
</dt>
<dd>                  REG_DWORD</dd>
</dl>
```

 

 



