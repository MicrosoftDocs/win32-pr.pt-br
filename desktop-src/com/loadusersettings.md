---
title: LoadUserSettings
description: Determina se o COM carregará o perfil do usuário para servidores COM em execução como a identidade do aplicativo de usuário de inicialização.
ms.assetid: 3e2b3249-3747-4d98-96da-f3e480a51d12
keywords:
- COM valor do registro LoadUserSettings COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4b82bd89015baa4c73c9200013e49c76523951218dfde62bbe39300eefdfe0a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119731036"
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

 

 




