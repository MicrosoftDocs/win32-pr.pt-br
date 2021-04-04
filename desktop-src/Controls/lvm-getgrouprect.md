---
title: Mensagem de LVM_GETGROUPRECT (commctrl. h)
description: Obtém o retângulo de um grupo especificado. Envie essa mensagem explicitamente ou usando a \_ macro GetGroupRect do ListView.
ms.assetid: 9441a6c5-11d8-4f52-80dd-1b60befd9b9d
keywords:
- Controles de LVM_GETGROUPRECT de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_GETGROUPRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab2cbdfb1ec6e670e7b5d333694f3a1ca56d287b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918034"
---
# <a name="lvm_getgrouprect-message"></a>\_Mensagem GETGROUPRECT LVM

Obtém o retângulo de um grupo especificado. Envie essa mensagem explicitamente ou usando a macro [**\_ GetGroupRect do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getgrouprect) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* \[ no\]
</dt> <dd>

Especifica o Group by **iGroupId** (consulte a estrutura [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) ).

</dd> <dt>

*lParam* \[ entrada, saída\]
</dt> <dd>

Um ponteiro para uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) para receber informações sobre o grupo especificado por *wParam*. O receptor da mensagem é responsável por definir os membros da estrutura com informações para o grupo especificado por *wParam*.

O processo de chamada é responsável por alocar memória para a estrutura. Defina o membro **superior** do [**Rect**](/previous-versions//dd162897(v=vs.85)) como um dos sinalizadores a seguir para especificar as coordenadas do retângulo a ser obtido.



| Valor                                                                                                                                                                  | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LVGGR_GROUP"></span><span id="lvggr_group"></span><dl> <dt>**grupo de LVGGR \_**</dt> </dl>                | Coordenadas de todo o grupo expandido.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="LVGGR_HEADER"></span><span id="lvggr_header"></span><dl> <dt>**\_cabeçalho LVGGR**</dt> </dl>             | Coordenadas do cabeçalho somente (grupo recolhido).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="LVGGR_LABEL"></span><span id="lvggr_label"></span><dl> <dt>**rótulo de LVGGR \_**</dt> </dl>                | Somente coordenadas do rótulo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="LVGGR_SUBSETLINK"></span><span id="lvggr_subsetlink"></span><dl> <dt>**LVGGR \_ SUBSETLINK**</dt> </dl> | Coordenadas somente do link de subconjunto (subconjunto de marcação). Um controle de exibição de lista pode limitar o número de itens visíveis exibidos em cada grupo. Um link é apresentado ao usuário para permitir que o usuário expanda o grupo. Esse sinalizador retornará o retângulo delimitador do link do subconjunto se o grupo for um subconjunto (estado do grupo de LVGS \_ subconjuntos, consulte estrutura [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup), **estado** do membro). Esse sinalizador é fornecido para que os aplicativos de acessibilidade possam localizar o link.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

