---
title: Mensagem de CB_GETTOPINDEX (WinUser. h)
description: Um aplicativo envia a \_ mensagem CB GETTOPINDEX para recuperar o índice de base zero do primeiro item visível na parte da caixa de listagem de uma caixa de combinação.
ms.assetid: vs|controls|~\controls\comboboxes\comboboxreference\comboboxmessages\cb_gettopindex.htm
keywords:
- Controles de CB_GETTOPINDEX de mensagens do Windows
topic_type:
- apiref
api_name:
- CB_GETTOPINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59d5d6834dd954261822c8b1cb1a449d16398284
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918433"
---
# <a name="cb_gettopindex-message"></a>\_Mensagem de GETTOPINDEX CB

Um aplicativo envia a mensagem **CB \_ GETTOPINDEX** para recuperar o índice de base zero do primeiro item visível na parte da caixa de listagem de uma caixa de combinação. Inicialmente, o item com o índice 0 está na parte superior da caixa de listagem, mas se o conteúdo da caixa de listagem tiver sido rolado, outro item poderá estar na parte superior.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Não usado; deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Não usado; deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a mensagem for bem-sucedida, o valor de retorno será o índice do primeiro item visível na caixa de listagem da caixa de combinação.

Se a mensagem falhar, o valor de retorno será CB \_ Err.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_SETTOPINDEX CB**](cb-settopindex.md)
</dt> </dl>

 

 





