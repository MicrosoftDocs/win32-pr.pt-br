---
title: UI_PKEY_FontProperties_Strikethrough
description: Identifica a \_ propriedade de \_ tachado PKEY fontproperties de interface do usuário \_ .
ms.assetid: 18ee653d-db01-4615-a85d-ad4ac6a0f422
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b07804a74671bb219b34b1c67580af083fd5c34c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366550"
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



|                                  |                                                                              |
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

 

 