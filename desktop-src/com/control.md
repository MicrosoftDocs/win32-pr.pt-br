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
# <a name="control"></a>Control

Identifica um objeto como um controle ActiveX.

## <a name="registry-entry"></a>Entrada do Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      Control
```

## <a name="remarks"></a>Comentários

Essa entrada opcional é usada por contêineres para preencher caixas de diálogo. O contêiner usa essa subchave para determinar se um objeto deve ser incluído em uma caixa de diálogo que exibe controles ActiveX. Um controle pode omitir essa entrada se for projetado para funcionar apenas com um contêiner específico e, portanto, não se destina a ser inserido em outros contêineres.

 

 




