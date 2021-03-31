---
title: Mensagem de LVM_SETCOLUMN (commctrl. h)
description: Define os atributos de uma coluna de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a \_ macro SetColumn de ListView.
ms.assetid: 8ca1c269-fd86-4561-940d-b75f8ca2b731
keywords:
- Controles de LVM_SETCOLUMN de mensagens do Windows
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
ms.openlocfilehash: 7251da70c7ac1e2cb7bbcf7b3e220a2f6cdf055f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918485"
---
# <a name="lvm_setcolumn-message"></a>\_Mensagem de SETcolumn do LVM

Define os atributos de uma coluna de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ SetColumn de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setcolumn) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice da coluna.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) que contém os novos atributos de coluna. O membro **Mask** especifica quais atributos de coluna definir. Se o membro de **máscara** especificar o \_ valor de texto LVCF, o membro **pszText** será o endereço de uma cadeia de caracteres terminada em nulo e o membro **cchTextMax** será ignorado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **LVM \_ SETCOLUMNW** (Unicode) e **LVM \_ SETCOLUMNW** (ANSI)<br/>               |



 

 





