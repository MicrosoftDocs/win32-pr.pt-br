---
title: UI_PKEY_FontProperties_Strikethrough
description: Identifica a \_ propriedade de \_ tachado PKEY fontproperties de interface do usuário \_ .
ms.assetid: 18ee653d-db01-4615-a85d-ad4ac6a0f422
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 746172ec2209861615375e73dee3f2336950a2dd93e76b33893190e9f7e8bc18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117850297"
---
# <a name="ui_pkey_fontproperties_strikethrough"></a>Interface do usuário \_ PKEY \_ fontproperties \_ tachado

Identifica a \_ propriedade de \_ tachado PKEY fontproperties de interface do usuário \_ .

```
propertyDescription
   name = UI_PKEY_FontProperties_Strikethrough
   shellPKey = UI_PKEY_FontProperties_Strikethrough
   formatID = 00000306-7363-696e-8441798acf5aebb7
   propID = 306
   typeInfo
      type = UI_FONTPROPERTIES
```

## <a name="remarks"></a>Comentários

A interface do usuário \_ PKEY \_ fontproperties \_ tachado é usada por um aplicativo para consultar o estado do botão **tachado** .

O valor da propriedade é da [**enumeração \_ fontproperties da interface do usuário**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties) .

O valor padrão é `UI_FONTPROPERTIES_NOTSET`.

A captura de tela a seguir mostra o botão **tachado** da faixa de opções [**FontControl**](windowsribbon-element-fontcontrol.md).

![captura de tela do elemento fontcontrol com o atributo richfont definido como true.](images/markup/fontcontrol-strikethrough.png)

A tabela a seguir descreve as propriedades e o resultado da interface do usuário.



|   Propriedade                       |    Resultado da IU                                                                 |
|----------------------------------|------------------------------------------------------------------------------|
| `UI_FONTPROPERTIES_NOTAVAILABLE` | O botão **tachado** está desabilitado e só pode ser definido pelo aplicativo. |
| `UI_FONTPROPERTIES_NOTSET`       | O botão **tachado** não está selecionado.                                    |
| `UI_FONTPROPERTIES_SET`          | O botão **tachado** está selecionado.                                        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Propriedades de controle de fonte](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**fonte de fontes da interface do usuário \_**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties)
</dt> <dt>

[Controle de fonte](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 