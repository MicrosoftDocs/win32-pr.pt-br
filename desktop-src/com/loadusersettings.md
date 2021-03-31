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
# <a name="loadusersettings"></a><span data-ttu-id="7a85c-104">LoadUserSettings</span><span class="sxs-lookup"><span data-stu-id="7a85c-104">LoadUserSettings</span></span>

<span data-ttu-id="7a85c-105">Determina se o COM carregará o perfil do usuário para servidores COM em execução como a identidade do aplicativo de usuário de inicialização.</span><span class="sxs-lookup"><span data-stu-id="7a85c-105">Determines whether COM will load the user profile for COM servers running as the launching user application identity.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="7a85c-106">Entrada do Registro</span><span class="sxs-lookup"><span data-stu-id="7a85c-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      LoadUserSettings = value
```

## <a name="remarks"></a><span data-ttu-id="7a85c-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="7a85c-107">Remarks</span></span>

<span data-ttu-id="7a85c-108">Esse é um valor de **reg \_ DWORD** .</span><span class="sxs-lookup"><span data-stu-id="7a85c-108">This is a **REG\_DWORD** value.</span></span> <span data-ttu-id="7a85c-109">Se o *valor* for diferente de zero, o com carregará o perfil da conta de usuário com a qual ele inicia o servidor com.</span><span class="sxs-lookup"><span data-stu-id="7a85c-109">If *value* is nonzero, COM loads the profile of the user account with which it launches the COM server.</span></span> <span data-ttu-id="7a85c-110">Se o *valor* for zero ou não estiver presente, o com não carregará o perfil da conta de usuário com a qual ele inicia o servidor com.</span><span class="sxs-lookup"><span data-stu-id="7a85c-110">If *value* is zero or not present, COM will not load the profile of the user account with which it launches the COM server.</span></span>

<span data-ttu-id="7a85c-111">Essa configuração será ignorada se uma entrada [**runas**](runas.md) estiver presente.</span><span class="sxs-lookup"><span data-stu-id="7a85c-111">This setting is ignored if a [**RunAs**](runas.md) entry is present.</span></span>

 

 




