---
title: LB_SETCURSEL mensagem (Winuser.h)
description: Seleciona uma cadeia de caracteres e rola-a para a exibição, se necessário. Quando a nova cadeia de caracteres é selecionada, a caixa de listagem remove o destaque da cadeia de caracteres selecionada anteriormente.
ms.assetid: 28d81f9d-a926-400c-8803-dcdb0e8f193d
keywords:
- LB_SETCURSEL controles Windows mensagem
topic_type:
- apiref
api_name:
- LB_SETCURSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b33964d98717ab84a325b5070eec6c4e1cacf334ba2272d4691d340a15af78a0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085336"
---
# <a name="lb_setcursel-message"></a>Mensagem \_ LB SETCURSEL

Seleciona uma cadeia de caracteres e rola-a para a exibição, se necessário. Quando a nova cadeia de caracteres é selecionada, a caixa de listagem remove o destaque da cadeia de caracteres selecionada anteriormente.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica o índice baseado em zero da cadeia de caracteres selecionada. Se esse parâmetro for -1, a caixa de listagem será definida para não ter nenhuma seleção.

Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : o parâmetro *wParam* é limitado a valores de 16 bits. Isso significa que as caixas de listagem não podem conter mais de 32.767 itens. Embora o número de itens seja restrito, o tamanho total em bytes dos itens em uma caixa de listagem é limitado apenas pela memória disponível.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se ocorrer um erro, o valor de retorno será LB \_ ERR. Se o *parâmetro wParam* for -1, o valor de retorno será LB \_ ERR, embora nenhum erro tenha ocorrido.

## <a name="remarks"></a>Comentários

Use essa mensagem somente com caixas de listagem de seleção única. Você não pode usá-lo para definir ou remover uma seleção em uma caixa de listagem de seleção múltipla.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**LB \_ GETCURSEL**](lb-getcursel.md)
</dt> </dl>

 

 





