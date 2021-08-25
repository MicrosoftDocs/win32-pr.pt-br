---
title: LB_SELITEMRANGEEX mensagem (Winuser.h)
description: Seleciona um ou mais itens consecutivos em uma caixa de listagem de seleção múltipla.
ms.assetid: aac85d72-43e2-4ab0-b9ee-c7a87e21d7a1
keywords:
- LB_SELITEMRANGEEX controles de Windows mensagem
topic_type:
- apiref
api_name:
- LB_SELITEMRANGEEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16e3112e36a7b212c1d0968ca738472000fabbf3d26d4d94e36ea9f21d80fe57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119799436"
---
# <a name="lb_selitemrangeex-message"></a>Mensagem LB \_ SELITEMRANGEEX

Seleciona um ou mais itens consecutivos em uma caixa de listagem de seleção múltipla.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica o índice baseado em zero do primeiro item a ser selecionado.

Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : o parâmetro *wParam* é limitado a valores de 16 bits. Isso significa que as caixas de listagem não podem conter mais de 32.767 itens. Embora o número de itens seja restrito, o tamanho total em bytes dos itens em uma caixa de listagem é limitado apenas pela memória disponível.

</dd> <dt>

*lParam* 
</dt> <dd>

Especifica o índice baseado em zero do último item a ser selecionado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se ocorrer um erro, o valor de retorno será LB \_ ERR.

## <a name="remarks"></a>Comentários

Se o *parâmetro wParam* for menor que o *parâmetro lParam,* o intervalo de itens especificado será selecionado. Se *wParam* for maior ou igual a *lParam,* o intervalo será removido do intervalo de itens especificado. Para selecionar apenas um item, selecione dois itens e, em seguida, desmarque o item indesejado.

Use essa mensagem somente com caixas de listagem de seleção múltipla.

Essa mensagem pode selecionar um intervalo somente dentro dos primeiros 65.536 itens.

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

[**LB \_ SELITEMRANGE**](lb-selitemrange.md)
</dt> <dt>

[**LB \_ SETSEL**](lb-setsel.md)
</dt> </dl>

 

 





