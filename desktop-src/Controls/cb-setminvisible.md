---
title: Mensagem de CB_SETMINVISIBLE (commctrl. h)
description: Um aplicativo envia uma \_ mensagem de SETMINVISIBLE CB para definir o número mínimo de itens visíveis na lista suspensa de uma caixa de combinação.
ms.assetid: 3cf9e488-50ce-4825-acf0-4e665d074f9e
keywords:
- Controles de CB_SETMINVISIBLE de mensagens do Windows
topic_type:
- apiref
api_name:
- CB_SETMINVISIBLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac88155424c0b1ecf6c91f398e7a9a2d437eff90
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085216"
---
# <a name="cb_setminvisible-message"></a>\_Mensagem de SETMINVISIBLE CB

Um aplicativo envia uma mensagem de **\_ SETMINVISIBLE CB** para definir o número mínimo de itens visíveis na lista suspensa de uma caixa de combinação.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica o número mínimo de itens visíveis.

</dd> <dt>

*lParam* 
</dt> <dd>

Esse parâmetro não é usado; Ele deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a mensagem for bem-sucedida, o valor de retorno será **true**. Caso contrário, o valor de retorno será **false**.

## <a name="remarks"></a>Comentários

Quando o número de itens na lista suspensa for maior que o mínimo, a caixa de combinação usará uma barra de rolagem. Por padrão, 30 é o número mínimo de itens visíveis.

Essa mensagem será ignorada se o controle da caixa de combinação tiver o estilo [**\_ NOINTEGRALHEIGHT CBS**](combo-box-styles.md).

Para usar **CB \_ SETMINVISIBLE**, o aplicativo deve especificar comctl32.dll versão 6 no manifesto. Para obter mais informações, consulte [habilitando estilos visuais](cookbook-overview.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**\_GETMINVISIBLE CB**](cb-getminvisible.md)
</dt> <dt>

[**SetMinVisible da ComboBox \_**](/windows/desktop/api/Commctrl/nf-commctrl-combobox_setminvisible)
</dt> </dl>

 

 





