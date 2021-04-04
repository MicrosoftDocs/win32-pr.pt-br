---
title: Mensagem de LB_GETSELCOUNT (WinUser. h)
description: Obtém o número total de itens selecionados em uma caixa de listagem de seleção múltipla.
ms.assetid: 1597f6d0-e8f2-4e10-8a0e-ef76192e6238
keywords:
- Controles de LB_GETSELCOUNT de mensagens do Windows
topic_type:
- apiref
api_name:
- LB_GETSELCOUNT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed73b387315d1b612241d41e47e6b613a3a75f12
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085407"
---
# <a name="lb_getselcount-message"></a>GETSELCOUNT de mensagens de LB \_

Obtém o número total de itens selecionados em uma caixa de listagem de seleção múltipla.

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

O valor de retorno é a contagem de itens selecionados na caixa de listagem. Se a caixa de listagem for uma caixa de listagem de seleção única, o valor de retorno será um erro de LB \_ .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_SETSEL lb**](lb-setsel.md)
</dt> </dl>

 

 





