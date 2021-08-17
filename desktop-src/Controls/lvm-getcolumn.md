---
title: Mensagem de LVM_GETCOLUMN (commctrl. h)
description: Obtém os atributos de uma coluna do controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a \_ macro GetColumn de ListView.
ms.assetid: 59b4bbfc-6c38-4faa-8f2e-3ea5d24e55a6
keywords:
- controles de Windows de mensagem de LVM_GETCOLUMN
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

## <a name="return-value"></a>Valor retornado

Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





