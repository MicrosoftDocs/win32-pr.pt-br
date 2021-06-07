---
title: UI_PKEY_ColorType
description: Identifica a \_ Propriedade ColorType da interface do usuário PKEY \_ .
ms.assetid: 7eaa9d8b-0c21-487c-9093-79ddffcae131
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9240d8c816adcf2674efcc2e7428d22b765f542
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443887"
---
# <a name="ui_pkey_colortype"></a>Cortype da interface do usuário \_ PKEY \_

Identifica a \_ Propriedade ColorType da interface do usuário PKEY \_ .

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

O ColorType da interface do usuário \_ PKEY \_ é usado por um aplicativo para consultar a configuração de cores do controle [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) .

O valor da propriedade é da [**enumeração \_ SWATCHCOLORTYPE da interface do usuário**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype) .



|    Propriedade                            |    Descrição                                                                                                                                                                             |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SWATCHCOLORTYPE da interface do usuário \_ \_   | O aplicativo deve tratar a configuração de cor como transparente. Normalmente usado em conjunto com a configuração cor **sem cor** .                                                   |
| interface do usuário \_ SWATCHCOLORTYPE \_ automática | O aplicativo deve consultar [GetSysColor (Color \_ WINDOWTEXT)](/windows/win32/api/winuser/nf-winuser-getsyscolor). Normalmente usado em conjunto com a configuração de cor **automática** . |
| interface do usuário \_ SWATCHCOLORTYPE \_ RGB       | O aplicativo deve consultar a [ \_ \_ cor de PKEY da interface do usuário](windowsribbon-reference-properties-uipkey-color.md) para a configuração de cor.                                                          |



 

\_O ColorType de PKEY de interface do usuário \_ é passado para o método de retorno de chamada [**IUICommandHandler:: execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) quando uma amostra de cor é selecionada em um [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Propriedades do seletor de cores](windowsribbon-reference-properties-colorpicker.md)
</dt> </dl>

 

 