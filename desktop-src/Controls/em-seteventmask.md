---
title: Mensagem de EM_SETEVENTMASK (RichEdit. h)
description: Define a máscara de evento para um controle de edição rico. A máscara de evento especifica quais códigos de notificação o controle envia para sua janela pai.
ms.assetid: 139f6e44-fc54-40f2-a3f6-2b7efc819cae
keywords:
- controles de Windows de mensagem de EM_SETEVENTMASK
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
ms.openlocfilehash: 244274d969473531bae7c1d124af24a88d6b98d9db8bdbe073d054a3a9e36ac1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048496"
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

## <a name="return-value"></a>Valor retornado

Essa mensagem retorna a máscara de evento anterior.

## <a name="remarks"></a>Comentários

A máscara de evento padrão (antes de qualquer é definida) é ENM \_ None.

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

[**em \_ GETEVENTMASK**](em-geteventmask.md)
</dt> <dt>

[**Sinalizadores de máscara de evento de controle de edição avançada**](rich-edit-control-event-mask-flags.md)
</dt> </dl>

 

 





