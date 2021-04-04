---
title: Mensagem de EM_SHOWSCROLLBAR (RichEdit. h)
description: Mostra ou oculta uma das barras de rolagem na janela host de um controle rich edit.
ms.assetid: 0a6ec010-4870-4faf-9dc2-1da961dc8194
keywords:
- Controles de EM_SHOWSCROLLBAR de mensagens do Windows
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
ms.openlocfilehash: eb569b194be3d744db67f98b71a595ba18a2d3a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918346"
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

## <a name="return-value"></a>Retornar valor

Essa mensagem não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método só é válido quando o controle está ativo no local. As chamadas feitas enquanto o controle estiver inativo pode falhar.

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

[**em \_ GETSCROLLPOS**](em-getscrollpos.md)
</dt> <dt>

[**em \_ SETSCROLLPOS**](em-setscrollpos.md)
</dt> </dl>

 

 





