---
title: LVM_REDRAWITEMS mensagem (Commctrl.h)
description: Força um controle de exibição de lista a redesenhar um intervalo de itens. Você pode enviar essa mensagem explicitamente ou usando a macro ListView \_ RedrawItems.
ms.assetid: a717b17f-6e0a-4804-96f9-da93392a19ec
keywords:
- LVM_REDRAWITEMS controles de Windows mensagem
topic_type:
- apiref
api_name:
- LVM_REDRAWITEMS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53fbee43ff8cfcbb14ab357b6e76ab709df3e4a797143d5c4fa2c9b1179153af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119261726"
---
# <a name="lvm_redrawitems-message"></a>Mensagem LVM \_ REDRADRADRAEMS

Força um controle de exibição de lista a redesenhar um intervalo de itens. Você pode enviar essa mensagem explicitamente ou usando a macro [**ListView \_ RedrawItems.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_redrawitems)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice do primeiro item a ser redesenhado.

</dd> <dt>

*lParam* 
</dt> <dd>

Índice do último item a ser redesenhado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna **TRUE se** for bem-sucedido ou FALSE **caso** contrário.

## <a name="remarks"></a>Comentários

Os itens especificados não são redesenhados até que a janela de exibição de lista receba uma mensagem [**WM \_ PAINT**](/windows/desktop/gdi/wm-paint) para reint. Para reint imediatamente, chame a [**função UpdateWindow**](/windows/desktop/api/winuser/nf-winuser-updatewindow) depois de usar essa macro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

