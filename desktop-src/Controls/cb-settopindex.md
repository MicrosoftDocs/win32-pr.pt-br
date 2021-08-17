---
title: Mensagem de CB_SETTOPINDEX (WinUser. h)
description: Um aplicativo envia a \_ mensagem CB SETTOPINDEX para garantir que um item específico esteja visível na caixa de listagem de uma caixa de combinação.
ms.assetid: vs|controls|~\controls\comboboxes\comboboxreference\comboboxmessages\cb_settopindex.htm
keywords:
- controles de Windows de mensagem de CB_SETTOPINDEX
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
ms.openlocfilehash: d9364ef5013ef692adda76f96752f11691d5f4cc87c857386914105d16decb11
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117832284"
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

## <a name="return-value"></a>Valor retornado

Se a mensagem for bem-sucedida, o valor de retorno será zero.

Se a mensagem falhar, o valor de retorno será CB \_ Err.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_GETTOPINDEX CB**](cb-gettopindex.md)
</dt> </dl>

 

 





