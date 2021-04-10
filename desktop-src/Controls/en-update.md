---
title: Código de notificação EN_UPDATE (WinUser. h)
description: Enviado quando um controle de edição está prestes a ser redesenhado.
ms.assetid: 59138736-6cc9-4a3f-95f3-ada9cbf253cb
keywords:
- EN_UPDATE de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- EN_UPDATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df0b045efcfb5d50cb2a85c9ae230e215263aa2e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086179"
---
# <a name="en_update-notification-code"></a>\_Código de notificação de atualização en

Enviado quando um controle de edição está prestes a ser redesenhado. Esse código de notificação é enviado depois que o controle tiver formatado o texto, mas antes de exibir o texto. Isso torna possível redimensionar a janela de controle de edição, se necessário. A janela pai do controle de edição recebe esse código de notificação por meio de uma mensagem de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) .


```C++
EN_UPDATE

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

**Edição avançada 1,0:** Para receber \_ códigos de notificação de atualização do en, especifique [**enm \_ Update**](rich-edit-control-event-mask-flags.md) na máscara enviada com a mensagem em [**\_ SETEVENTMASK**](em-seteventmask.md) .

**Edição avançada 2,0 e posterior:** O sinalizador de [**\_ atualização do enm**](rich-edit-control-event-mask-flags.md) é ignorado. O \_ código de notificação de atualização en sempre é recebido. No entanto, quando o Microsoft Rich Edit 3,0 emula o Microsoft Rich Edit 1,0, para receber \_ códigos de notificação de atualização, você deve especificar **enm \_ Update** na máscara enviada com a mensagem em [**\_ SETEVENTMASK**](em-seteventmask.md) .

Para obter informações sobre a compatibilidade das versões de edição rica com as várias versões do sistema, consulte [sobre controles de edição avançados](about-rich-edit-controls.md).

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

[alteração de EN \_](en-change.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**comando do WM \_**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

