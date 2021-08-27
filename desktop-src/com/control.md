---
title: Control
description: identifica um objeto como um controle de ActiveX.
ms.assetid: 2487e642-1d21-4811-87dd-b280be98a44b
keywords:
- Controlar chave de registro COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03aa6a0b131dd5fc2ba10d9aaeabafd06b19b73bb1e9422c28e5bec45ea43cbb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120506"
---
# <a name="control"></a>Control

identifica um objeto como um controle de ActiveX.

## <a name="registry-entry"></a>Entrada do Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      Control
```

## <a name="remarks"></a>Comentários

Essa entrada opcional é usada por contêineres para preencher caixas de diálogo. o contêiner usa essa subchave para determinar se um objeto deve ser incluído em uma caixa de diálogo que exibe ActiveX controles. Um controle pode omitir essa entrada se for projetado para funcionar apenas com um contêiner específico e, portanto, não se destina a ser inserido em outros contêineres.

 

 




