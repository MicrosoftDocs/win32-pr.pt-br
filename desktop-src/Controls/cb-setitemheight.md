---
title: Mensagem de CB_SETITEMHEIGHT (WinUser. h)
description: Um aplicativo envia uma \_ mensagem de SETITEMHEIGHT CB para definir a altura dos itens de lista ou o campo de seleção em uma caixa de combinação.
ms.assetid: 25a01170-5ffc-4d86-b696-706f5375570b
keywords:
- controles de Windows de mensagem de CB_SETITEMHEIGHT
topic_type:
- apiref
api_name:
- CB_SETITEMHEIGHT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b97e83d13e66d0a8252fdc1974c775188f8009958a3f286916b0e46ea4f0e88c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119699436"
---
# <a name="cb_setitemheight-message"></a>\_Mensagem de SETITEMHEIGHT CB

Um aplicativo envia uma mensagem de **\_ SETITEMHEIGHT CB** para definir a altura dos itens de lista ou o campo de seleção em uma caixa de combinação.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica o componente da caixa de combinação para a qual definir a altura.

Esse parâmetro deve ser 1 para definir a altura do campo de seleção. Ele deve ser zero para definir a altura dos itens de lista, a menos que a caixa de combinação tenha o estilo [**\_ OwnerDrawVariable do CBS**](combo-box-styles.md) . Nesse caso, o parâmetro *wParam* é o índice de base zero de um item de lista específico.

</dd> <dt>

*lParam* 
</dt> <dd>

Especifica a altura, em pixels, do componente da caixa de combinação identificado por *wParam*.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se o índice ou a altura for inválido, o valor de retorno será CB \_ Err.

## <a name="remarks"></a>Comentários

A altura do campo de seleção em uma caixa de combinação é definida independentemente da altura dos itens da lista. Um aplicativo deve garantir que a altura do campo de seleção não seja menor do que a altura de um item de lista específico.

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

[**\_GETITEMHEIGHT CB**](cb-getitemheight.md)
</dt> <dt>

[**MEASUREITEM do WM \_**](wm-measureitem.md)
</dt> </dl>

 

 





