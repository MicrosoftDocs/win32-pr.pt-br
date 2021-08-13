---
title: Mensagem de LB_DELETESTRING (WinUser. h)
description: Exclui uma cadeia de caracteres em uma caixa de listagem.
ms.assetid: 3f360e07-b70d-4bfc-89d4-18d3b18b0fcf
keywords:
- controles de Windows de mensagem de LB_DELETESTRING
topic_type:
- apiref
api_name:
- LB_DELETESTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3329f82babea73a6392f7c360623fdeadec843dfcfd62e70106e7fb1cb0367ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118671671"
---
# <a name="lb_deletestring-message"></a>LB \_ mensagem de exclusão

Exclui uma cadeia de caracteres em uma caixa de listagem.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O índice de base zero da cadeia de caracteres a ser excluída.

Windows 95/Windows 98/Windows Millennium Edition (Windows Me): o parâmetro *wParam* é limitado a valores de 16 bits. Isso significa que as caixas de listagem não podem conter mais de 32.767 itens. Embora o número de itens seja restrito, o tamanho total em bytes dos itens em uma caixa de listagem é limitado apenas pela memória disponível.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno é uma contagem das cadeias de caracteres restantes na lista. O valor de retorno será LB \_ Err se o parâmetro *wParam* especificar um índice maior que o número de itens na lista.

## <a name="remarks"></a>Comentários

Se um aplicativo criar a caixa de listagem com um estilo desenhado pelo proprietário, mas sem o estilo de [**lbs \_ HASSTRINGS**](list-box-styles.md) , o sistema enviará uma mensagem do [**WM \_ DELETEITEM**](wm-deleteitem.md) para o proprietário da caixa de listagem para que o aplicativo possa liberar quaisquer dados adicionais associados ao item.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**seqüência de caracteres de LB \_**](lb-addstring.md)
</dt> <dt>

[**KG \_ InsertString**](lb-insertstring.md)
</dt> <dt>

[**DELETEITEM do WM \_**](wm-deleteitem.md)
</dt> </dl>

 

 





