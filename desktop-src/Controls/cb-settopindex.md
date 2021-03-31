---
title: Mensagem de CB_SETTOPINDEX (WinUser. h)
description: Um aplicativo envia a \_ mensagem CB SETTOPINDEX para garantir que um item específico esteja visível na caixa de listagem de uma caixa de combinação.
ms.assetid: vs|controls|~\controls\comboboxes\comboboxreference\comboboxmessages\cb_settopindex.htm
keywords:
- Controles de CB_SETTOPINDEX de mensagens do Windows
topic_type:
- apiref
api_name:
- CB_SETTOPINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f402cbd16cd61a829a2221600bd3c548829f348
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644304"
---
# <a name="cb_settopindex-message"></a>\_Mensagem de SETTOPINDEX CB

Um aplicativo envia a mensagem **CB \_ SETTOPINDEX** para garantir que um item específico esteja visível na caixa de listagem de uma caixa de combinação. O sistema rola o conteúdo da caixa de listagem para que o item especificado seja exibido na parte superior da caixa de listagem ou o intervalo máximo de rolagem tenha sido atingido.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica o índice de base zero do item de lista.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a mensagem for bem-sucedida, o valor de retorno será zero.

Se a mensagem falhar, o valor de retorno será CB \_ Err.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**\_GETTOPINDEX CB**](cb-gettopindex.md)
</dt> </dl>

 

 





