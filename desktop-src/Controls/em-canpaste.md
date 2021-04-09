---
title: Mensagem de EM_CANPASTE (RichEdit. h)
description: Determina se um controle de edição rico pode colar um formato de área de transferência especificado.
ms.assetid: 1b858ad8-1312-407b-b12a-c63668ba9f72
keywords:
- Controles de EM_CANPASTE de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_CANPASTE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aad400b610a033b6f67177da99876a892d294ec8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009529"
---
# <a name="em_canpaste-message"></a>\_Mensagem em CANpaste

Determina se um controle de edição rico pode colar um formato de área de transferência especificado.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica os [formatos da área de transferência](/windows/desktop/dataxchg/clipboard-formats) a serem experimentados. Para testar qualquer formato atualmente na área de transferência, defina esse parâmetro como zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Esse parâmetro não é usado; Ele deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se o formato da área de transferência puder ser colado, o valor de retorno será um valor diferente de zero.

Se o formato da área de transferência não puder ser colado, o valor de retorno será zero.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> </dl>

 

