---
title: Mensagem de LVM_GETFOOTERITEMRECT (commctrl. h)
description: Obtém as coordenadas de um rodapé para um item especificado em um controle de exibição de lista. Envie essa mensagem explicitamente ou usando a \_ macro GetFooterItemRect do ListView.
ms.assetid: 4a6055d3-1cc1-4c3d-a5f6-006617ff3bce
keywords:
- Controles de LVM_GETFOOTERITEMRECT de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_GETFOOTERITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 142cb92806fa1d58faa0414c10c41bd2815d5b6b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104163579"
---
# <a name="lvm_getfooteritemrect-message"></a>\_Mensagem GETFOOTERITEMRECT LVM

Obtém as coordenadas de um rodapé para um item especificado em um controle de exibição de lista. Envie essa mensagem explicitamente ou usando a macro [**\_ GetFooterItemRect do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfooteritemrect) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* \[ no\]
</dt> <dd>

O índice do item no controle de exibição de lista.

</dd> <dt>

*lParam* \[ entrada, saída\]
</dt> <dd>

Um ponteiro para uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) para receber as coordenadas. O aplicativo de chamada é responsável por alocar essa estrutura. As coordenadas recebidas são expressas como coordenadas do cliente.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

