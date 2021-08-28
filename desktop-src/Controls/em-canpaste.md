---
title: Mensagem de EM_CANPASTE (RichEdit. h)
description: Determina se um controle de edição rico pode colar um formato de área de transferência especificado.
ms.assetid: 1b858ad8-1312-407b-b12a-c63668ba9f72
keywords:
- controles de Windows de mensagem de EM_CANPASTE
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
ms.openlocfilehash: 24f2d831cd3b3d04fcb7859d2b5936b7354fbb6b638558d605c9f8c5a6ee6333
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916056"
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

## <a name="return-value"></a>Valor retornado

Se o formato da área de transferência puder ser colado, o valor de retorno será um valor diferente de zero.

Se o formato da área de transferência não puder ser colado, o valor de retorno será zero.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> </dl>

 

