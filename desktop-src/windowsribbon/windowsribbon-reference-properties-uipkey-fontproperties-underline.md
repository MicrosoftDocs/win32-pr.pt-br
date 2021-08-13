---
title: UI_PKEY_FontProperties_Underline
description: Identifica a propriedade sublinhada \_ \_ FontProperties PKEY da interface do \_ usuário.
ms.assetid: 88492558-ab19-4606-8fe0-5f100677b88a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b75142e08549c2084ebcd37e82943ed63fdfb5b278faef01c4ad79441fa36915
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118706712"
---
# <a name="ui_pkey_fontproperties_underline"></a>\_Sublinhado FontProperties de PKEY \_ \_ da interface do usuário

Identifica a propriedade sublinhada \_ \_ FontProperties PKEY da interface do \_ usuário.

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

O sublinhado FontProperties PKEY da interface do usuário é usado por um aplicativo para consultar o \_ \_ estado do botão \_ **Sublinhado.**

O valor da propriedade é da [**enumeração \_ FONTUNDERLINE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontunderline) da interface do usuário.

O valor padrão é `UI_FONTUNDERLINE_NOTSET`.

A captura de tela a seguir mostra **o botão Sublinhado** do FontControl da Faixa [**de Opções.**](windowsribbon-element-fontcontrol.md)

![captura de tela do elemento fontcontrol com o atributo richfont definido como true.](images/markup/fontcontrol-underline.png)

A tabela a seguir descreve as propriedades e o resultado da interface do usuário.



|      Propriedade                   |       Resultado da interface do usuário                                                          |
|---------------------------------|--------------------------------------------------------------------------|
| `UI_FONTUNDERLINE_NOTAVAILABLE` | **O botão** sublinhado está desabilitado e só pode ser definido pelo aplicativo. |
| `UI_FONTUNDERLINE_NOTSET`       | **O botão** Sublinhado não está selecionado.                                    |
| `UI_FONTUNDERLINE_SET`          | **O botão** Sublinhado está selecionado.                                        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Propriedades do controle de fonte](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**\_FONTUNDERLINE DA INTERFACE DO USUÁRIO**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontunderline)
</dt> <dt>

[Controle de fonte](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 