---
title: LVM_GETNEXTITEM mensagem (Commctrl.h)
description: Pesquisa um item de exibição de lista que tem as propriedades especificadas e tem a relação especificada com um item especificado. Você pode enviar essa mensagem explicitamente ou usando a \_ macro ListView GetNextItem.
ms.assetid: 2d458f12-b9d3-4b9e-bcb4-927c14c16537
keywords:
- LVM_GETNEXTITEM controles de Windows mensagem
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
ms.openlocfilehash: 40e8e6fdf068f06176d6965a2fb885b349a74ea5cde73c5952d16d7c76512ae8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002556"
---
# <a name="lvm_getnextitem-message"></a>Mensagem GETNEXTITEM do LVM \_

Pesquisa um item de exibição de lista que tem as propriedades especificadas e tem a relação especificada com um item especificado. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ ListView GetNextItem.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getnextitem)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice do item com o que iniciar a pesquisa ou -1 para encontrar o primeiro item que corresponde aos sinalizadores especificados. O próprio item especificado é excluído da pesquisa.

</dd> <dt>

*lParam* 
</dt> <dd>

Especifica a relação com o item especificado em *wParam*. Isso pode ser uma ou uma combinação dos seguintes valores:



| Valor                                                                                                                                                                                                                                                             | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt></dt><dt>Pesquisa por índice.</dt> </dl>                                                                                                               |                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="_______________LVNI_ALL"></span><span id="_______________lvni_all"></span><dl> <dt> **LVNI \_ ALL**</dt><dt></dt> </dl>                               | Pesquisa um item subsequente por índice, o valor padrão.<br/>                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="_______________LVNI_PREVIOUS"></span><span id="_______________lvni_previous"></span><dl> <dt> **LVNI \_ PREVIOUS**</dt><dt></dt> </dl>                | **Windows Vista e posterior:** Pesquisa um item que é ordenado antes do item especificado em *wParam*. O sinalizador LVNI PREVIOUS não é direcional (LVNI ACIMA encontrará o item posicionado acima, enquanto LVNI PREVIOUS encontrará o \_ \_ item ordenado \_ antes.) O sinalizador LVNI PREVIOUS basicamente inverte a lógica da pesquisa executada pelas mensagens \_ **\_ GETNEXTITEM** ou [**LVM \_ GETNEXTITEMINDEX LVM.**](lvm-getnextitemindex.md)<br/> |
| <dl> <dt></dt><dt>Pesquisa por relação física com o índice do item em que a pesquisa deve começar.</dt> </dl>                                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="_______________LVNI_ABOVE"></span><span id="_______________lvni_above"></span><dl> <dt> **LVNI \_ ACIMA**</dt><dt></dt> </dl>                         | Pesquisa um item que está acima do item especificado.<br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="_______________LVNI_BELOW"></span><span id="_______________lvni_below"></span><dl> <dt> **LVNI \_ ABAIXO**</dt><dt></dt> </dl>                         | Pesquisa um item que está abaixo do item especificado.<br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="_______________LVNI_TOLEFT"></span><span id="_______________lvni_toleft"></span><dl> <dt> **LVNI \_ TOLEFT**</dt><dt></dt> </dl>                      | Pesquisa um item à esquerda do item especificado.<br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="_______________LVNI_TORIGHT"></span><span id="_______________lvni_toright"></span><dl> <dt> **LVNI \_ TORIGHT**</dt><dt></dt> </dl>                   | Pesquisa um item à direita do item especificado.<br/>                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="_______________LVNI_DIRECTIONMASK"></span><span id="_______________lvni_directionmask"></span><dl> <dt> **LVNI \_ DIRECTIONMASK**</dt><dt></dt> </dl> | **Windows Vista e posterior:** Uma máscara de sinalizador direcional com o valor da seguinte forma: \_ \| LVNI ABOVE LVNI \_ BELOW \| LVNI \_ TOLEFT \| LVNI \_ TORIGHT.<br/>                                                                                                                                                                                                                                                                                                   |
| <dl> <dt></dt><dt>O estado do item a ser considerado pode ser especificado com um</dt> ou uma combinação dos seguintes valores: </dl>                                |                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="_______________LVNI_CUT"></span><span id="_______________lvni_cut"></span><dl> <dt> **LVNI \_ CUT**</dt><dt></dt> </dl>                               | O item tem o [**sinalizador de estado \_ LVIS CUT**](list-view-item-states.md) definido.<br/>                                                                                                                                                                                                                                                                                                                                                       |
| <span id="_______________LVNI_DROPHILITED"></span><span id="_______________lvni_drophilited"></span><dl> <dt> **LVNI \_ DROPHILITED**</dt><dt></dt> </dl>       | O item tem o [**sinalizador de estado \_ DROPHILITED LVIS**](list-view-item-states.md) definido<br/>                                                                                                                                                                                                                                                                                                                                        |
| <span id="_______________LVNI_FOCUSED"></span><span id="_______________lvni_focused"></span><dl> <dt> **LVNI \_ FOCALIZADO**</dt><dt></dt> </dl>                   | O item tem o [**sinalizador de estado \_ LVIS FOCUSED**](list-view-item-states.md) definido.<br/>                                                                                                                                                                                                                                                                                                                                               |
| <span id="_______________LVNI_SELECTED"></span><span id="_______________lvni_selected"></span><dl> <dt> **LVNI \_ SELECTED**</dt><dt></dt> </dl>                | O item tem o [**sinalizador de estado LVIS \_ SELECTED**](list-view-item-states.md) definido.<br/>                                                                                                                                                                                                                                                                                                                                             |
| <span id="_______________LVNI_STATEMASK"></span><span id="_______________lvni_statemask"></span><dl> <dt> **LVNI \_ STATEMASK**</dt><dt></dt> </dl>             | **Windows Vista e posterior:** Uma máscara de sinalizador de estado com o valor da seguinte \_ \| forma: LVNI FOCUSED LVNI \_ SELECTED \| \_ \| LVNI CUT LVNI \_ DROPHILITED.<br/>                                                                                                                                                                                                                                                                                                   |
| <dl> <dt></dt><dt>Pesquisa por aparência de itens ou por grupo</dt> </dl>                                                                                      |                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="_______________LVNI_VISIBLEORDER"></span><span id="_______________lvni_visibleorder"></span><dl> <dt> **LVNI \_ VISIBLEORDER**</dt><dt></dt> </dl>    | **Windows Vista e posterior:** Pesquise a ordem visível.<br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="_______________LVNI_VISIBLEONLY"></span><span id="_______________lvni_visibleonly"></span><dl> <dt> **LVNI \_ VISIBLEONLY**</dt><dt></dt> </dl>       | **Windows Vista e posterior:** Pesquise os itens visíveis.<br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="_______________LVNI_SAMEGROUPONLY"></span><span id="_______________lvni_samegrouponly"></span><dl> <dt> **LVNI \_ SAMEGROUPONLY**</dt><dt></dt> </dl> | **Windows Vista e posterior:** Pesquise o grupo atual.<br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| <dl> <dt></dt><dt>Se um item não tiver todos os sinalizadores de estado especificados definidos,</dt> a pesquisa continuará com o próximo item. </dl>                          |                                                                                                                                                                                                                                                                                                                                                                                                                                                       |



 

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna o índice do próximo item se for bem-sucedido ou -1 caso contrário.

## <a name="remarks"></a>Comentários

Observe que os seguintes sinalizadores, para uso somente com o Windows Vista, são mutuamente exclusivos de quaisquer outros sinalizadores em uso: LVNI \_ VISIBLEONLY, LVNI \_ SAMEGROUPONLY, LVNI \_ VISIBLEORDER, LVNI \_ DIRECTIONMASK e LVNI \_ STATEMASK.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





