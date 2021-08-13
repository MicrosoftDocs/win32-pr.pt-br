---
title: EM_STOPGROUPTYPING mensagem (Richedit.h)
description: Impede que um controle de edição rico colete ações de digitação adicionais na ação de desfazer atual. O controle armazena a próxima ação de digitação, se alguma, em uma nova ação na fila de desfazer.
ms.assetid: 3059826f-84d1-4b7b-b4a8-da17d5f41013
keywords:
- EM_STOPGROUPTYPING controles de Windows mensagem
topic_type:
- apiref
api_name:
- EM_STOPGROUPTYPING
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e62a5d652218b24240ce612851c4c08e335b31230532bc778bb44c5d7e74854
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118672274"
---
# <a name="em_stopgrouptyping-message"></a>Mensagem EM \_ STOPGROUPTYPING

Impede que um controle de edição rico colete ações de digitação adicionais na ação de desfazer atual. O controle armazena a próxima ação de digitação, se alguma, em uma nova ação na fila de desfazer.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Não usado; deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Não usado; deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno é zero. Essa mensagem não pode falhar.

## <a name="remarks"></a>Comentários

Um controle de edição rica grupos de ações de digitação consecutivas, incluindo caracteres excluídos usando a chave **BackSpace,** em uma única ação desfazer até que um dos seguintes eventos ocorra:

-   O controle recebe uma **mensagem EM \_ STOPGROUPTYPING.**
-   O controle perde o foco.
-   O usuário move a seleção atual usando as teclas de direção ou clicando no mouse.
-   O usuário pressiona a **tecla Delete.**
-   O usuário executa qualquer outra ação, como uma operação de colar que **não envolva** digitação.

Você pode enviar a mensagem **EM \_ STOPGROUPTYPING** para interromper ações de digitação consecutivas em grupos de desfazer menores. Por exemplo, você pode enviar **EM \_ STOPGROUPTYPING após** cada caractere ou em cada quebra de palavra.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**EM \_ UNDO**](em-undo.md)
</dt> </dl>

 

 





