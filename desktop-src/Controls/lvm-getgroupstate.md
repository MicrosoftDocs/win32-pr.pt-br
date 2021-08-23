---
title: LVM_GETGROUPSTATE mensagem (Commctrl.h)
description: Obtém o estado de um grupo especificado. Envie essa mensagem explicitamente ou usando a macro ListView \_ GetGroupState.
ms.assetid: f087d17f-9066-44fb-b21b-ac7ceb56eb45
keywords:
- LVM_GETGROUPSTATE controles de Windows mensagem
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
ms.openlocfilehash: 66272dd259e80f239804ffadbd706370f948a2505173cc03aaa40057b273a629
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958425"
---
# <a name="lvm_getgroupstate-message"></a>Mensagem GETGROUPSTATE do LVM \_

Obtém o estado de um grupo especificado. Envie essa mensagem explicitamente ou usando a [**macro ListView \_ GetGroupState.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getgroupstate)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* \[ Em\]
</dt> <dd>

Especifica o grupo por **iGroupId** (consulte [**estrutura LVGROUP).**](/windows/win32/api/commctrl/ns-commctrl-lvgroup)

</dd> <dt>

*lParam* \[ Em\]
</dt> <dd>

Especifica os valores de estado a recuperar. Essa é uma combinação dos sinalizadores listados para o **membro de** estado do [**LVGROUP.**](/windows/win32/api/commctrl/ns-commctrl-lvgroup)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna a combinação de valores de estado definidos. Por exemplo, se *lParam* for LVGS COLLAPSED e o valor retornado for zero, o estado \_ LVGS \_ COLLAPSED não será definido. Zero será retornado se o grupo não for encontrado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





