---
title: Mensagem de CB_SETITEMDATA (WinUser. h)
description: Um aplicativo envia uma \_ mensagem de SETITEMDATA CB para definir o valor associado ao item especificado em uma caixa de combinação.
ms.assetid: 8be9eb57-a635-4c52-9838-556368813c74
keywords:
- Controles de CB_SETITEMDATA de mensagens do Windows
topic_type:
- apiref
api_name:
- CB_SETITEMDATA
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbb1603f9906ebf30a391b57bd812dc2002136c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824572"
---
# <a name="cb_setitemdata-message"></a>\_Mensagem de SETITEMDATA CB

Um aplicativo envia uma mensagem de **\_ SETITEMDATA CB** para definir o valor associado ao item especificado em uma caixa de combinação.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica o índice de base zero do item.

</dd> <dt>

*lParam* 
</dt> <dd>

Especifica o novo valor a ser associado ao item.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se ocorrer um erro, o valor de retorno será CB \_ Err.

## <a name="remarks"></a>Comentários

Se o item especificado estiver em uma caixa de combinação desenhada pelo proprietário criada sem o estilo [**\_ HASSTRINGS do CBS**](combo-box-styles.md) , essa mensagem substituirá o valor no parâmetro *lParam* da mensagem [**CB \_ AddString**](cb-addstring.md) ou [**CB \_ InsertString**](cb-insertstring.md) que adicionou o item à caixa de combinação.

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

[**AddString CB \_**](cb-addstring.md)
</dt> <dt>

[**\_GETITEMDATA CB**](cb-getitemdata.md)
</dt> <dt>

[**inserção de CB \_**](cb-insertstring.md)
</dt> </dl>

 

 





