---
title: Mensagem de LVM_GETCOLUMN (commctrl. h)
description: Obtém os atributos de uma coluna do controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a \_ macro GetColumn de ListView.
ms.assetid: 59b4bbfc-6c38-4faa-8f2e-3ea5d24e55a6
keywords:
- Controles de LVM_GETCOLUMN de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_GETCOLUMN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3eebf57138d27c31c5594f271e5d36a052b81673
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454632"
---
# <a name="lvm_getcolumn-message"></a>\_Mensagem de GETcolumn do LVM

Obtém os atributos de uma coluna do controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ GetColumn de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcolumn) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O índice da coluna.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma estrutura [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) que especifica as informações para recuperar e receber informações sobre a coluna. O membro **Mask** especifica quais atributos de coluna recuperar. Se o membro de **máscara** especificar o \_ valor de texto LVCF, o membro **pszText** deverá conter o endereço do buffer que receberá o texto do item e o membro **cchTextMax** deverá especificar o tamanho do buffer.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





