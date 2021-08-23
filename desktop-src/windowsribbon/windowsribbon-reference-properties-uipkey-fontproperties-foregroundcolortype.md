---
title: UI_PKEY_FontProperties_ForegroundColorType
description: Identifica a propriedade \_ \_ FontProperties \_ ForegroundColorType da IU PKEY.
ms.assetid: ab04c0b0-911f-4649-9ce8-5ecd847abf9f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d26b324a4e504c5ef98850f2bbcabd55b34525650b0ecfd3c201d45896e0c800
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118438645"
---
# <a name="ui_pkey_fontproperties_foregroundcolortype"></a>\_ \_ FontProperties \_ ForegroundColorType da interface do usuário

Identifica a propriedade \_ \_ FontProperties \_ ForegroundColorType da IU PKEY.

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

A interface do usuário PKEY FontProperties ForegroundColorType é usada por um aplicativo, em conjunto com a interface do usuário \_ \_ \_ [ \_ PKEY \_ FontProperties \_ ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md), para consultar as **configurações da** galeria de cores do texto.

O valor da propriedade é da [**enumeração \_ SWATCHCOLORTYPE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype) da interface do usuário.

O valor padrão é `UI_SWATCHCOLORTYPE_RGB`.

A tabela a seguir descreve os valores da propriedade.



|     Valor                           |     Descrição                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `UI_SWATCHCOLORTYPE_NOCOLOR`   | Sem suporte do [**FontControl.**](windowsribbon-element-fontcontrol.md)                                                                                                                                                                                                                                                                                                                                        |
| `UI_SWATCHCOLORTYPE_AUTOMATIC` | O aplicativo deve consultar a métrica do sistema apropriada para  o valor de cor normalmente Windows cor de texto do tema atual que é recuperada com GetSysColor(COLOR \_ WINDOWTEXT).                                                                                                                                                                                                                                  |
| `UI_SWATCHCOLORTYPE_RGB`       | O aplicativo deve consultar [ \_ \_ FontProperties \_ ForegroundColor da interface](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md) do usuário para o valor de cor. O valor de cor da interface do usuário [ \_ PKEY \_ FontProperties \_ ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md) é exibido no botão Cor do texto e selecionado na **Galeria de cores do** texto. <br/> |



 

A interface do usuário PKEY FontProperties ForegroundColorType é passada para o método de retorno de chamada \_ \_ \_ [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute)  quando um swatch de cor é selecionado em uma galeria de [**cores de Texto FontControl.**](windowsribbon-element-fontcontrol.md)

> [!Note]  
> É altamente recomendável que o  aplicativo desem conjunto apenas um valor de cor de texto inicial e não de novo esse valor quando o cursor é reposicionado dentro de um documento. A última seleção deve ser mantida para evitar a necessidade de selecionar a cor desejada.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Propriedades do controle de fonte](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**UI \_ SWATCHCOLORTYPE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype)
</dt> <dt>

[Controle de fonte](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

