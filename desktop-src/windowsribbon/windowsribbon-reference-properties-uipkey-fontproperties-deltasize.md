---
title: UI_PKEY_FontProperties_DeltaSize
description: Identifica a propriedade da interface do usuário \_ PKEY \_ fontproperties \_ DeltaSize.
ms.assetid: 021a6c79-1d3e-47d2-9601-cdaa2e66a50a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a35d2660d2221b4edad567b0fd05eb8283fce4b3cc7d1cb8e35c735838f385d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118438744"
---
# <a name="ui_pkey_fontproperties_deltasize"></a>Interface do usuário \_ PKEY \_ fontproperties \_ DeltaSize

Identifica a propriedade da interface do usuário \_ PKEY \_ fontproperties \_ DeltaSize.

```
propertyDescription
   name = UI_PKEY_FontProperties_DeltaSize
   shellPKey = UI_PKEY_FontProperties_DeltaSize
   formatID = 00000309-7363-696e-8441798acf5aebb7
   propID = 313
   typeInfo
      type = UI_FONTDELTASIZE
```

## <a name="remarks"></a>Comentários

A interface do usuário \_ PKEY \_ fontproperties \_ DeltaSize é usada por um aplicativo em casos em que não é possível que o aplicativo especifique um valor para o **tamanho da fonte**, como quando uma execução de texto de tamanho heterogêneo é selecionada. O controle **tamanho da fonte** está definido como em branco e a interface do usuário \_ PKEY \_ fontproperties \_ DeltaSize é usada para capturar a interação do usuário com os botões **aumentar fonte** e **reduzir fonte** .

A interface do usuário \_ PKEY \_ fontproperties \_ DeltaSize está incluída na [interface do usuário \_ PKEY \_ fontproperties \_ alterproperties](windowsribbon-reference-properties-uipkey-fontproperties-changedproperties.md).

A captura de tela a seguir mostra os botões **aumentar fonte** e **redução de fonte** da faixa de opções [**FontControl**](windowsribbon-element-fontcontrol.md).

![captura de tela dos botões aumentar fonte e reduzir fonte no fontcontrol.](images/markup/fontcontrol-incdec.png)

A tabela a seguir descreve os valores da propriedade.



|     Valor                 |  Descrição                    |
|---------------------------|---------------------------------|
| `UI_FONTDELTASIZE_GROW`   | Botão **aumentar fonte** clicado.   |
| `UI_FONTDELTASIZE_SHRINK` | Botão **reduzir fonte** clicado. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Propriedades de controle de fonte](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**FONTDELTASIZE da interface do usuário \_**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontdeltasize)
</dt> <dt>

[Controle de fonte](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 