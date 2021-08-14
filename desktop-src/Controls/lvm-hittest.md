---
title: LVM_HITTEST mensagem (Commctrl.h)
description: Determina qual item de exibição de lista, se algum, está em uma posição especificada. Você pode enviar essa mensagem explicitamente ou usando a macro ListView \_ HitTest.
ms.assetid: 81df4ed1-30bd-4b63-9cb9-5163cb7cf52c
keywords:
- LVM_HITTEST controles de Windows mensagem
topic_type:
- apiref
api_name:
- LVM_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81308249992b134dd3fa2bd0bc43ff0074bc3bae7048072ada7d68b0a867a979
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958165"
---
# <a name="lvm_hittest-message"></a>Mensagem LVM \_ HITTEST

Determina qual item de exibição de lista, se algum, está em uma posição especificada. Você pode enviar essa mensagem explicitamente ou usando a [**macro ListView \_ HitTest.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_hittest)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser 0. **Windows Vista.** Deve ser -1 se os membros **iGroup** e **iSubItem** da estrutura *lParam* devem ser recuperados.</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma [**estrutura LVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) que contém a posição para o teste de acerto e recebe informações sobre os resultados do teste de acerto.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna o índice do item na posição especificada, caso contrário, ou -1.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





