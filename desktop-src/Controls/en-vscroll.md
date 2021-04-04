---
title: Código de notificação EN_VSCROLL (WinUser. h)
description: Enviado quando o usuário clica na barra de rolagem vertical do controle de edição ou quando o usuário rola a roda do mouse sobre o controle de edição.
ms.assetid: 46307dee-3c5c-4020-9c2b-ec4638a0cea5
keywords:
- EN_VSCROLL de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- EN_VSCROLL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de1f99b9ea05d037b5c00562a24bda1e434ce08d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824793"
---
# <a name="en_vscroll-notification-code"></a>\_Código de notificação en VSCROLL

Enviado quando o usuário clica na barra de rolagem vertical do controle de edição ou quando o usuário rola a roda do mouse sobre o controle de edição. A janela pai do controle de edição recebe esse código de notificação por meio de uma mensagem de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) . A janela pai é notificada antes da atualização da tela.


```C++
EN_VSCROLL

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contém o identificador do controle de edição. O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica o código de notificação.

</dd> <dt>

*lParam* 
</dt> <dd>

Um identificador para o controle de edição.

</dd> </dl>

## <a name="remarks"></a>Comentários

Esta mensagem é enviada para os seguintes eventos de mouse na barra de rolagem vertical: clicando no botão de seta ou clicando entre o botão de seta e o polegar. No entanto, a mensagem não é enviada ao clicar no próprio mouse da barra de rolagem. A mensagem também é enviada quando um evento de teclado causa uma alteração na área de exibição do controle de edição, por exemplo, pressionando HOME, END, PAGE UP, PAGE DOWN, seta para cima ou seta para baixo.

A roda do mouse é um mouse que tem uma roda central que rola. Para obter mais informações, consulte "a roda do mouse" [sobre a entrada do mouse](/windows/desktop/inputdev/about-mouse-input).

**Edição avançada:** Com suporte no Microsoft Rich Edit 1,0 e posterior. Para receber \_ códigos de notificação do en VSCROLL, especifique [**enm \_ Scroll**](rich-edit-control-event-mask-flags.md) na máscara enviada com a mensagem [**\_ SETEVENTMASK**](em-seteventmask.md) . Para obter informações sobre a compatibilidade das versões de edição rica com as várias versões do sistema, consulte [sobre controles de edição avançados](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[HSCROLL de EN \_](en-hscroll.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Usando controles de edição](using-edit-controls.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**comando do WM \_**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

