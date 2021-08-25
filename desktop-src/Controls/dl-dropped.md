---
title: DL_DROPPED código de notificação (commctrl. h)
description: Sinaliza que o usuário concluiu uma operação de arrastar liberando o botão esquerdo do mouse. Uma caixa de listagem de arrastar envia esse código de notificação para sua janela pai na forma de uma mensagem de arrastar lista. Para obter mais informações, consulte arrastar mensagens da caixa de listagem.
ms.assetid: 81b9b424-2735-407d-bac9-f03ea2f48b4e
keywords:
- DL_DROPPED código de notificação Windows controles
topic_type:
- apiref
api_name:
- DL_DROPPED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c245cbb85a4e67845bd86a25b4cccb2f2aa0dc1d9d9613afd1d685037c5e1ef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002716"
---
# <a name="dl_dropped-notification-code"></a>\_Código de notificação removido da DL

Sinaliza que o usuário concluiu uma operação de arrastar liberando o botão esquerdo do mouse. Uma caixa de listagem de arrastar envia esse código de notificação para sua janela pai na forma de uma mensagem de arrastar lista. Para obter mais informações, consulte [arrastar mensagens da caixa de listagem](about-list-boxes.md).


```C++
DL_DROPPED

    pDragInfo = (LPARAM)(LPDRAGLISTINFO) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma estrutura [**DRAGLISTINFO**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo) que contém o \_ código de notificação DL removido, o identificador para a caixa de listagem de arrastar e a posição do cursor.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Esse código de notificação normalmente é processado pela inserção do item que está sendo arrastado para a lista na frente do item sob o cursor. Para recuperar o índice do item na posição do cursor, use a função [**LBItemFromPt**](/windows/desktop/api/Commctrl/nf-commctrl-lbitemfrompt) . Observe que o \_ código de notificação DL removido é enviado mesmo que o cursor não esteja em um item de lista. Nesse caso, **LBItemFromPt** retorna-1.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





