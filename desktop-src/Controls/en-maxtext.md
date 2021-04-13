---
title: Código de notificação EN_MAXTEXT (WinUser. h)
description: Enviado quando a inserção do texto atual excedeu o número especificado de caracteres para o controle de edição.
ms.assetid: b03835d6-d06f-415a-97f2-d2b62b17e175
keywords:
- EN_MAXTEXT de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- EN_MAXTEXT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 454b48fb232f2225696efacc44d54660d3a83185
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499668"
---
# <a name="en_maxtext-notification-code"></a>\_Código de notificação en MAXTEXT

Enviado quando a inserção do texto atual excedeu o número especificado de caracteres para o controle de edição. A inserção do texto foi truncada.

Esse código de notificação também é enviado quando um controle de edição não tem o estilo [**es \_ AUTOHSCROLL**](edit-control-styles.md) e o número de caracteres a serem inseridos excede a largura do controle de edição.

Esse código de notificação também é enviado quando um controle de edição não tem o estilo [**es \_ AUTOVSCROLL**](edit-control-styles.md) e o número total de linhas resultante de uma inserção de texto excede a altura do controle de edição.

A janela pai do controle de edição recebe esse código de notificação por meio de uma mensagem de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) .


```C++
EN_MAXTEXT

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

A janela pai sempre recebe uma mensagem de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) para esse evento, ela não requer uma máscara de notificação enviada com em [**\_ SETEVENTMASK**](em-seteventmask.md).

**Edição avançada:** Com suporte no Microsoft Rich Edit 1,0 e posterior. Para obter informações sobre a compatibilidade das versões de edição rica com as várias versões do sistema, consulte [sobre controles de edição avançados](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**comando do WM \_**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

