---
title: UI_PKEY_FontProperties_Underline
description: Identifica a \_ propriedade de \_ sublinhado PKEY fontproperties subinterface \_ .
ms.assetid: 88492558-ab19-4606-8fe0-5f100677b88a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 380c3fdadb636775f80b789a585c42ff2369234a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454182"
---
# <a name="ui_pkey_fontproperties_underline"></a>Interface do usuário \_ PKEY \_ fontproperties \_ sublinhado

Identifica a \_ propriedade de \_ sublinhado PKEY fontproperties subinterface \_ .

```
propertyDescription
   name = UI_PKEY_FontProperties_Underline
   shellPKey = UI_PKEY_FontProperties_Underline
   formatID = 00000305-7363-696e-8441798acf5aebb7
   propID = 305
   typeInfo
      type = UI_FONTUNDERLINE
```

## <a name="remarks"></a>Comentários

A interface do usuário \_ PKEY \_ FontProperty \_ Underline é usada por um aplicativo para consultar o estado do botão **sublinhado** .

O valor da propriedade é da [**enumeração \_ FonteSublinhada da interface do usuário**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontunderline) .

O valor padrão é `UI_FONTUNDERLINE_NOTSET`.

A captura de tela a seguir mostra o botão **sublinhado** da faixa de opções [**FontControl**](windowsribbon-element-fontcontrol.md).

![captura de tela do elemento fontcontrol com o atributo richfont definido como true.](images/markup/fontcontrol-underline.png)

A tabela a seguir descreve as propriedades e o resultado da interface do usuário.



|                                 |                                                                          |
|---------------------------------|--------------------------------------------------------------------------|
| `UI_FONTUNDERLINE_NOTAVAILABLE` | O botão **sublinhado** está desabilitado e só pode ser definido pelo aplicativo. |
| `UI_FONTUNDERLINE_NOTSET`       | O botão **sublinhado** não está selecionado.                                    |
| `UI_FONTUNDERLINE_SET`          | O botão **sublinhado** está selecionado.                                        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Propriedades de controle de fonte](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**FonteSublinhada da interface do usuário \_**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontunderline)
</dt> <dt>

[Controle de fonte](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 