---
title: UI_PKEY_FontProperties_Italic
description: Identifica a propriedade de itálico da interface do usuário \_ PKEY \_ fontproperties \_ .
ms.assetid: 53edd88e-ed7e-4385-9fd9-bfa90be348cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00825807c57632b1bbea69c47bc9b90d705efa94
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366155"
---
# <a name="ui_pkey_fontproperties_italic"></a>Interface do usuário \_ PKEY \_ fontproperties \_ itálico

Identifica a propriedade de itálico da interface do usuário \_ PKEY \_ fontproperties \_ .

```
propertyDescription
   name = UI_PKEY_FontProperties_Italic
   shellPKey = UI_PKEY_FontProperties_Italic
   formatID = 00000304-7363-696e-8441798acf5aebb7
   propID = 304
   typeInfo
      type = UI_FONTPROPERTIES
```

## <a name="remarks"></a>Comentários

A interface do usuário \_ PKEY \_ FontProperty \_ Italic é usada por um aplicativo para consultar o estado do botão **itálico** .

O valor da propriedade é da [**enumeração \_ fontproperties da interface do usuário**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties) .

O valor padrão é `UI_FONTPROPERTIES_NOTSET`.

A tabela a seguir descreve as propriedades e o resultado da interface do usuário.



|                                  |                                                                       |
|----------------------------------|-----------------------------------------------------------------------|
| `UI_FONTPROPERTIES_NOTAVAILABLE` | O botão **itálico** está desabilitado e só pode ser definido pelo aplicativo. |
| `UI_FONTPROPERTIES_NOTSET`       | O botão **itálico** não está selecionado.                                    |
| `UI_FONTPROPERTIES_SET`          | O botão **itálico** está selecionado.                                        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Propriedades de controle de fonte](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**fonte de fontes da interface do usuário \_**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties)
</dt> <dt>

[Controle de fonte](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 