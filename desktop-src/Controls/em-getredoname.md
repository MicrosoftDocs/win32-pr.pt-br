---
title: EM_GETREDONAME mensagem (Richedit.h)
description: Recupera o tipo da próxima ação, se alguma, na fila refazer do controle de edição rich.
ms.assetid: 8649236f-32dc-45d3-847e-c9f65ffba44c
keywords:
- EM_GETREDONAME controles de Windows mensagem
topic_type:
- apiref
api_name:
- EM_GETREDONAME
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9687ae54223ec7cc0f908d747eff2504216b79469b5f285863f8c8ffdfe91b3b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048816"
---
# <a name="em_getredoname-message"></a>Mensagem EM \_ GETREDONAME

Recupera o tipo da próxima ação, se alguma, na fila refazer do controle de edição rich.

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

Se a fila de refazer para o controle não estiver vazia, o valor retornado será um valor de enumeração [**UNDONAMEID**](/windows/desktop/api/Richedit/ne-richedit-undonameid) que indica o tipo da próxima ação na fila de refazer do controle.

Se não houver nenhuma ação redoável ou o tipo da próxima ação redoável for desconhecido, o valor de retorno será zero.

## <a name="remarks"></a>Comentários

Os tipos de ações que podem ser desfeitas ou refeitas incluem operações de digitação, exclusão, arrastar e soltar, recortar e colar. Essas informações podem ser úteis para aplicativos que fornecem uma interface do usuário estendida para operações de desfazer e refazer, como uma caixa de listagem lista de ações redoáveis.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**EM \_ GETUNDONAME**](em-getundoname.md)
</dt> <dt>

[**EM \_ REDO**](em-redo.md)
</dt> <dt>

[**EM \_ UNDO**](em-undo.md)
</dt> <dt>

[**UNDONAMEID**](/windows/desktop/api/Richedit/ne-richedit-undonameid)
</dt> </dl>

 

 





