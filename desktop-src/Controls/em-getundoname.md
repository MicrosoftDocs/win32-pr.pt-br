---
title: Mensagem de EM_GETUNDONAME (RichEdit. h)
description: O Microsoft rich edit 2,0 e posterior recupera o tipo da próxima ação de desfazer, se houver. Microsoft Rich Edit 1,0 não há suporte para essa mensagem.
ms.assetid: 43351909-f8bc-425a-9d9b-655e3b47eb75
keywords:
- Controles de EM_GETUNDONAME de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_GETUNDONAME
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0c29b5815da5569059ba80c007d6af39d1e389f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918881"
---
# <a name="em_getundoname-message"></a>\_Mensagem em GETundoname

Microsoft rich edit 2,0 e posterior: recupera o tipo da próxima ação de desfazer, se houver.

Microsoft Rich Edit 1,0: não há suporte para essa mensagem.

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

Se houver uma ação de desfazer, o valor retornado será um valor de enumeração [**UNDONAMEID**](/windows/desktop/api/Richedit/ne-richedit-undonameid) que indica o tipo da próxima ação na fila de desfazer do controle.

Se não houver ações que possam ser desfeitas ou o tipo da próxima ação de desfazer for desconhecido, o valor de retorno será zero.

## <a name="remarks"></a>Comentários

Os tipos de ações que podem ser desfeitas ou refeitos incluem operações de digitação, exclusão, arrastar, soltar, recortar e colar. Essas informações podem ser úteis para aplicativos que fornecem uma interface do usuário estendida para operações de desfazer e refazer, como uma caixa de listagem suspensa de ações que podem ser desfeitas.

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

[**em \_ refazer**](em-getredoname.md)
</dt> <dt>

[**em \_ refazer**](em-redo.md)
</dt> <dt>

[**em \_ desfazer**](em-undo.md)
</dt> <dt>

[**UNDONAMEID**](/windows/desktop/api/Richedit/ne-richedit-undonameid)
</dt> </dl>

 

 





