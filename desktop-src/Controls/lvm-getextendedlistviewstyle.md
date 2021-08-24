---
title: LVM_GETEXTENDEDLISTVIEWSTYLE mensagem (Commctrl.h)
description: Obtém os estilos estendidos que estão atualmente em uso para um determinado controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usar a \_ macro ListView GetExtendedListViewStyle.
ms.assetid: 5cfccdb8-a81c-4fa9-a4fa-19cf49bd6ce0
keywords:
- LVM_GETEXTENDEDLISTVIEWSTYLE controles de Windows mensagem
topic_type:
- apiref
api_name:
- LVM_GETEXTENDEDLISTVIEWSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d04b2f83f5a8bd55f01aa84e315512c5ccb1b28b17f196c0199fc417544a6737
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119968296"
---
# <a name="lvm_getextendedlistviewstyle-message"></a>Mensagem \_ GETEXTENDEDLISTVIEWSTYLE LVM

Obtém os estilos estendidos que estão atualmente em uso para um determinado controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usar a macro [**\_ ListView GetExtendedListViewStyle.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getextendedlistviewstyle)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um **DWORD** que representa os estilos atualmente em uso para um determinado controle de exibição de lista. Esse valor pode ser uma combinação de [Estilos List-View Estendidos.](extended-list-view-styles.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





