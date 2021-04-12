---
title: Control
description: Identifica um objeto como um controle ActiveX.
ms.assetid: 2487e642-1d21-4811-87dd-b280be98a44b
keywords:
- Controlar chave de registro COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3722d85b38399d7e95f226749bda45ccc82d1369
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364441"
---
# <a name="control"></a><span data-ttu-id="b03c6-104">Control</span><span class="sxs-lookup"><span data-stu-id="b03c6-104">Control</span></span>

<span data-ttu-id="b03c6-105">Identifica um objeto como um controle ActiveX.</span><span class="sxs-lookup"><span data-stu-id="b03c6-105">Identifies an object as an ActiveX Control.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="b03c6-106">Entrada do Registro</span><span class="sxs-lookup"><span data-stu-id="b03c6-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      Control
```

## <a name="remarks"></a><span data-ttu-id="b03c6-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="b03c6-107">Remarks</span></span>

<span data-ttu-id="b03c6-108">Essa entrada opcional é usada por contêineres para preencher caixas de diálogo.</span><span class="sxs-lookup"><span data-stu-id="b03c6-108">This optional entry is used by containers to fill in dialog boxes.</span></span> <span data-ttu-id="b03c6-109">O contêiner usa essa subchave para determinar se um objeto deve ser incluído em uma caixa de diálogo que exibe controles ActiveX.</span><span class="sxs-lookup"><span data-stu-id="b03c6-109">The container uses this subkey to determine whether to include an object in a dialog box that displays ActiveX Controls.</span></span> <span data-ttu-id="b03c6-110">Um controle pode omitir essa entrada se for projetado para funcionar apenas com um contêiner específico e, portanto, não se destina a ser inserido em outros contêineres.</span><span class="sxs-lookup"><span data-stu-id="b03c6-110">A control can omit this entry if it is designed to work only with a specific container and therefore does is not intended to be inserted in other containers.</span></span>

 

 




