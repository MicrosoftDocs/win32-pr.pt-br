---
title: Mensagem de LVM_HITTEST (commctrl. h)
description: Determina qual item de exibição de lista, se houver, está em uma posição especificada. Você pode enviar essa mensagem explicitamente ou usando a \_ macro HitTest do ListView.
ms.assetid: 81df4ed1-30bd-4b63-9cb9-5163cb7cf52c
keywords:
- Controles de LVM_HITTEST de mensagens do Windows
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
ms.openlocfilehash: 4fb770c8f5a47f1dcbbf23a11443afa581aea2e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918964"
---
# <a name="lvm_hittest-message"></a>Mensagem de HITTEST do LVM \_

Determina qual item de exibição de lista, se houver, está em uma posição especificada. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ HitTest do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_hittest) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser 0. **Windows Vista.** Deve ser-1 se os membros **iGroup** e **ISubItem** da estrutura *lParam* forem recuperados.</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**LVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) que contém a posição para o teste de clique e recebe informações sobre os resultados do teste de clique.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o índice do item na posição especificada, se houver, ou-1 caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





