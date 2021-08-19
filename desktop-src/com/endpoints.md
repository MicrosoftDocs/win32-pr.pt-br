---
title: Pontos de extremidade
description: Configura um aplicativo COM para usar um número de porta TCP especificado para comunicações DCOM.
ms.assetid: 2a286a13-24b8-418a-b29b-5543a1c56c45
keywords:
- Valor de registro de pontos de extremidade COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48ee2444be55aaf32c028792100e3e6f0ed6989509b7c0af02c5d83bd739fa27
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048314"
---
# <a name="endpoints"></a>Pontos de extremidade

Configura um aplicativo COM para usar um número de porta TCP especificado para comunicações DCOM.

## <a name="registry-entry"></a>Entrada do Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      Endpoints = ncacn_ip_tcp,0,port
```

## <a name="remarks"></a>Comentários

Esse é um valor **reg de \_ vários \_ sz** .

O valor da *porta* é um número entre 1024 e 65535, que especifica o número da porta TCP que seu aplicativo com usará para comunicações DCOM. Se você não especificar essa chave do registro, os números de porta para comunicações DCOM serão atribuídos dinamicamente. Na maioria dos cenários, você pode preferir deixar essa chave do registro indefinida e permitir que o DCOM atribua números de porta dinamicamente.

 

 




