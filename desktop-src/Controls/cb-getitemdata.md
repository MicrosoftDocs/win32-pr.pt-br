---
title: Mensagem de CB_GETITEMDATA (WinUser. h)
description: Um aplicativo envia uma \_ mensagem GETITEMDATA CB para uma caixa de combinação para recuperar o valor fornecido pelo aplicativo associado ao item especificado na caixa de combinação.
ms.assetid: 433b7f75-2831-4919-b931-c17ba651d145
keywords:
- controles de Windows de mensagem de CB_GETITEMDATA
topic_type:
- apiref
api_name:
- CB_GETITEMDATA
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8427e666668303456d16c00ae460a608a51bc31cd59e0ee6fa6851031057695b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019924"
---
# <a name="cb_getitemdata-message"></a>\_Mensagem de GETITEMDATA CB

Um aplicativo envia uma **mensagem \_ GETITEMDATA CB** para uma caixa de combinação para recuperar o valor fornecido pelo aplicativo associado ao item especificado na caixa de combinação.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O índice de base zero do item.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno é o valor associado ao item. Se ocorrer um erro, será CB \_ Err.

Se o item estiver em uma caixa de combinação desenhada pelo proprietário criada sem o estilo [**\_ HASSTRINGS do CBS**](combo-box-styles.md) , o valor de retorno será o valor contido no parâmetro *lParam* da mensagem [**CB \_ AddString**](cb-addstring.md) ou [**CB \_ InsertString**](cb-insertstring.md) , que adicionou o item à caixa de combinação. Se o estilo **CBS \_ HASSTRINGS** não for usado, o valor de retorno será o parâmetro *lParam* contido em uma mensagem [**CB \_ SETITEMDATA**](cb-setitemdata.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**AddString CB \_**](cb-addstring.md)
</dt> <dt>

[**inserção de CB \_**](cb-insertstring.md)
</dt> <dt>

[**\_SETITEMDATA CB**](cb-setitemdata.md)
</dt> </dl>

 

 





