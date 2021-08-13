---
title: UI_PKEY_FontProperties_Italic
description: Identifica a propriedade de itálico da interface do usuário \_ PKEY \_ fontproperties \_ .
ms.assetid: 53edd88e-ed7e-4385-9fd9-bfa90be348cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 000bb72e1ba43b29f5e3815fe42d0ace454ff0219a188a128b422e4a621af210
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118438531"
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



|    Propriedade                      |       Resultado da IU                                                       |
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

 

 