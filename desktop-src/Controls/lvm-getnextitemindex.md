---
title: Mensagem de LVM_GETNEXTITEMINDEX (commctrl. h)
description: Recupera o índice de um item em um controle de exibição de lista especificado que corresponde às propriedades especificadas e à relação com outro item. Envie essa mensagem explicitamente ou usando a \_ macro GetNextItemIndex do ListView.
ms.assetid: vs|controls|~\controls\listview\messages\lvm_getnextitemindex.htm
keywords:
- Controles de LVM_GETNEXTITEMINDEX de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_GETNEXTITEMINDEX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cfc393aee4f275e941a04bb3f23ee4c2c3ac529
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086162"
---
# <a name="lvm_getnextitemindex-message"></a>\_Mensagem GETNEXTITEMINDEX LVM

Recupera o índice de um item em um controle de exibição de lista especificado que corresponde às propriedades especificadas e à relação com outro item. Envie essa mensagem explicitamente ou usando a macro [**\_ GetNextItemIndex do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getnextitemindex) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* \[ entrada, saída\]
</dt> <dd>

Um ponteiro para a estrutura [**LVITEMINDEX**](/windows/win32/api/commctrl/ns-commctrl-lvitemindex) do item para iniciar a pesquisa, ou-1 para localizar o primeiro item que corresponde aos sinalizadores especificados. O processo de chamada é responsável por alocar essa estrutura e definir seus membros.

</dd> <dt>

*lParam* 
</dt> <dd>

Especifica a relação com o item listado no parâmetro *wParam*. Isso pode ser um ou uma combinação dos seguintes valores:



