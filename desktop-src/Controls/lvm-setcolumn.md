---
title: LVM_SETCOLUMN mensagem (Commctrl.h)
description: Define os atributos de uma coluna de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a macro ListView \_ SetColumn.
ms.assetid: 8ca1c269-fd86-4561-940d-b75f8ca2b731
keywords:
- LVM_SETCOLUMN controles de Windows mensagem
topic_type:
- apiref
api_name:
- LVM_SETCOLUMN
- LVM_SETCOLUMNW
- LVM_SETCOLUMNW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cca00e62d941a753c70e0dd31c1af4003fe639d49503be7009fe5a010febf0c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019214"
---
# <a name="lvm_setcolumn-message"></a>Mensagem LVM \_ SETCOLUMN

Define os atributos de uma coluna de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a [**macro ListView \_ SetColumn.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setcolumn)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice da coluna.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma [**estrutura LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) que contém os novos atributos de coluna. O **membro mask** especifica quais atributos de coluna definir. Se o **membro mask** especificar o valor text LVCF, o membro pszText será o endereço de uma cadeia de caracteres terminada em nulo e o membro \_ **cchTextMax** será ignorado. 

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna **TRUE se** for bem-sucedido ou FALSE **caso** contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **LVM \_ SETCOLUMNW** (Unicode) e **LVM \_ SETCOLUMNW** (ANSI)<br/>               |



 

 





