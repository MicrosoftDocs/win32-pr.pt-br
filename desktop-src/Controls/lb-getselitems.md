---
title: Mensagem de LB_GETSELITEMS (WinUser. h)
description: Preenche um buffer com uma matriz de inteiros que especificam os números de item dos itens selecionados em uma caixa de listagem de seleção múltipla.
ms.assetid: 95dd72ef-76a5-4188-b2c8-d4c5eb2f34e3
keywords:
- Controles de LB_GETSELITEMS de mensagens do Windows
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
ms.openlocfilehash: 703988749cc5091bc3196f7c6e70364edb40ee04
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918523"
---
# <a name="lb_getselitems-message"></a>GETSELITEMS de mensagens de LB \_

Preenche um buffer com uma matriz de inteiros que especificam os números de item dos itens selecionados em uma caixa de listagem de seleção múltipla.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O número máximo de itens selecionados cujos números de item devem ser colocados no buffer.

Windows 95/Windows 98/Windows Millennium Edition (Windows me): o parâmetro *wParam* é limitado a valores de 16 bits. Isso significa que as caixas de listagem não podem conter mais de 32.767 itens. Embora o número de itens seja restrito, o tamanho total em bytes dos itens em uma caixa de listagem é limitado apenas pela memória disponível.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para um buffer grande o suficiente para o número de inteiros especificados pelo parâmetro *wParam* .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno é o número de itens colocados no buffer. Se a caixa de listagem for uma caixa de listagem de seleção única, o valor de retorno será um erro de LB \_ .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_GETSELCOUNT lb**](lb-getselcount.md)
</dt> </dl>

 

 





