---
title: Mensagem de LVM_GETEXTENDEDLISTVIEWSTYLE (commctrl. h)
description: Obtém os estilos estendidos que estão em uso no momento para um determinado controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usar a \_ macro GetExtendedListViewStyle do ListView.
ms.assetid: 5cfccdb8-a81c-4fa9-a4fa-19cf49bd6ce0
keywords:
- Controles de LVM_GETEXTENDEDLISTVIEWSTYLE de mensagens do Windows
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
ms.openlocfilehash: 273da9e7eac85475b90ad05dc5fdd7f70d524562
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008863"
---
# <a name="lvm_getextendedlistviewstyle-message"></a>\_Mensagem GETEXTENDEDLISTVIEWSTYLE LVM

Obtém os estilos estendidos que estão em uso no momento para um determinado controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ GetExtendedListViewStyle do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getextendedlistviewstyle) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um **DWORD** que representa os estilos atualmente em uso para um determinado controle de exibição de lista. Esse valor pode ser uma combinação de [estilos de List-View estendidos](extended-list-view-styles.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





