---
title: Mensagem de LVM_REDRAWITEMS (commctrl. h)
description: Força um controle de exibição de lista a redesenhar um intervalo de itens. Você pode enviar essa mensagem explicitamente ou usando a \_ macro RedrawItems do ListView.
ms.assetid: a717b17f-6e0a-4804-96f9-da93392a19ec
keywords:
- Controles de LVM_REDRAWITEMS de mensagens do Windows
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
ms.openlocfilehash: 42568a9ab78361a28a99eee372674287a24d03cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009349"
---
# <a name="lvm_redrawitems-message"></a>\_Mensagem REDRAWITEMS LVM

Força um controle de exibição de lista a redesenhar um intervalo de itens. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ RedrawItems do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_redrawitems) .

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

## <a name="return-value"></a>Retornar valor

Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.

## <a name="remarks"></a>Comentários

Os itens especificados não são, na verdade, redesenhados até que a janela de exibição de lista receba uma mensagem de [**\_ pintura do WM**](/windows/desktop/gdi/wm-paint) para redesenhar. Para redesenhar imediatamente, chame a função [**UpdateWindow**](/windows/desktop/api/winuser/nf-winuser-updatewindow) depois de usar essa macro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

