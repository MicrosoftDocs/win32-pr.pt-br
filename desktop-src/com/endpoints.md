---
title: Pontos de extremidade
description: Configura um aplicativo COM para usar um número de porta TCP especificado para comunicações DCOM.
ms.assetid: 2a286a13-24b8-418a-b29b-5543a1c56c45
keywords:
- Valor de registro de pontos de extremidade COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0addcd6c09b409629bb4a7157241d57476cafe3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363843"
---
# <a name="endpoints"></a><span data-ttu-id="97cfc-104">Pontos de extremidade</span><span class="sxs-lookup"><span data-stu-id="97cfc-104">Endpoints</span></span>

<span data-ttu-id="97cfc-105">Configura um aplicativo COM para usar um número de porta TCP especificado para comunicações DCOM.</span><span class="sxs-lookup"><span data-stu-id="97cfc-105">Configures a COM application to use a specified TCP port number for DCOM communications.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="97cfc-106">Entrada do Registro</span><span class="sxs-lookup"><span data-stu-id="97cfc-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      Endpoints = ncacn_ip_tcp,0,port
```

## <a name="remarks"></a><span data-ttu-id="97cfc-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="97cfc-107">Remarks</span></span>

<span data-ttu-id="97cfc-108">Esse é um valor **reg de \_ vários \_ sz** .</span><span class="sxs-lookup"><span data-stu-id="97cfc-108">This is a **REG\_MULTI\_SZ** value.</span></span>

<span data-ttu-id="97cfc-109">O valor da *porta* é um número entre 1024 e 65535, que especifica o número da porta TCP que seu aplicativo com usará para comunicações DCOM.</span><span class="sxs-lookup"><span data-stu-id="97cfc-109">The *port* value is a number between 1024 and 65535 that specifies the TCP port number that your COM application will use for DCOM communications.</span></span> <span data-ttu-id="97cfc-110">Se você não especificar essa chave do registro, os números de porta para comunicações DCOM serão atribuídos dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="97cfc-110">If you do not specify this registry key, port numbers for DCOM communications are dynamically assigned.</span></span> <span data-ttu-id="97cfc-111">Na maioria dos cenários, você pode preferir deixar essa chave do registro indefinida e permitir que o DCOM atribua números de porta dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="97cfc-111">In most scenarios, you might prefer to leave this registry key undefined and allow DCOM to dynamically assign port numbers.</span></span>

 

 




