---
title: LVM_SETTOOLTIPS mensagem (Commctrl.h)
description: Define o controle de dica de ferramenta que o controle de exibição de lista usará para exibir dicas de ferramenta. Você pode enviar essa mensagem explicitamente ou usar a \_ macro ListView SetToolTips.
ms.assetid: 5b4335a4-e9f0-4b13-b00b-516af3b60bf1
keywords:
- LVM_SETTOOLTIPS controles Windows mensagem
topic_type:
- apiref
api_name:
- LVM_SETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bf2256d94630b8e792fd1f148864f3588b27e73ea5781eb0bdcd24bf9571507
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118170392"
---
# <a name="lvm_settooltips-message"></a>Mensagem LVM \_ SETTOOLTIPS

Define o controle de dica de ferramenta que o controle de exibição de lista usará para exibir dicas de ferramenta. Você pode enviar essa mensagem explicitamente ou usar a macro [**\_ ListView SetToolTips.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settooltips)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Lidar com o controle de dica de ferramenta a ser definido.</dd> <dt>

*lParam* 
</dt> <dd>

Deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna o alça para o controle de dica de ferramenta anterior.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**LVM \_ GETTOOLTIPS**](lvm-gettooltips.md)
</dt> </dl>

 

 





