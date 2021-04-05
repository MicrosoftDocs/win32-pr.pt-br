---
title: Mensagem de EM_UNDO (WinUser. h)
description: Essa mensagem desfaz a última operação de controle de edição na fila de desfazer do controle. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.
ms.assetid: c4bff128-0383-40c5-8f29-7738f7f26871
keywords:
- Controles de EM_UNDO de mensagens do Windows
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
ms.openlocfilehash: 4c75d79e7ed25e582682830b1323c27878bbdbb3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644669"
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

## <a name="return-value"></a>Retornar valor

Para um controle de edição de linha única, o valor de retorno é sempre **verdadeiro**.

Para um controle de edição de várias linhas, o valor de retorno será **true** se a operação de desfazer for bem-sucedida ou **false** se a operação de desfazer falhar.

## <a name="remarks"></a>Comentários

**Editar controles e edição avançada 1,0:** Uma operação de desfazer também pode ser desfeita. Por exemplo, você pode restaurar texto excluído com a primeira mensagem em **\_ desfazer** e remover o texto novamente com uma segunda mensagem **em \_ desfazer** , contanto que não haja uma operação de edição intermediária.

**Edição avançada 2,0 e posterior:** O recurso de desfazer é de vários níveis e, portanto, enviar duas mensagens em **\_ desfazer** fará com que as duas últimas operações na fila de desfazer sejam desfeitas. Para refazer uma operação, envie a mensagem em [**\_ refazer**](em-redo.md) .

**Edição avançada:** Com suporte no Microsoft Rich Edit 1,0 e posterior. Para obter informações sobre a compatibilidade das versões de edição rica com as várias versões do sistema, consulte [sobre controles de edição avançados](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**em \_ CANcelamento**](em-canundo.md)
</dt> </dl>

 

 





