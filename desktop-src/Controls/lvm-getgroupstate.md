---
title: Mensagem de LVM_GETGROUPSTATE (commctrl. h)
description: Obtém o estado de um grupo especificado. Envie essa mensagem explicitamente ou usando a \_ macro Getgroupstate do ListView.
ms.assetid: f087d17f-9066-44fb-b21b-ac7ceb56eb45
keywords:
- Controles de LVM_GETGROUPSTATE de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_GETGROUPSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17b5bb25fd517816afd04bb700211222e6985f5d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454699"
---
# <a name="lvm_getgroupstate-message"></a>Mensagem do LVM \_ GETgroupstate

Obtém o estado de um grupo especificado. Envie essa mensagem explicitamente ou usando a macro [**\_ getgroupstate do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getgroupstate) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* \[ no\]
</dt> <dd>

Especifica o Group by **iGroupId** (consulte a estrutura [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) ).

</dd> <dt>

*lParam* \[ no\]
</dt> <dd>

Especifica os valores de estado a serem recuperados. Essa é uma combinação dos sinalizadores listados para o membro de **estado** de [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna a combinação de valores de estado que são definidos. Por exemplo, se *lParam* for LVGS \_ recolhido e o valor retornado for zero, o \_ estado LVGS recolhido não será definido. Zero será retornado se o grupo não for encontrado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





