---
title: UI_PKEY_FontProperties_BackgroundColorType
description: Identifica a propriedade backgroundcolortype da interface do usuário \_ PKEY \_ FontProperty \_ .
ms.assetid: d93f4d9f-3d35-4066-be94-f6b6b4302bff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 568898cb2706eb932ea708f929aa4791f0643c74
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454102"
---
# <a name="ui_pkey_fontproperties_backgroundcolortype"></a>IU \_ PKEY \_ FontProperty \_ backgroundcolortype

Identifica a propriedade backgroundcolortype da interface do usuário \_ PKEY \_ FontProperty \_ .

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

A interface do usuário \_ PKEY \_ FontProperty \_ backgroundcolortype é usada por um aplicativo, em conjunto com a [interface do usuário \_ PKEY \_ fontproperties \_ backgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor), para consultar as configurações da Galeria de **cores de realce de texto** .

O valor da propriedade é da [**enumeração \_ SWATCHCOLORTYPE da interface do usuário**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype) .

O valor padrão é `UI_SWATCHCOLORTYPE_RGB`.

A tabela a seguir descreve os valores da propriedade.



|                                |                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `UI_SWATCHCOLORTYPE_NOCOLOR`   | O aplicativo deve consultar a métrica do sistema apropriada para o valor de cor normalmente a **cor de fundo da janela** de tema atual do Windows que é recuperada com GetSysColor (janela de cores \_ ).                                                                                                                                                                                                                                                                 |
| `UI_SWATCHCOLORTYPE_AUTOMATIC` | Não há suporte para o [**FontControl**](windowsribbon-element-fontcontrol.md).                                                                                                                                                                                                                                                                                                                                                                                |
| `UI_SWATCHCOLORTYPE_RGB`       | O aplicativo deve consultar a [interface do usuário \_ PKEY \_ fontproperties \_ backgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor) para o valor de cor. O valor de cor da [interface do usuário \_ PKEY \_ fontproperties \_ backgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor) é exibido no botão de **cor de realce de texto** e selecionado na Galeria de cores de **realce de texto** .<br/> |



 

A interface do usuário \_ PKEY \_ FontProperty \_ backgroundcolortype é passada para o método de retorno de chamada [**IUICommandHandler:: execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) quando uma amostra de cor é selecionada em uma galeria de **cores de realce de texto** [**FontControl**](windowsribbon-element-fontcontrol.md) .

> [!Note]  
> É altamente recomendável que o aplicativo defina apenas um valor de **cor de realce de texto** inicial e não redefina esse valor quando o cursor for reposicionado em um documento. A última seleção deve ser mantida para evitar a necessidade de selecionar novamente a cor desejada.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Propriedades de controle de fonte](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**SWATCHCOLORTYPE da interface do usuário \_**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype)
</dt> <dt>

[Controle de fonte](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

