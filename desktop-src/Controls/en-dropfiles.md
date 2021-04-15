---
title: EN_DROPFILES código de notificação (RichEdit. h)
description: Notifica uma janela pai do controle de edição rico que o usuário está tentando soltar arquivos no controle. Um controle de edição rico envia esse código de notificação na forma de uma \_ mensagem de notificação do WM quando recebe \_ a mensagem DropFiles do WM.
ms.assetid: fcae0ff8-ce37-4c71-b14c-cbd6429b4ab3
keywords:
- EN_DROPFILES de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- EN_DROPFILES
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72c0ed1a4a9b95348b1de20e54fcf3b167df19f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454705"
---
# <a name="en_dropfiles-notification-code"></a>\_Código de notificação en DropFiles

Notifica uma janela pai do controle de edição rico que o usuário está tentando soltar arquivos no controle. Um controle de edição rico envia esse código de notificação na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) quando recebe a mensagem [**\_ DropFiles do WM**](/windows/desktop/shell/wm-dropfiles) .


```C++
EN_DROPFILES

      penDropFiles = (ENDROPFILES *) lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Uma estrutura [**ENDROPFILES**](/windows/desktop/api/Richedit/ns-richedit-endropfiles) que recebe informações de arquivos soltos.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornar um valor diferente de zero para permitir a operação DROP.

Retornar zero para ignorar a operação de soltar.

## <a name="remarks"></a>Comentários

Para um controle de edição rico receber mensagens do [**WM \_ DropFiles**](/windows/desktop/shell/wm-dropfiles) , a janela pai deve registrar o controle como um destino de soltar usando a função [**DragAcceptFiles**](/windows/desktop/api/shellapi/nf-shellapi-dragacceptfiles) . O controle não se registra.

Para receber \_ códigos de notificação do en DropFiles, especifique [**enm \_ DropFiles**](rich-edit-control-event-mask-flags.md) na máscara enviada com a mensagem em [**\_ SETEVENTMASK**](em-seteventmask.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**ENDROPFILES**](/windows/desktop/api/Richedit/ns-richedit-endropfiles)
</dt> </dl>

 

