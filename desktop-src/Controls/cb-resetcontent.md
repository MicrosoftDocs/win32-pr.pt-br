---
title: Mensagem de CB_RESETCONTENT (WinUser. h)
description: Remove todos os itens da caixa de listagem e edita o controle de uma caixa de combinação.
ms.assetid: 55203c34-87ca-46e9-a914-a480d43ccadd
keywords:
- Controles de CB_RESETCONTENT de mensagens do Windows
topic_type:
- apiref
api_name:
- CB_RESETCONTENT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3567f31ef98fffe42e53c4811acc786d41ae9f78
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824404"
---
# <a name="cb_resetcontent-message"></a>\_Mensagem de RESETCONTENT CB

Remove todos os itens da caixa de listagem e edita o controle de uma caixa de combinação.

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

Essa mensagem sempre retorna CB \_ OK.

## <a name="remarks"></a>Comentários

Se você criar a caixa de combinação com um estilo desenhado pelo proprietário, mas sem o estilo [**CBS \_ HASSTRINGS**](combo-box-styles.md) , o proprietário da caixa de combinação receberá uma mensagem [**\_ DELETEITEM do WM**](wm-deleteitem.md) para cada item na caixa de combinação.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

**Referência**
</dt> <dt>

[**excluído de CB \_**](cb-deletestring.md)
</dt> <dt>

[**DELETEITEM do WM \_**](wm-deleteitem.md)
</dt> </dl>

 

 





