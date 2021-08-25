---
title: LB_RESETCONTENT mensagem (Winuser.h)
description: Remove todos os itens de uma caixa de listagem.
ms.assetid: 3865e45e-62da-457a-801c-2f9a61687022
keywords:
- LB_RESETCONTENT controles de Windows mensagem
topic_type:
- apiref
api_name:
- LB_RESETCONTENT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c896263cd4a695583bda299b0feeff552a05ef2c938b9df348da685821c46652
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085366"
---
# <a name="lb_resetcontent-message"></a>Mensagem LB \_ RESETCONTENT

Remove todos os itens de uma caixa de listagem.

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

Essa mensagem não retorna um valor.

## <a name="remarks"></a>Comentários

Se a caixa de listagem tiver um estilo desenhado pelo proprietário, mas não o estilo [**\_ HASSTRINGS do LBS,**](list-box-styles.md) o proprietário da caixa de listagem receberá uma mensagem [**WM \_ DELETEITEM**](wm-deleteitem.md) para cada item na caixa de listagem.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**WM \_ DELETEITEM**](wm-deleteitem.md)
</dt> </dl>

 

 





