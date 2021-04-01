---
title: DL_DROPPED código de notificação (commctrl. h)
description: Sinaliza que o usuário concluiu uma operação de arrastar liberando o botão esquerdo do mouse. Uma caixa de listagem de arrastar envia esse código de notificação para sua janela pai na forma de uma mensagem de arrastar lista. Para obter mais informações, consulte arrastar mensagens da caixa de listagem.
ms.assetid: 81b9b424-2735-407d-bac9-f03ea2f48b4e
keywords:
- DL_DROPPED de código de notificação controles do Windows
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
ms.openlocfilehash: e1b2480360ea38a00c4dd8efe6eb84eed8999890
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824870"
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

## <a name="return-value"></a>Retornar valor

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Esse código de notificação normalmente é processado pela inserção do item que está sendo arrastado para a lista na frente do item sob o cursor. Para recuperar o índice do item na posição do cursor, use a função [**LBItemFromPt**](/windows/desktop/api/Commctrl/nf-commctrl-lbitemfrompt) . Observe que o \_ código de notificação DL removido é enviado mesmo que o cursor não esteja em um item de lista. Nesse caso, **LBItemFromPt** retorna-1.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





