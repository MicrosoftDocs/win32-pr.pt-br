---
title: Código de notificação EN_HSCROLL (WinUser. h)
description: Enviado quando o usuário clica na barra de rolagem horizontal do controle de edição. A janela pai do controle de edição recebe esse código de notificação por meio de uma mensagem de comando do WM \_ . A janela pai é notificada antes da atualização da tela.
ms.assetid: beaaa80c-4108-4a8e-aed8-04c9a3a08f3e
keywords:
- EN_HSCROLL de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- EN_HSCROLL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6f90f6e781409419e39390e64251506b4cc915a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824521"
---
# <a name="en_hscroll-notification-code"></a>\_Código de notificação en HSCROLL

Enviado quando o usuário clica na barra de rolagem horizontal do controle de edição. A janela pai do controle de edição recebe esse código de notificação por meio de uma mensagem de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) . A janela pai é notificada antes da atualização da tela.


```C++
EN_HSCROLL

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

Este código de notificação é enviado para os seguintes eventos de mouse na barra de rolagem horizontal: clicando no botão de seta ou clicando entre o botão de seta e o polegar. No entanto, o código de notificação não é enviado ao clicar no polegar da barra de rolagem. O código de notificação também é enviado quando um evento de teclado causa uma alteração na área de exibição do controle de edição, por exemplo, pressionando HOME, END, seta para a esquerda ou seta para a direita.

**Edição avançada:** Com suporte no Microsoft Rich Edit 1,0 e posterior. Para receber códigos de notificação do **en \_ HSCROLL** , especifique [**enm \_ Scroll**](rich-edit-control-event-mask-flags.md) na máscara enviada com a mensagem [**\_ SETEVENTMASK**](em-seteventmask.md) . Para obter informações sobre a compatibilidade das versões de edição rica com as várias versões do sistema, consulte [sobre controles de edição avançados](about-rich-edit-controls.md).

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

[VSCROLL de EN \_](en-vscroll.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**comando do WM \_**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

