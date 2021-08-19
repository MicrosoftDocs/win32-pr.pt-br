---
title: UI_PKEY_FontProperties_BackgroundColorType
description: Identifica a propriedade \_ \_ FontProperties BackgroundColorType da interface do \_ usuário PKEY.
ms.assetid: d93f4d9f-3d35-4066-be94-f6b6b4302bff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a28bd653b3bcf62eaf8cab797b3bc45d97b88e15bef4bb0fdd3407bdd95ca28e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118438665"
---
# <a name="ui_pkey_fontproperties_backgroundcolortype"></a>\_ \_ FontProperties \_ BackgroundColorType da interface do usuário PKEY

Identifica a propriedade \_ \_ FontProperties BackgroundColorType da interface do \_ usuário PKEY.

```
propertyDescription
   name = UI_PKEY_FontProperties_BackgroundColorType
   shellPKey = UI_PKEY_FontProperties_BackgroundColorType
   formatID = 00000311-7363-696e-8441798acf5aebb7
   propID = 311
   typeInfo
      type = UI_SWATCHCOLORTYPE
```

## <a name="remarks"></a>Comentários

UI PKEY FontProperties BackgroundColorType é usado por um aplicativo, em conjunto com a interface do usuário \_ \_ \_ [ \_ PKEY \_ FontProperties \_ BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor),  para consultar as configurações da galeria de cores de realçadas de texto.

O valor da propriedade é da [**enumeração \_ SWATCHCOLORTYPE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype) da interface do usuário.

O valor padrão é `UI_SWATCHCOLORTYPE_RGB`.

A tabela a seguir descreve os valores da propriedade.



|   Propriedade                             |   Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `UI_SWATCHCOLORTYPE_NOCOLOR`   | O aplicativo deve consultar a métrica do sistema apropriada para  o valor de cor normalmente a cor da tela de fundo da janela Windows tema atual que é recuperada com GetSysColor(COLOR \_ WINDOW).                                                                                                                                                                                                                                                                 |
| `UI_SWATCHCOLORTYPE_AUTOMATIC` | Sem suporte do [**FontControl.**](windowsribbon-element-fontcontrol.md)                                                                                                                                                                                                                                                                                                                                                                                |
| `UI_SWATCHCOLORTYPE_RGB`       | O aplicativo deve consultar [ \_ \_ FontProperties \_ BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor) da interface do usuário para o valor de cor. O valor de cor da interface do usuário [ \_ PKEY \_ FontProperties \_ BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor) é exibido no botão Cor de realçada de texto e selecionado na Galeria de cores de **realçada de** texto. <br/> |



 

FontProperties BackgroundColorType da interface do usuário PKEY é passado para o método de retorno de chamada \_ \_ \_ [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute)  quando um swatch de cor é selecionado em uma galeria de cores de realçamento de Texto [**FontControl.**](windowsribbon-element-fontcontrol.md)

> [!Note]  
> É altamente recomendável que o  aplicativo desem conjunto apenas um valor de cor de realçaamento de texto inicial e não de novo esse valor quando o cursor é reposicionado dentro de um documento. A última seleção deve ser mantida para evitar a necessidade de selecionar a cor desejada.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Propriedades do controle de fonte](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**UI \_ SWATCHCOLORTYPE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype)
</dt> <dt>

[Controle de fonte](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

