---
title: Mensagem de EM_SHOWSCROLLBAR (RichEdit. h)
description: Mostra ou oculta uma das barras de rolagem na janela host de um controle rich edit.
ms.assetid: 0a6ec010-4870-4faf-9dc2-1da961dc8194
keywords:
- controles de Windows de mensagem de EM_SHOWSCROLLBAR
topic_type:
- apiref
api_name:
- EM_SHOWSCROLLBAR
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc3988ced825fed457549fc9f662a418295de7df6085f04c3e71255ca4ad54c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117831136"
---
# <a name="em_showscrollbar-message"></a>Na \_ mensagem de ScrollBar

Mostra ou oculta uma das barras de rolagem na janela host de um controle rich edit.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identifica a barra de rolagem a ser exibida: horizontal ou vertical. Esse parâmetro deve ser **SB \_ Vert** ou **SB \_ na horizontal**.

</dd> <dt>

*lParam* 
</dt> <dd>

Especifica se a barra de rolagem deve ser mostrada ou ocultada. Especifique **true** para mostrar a barra de rolagem e **false** para ocultá-la.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Essa mensagem não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método só é válido quando o controle está ativo no local. As chamadas feitas enquanto o controle estiver inativo pode falhar.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**em \_ GETSCROLLPOS**](em-getscrollpos.md)
</dt> <dt>

[**em \_ SETSCROLLPOS**](em-setscrollpos.md)
</dt> </dl>

 

 





