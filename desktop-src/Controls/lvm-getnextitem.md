---
title: Mensagem de LVM_GETNEXTITEM (commctrl. h)
description: Pesquisa um item de exibição de lista que tem as propriedades especificadas e possui a relação especificada para um item especificado. Você pode enviar essa mensagem explicitamente ou usando a \_ macro GetNextItem do ListView.
ms.assetid: 2d458f12-b9d3-4b9e-bcb4-927c14c16537
keywords:
- Controles de LVM_GETNEXTITEM de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_GETNEXTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7c4282ebf3572587dd5c8b8b3df1906a51a920e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918969"
---
# <a name="lvm_getnextitem-message"></a>\_Mensagem GETNEXTITEM LVM

Pesquisa um item de exibição de lista que tem as propriedades especificadas e possui a relação especificada para um item especificado. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ GetNextItem do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getnextitem) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice do item no qual começar a pesquisa, ou-1 para localizar o primeiro item que corresponde aos sinalizadores especificados. O item especificado em si é excluído da pesquisa.

</dd> <dt>

*lParam* 
</dt> <dd>

Especifica a relação com o item especificado em *wParam*. Isso pode ser um ou uma combinação dos seguintes valores:



| Valor                                                                                                                                                                                                                                                             | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt></dt><dt>Pesquisa por índice.</dt> </dl>                                                                                                               |                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="_______________LVNI_ALL"></span><span id="_______________lvni_all"></span><dl> <dt> **LVNI \_ tudo**</dt><dt></dt> </dl>                               | Procura um item subsequente por índice, o valor padrão.<br/>                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="_______________LVNI_PREVIOUS"></span><span id="_______________lvni_previous"></span><dl> <dt> **LVNI \_ anterior**</dt><dt></dt> </dl>                | **Windows Vista e posterior:** Pesquisa um item que é ordenado antes do item especificado em *wParam*. O \_ sinalizador LVNI anterior não é direcional (LVNI \_ acima encontrará o item posicionado acima, enquanto \_ o LVNI anterior encontrará o item solicitado anteriormente.) O \_ sinalizador anterior LVNI basicamente reverte a lógica da pesquisa executada pelas mensagens **LVM \_ GETNEXTITEM** ou [**LVM \_ GETNEXTITEMINDEX**](lvm-getnextitemindex.md) .<br/> |
| <dl> <dt></dt><dt>Pesquisa por relação física com o índice do item em que a pesquisa deve começar.</dt> </dl>                                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="_______________LVNI_ABOVE"></span><span id="_______________lvni_above"></span><dl> <dt> **LVNI \_ acima**</dt><dt></dt> </dl>                         | Pesquisa um item que está acima do item especificado.<br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="_______________LVNI_BELOW"></span><span id="_______________lvni_below"></span><dl> <dt> **LVNI \_ abaixo**</dt><dt></dt> </dl>                         | Pesquisa um item que está abaixo do item especificado.<br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="_______________LVNI_TOLEFT"></span><span id="_______________lvni_toleft"></span><dl> <dt> **LVNI \_ toleft**</dt><dt></dt> </dl>                      | Procura um item à esquerda do item especificado.<br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="_______________LVNI_TORIGHT"></span><span id="_______________lvni_toright"></span><dl> <dt> **LVNI \_ todireita**</dt><dt></dt> </dl>                   | Procura um item à direita do item especificado.<br/>                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="_______________LVNI_DIRECTIONMASK"></span><span id="_______________lvni_directionmask"></span><dl> <dt> **LVNI \_ DIRECTIONMASK**</dt><dt></dt> </dl> | **Windows Vista e posterior:** Uma máscara de sinalizador direcional com o valor da seguinte maneira: LVNI \_ acima \| LVNI \_ abaixo \| LVNI \_ \| LVNI à \_ direita.<br/>                                                                                                                                                                                                                                                                                                   |
| <dl> <dt></dt><dt>O estado do item a ser localizado pode ser especificado com um ou uma combinação dos seguintes valores:</dt> </dl>                                |                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="_______________LVNI_CUT"></span><span id="_______________lvni_cut"></span><dl> <dt> **LVNI \_ recortar**</dt><dt></dt> </dl>                               | O item tem o sinalizador de estado de [**\_ recorte LVIS**](list-view-item-states.md) definido.<br/>                                                                                                                                                                                                                                                                                                                                                       |
| <span id="_______________LVNI_DROPHILITED"></span><span id="_______________lvni_drophilited"></span><dl> <dt> **LVNI \_ DROPHILITED**</dt><dt></dt> </dl>       | O item tem o sinalizador de estado [**LVIS \_ DROPHILITED**](list-view-item-states.md) definido<br/>                                                                                                                                                                                                                                                                                                                                        |
| <span id="_______________LVNI_FOCUSED"></span><span id="_______________lvni_focused"></span><dl> <dt> **LVNI com \_ foco**</dt><dt></dt> </dl>                   | O item tem o sinalizador de estado [**LVIS \_ focalizado**](list-view-item-states.md) definido.<br/>                                                                                                                                                                                                                                                                                                                                               |
| <span id="_______________LVNI_SELECTED"></span><span id="_______________lvni_selected"></span><dl> <dt> **LVNI \_ selecionado**</dt><dt></dt> </dl>                | O item tem o sinalizador de estado [**LVIS \_ selecionado**](list-view-item-states.md) definido.<br/>                                                                                                                                                                                                                                                                                                                                             |
| <span id="_______________LVNI_STATEMASK"></span><span id="_______________lvni_statemask"></span><dl> <dt> **LVNI \_ STATEMASK**</dt><dt></dt> </dl>             | **Windows Vista e posterior:** Uma máscara de sinalizador de estado com o valor da seguinte maneira: LVNI \_ focalizado \| LVNI \_ selecionado \| LVNI \_ recortar \| LVNI \_ DROPHILITED.<br/>                                                                                                                                                                                                                                                                                                   |
| <dl> <dt></dt><dt>Pesquisa por aparência de itens ou por grupo</dt> </dl>                                                                                      |                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="_______________LVNI_VISIBLEORDER"></span><span id="_______________lvni_visibleorder"></span><dl> <dt> **LVNI \_ VISIBLEORDER**</dt><dt></dt> </dl>    | **Windows Vista e posterior:** Pesquise a ordem visível.<br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="_______________LVNI_VISIBLEONLY"></span><span id="_______________lvni_visibleonly"></span><dl> <dt> **LVNI \_ VISIBLEONLY**</dt><dt></dt> </dl>       | **Windows Vista e posterior:** Pesquisar os itens visíveis.<br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="_______________LVNI_SAMEGROUPONLY"></span><span id="_______________lvni_samegrouponly"></span><dl> <dt> **LVNI \_ SAMEGROUPONLY**</dt><dt></dt> </dl> | **Windows Vista e posterior:** Pesquise o grupo atual.<br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| <dl> <dt></dt><dt>Se um item não tiver todos os sinalizadores de estado especificados definidos, a pesquisa continuará com o próximo item.</dt> </dl>                          |                                                                                                                                                                                                                                                                                                                                                                                                                                                       |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o índice do próximo item, se for bem-sucedido, ou-1 caso contrário.

## <a name="remarks"></a>Comentários

Observe que os sinalizadores a seguir, para uso somente com o Windows Vista, são mutuamente exclusivos de quaisquer outros sinalizadores em uso: LVNI \_ VISIBLEONLY, LVNI \_ SAMEGROUPONLY, LVNI \_ VISIBLEORDER, LVNI \_ DIRECTIONMASK e LVNI \_ STATEMASK.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





