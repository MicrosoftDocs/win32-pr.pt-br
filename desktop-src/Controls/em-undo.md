---
title: Mensagem de EM_UNDO (WinUser. h)
description: Essa mensagem desfaz a última operação de controle de edição na fila de desfazer do controle. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.
ms.assetid: c4bff128-0383-40c5-8f29-7738f7f26871
keywords:
- controles de Windows de mensagem de EM_UNDO
topic_type:
- apiref
api_name:
- EM_UNDO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 452d82e6d0685314a79f1f95cff487ee3f52e2d1b70925c3e6e72f9263f442e0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047916"
---
# <a name="em_undo-message"></a>\_Mensagem em desfazer

Essa mensagem desfaz a última operação de controle de edição na fila de desfazer do controle. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.

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

Para um controle de edição de linha única, o valor de retorno é sempre **verdadeiro**.

Para um controle de edição de várias linhas, o valor de retorno será **true** se a operação de desfazer for bem-sucedida ou **false** se a operação de desfazer falhar.

## <a name="remarks"></a>Comentários

**Editar controles e edição avançada 1,0:** Uma operação de desfazer também pode ser desfeita. Por exemplo, você pode restaurar texto excluído com a primeira mensagem em **\_ desfazer** e remover o texto novamente com uma segunda mensagem **em \_ desfazer** , contanto que não haja uma operação de edição intermediária.

**Edição avançada 2,0 e posterior:** O recurso de desfazer é de vários níveis e, portanto, enviar duas mensagens em **\_ desfazer** fará com que as duas últimas operações na fila de desfazer sejam desfeitas. Para refazer uma operação, envie a mensagem em [**\_ refazer**](em-redo.md) .

**Edição avançada:** Com suporte no Microsoft Rich Edit 1,0 e posterior. Para obter informações sobre a compatibilidade das versões de edição rica com as várias versões do sistema, consulte [sobre controles de edição avançados](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**em \_ CANcelamento**](em-canundo.md)
</dt> </dl>

 

 





