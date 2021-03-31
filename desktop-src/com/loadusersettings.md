---
title: LoadUserSettings
description: Determina se o COM carregará o perfil do usuário para servidores COM em execução como a identidade do aplicativo de usuário de inicialização.
ms.assetid: 3e2b3249-3747-4d98-96da-f3e480a51d12
keywords:
- COM valor do registro LoadUserSettings COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e14282b00bc2c2d9b989e19480047f115623d55
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916468"
---
# <a name="loadusersettings"></a>LoadUserSettings

Determina se o COM carregará o perfil do usuário para servidores COM em execução como a identidade do aplicativo de usuário de inicialização.

## <a name="registry-entry"></a>Entrada do Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      LoadUserSettings = value
```

## <a name="remarks"></a>Comentários

Esse é um valor de **reg \_ DWORD** . Se o *valor* for diferente de zero, o com carregará o perfil da conta de usuário com a qual ele inicia o servidor com. Se o *valor* for zero ou não estiver presente, o com não carregará o perfil da conta de usuário com a qual ele inicia o servidor com.

Essa configuração será ignorada se uma entrada [**runas**](runas.md) estiver presente.

 

 




