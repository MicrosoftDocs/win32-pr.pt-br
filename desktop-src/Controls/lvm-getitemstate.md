---
title: LVM_GETITEMSTATE mensagem (Commctrl.h)
description: Recupera o estado de um item de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a \_ macro ListView GetItemState.
ms.assetid: 862960ed-a64a-4d66-b384-9228932eae6f
keywords:
- LVM_GETITEMSTATE controles de Windows mensagem
topic_type:
- apiref
api_name:
- LVM_GETITEMSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4737be14f3e975f87a6cbea460ef53dd40ecbb7b6a2d06c39a247dbe8aa0a14e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958295"
---
# <a name="lvm_getitemstate-message"></a>Mensagem LVM \_ GETITEMSTATE

Recupera o estado de um item de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ ListView GetItemState.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemstate)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice do item de exibição de lista.

</dd> <dt>

*lParam* 
</dt> <dd>

Informações de estado a recuperar. Esse parâmetro pode ser uma combinação dos seguintes valores:



| Valor                                                                                                                                                                           | Significado                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LVIS_CUT"></span><span id="lvis_cut"></span><dl> <dt>**LVIS \_ CUT**</dt> </dl>                                  | O item é marcado para uma operação de recortar e colar.<br/>                                                                                                         |
| <span id="LVIS_DROPHILITED"></span><span id="lvis_drophilited"></span><dl> <dt>**LVIS \_ DROPHILITED**</dt> </dl>          | O item é realçada como um destino do tipo "arrastar e soltar".<br/>                                                                                                        |
| <span id="LVIS_FOCUSED"></span><span id="lvis_focused"></span><dl> <dt>**LVIS \_ FOCALIZADO**</dt> </dl>                      | O item tem o foco, portanto, está entre um retângulo de foco padrão. Embora mais de um item possa ser selecionado, apenas um item pode ter o foco.<br/> |
| <span id="LVIS_SELECTED"></span><span id="lvis_selected"></span><dl> <dt>**LVIS \_ SELECTED**</dt> </dl>                   | O item está selecionado. A aparência de um item selecionado depende se ele tem o foco e também as cores do sistema usadas para seleção.<br/>             |
| <span id="LVIS_OVERLAYMASK"></span><span id="lvis_overlaymask"></span><dl> <dt>**SOBREPOSIÇÃO DE \_ LVISMASK**</dt> </dl>          | Use essa máscara para recuperar o índice de imagem de sobreposição do item.<br/>                                                                                                 |
| <span id="LVIS_STATEIMAGEMASK"></span><span id="lvis_stateimagemask"></span><dl> <dt>**LVIS \_ STATEIMAGEMASK**</dt> </dl> | Use essa máscara para recuperar o índice de imagem de estado do item.<br/>                                                                                                   |



 

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna o estado atual do item especificado. Os únicos bits válidos no valor de retorno são aqueles que correspondem aos bits definidos no *parâmetro lParam.*

## <a name="remarks"></a>Comentários

As informações de estado de um item incluem um conjunto de sinalizadores de bits, bem como índices de lista de imagens que indicam a imagem de estado do item e a imagem de sobreposição.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**LVM \_ SETITEMSTATE**](lvm-setitemstate.md)
</dt> </dl>

 

 





