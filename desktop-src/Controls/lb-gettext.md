---
title: LB_GETTEXT mensagem (Winuser.h)
description: Obtém uma cadeia de caracteres de uma caixa de listagem.
ms.assetid: 6bf7ec3b-237b-4668-9493-40c098a32428
keywords:
- LB_GETTEXT controles de Windows mensagem
topic_type:
- apiref
api_name:
- LB_GETTEXT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b2aa37a2d07e440aac615d1edc1e6f91c6a60e71a96418cd443daff9809ec18
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119434093"
---
# <a name="lb_gettext-message"></a>Mensagem \_ GETTEXT do LB

Obtém uma cadeia de caracteres de uma caixa de listagem.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O índice baseado em zero da cadeia de caracteres a ser recuperada.

Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : o parâmetro *wParam* é limitado a valores de 16 bits. Isso significa que as caixas de listagem não podem conter mais de 32.767 itens. Embora o número de itens seja restrito, o tamanho total em bytes dos itens em uma caixa de listagem é limitado apenas pela memória disponível.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para o buffer que receberá a cadeia de caracteres; é o tipo **LPTSTR,** que é subsequentemente lançado em **um LPARAM.** O buffer deve ter espaço suficiente para a cadeia de caracteres e um caractere nulo de terminação. Uma [**mensagem \_ LB GETTEXTLEN**](lb-gettextlen.md) pode ser enviada antes da mensagem **\_ GETTEXT do LB** para recuperar o comprimento, em **TCHAR** s, da cadeia de caracteres.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno é o comprimento da cadeia de caracteres, em **TCHAR** s, excluindo o caractere nulo de terminação. Se *wParam* não especificar um índice válido, o valor de retorno será LB \_ ERR.

## <a name="remarks"></a>Comentários

Se a caixa de listagem tiver um estilo desenhado pelo proprietário, mas não o estilo [**\_ HASSTRINGS do LBS,**](list-box-styles.md) o buffer apontado pelo parâmetro *lParam* receberá o valor associado ao item (os dados do item).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**LB \_ GETTEXTLEN**](lb-gettextlen.md)
</dt> </dl>

 

 





