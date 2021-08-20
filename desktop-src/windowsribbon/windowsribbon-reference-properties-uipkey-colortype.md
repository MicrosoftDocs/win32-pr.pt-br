---
title: UI_PKEY_ColorType
description: Identifica a propriedade \_ ColorType PKEY \_ da interface do usuário.
ms.assetid: 7eaa9d8b-0c21-487c-9093-79ddffcae131
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4e676db37c0ac6c868c3bbbe20145b171fd63a88d1a704717be58cb5d71b6a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118031763"
---
# <a name="ui_pkey_colortype"></a>ColorType \_ PKEY \_ da interface do usuário

Identifica a propriedade \_ ColorType PKEY \_ da interface do usuário.

```
propertyDescription
   name = UI_PKEY_ColorType
   shellPKey = UI_PKEY_ColorType
   formatID = 00000401-7363-696e-8441798acf5aebb7
   propID = 401
   typeInfo
      type = UI_SWATCHCOLORTYPE
```

## <a name="remarks"></a>Comentários

ColorType PKEY da interface do usuário é usado por um aplicativo para \_ \_ consultar a configuração de cor do controle [**DropDownColorPicker.**](windowsribbon-element-dropdowncolorpicker.md)

O valor da propriedade é da [**enumeração \_ SWATCHCOLORTYPE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype) da interface do usuário.



|    Propriedade                            |    Descrição                                                                                                                                                                             |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| UI \_ SWATCHCOLORTYPE \_ NOCOLOR   | O aplicativo deve tratar a configuração de cor como transparente. Normalmente usado em conjunto com a **configuração Nenhuma cor** de cor.                                                   |
| UI \_ SWATCHCOLORTYPE \_ AUTOMATIC | O aplicativo deve consultar [GetSysColor(COLOR \_ WINDOWTEXT).](/windows/win32/api/winuser/nf-winuser-getsyscolor) Normalmente usado em conjunto com a **configuração de Cor** automática. |
| UI \_ SWATCHCOLORTYPE \_ RGB       | O aplicativo deve consultar a [cor \_ PKEY da interface \_ do usuário](windowsribbon-reference-properties-uipkey-color.md) para a configuração de cor.                                                          |



 

ColorType PKEY da interface do usuário é passado para o método de retorno de chamada \_ \_ [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) quando uma amostra de cor é selecionada em [**um DropDownColorPicker.**](windowsribbon-element-dropdowncolorpicker.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Seletor de Cor propriedades](windowsribbon-reference-properties-colorpicker.md)
</dt> </dl>

 

 