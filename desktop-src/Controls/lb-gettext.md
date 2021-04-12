---
title: Mensagem de LB_GETTEXT (WinUser. h)
description: Obtém uma cadeia de caracteres de uma caixa de listagem.
ms.assetid: 6bf7ec3b-237b-4668-9493-40c098a32428
keywords:
- Controles de LB_GETTEXT de mensagens do Windows
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
ms.openlocfilehash: c3dd5e2c7a9e6c1c1aa1b847592555a013766134
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455660"
---
# <a name="lb_gettext-message"></a>A \_ mensagem GETtext de lb

Obtém uma cadeia de caracteres de uma caixa de listagem.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O índice de base zero da cadeia de caracteres a ser recuperada.

Windows 95/Windows 98/Windows Millennium Edition (Windows me): o parâmetro *wParam* é limitado a valores de 16 bits. Isso significa que as caixas de listagem não podem conter mais de 32.767 itens. Embora o número de itens seja restrito, o tamanho total em bytes dos itens em uma caixa de listagem é limitado apenas pela memória disponível.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para o buffer que receberá a cadeia de caracteres; é o tipo **LPTSTR** , que é posteriormente convertido em um **lParam**. O buffer deve ter espaço suficiente para a cadeia de caracteres e um caractere nulo de terminação. Uma mensagem de [**\_ GETTEXTLEN de lb**](lb-gettextlen.md) pode ser enviada antes da mensagem de **\_ gettext do lb** para recuperar o comprimento, em **TCHAR** s, da cadeia de caracteres.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno é o comprimento da cadeia de caracteres, em **TCHAR** s, excluindo o caractere nulo de terminação. Se *wParam* não especificar um índice válido, o valor de retorno será um \_ erro de lb.

## <a name="remarks"></a>Comentários

Se a caixa de listagem tiver um estilo desenhado pelo proprietário, mas não o estilo de [**lbs \_ HASSTRINGS**](list-box-styles.md) , o buffer apontado pelo parâmetro *lParam* receberá o valor associado ao item (os dados do item).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_GETTEXTLEN lb**](lb-gettextlen.md)
</dt> </dl>

 

 





