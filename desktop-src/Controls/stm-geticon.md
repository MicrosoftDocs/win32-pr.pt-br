---
title: STM_GETICON mensagem (Winuser.h)
description: Um aplicativo envia a mensagem GETICON do STM para recuperar um alçado para o ícone associado a um controle estático que \_ tem o estilo ÍCONE do SS. \_
ms.assetid: e6b0a006-696b-401d-b894-b1db697c8939
keywords:
- STM_GETICON controles de Windows mensagem
topic_type:
- apiref
api_name:
- STM_GETICON
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d33aab01e668f4b77e36a0a62b8eab75f3ee5db82188416c295c04cdf9bcb078
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084946"
---
# <a name="stm_geticon-message"></a>Mensagem \_ GETICON stm

Um aplicativo envia a **mensagem \_ GETICON do STM** para recuperar um alçado para o ícone associado a um controle estático que tem o estilo ÍCONE do SS. \_

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

O valor de retorno será um handle para o ícone ou **NULL** se o controle estático não tiver nenhum ícone associado ou se ocorrer um erro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**STM \_ SETICON**](stm-seticon.md)
</dt> </dl>

 

 