| Valor                                                                                                                                                                                                                                                             | Significado                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt></dt><dt>Pesquisa por índice.</dt> </dl>                                                                                                               |                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="_______________LVNI_ALL"></span><span id="_______________lvni_all"></span><dl> <dt> **LVNI \_ tudo**</dt><dt></dt> </dl>                               | Procura um item subsequente por índice, o valor padrão.<br/>                                                                                                                                                                                                                                                                                                                                            |
| <dl> <dt></dt><dt>Pesquisa por relação física com o índice do item em que a pesquisa deve começar.</dt> </dl>                                         |                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="_______________LVNI_ABOVE"></span><span id="_______________lvni_above"></span><dl> <dt> **LVNI \_ acima**</dt><dt></dt> </dl>                         | Pesquisa um item que está acima do item especificado.<br/>                                                                                                                                                                                                                                                                                                                                                 |
| <span id="_______________LVNI_BELOW"></span><span id="_______________lvni_below"></span><dl> <dt> **LVNI \_ abaixo**</dt><dt></dt> </dl>                         | Pesquisa um item que está abaixo do item especificado.<br/>                                                                                                                                                                                                                                                                                                                                                 |
| <span id="_______________LVNI_TOLEFT"></span><span id="_______________lvni_toleft"></span><dl> <dt> **LVNI \_ toleft**</dt><dt></dt> </dl>                      | Procura um item à esquerda do item especificado.<br/>                                                                                                                                                                                                                                                                                                                                                |
| <span id="_______________LVNI_PREVIOUS"></span><span id="_______________lvni_previous"></span><dl> <dt> **LVNI \_ anterior**</dt><dt></dt> </dl>                | **Windows Vista e posterior:** Pesquisa um item que é ordenado antes do item especificado em *wParam*. O \_ sinalizador LVNI anterior não é direcional (LVNI \_ acima encontrará o item posicionado acima, enquanto \_ o LVNI anterior encontrará o item solicitado anteriormente.) O \_ sinalizador anterior LVNI basicamente reverte a lógica da pesquisa executada pelas \_ mensagens LVM GETNEXTITEM ou LVM \_ GETNEXTITEMINDEX.<br/> |
| <span id="_______________LVNI_TORIGHT"></span><span id="_______________lvni_toright"></span><dl> <dt> **LVNI \_ todireita**</dt><dt></dt> </dl>                   | Procura um item à direita do item especificado.<br/>                                                                                                                                                                                                                                                                                                                                               |
| <span id="_______________LVNI_DIRECTIONMASK"></span><span id="_______________lvni_directionmask"></span><dl> <dt> **LVNI \_ DIRECTIONMASK**</dt><dt></dt> </dl> | **Windows Vista e posterior:** Uma máscara de sinalizador direcional com o valor da seguinte maneira: LVNI \_ acima \| LVNI \_ abaixo \| LVNI \_ \| LVNI à \_ direita.<br/>                                                                                                                                                                                                                                                               |
| <dl> <dt></dt><dt>O estado do item a ser localizado pode ser especificado com um ou uma combinação dos seguintes valores:</dt> </dl>                                |                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="_______________LVNI_CUT"></span><span id="_______________lvni_cut"></span><dl> <dt> **LVNI \_ recortar**</dt><dt></dt> </dl>                               | O item tem o sinalizador de estado de [**\_ recorte LVIS**](list-view-item-states.md) definido.<br/>                                                                                                                                                                                                                                                                                                                   |
| <span id="_______________LVNI_DROPHILITED"></span><span id="_______________lvni_drophilited"></span><dl> <dt> **LVNI \_ DROPHILITED**</dt><dt></dt> </dl>       | O item tem o sinalizador de estado [**LVIS \_ DROPHILITED**](list-view-item-states.md) definido<br/>                                                                                                                                                                                                                                                                                                    |
| <span id="_______________LVNI_FOCUSED"></span><span id="_______________lvni_focused"></span><dl> <dt> **LVNI com \_ foco**</dt><dt></dt> </dl>                   | O item tem o sinalizador de estado [**LVIS \_ focalizado**](list-view-item-states.md) definido.<br/>                                                                                                                                                                                                                                                                                                           |
| <span id="_______________LVNI_SELECTED"></span><span id="_______________lvni_selected"></span><dl> <dt> **LVNI \_ selecionado**</dt><dt></dt> </dl>                | O item tem o sinalizador de estado [**LVIS \_ selecionado**](list-view-item-states.md) definido.<br/>                                                                                                                                                                                                                                                                                                         |
| <span id="_______________LVNI_STATEMASK"></span><span id="_______________lvni_statemask"></span><dl> <dt> **LVNI \_ STATEMASK**</dt><dt></dt> </dl>             | **Windows Vista e posterior:** Uma máscara de sinalizador de estado com o valor da seguinte maneira: LVNI \_ focalizado \| LVNI \_ selecionado \| LVNI \_ recortar \| LVNI \_ DROPHILITED.<br/>                                                                                                                                                                                                                                                               |
| <dl> <dt></dt><dt>Pesquisa por aparência de itens ou por grupo.</dt> </dl>                                                                                     |                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="_______________LVNI_VISIBLEORDER"></span><span id="_______________lvni_visibleorder"></span><dl> <dt> **LVNI \_ VISIBLEORDER**</dt><dt></dt> </dl>    | **Windows Vista e posterior:** Pesquise a ordem visível.<br/>                                                                                                                                                                                                                                                                                                                                                 |
| <span id="_______________LVNI_VISIBLEONLY"></span><span id="_______________lvni_visibleonly"></span><dl> <dt> **LVNI \_ VISIBLEONLY**</dt><dt></dt> </dl>       | **Windows Vista e posterior:** Pesquisar os itens visíveis.<br/>                                                                                                                                                                                                                                                                                                                                                 |
| <span id="_______________LVNI_SAMEGROUPONLY"></span><span id="_______________lvni_samegrouponly"></span><dl> <dt> **LVNI \_ SAMEGROUPONLY**</dt><dt></dt> </dl> | **Windows Vista e posterior:** Pesquise o grupo atual.<br/>                                                                                                                                                                                                                                                                                                                                                 |
| <dl> <dt></dt><dt>Se um item não tiver todos os sinalizadores de estado especificados definidos, a pesquisa continuará com o próximo item.</dt> </dl>                          |                                                                                                                                                                                                                                                                                                                                                                                                                   |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.

## <a name="remarks"></a>Comentários

Observe que os sinalizadores a seguir, para uso somente com o Windows Vista, são mutuamente exclusivos de quaisquer outros sinalizadores em uso: LVNI \_ Previous, LVNI \_ VISIBLEONLY, LVNI \_ SAMEGROUPONLY, LVNI \_ VISIBLEORDER, LVNI \_ DIRECTIONMASK e LVNI \_ STATEMASK.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_GETNEXTITEM LVM**](lvm-getnextitem.md)
</dt> </dl>

 

 





