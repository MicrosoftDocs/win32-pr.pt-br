---
title: Mensagem de EM_SETEVENTMASK (RichEdit. h)
description: Define a máscara de evento para um controle de edição rico. A máscara de evento especifica quais códigos de notificação o controle envia para sua janela pai.
ms.assetid: 139f6e44-fc54-40f2-a3f6-2b7efc819cae
keywords:
- Controles de EM_SETEVENTMASK de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_SETEVENTMASK
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd4d79d23f7b56a29bc4f5142ed03b23e8081687
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455763"
---
# <a name="em_seteventmask-message"></a>\_Mensagem em SETEVENTMASK

Define a máscara de evento para um controle de edição rico. A máscara de evento especifica quais códigos de notificação o controle envia para sua janela pai.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Esse parâmetro não é usado; Ele deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Nova máscara de evento para o controle de edição rico. Para obter uma lista de máscaras de eventos, consulte [**sinalizadores de máscara de evento de controle de edição avançada**](rich-edit-control-event-mask-flags.md).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa mensagem retorna a máscara de evento anterior.

## <a name="remarks"></a>Comentários

A máscara de evento padrão (antes de qualquer é definida) é ENM \_ None.

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

[**em \_ GETEVENTMASK**](em-geteventmask.md)
</dt> <dt>

[**Sinalizadores de máscara de evento de controle de edição avançada**](rich-edit-control-event-mask-flags.md)
</dt> </dl>

 

 





