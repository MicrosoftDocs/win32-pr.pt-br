---
title: Mensagem de CB_DELETESTRING (WinUser. h)
description: Exclui uma cadeia de caracteres na caixa de listagem de uma caixa de combinação.
ms.assetid: 8d526796-04ef-4c01-94d6-fb50e6fef27b
keywords:
- Controles de CB_DELETESTRING de mensagens do Windows
topic_type:
- apiref
api_name:
- CB_DELETESTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb0d3900c86874db1113c219fd9f7967c5f6bb6e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086330"
---
# <a name="cb_deletestring-message"></a>\_Mensagem excluída CB

Exclui uma cadeia de caracteres na caixa de listagem de uma caixa de combinação.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O índice de base zero da cadeia de caracteres a ser excluída.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno é uma contagem das cadeias de caracteres restantes na lista. Se o parâmetro *wParam* especificar um índice maior que o número de itens na lista, o valor de retorno será CB \_ Err.

## <a name="remarks"></a>Comentários

Se você criar a caixa de combinação com um estilo desenhado pelo proprietário, mas sem o estilo [**CBS \_ HASSTRINGS**](combo-box-styles.md) , o sistema enviará uma mensagem do [**WM \_ DELETEITEM**](wm-deleteitem.md) para o proprietário da caixa de combinação para que o aplicativo possa liberar quaisquer dados adicionais associados ao item.

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

[**\_RESETCONTENT CB**](cb-resetcontent.md)
</dt> <dt>

[**DELETEITEM do WM \_**](wm-deleteitem.md)
</dt> </dl>

 

 





