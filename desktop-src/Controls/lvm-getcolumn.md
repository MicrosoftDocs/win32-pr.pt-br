---
title: LVM_GETCOLUMN mensagem (Commctrl.h)
description: Obtém os atributos da coluna de um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a \_ macro GetColumn ListView.
ms.assetid: 59b4bbfc-6c38-4faa-8f2e-3ea5d24e55a6
keywords:
- LVM_GETCOLUMN controles Windows mensagem
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
ms.openlocfilehash: b65478d1d249740c630499fd4837e31d4eba7b992cf3ef3682c4e7b72d0706cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118411732"
---
# <a name="lvm_getcolumn-message"></a>Mensagem GETCOLUMN do LVM \_

Obtém os atributos da coluna de um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ GetColumn ListView.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcolumn)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O índice da coluna.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma [**estrutura LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) que especifica as informações a recuperar e recebe informações sobre a coluna. O **membro mask** especifica quais atributos de coluna recuperar. Se  o membro mask especificar o valor de TEXT LVCF, o membro pszText deverá conter o endereço do buffer que recebe o texto do item e o membro \_ **cchTextMax** deverá especificar o tamanho do buffer. 

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna **TRUE se** for bem-sucedido ou FALSE **caso** contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





