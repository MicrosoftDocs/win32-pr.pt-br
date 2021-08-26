---
title: LB_GETSELITEMS mensagem (Winuser.h)
description: Preenche um buffer com uma matriz de inteiros que especificam os números de item dos itens selecionados em uma caixa de listagem de seleção múltipla.
ms.assetid: 95dd72ef-76a5-4188-b2c8-d4c5eb2f34e3
keywords:
- LB_GETSELITEMS controles Windows mensagem
topic_type:
- apiref
api_name:
- LB_GETSELITEMS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a541c7efb0acb8d462cce42f0323393baff58e51d63e6a78a72a9d334c0eae81
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085496"
---
# <a name="lb_getselitems-message"></a>Mensagem \_ LB GETSELITEMS

Preenche um buffer com uma matriz de inteiros que especificam os números de item dos itens selecionados em uma caixa de listagem de seleção múltipla.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O número máximo de itens selecionados cujos números de item devem ser colocados no buffer.

Windows 95/Windows 98/Windows Edition DaNium (Windows Me) : o parâmetro *wParam* é limitado a valores de 16 bits. Isso significa que as caixas de listagem não podem conter mais de 32.767 itens. Embora o número de itens seja restrito, o tamanho total em bytes dos itens em uma caixa de listagem é limitado apenas pela memória disponível.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para um buffer grande o suficiente para o número de inteiros especificado pelo *parâmetro wParam.*

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno é o número de itens colocados no buffer. Se a caixa de listagem for uma caixa de listagem de seleção única, o valor de retorno será LB \_ ERR.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**LB \_ GETSELCOUNT**](lb-getselcount.md)
</dt> </dl>

 

 





