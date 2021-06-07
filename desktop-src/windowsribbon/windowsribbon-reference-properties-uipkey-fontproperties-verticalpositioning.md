---
title: UI_PKEY_FontProperties_VerticalPositioning
description: Identifica a propriedade da interface do usuário \_ PKEY \_ fontproperties \_ VerticalPositioning.
ms.assetid: a92f845e-b0fc-4e23-9d06-ca16d2becf0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 954b01ff3271b9f74fac2c130c697a70e910fc93
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444297"
---
# <a name="ui_pkey_fontproperties_verticalpositioning"></a>Interface do usuário \_ PKEY \_ fontproperties \_ VerticalPositioning

Identifica a propriedade da interface do usuário \_ PKEY \_ fontproperties \_ VerticalPositioning.

```
propertyDescription
   name = UI_PKEY_FontProperties_VerticalPositioning
   shellPKey = UI_PKEY_FontProperties_VerticalPositioning
   formatID = 00000307-7363-696e-8441798acf5aebb7
   propID = 307
   typeInfo
      type = UI_FONTVERTICALPOSITION
```

## <a name="remarks"></a>Comentários

A interface do usuário \_ PKEY \_ fontproperties \_ VerticalPositioning é usada por um aplicativo para consultar o valor dos controles **sobrescrito** e **subscrito** .

O valor da propriedade é da [**enumeração \_ FONTVERTICALPOSITION da interface do usuário**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontverticalposition) .

O valor padrão é `UI_FONTVERTICALPOSITION_NOTSET`.

A captura de tela a seguir mostra os botões **sobrescrito** e **subscrito** da faixa de opções [**FontControl**](windowsribbon-element-fontcontrol.md).

![captura de tela do elemento fontcontrol com o atributo richfont definido como true.](images/markup/fontcontrol-subsuper.png)

A tabela a seguir descreve as propriedades e o resultado da interface do usuário.



|     Propriedade                           |          Resultado da IU                                                                             |
|----------------------------------------|------------------------------------------------------------------------------------------------|
| `UI_FONTVERTICALPOSITION_NOTAVAILABLE` | Os botões **sobrescrito** e **subscrito** estão desabilitados e só podem ser definidos pelo aplicativo. |
| `UI_FONTVERTICALPOSITION_NOTSET`       | Os botões **sobrescrito** e **subscrito** não estão selecionados.                                    |
| `UI_FONTVERTICALPOSITION_SUPERSCRIPT`  | O botão **sobrescrito** está selecionado.                                                            |
| `UI_FONTVERTICALPOSITION_SUBSCRIPT`    | O botão **subscrito** está selecionado.                                                              |



 

> [!Note]  
> Os botões **sobrescrito** e **subscrito** não podem ser selecionados.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Propriedades de controle de fonte](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**FONTVERTICALPOSITION da interface do usuário \_**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontverticalposition)
</dt> <dt>

[Controle de fonte](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 