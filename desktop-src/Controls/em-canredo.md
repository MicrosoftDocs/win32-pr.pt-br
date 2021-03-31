---
title: Mensagem de EM_CANREDO (RichEdit. h)
description: Determina se há alguma ação na fila de restauração do controle.
ms.assetid: 4a76adc8-f815-4cf7-8742-b7695e5a0f64
keywords:
- Controles de EM_CANREDO de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_CANREDO
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccfb12f8e72bdf5321151cd3a70b74f322a46591
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824570"
---
# <a name="em_canredo-message"></a>\_Mensagem em refazer

Determina se há alguma ação na fila de restauração do controle.

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

Se houver ações na fila de restauração do controle, o valor de retorno será um valor diferente de zero.

Se a fila de restauração estiver vazia, o valor de retorno será zero.

## <a name="remarks"></a>Comentários

Para refazer a operação de desfazer mais recente, envie a mensagem em [**\_ refazer**](em-redo.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

**Referência**
</dt> <dt>

[**em \_ refazer**](em-getredoname.md)
</dt> <dt>

[**em \_ GETundoname**](em-getundoname.md)
</dt> <dt>

[**em \_ refazer**](em-redo.md)
</dt> <dt>

[**em \_ desfazer**](em-undo.md)
</dt> </dl>

 

 





