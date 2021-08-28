---
title: Mensagem de LVM_GETITEMINDEXRECT (commctrl. h)
description: Recupera o retângulo delimitador para todo ou parte de um subitem no modo de exibição atual de um controle de exibição de lista. Envie essa mensagem explicitamente ou usando a \_ macro GetItemIndexRect do ListView.
ms.assetid: 17704d24-c029-4d41-b198-04d1e78698e0
keywords:
- controles de Windows de mensagem de LVM_GETITEMINDEXRECT
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
ms.openlocfilehash: 91aa3e6d0420bfddb974d13f210c84241cefc5d79f0ee5a82920bdc2961879dc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119770366"
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

## <a name="return-value"></a>Valor retornado

Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

