---
title: Mensagem de LB_SETCARETINDEX (WinUser. h)
description: Define o retângulo de foco para o item no índice especificado em uma caixa de listagem de seleção múltipla. Se o item não estiver visível, ele será rolado para a exibição.
ms.assetid: vs|controls|~\controls\listboxes\listboxreference\listboxmessages\lb_setcaretindex.htm
keywords:
- Controles de LB_SETCARETINDEX de mensagens do Windows
topic_type:
- apiref
api_name:
- LB_SETCARETINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 857e5c2637e5bcc90b2c60bfd8295a91ff297fb3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824678"
---
# <a name="lb_setcaretindex-message"></a>SETCARETINDEX de mensagens de LB \_

Define o retângulo de foco para o item no índice especificado em uma caixa de listagem de seleção múltipla. Se o item não estiver visível, ele será rolado para a exibição.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica o índice de base zero do item da caixa de listagem que deve receber o retângulo de foco.

Windows 95/Windows 98/Windows Millennium Edition (Windows me): o parâmetro *wParam* é limitado a valores de 16 bits. Isso significa que as caixas de listagem não podem conter mais de 32.767 itens. Embora o número de itens seja restrito, o tamanho total em bytes dos itens em uma caixa de listagem é limitado apenas pela memória disponível.

</dd> <dt>

*lParam* 
</dt> <dd>

Se esse valor for **false**, o item será rolado até que fique totalmente visível; Se for **true**, o item será rolado até que seja pelo menos parcialmente visível.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se ocorrer um erro, o valor de retorno será um erro de LB \_ (-1). Caso contrário, LB \_ OK (0) será retornado.

## <a name="remarks"></a>Comentários

Se essa mensagem for enviada para uma caixa de listagem de seleção única que não contém um item selecionado, o índice de cursor será definido como o item especificado pelo parâmetro *wParam* . Se a caixa de listagem de seleção única contiver um item selecionado, a caixa de listagem retornará um erro de LB \_ .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_GETCARETINDEX lb**](lb-getcaretindex.md)
</dt> </dl>

 

 





