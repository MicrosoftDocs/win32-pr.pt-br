---
title: Mensagem de EM_STOPGROUPTYPING (RichEdit. h)
description: Interrompe um controle de edição rico da coleta de ações de digitação adicionais na ação de desfazer atual. O controle armazena a próxima ação de digitação, se houver, em uma nova ação na fila de desfazer.
ms.assetid: 3059826f-84d1-4b7b-b4a8-da17d5f41013
keywords:
- Controles de EM_STOPGROUPTYPING de mensagens do Windows
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
ms.openlocfilehash: eced7ff12526296552e4adcc38c927ae94ee0502
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644583"
---
# <a name="em_stopgrouptyping-message"></a>\_Mensagem em STOPGROUPTYPING

Interrompe um controle de edição rico da coleta de ações de digitação adicionais na ação de desfazer atual. O controle armazena a próxima ação de digitação, se houver, em uma nova ação na fila de desfazer.

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

## <a name="return-value"></a>Retornar valor

O valor de retorno é zero. Esta mensagem não pode falhar.

## <a name="remarks"></a>Comentários

Um controle de edição rico agrupa ações de digitação consecutivas, incluindo caracteres excluídos usando a tecla **Backspace** , em uma única ação desfazer até que um dos seguintes eventos ocorra:

-   O controle recebe uma mensagem em **\_ STOPGROUPTYPING** .
-   O controle perde o foco.
-   O usuário move a seleção atual, seja usando as teclas de direção ou clicando com o mouse.
-   O usuário pressiona a tecla **delete** .
-   O usuário executa qualquer outra ação, como uma operação de colagem que não **envolve a** digitação.

Você pode enviar a mensagem em **\_ STOPGROUPTYPING** para interromper as ações de digitação consecutivas em grupos de desfazer menores. Por exemplo, você poderia enviar **em \_ STOPGROUPTYPING** depois de cada caractere ou de cada quebra de palavra.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**em \_ desfazer**](em-undo.md)
</dt> </dl>

 

 





