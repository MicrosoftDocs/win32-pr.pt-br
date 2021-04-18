---
title: UI_PKEY_FontProperties_ForegroundColorType
description: Identifica a propriedade da interface do usuário \_ PKEY \_ fontproperties \_ ForegroundColorType.
ms.assetid: ab04c0b0-911f-4649-9ce8-5ecd847abf9f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5589e9b21fc7ab0884a3cac51eba114ee77036b3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366271"
---
# <a name="ui_pkey_fontproperties_foregroundcolortype"></a>Interface do usuário \_ PKEY \_ fontproperties \_ ForegroundColorType

Identifica a propriedade da interface do usuário \_ PKEY \_ fontproperties \_ ForegroundColorType.

```
propertyDescription
   name = UI_PKEY_FontProperties_ForegroundColorType
   shellPKey = UI_PKEY_FontProperties_ForegroundColorType
   formatID = 00000310-7363-696e-8441798acf5aebb7
   propID = 310
   typeInfo
      type = UI_SWATCHCOLORTYPE
```

## <a name="remarks"></a>Comentários

A interface do usuário \_ PKEY \_ fontproperties \_ ForegroundColorType é usada por um aplicativo, em conjunto com a [interface do usuário \_ PKEY \_ fontproperties \_ ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md), para consultar as configurações da Galeria de **cores de texto** .

O valor da propriedade é da [**enumeração \_ SWATCHCOLORTYPE da interface do usuário**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype) .

O valor padrão é `UI_SWATCHCOLORTYPE_RGB`.

A tabela a seguir descreve os valores da propriedade.



|                                |                                                                                                                                                                                                                                                                                                                                                                                                                       |
|--------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `UI_SWATCHCOLORTYPE_NOCOLOR`   | Não há suporte para o [**FontControl**](windowsribbon-element-fontcontrol.md).                                                                                                                                                                                                                                                                                                                                        |
| `UI_SWATCHCOLORTYPE_AUTOMATIC` | O aplicativo deve consultar a métrica de sistema apropriada para o valor de cor normalmente a **cor de texto** do tema do Windows atual que é recuperada com GETSYSCOLOR (Color \_ WINDOWTEXT).                                                                                                                                                                                                                                  |
| `UI_SWATCHCOLORTYPE_RGB`       | O aplicativo deve consultar a [interface do usuário \_ PKEY \_ fontproperties \_ ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md) para o valor de cor. O valor de cor da [interface do usuário \_ PKEY \_ fontproperties \_ ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md) é exibido no botão de **cor do texto** e selecionado na Galeria de cores de **texto** .<br/> |



 

A interface do usuário \_ PKEY \_ fontproperties \_ ForegroundColorType é passada para o método de retorno de chamada [**IUICommandHandler:: execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) quando uma amostra de cor é selecionada em uma galeria de **cores de texto** [**FontControl**](windowsribbon-element-fontcontrol.md) .

> [!Note]  
> É altamente recomendável que o aplicativo defina apenas um valor de **cor de texto** inicial e não redefina esse valor quando o cursor for reposicionado em um documento. A última seleção deve ser mantida para evitar a necessidade de selecionar novamente a cor desejada.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Propriedades de controle de fonte](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**SWATCHCOLORTYPE da interface do usuário \_**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype)
</dt> <dt>

[Controle de fonte](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

