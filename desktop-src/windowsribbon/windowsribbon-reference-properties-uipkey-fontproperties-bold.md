---
title: UI_PKEY_FontProperties_Bold
description: Identifica a propriedade de interface de usuário \_ PKEY \_ FontProperty \_ Bold.
ms.assetid: 9d33142a-bd63-423e-ba77-083c86bce1e7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dca8a58b9c5bfa51cfba8d80a477dafb744dfb8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105813597"
---
# <a name="ui_pkey_fontproperties_bold"></a>Interface do usuário \_ PKEY \_ FontProperty \_ bold

Identifica a propriedade de interface de usuário \_ PKEY \_ FontProperty \_ Bold.

```
propertyDescription
   name = UI_PKEY_FontProperties_Bold
   shellPKey = UI_PKEY_FontProperties_Bold
   formatID = 00000303-7363-696e-8441798acf5aebb7
   propID = 303
   typeInfo
      type = UI_FONTPROPERTIES
```

## <a name="remarks"></a>Comentários

A interface do usuário \_ PKEY \_ FontProperty \_ Bold é usada por um aplicativo para consultar o estado do botão **negrito** .

O valor da propriedade é da [**enumeração \_ fontproperties da interface do usuário**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties) .

O valor padrão é `UI_FONTPROPERTIES_NOTSET`.

A tabela a seguir descreve as propriedades e o resultado da interface do usuário.



|                                  |                                                                     |
|----------------------------------|---------------------------------------------------------------------|
| `UI_FONTPROPERTIES_NOTAVAILABLE` | O botão **negrito** está desabilitado e só pode ser definido pelo aplicativo. |
| `UI_FONTPROPERTIES_NOTSET`       | O botão **negrito** não está selecionado.                                    |
| `UI_FONTPROPERTIES_SET`          | O botão **negrito** está selecionado.                                        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Propriedades de controle de fonte](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**fonte de fontes da interface do usuário \_**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties)
</dt> <dt>

[Controle de fonte](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 