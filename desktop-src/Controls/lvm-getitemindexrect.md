---
title: Mensagem de LVM_GETITEMINDEXRECT (commctrl. h)
description: Recupera o retângulo delimitador para todo ou parte de um subitem no modo de exibição atual de um controle de exibição de lista. Envie essa mensagem explicitamente ou usando a \_ macro GetItemIndexRect do ListView.
ms.assetid: 17704d24-c029-4d41-b198-04d1e78698e0
keywords:
- Controles de LVM_GETITEMINDEXRECT de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_GETITEMINDEXRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31ccd114713326c4796ca69f56fc2c38daf145db
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455748"
---
# <a name="lvm_getitemindexrect-message"></a>\_Mensagem GETITEMINDEXRECT LVM

Recupera o retângulo delimitador para todo ou parte de um subitem no modo de exibição atual de um controle de exibição de lista. Envie essa mensagem explicitamente ou usando a macro [**\_ GetItemIndexRect do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemindexrect) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* \[ no\]
</dt> <dd>

Um ponteiro para uma estrutura [**LVITEMINDEX**](/windows/win32/api/commctrl/ns-commctrl-lvitemindex) para o item pai do subitem. O processo de chamada é responsável por alocar essa estrutura e definir seus membros. *wParam* não deve ser **nulo**.

</dd> <dt>

*lParam* \[ entrada, saída\]
</dt> <dd>

Um ponteiro para uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) para receber as coordenadas. O processo de chamada é responsável por alocar essa estrutura. *lParam* não deve ser **nulo**. Defina o membro **superior** como o índice do subitem. Defina o membro **esquerdo** como um dos valores a seguir, indicando a parte do subitem para o qual o retângulo delimitador será recuperado.



| Valor                                                                                                                                                   | Significado                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="LVIR_BOUNDS"></span><span id="lvir_bounds"></span><dl> <dt>**limites do LVIR \_**</dt> </dl> | Retorna o retângulo delimitador do subitem inteiro, incluindo o ícone e o rótulo.<br/> |
| <span id="LVIR_ICON"></span><span id="lvir_icon"></span><dl> <dt>**ícone de LVIR \_**</dt> </dl>       | Retorna o retângulo delimitador do ícone ou ícone pequeno do subitem.<br/>            |
| <span id="LVIR_LABEL"></span><span id="lvir_label"></span><dl> <dt>**rótulo de LVIR \_**</dt> </dl>    | Retorna o retângulo delimitador do texto do subitem.<br/>                                 |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

