---
title: Código de notificação EN_CHANGE (WinUser. h)
description: Enviado quando o usuário executou uma ação que pode ter alterado o texto em um controle de edição.
ms.assetid: 8a04e6fb-ae9d-4d94-8047-6de96df899f5
keywords:
- EN_CHANGE de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- EN_CHANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8ef26d1ec4f8ec1dc93e54d46b88c4fe7cc872b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824300"
---
# <a name="en_change-notification-code"></a>& \_ código de notificação de alteração

Enviado quando o usuário executou uma ação que pode ter alterado o texto em um controle de edição. Ao contrário do código de notificação da [ \_ atualização en](en-update.md) , esse código de notificação é enviado depois que o sistema atualiza a tela. A janela pai do controle de edição recebe esse código de notificação por meio de uma mensagem de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) .


```C++
EN_CHANGE

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

**Edição avançada:** Com suporte no Microsoft Rich Edit 1,0 e posterior. Para receber \_ códigos de notificação de alteração, [**especifique enm \_ alteração**](rich-edit-control-event-mask-flags.md) na máscara enviada com a mensagem em [**\_ SETEVENTMASK**](em-seteventmask.md) . Para obter informações sobre a compatibilidade das versões de edição rica com as várias versões do sistema, consulte [sobre controles de edição avançados](about-rich-edit-controls.md).

O \_ código de notificação de alteração en não é enviado quando o estilo [**\_ multilinha es**](edit-control-styles.md) é usado e o texto é enviado por meio do [**WM \_ SetText**](/windows/desktop/winmsg/wm-settext).

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

[atualização do EN \_](en-update.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**comando do WM \_**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

