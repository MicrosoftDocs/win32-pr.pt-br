---
title: TVM_SETBKCOLOR mensagem (Commctrl.h)
description: Define a cor da tela de fundo do controle. Você pode enviar essa mensagem explicitamente ou usando a macro TreeView \_ SetBkColor.
ms.assetid: 087f5e0b-ac73-4db4-b82e-15c7641b681c
keywords:
- TVM_SETBKCOLOR controles de Windows mensagem
topic_type:
- apiref
api_name:
- TVM_SETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0609a15be2b8e05b1f8ca8f4f999cd4888ee946969c25f5bc1d86420b7529f2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060116"
---
# <a name="tvm_setbkcolor-message"></a>Mensagem TVM \_ SETBKCOLOR

Define a cor da tela de fundo do controle. Você pode enviar essa mensagem explicitamente ou usando a [**macro TreeView \_ SetBkColor.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setbkcolor)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

[**Valor COLORREF**](/windows/desktop/gdi/colorref) que contém a nova cor da tela de fundo. Se esse valor for -1, o controle será revertido para usando a cor do sistema para a cor da tela de fundo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um [**valor COLORREF**](/windows/desktop/gdi/colorref) que representa a cor da tela de fundo anterior. Se esse valor for -1, o controle estava usando a cor do sistema para a cor da tela de fundo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**TVM \_ GETBKCOLOR**](tvm-getbkcolor.md)
</dt> </dl>

 

