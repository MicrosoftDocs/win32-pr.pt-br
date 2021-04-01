---
title: Mensagem de EM_GETEVENTMASK (RichEdit. h)
description: Recupera a máscara de evento para um controle de edição rico. A máscara de evento especifica quais códigos de notificação o controle envia para sua janela pai.
ms.assetid: cdf99f2a-e747-4b0e-9235-2719477c3ce2
keywords:
- Controles de EM_GETEVENTMASK de mensagens do Windows
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
ms.openlocfilehash: 4f4d231bbb9d5592ff2f90da6a5096783b38c292
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918810"
---
# <a name="em_geteventmask-message"></a>\_Mensagem em GETEVENTMASK

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

## <a name="return-value"></a>Retornar valor

Essa mensagem retorna a máscara de evento para o controle rich edit.

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

[**em \_ SETEVENTMASK**](em-seteventmask.md)
</dt> <dt>

[**Sinalizadores de máscara de evento de controle de edição avançada**](rich-edit-control-event-mask-flags.md)
</dt> </dl>

 

 





