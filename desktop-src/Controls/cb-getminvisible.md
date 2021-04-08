---
title: Mensagem de CB_GETMINVISIBLE (commctrl. h)
description: Obtém o número mínimo de itens visíveis na lista suspensa de uma caixa de combinação.
ms.assetid: 9861358a-1ef9-4d78-8ec8-561b97f3f18e
keywords:
- Controles de CB_GETMINVISIBLE de mensagens do Windows
topic_type:
- apiref
api_name:
- CB_GETMINVISIBLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3dcf4fe5088d9c994e232a64ba16bbddf11b0d48
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824405"
---
# <a name="cb_getminvisible-message"></a>\_Mensagem de GETMINVISIBLE CB

Obtém o número mínimo de itens visíveis na lista suspensa de uma caixa de combinação.

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

O valor de retorno é o número mínimo de itens visíveis.

## <a name="remarks"></a>Comentários

Quando o número de itens na lista suspensa for maior que o mínimo, a caixa de combinação usará uma barra de rolagem.

Essa mensagem será ignorada se o controle da caixa de combinação tiver o estilo [**\_ NOINTEGRALHEIGHT CBS**](combo-box-styles.md).

Para usar **CB \_ GETMINVISIBLE**, o aplicativo deve especificar comctl32.dll versão 6 no manifesto. Para obter mais informações, consulte [habilitando estilos visuais](cookbook-overview.md).

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

[**\_SETMINVISIBLE CB**](cb-setminvisible.md)
</dt> <dt>

[**GetMinVisible da ComboBox \_**](/windows/desktop/api/Commctrl/nf-commctrl-combobox_getminvisible)
</dt> </dl>

 

 





