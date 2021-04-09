---
title: Mensagem de LVM_GETITEMRECT (commctrl. h)
description: Recupera o retângulo delimitador para todo ou parte de um item no modo de exibição atual. Você pode enviar essa mensagem explicitamente ou usando a \_ macro GetItemRect do ListView.
ms.assetid: 7ce74b65-3360-42b4-9889-d90aefe2d284
keywords:
- Controles de LVM_GETITEMRECT de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_GETITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd0915c9afc16f13ac8f36a639524fb5af6e8082
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009650"
---
# <a name="lvm_getitemrect-message"></a>\_Mensagem GETITEMRECT LVM

Recupera o retângulo delimitador para todo ou parte de um item no modo de exibição atual. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ GetItemRect do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemrect) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* \[ no\]
</dt> <dd>

Índice do item de exibição de lista.

</dd> <dt>

*lParam* \[ entrada, saída\]
</dt> <dd>

Ponteiro para uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) que recebe o retângulo delimitador. Quando a mensagem é enviada, o membro **à esquerda** dessa estrutura é usado para especificar a parte do item de exibição de lista do qual recuperar o retângulo delimitador. Ele deve ser definido como um dos seguintes valores:



| Valor                                                                                                                                                                     | Significado                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span id="LVIR_BOUNDS"></span><span id="lvir_bounds"></span><dl> <dt>**limites do LVIR \_**</dt> </dl>                   | Retorna o retângulo delimitador do item inteiro, incluindo o ícone e o rótulo.<br/>                     |
| <span id="LVIR_ICON"></span><span id="lvir_icon"></span><dl> <dt>**ícone de LVIR \_**</dt> </dl>                         | Retorna o retângulo delimitador do ícone ou ícone pequeno.<br/>                                            |
| <span id="LVIR_LABEL"></span><span id="lvir_label"></span><dl> <dt>**rótulo de LVIR \_**</dt> </dl>                      | Retorna o retângulo delimitador do texto do item.<br/>                                                     |
| <span id="LVIR_SELECTBOUNDS"></span><span id="lvir_selectbounds"></span><dl> <dt>**LVIR \_ SELECTBOUNDS**</dt> </dl> | Retorna a União do ícone LVIR \_ e dos \_ retângulos de rótulo LVIR, mas exclui colunas na exibição de relatório.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

