---
title: EM_GETEVENTMASK mensagem (Richedit.h)
description: Recupera a máscara de evento para um controle de edição rico. A máscara de evento especifica quais códigos de notificação o controle envia para sua janela pai.
ms.assetid: cdf99f2a-e747-4b0e-9235-2719477c3ce2
keywords:
- EM_GETEVENTMASK controles de Windows mensagem
topic_type:
- apiref
api_name:
- EM_GETEVENTMASK
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4261869276015151e920e96e6c419675a1bce097384d6a918c2eac2b8005393
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049226"
---
# <a name="em_geteventmask-message"></a>Mensagem \_ EM GETEVENTMASK

Recupera a máscara de evento para um controle de edição rico. A máscara de evento especifica quais códigos de notificação o controle envia para sua janela pai.

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

Essa mensagem retorna a máscara de evento para o controle de edição rich.

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

[**EM \_ SETEVENTMASK**](em-seteventmask.md)
</dt> <dt>

[**Sinalizadores de máscara de evento rich edit control**](rich-edit-control-event-mask-flags.md)
</dt> </dl>

 

 





