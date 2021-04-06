---
title: Mensagem de LB_SETITEMDATA (WinUser. h)
description: Define um valor associado ao item especificado em uma caixa de listagem.
ms.assetid: df974fa2-114a-43ef-b0ac-0451c31d95cd
keywords:
- Controles de LB_SETITEMDATA de mensagens do Windows
topic_type:
- apiref
api_name:
- LB_SETITEMDATA
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02d9f9cc952ea3bf2d83358ce3b15ce6c3a2546b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086173"
---
# <a name="lb_setitemdata-message"></a>SETITEMDATA de mensagens de LB \_

Define um valor associado ao item especificado em uma caixa de listagem.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica o índice de base zero do item. Se esse valor for-1, o valor de *lParam* se aplicará a todos os itens na caixa de listagem.

Windows 95/Windows 98/Windows Millennium Edition (Windows me): o parâmetro *wParam* é limitado a valores de 16 bits. Isso significa que as caixas de listagem não podem conter mais de 32.767 itens. Embora o número de itens seja restrito, o tamanho total em bytes dos itens em uma caixa de listagem é limitado apenas pela memória disponível.

</dd> <dt>

*lParam* 
</dt> <dd>

Especifica o valor a ser associado ao item.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se ocorrer um erro, o valor de retorno será um erro de LB \_ .

## <a name="remarks"></a>Comentários

Se o item estiver em uma caixa de listagem desenhada pelo proprietário criada sem o estilo de [**lbs \_ HASSTRINGS**](list-box-styles.md) , essa mensagem substituirá o valor contido no parâmetro *lParam* da mensagem do [**lb \_ AddString**](lb-addstring.md) ou [**lb \_ InsertString**](lb-insertstring.md) que adicionou o item à caixa de listagem.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**seqüência de caracteres de LB \_**](lb-addstring.md)
</dt> <dt>

[**\_GETITEMDATA lb**](lb-getitemdata.md)
</dt> <dt>

[**KG \_ InsertString**](lb-insertstring.md)
</dt> </dl>

 

 





