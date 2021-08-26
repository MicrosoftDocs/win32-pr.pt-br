---
title: BM_SETSTATE mensagem (Winuser.h)
description: Define o estado de realça de um botão. O estado de realça indica se o botão está realçado como se o usuário o tivesse pressionado. Você pode enviar essa mensagem explicitamente ou usar a \_ macro Button SetState.
ms.assetid: 675ebe8d-b381-46ca-b328-ebe9f25d864a
keywords:
- BM_SETSTATE controles de Windows mensagem
topic_type:
- apiref
api_name:
- BM_SETSTATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e3bb9451041c602541f039afcd85a895af2f02302dc5d55d64fbefb5bc6e3ff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119921206"
---
# <a name="bm_setstate-message"></a>Mensagem BM \_ SETSTATE

Define o estado de realça de um botão. O estado de realça indica se o botão está realçado como se o usuário o tivesse pressionado. Você pode enviar essa mensagem explicitamente ou usar a macro [**\_ Button SetState.**](/windows/desktop/api/Windowsx/nf-windowsx-button_setstate)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um **BOOL** que especifica se o botão está realçada. Um valor true **realça** o botão. Um valor false **remove** qualquer realçamento.

</dd> <dt>

*lParam* 
</dt> <dd>

Não usado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Essa mensagem sempre retorna zero.

## <a name="remarks"></a>Comentários

Realçamento afeta apenas a aparência de um botão. Ele não tem efeito sobre o estado de verificação de um botão de rádio ou caixa de seleção.

Um botão é realçado automaticamente quando o usuário posiciona o cursor sobre ele e pressiona e mantém o botão esquerdo do mouse. O realçamento é removido quando o usuário libera o botão do mouse.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**BM \_ GETSTATE**](bm-getstate.md)
</dt> <dt>

[**BM \_ SETCHECK**](bm-setcheck.md)
</dt> </dl>

 

 





