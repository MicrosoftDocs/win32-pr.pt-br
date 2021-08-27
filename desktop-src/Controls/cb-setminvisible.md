---
title: Mensagem de CB_SETMINVISIBLE (commctrl. h)
description: Um aplicativo envia uma \_ mensagem de SETMINVISIBLE CB para definir o número mínimo de itens visíveis na lista suspensa de uma caixa de combinação.
ms.assetid: 3cf9e488-50ce-4825-acf0-4e665d074f9e
keywords:
- controles de Windows de mensagem de CB_SETMINVISIBLE
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
ms.openlocfilehash: 7a9790c43141ef836c1dec86304f260b0490854b593b7005b594d2a718332296
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120063316"
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

## <a name="return-value"></a>Valor retornado

Se a mensagem for bem-sucedida, o valor de retorno será **true**. Caso contrário, o valor de retorno será **false**.

## <a name="remarks"></a>Comentários

Quando o número de itens na lista suspensa for maior que o mínimo, a caixa de combinação usará uma barra de rolagem. Por padrão, 30 é o número mínimo de itens visíveis.

Essa mensagem será ignorada se o controle da caixa de combinação tiver o estilo [**\_ NOINTEGRALHEIGHT CBS**](combo-box-styles.md).

Para usar **CB \_ SETMINVISIBLE**, o aplicativo deve especificar comctl32.dll versão 6 no manifesto. Para obter mais informações, consulte [habilitando estilos visuais](cookbook-overview.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**\_GETMINVISIBLE CB**](cb-getminvisible.md)
</dt> <dt>

[**SetMinVisible da ComboBox \_**](/windows/desktop/api/Commctrl/nf-commctrl-combobox_setminvisible)
</dt> </dl>

 

 





