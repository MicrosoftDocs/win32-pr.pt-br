---
title: EN_SAVECLIPBOARD código de notificação (RichEdit. h)
description: Notifica a janela pai do controle de edição rico que o controle está fechando e a área de transferência contém informações. Um controle de edição rico envia esse código de notificação na forma de uma \_ mensagem de notificação do WM.
ms.assetid: e8b95e80-6494-4153-8e78-ede9ed17c66f
keywords:
- EN_SAVECLIPBOARD de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- EN_SAVECLIPBOARD
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a1fd7c6e11ed82a7f77483c692dd68f860395c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824340"
---
# <a name="en_saveclipboard-notification-code"></a>\_Código de notificação en SAVECLIPBOARD

Notifica a janela pai do controle de edição rico que o controle está fechando e a área de transferência contém informações. Um controle de edição rico envia esse código de notificação na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
EN_SAVECLIPBOARD

    penSaveClipboard = (ENSAVECLIPBOARD *) lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Uma estrutura [**ENSAVECLIPBOARD**](/windows/desktop/api/Richedit/ns-richedit-ensaveclipboard) que contém informações sobre informações da área de transferência.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna zero se a área de transferência deve ser disponibilizada para outros aplicativos.

Retorna um valor diferente de zero se a área de transferência não deve ser salva.

## <a name="remarks"></a>Comentários

A janela pai sempre obterá uma mensagem de [**\_ notificação do WM**](wm-notify.md) para esse evento; ela não requer uma máscara de notificação enviada com em [**\_ SETEVENTMASK**](em-seteventmask.md).

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

[**ENSAVECLIPBOARD**](/windows/desktop/api/Richedit/ns-richedit-ensaveclipboard)
</dt> </dl>

 

 





