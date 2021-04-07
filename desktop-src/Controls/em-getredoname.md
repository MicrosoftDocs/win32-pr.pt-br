---
title: Mensagem de EM_GETREDONAME (RichEdit. h)
description: Recupera o tipo da próxima ação, se houver, na fila de restauração do controle de edição avançada.
ms.assetid: 8649236f-32dc-45d3-847e-c9f65ffba44c
keywords:
- Controles de EM_GETREDONAME de mensagens do Windows
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
ms.openlocfilehash: 9ea44257344b9ebdb8ffe91ad97e939aae0db9b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918561"
---
# <a name="em_getredoname-message"></a>\_Mensagem em refazer

Recupera o tipo da próxima ação, se houver, na fila de restauração do controle de edição avançada.

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

Se a fila de restauração do controle não estiver vazia, o valor retornado será um valor de enumeração [**UNDONAMEID**](/windows/desktop/api/Richedit/ne-richedit-undonameid) que indica o tipo da próxima ação na fila de restauração do controle.

Se não houver ações refazêveis ou o tipo da próxima ação refeita for desconhecido, o valor de retorno será zero.

## <a name="remarks"></a>Comentários

Os tipos de ações que podem ser desfeitas ou refeitos incluem as operações de digitação, exclusão, arrastar e soltar, recortar e colar. Essas informações podem ser úteis para aplicativos que fornecem uma interface do usuário estendida para operações de desfazer e refazer, como uma caixa de listagem suspensa de ações refazêveis.

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

[**em \_ GETundoname**](em-getundoname.md)
</dt> <dt>

[**em \_ refazer**](em-redo.md)
</dt> <dt>

[**em \_ desfazer**](em-undo.md)
</dt> <dt>

[**UNDONAMEID**](/windows/desktop/api/Richedit/ne-richedit-undonameid)
</dt> </dl>

 

 





