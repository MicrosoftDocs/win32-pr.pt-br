---
title: EN_IMECHANGE código de notificação (RichEdit. h)
description: Notifica um pai do controle de edição rico de que o status de conversão do IME foi alterado.
ms.assetid: 2893e4ef-5904-4a57-95c5-3f6cfbb60d90
keywords:
- EN_IMECHANGE de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- EN_IMECHANGE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fa0e0c8fe4e7d6d8de876a5d1a1fb7a10754096
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009401"
---
# <a name="en_imechange-notification-code"></a>\_Código de notificação en IMECHANGE

Notifica um pai do controle de edição rico de que o status de conversão do IME foi alterado. Esse código de notificação está disponível *apenas* para versões em idiomas asiáticos do sistema operacional. Um controle de edição rico envia esse código de notificação na forma de uma mensagem de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) .


```C++
EN_IMECHANGE

    WPARAM wParam
    LPARAM lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contém o identificador do controle de edição rico. O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica o código de notificação.

</dd> <dt>

*lParam* 
</dt> <dd>

Manipular para o controle de edição rico.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse código de notificação retorna zero.

## <a name="remarks"></a>Comentários

Para receber \_ códigos de notificação do en IMECHANGE, especifique [**enm \_ IMECHANGE**](rich-edit-control-event-mask-flags.md) na máscara enviada com a mensagem em [**\_ SETEVENTMASK**](em-seteventmask.md) .

> [!Note]  
> Esse código de notificação só tem suporte na versão asiática do Rich Edit 1,0. Não há suporte para ele em versões posteriores. Para obter informações sobre a compatibilidade das versões de edição rica com as várias versões do sistema, consulte [sobre controles de edição avançados](about-rich-edit-controls.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Outros recursos**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**comando do WM \_**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

