---
title: Mensagem de LVM_GETITEMSTATE (commctrl. h)
description: Recupera o estado de um item de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a \_ macro GetItemState do ListView.
ms.assetid: 862960ed-a64a-4d66-b384-9228932eae6f
keywords:
- Controles de LVM_GETITEMSTATE de mensagens do Windows
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
ms.openlocfilehash: 817b355e78f22c01c289f681d256ee6b4d0aa882
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455747"
---
# <a name="lvm_getitemstate-message"></a>Mensagem do LVM \_ GETitemstate

Recupera o estado de um item de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ GetItemState do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemstate) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice do item de exibição de lista.

</dd> <dt>

*lParam* 
</dt> <dd>

Informações de estado a serem recuperadas. Esse parâmetro pode ser uma combinação dos seguintes valores:



| Valor                                                                                                                                                                           | Significado                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LVIS_CUT"></span><span id="lvis_cut"></span><dl> <dt>**LVIS \_ recortar**</dt> </dl>                                  | O item é marcado para uma operação de recortar e colar.<br/>                                                                                                         |
| <span id="LVIS_DROPHILITED"></span><span id="lvis_drophilited"></span><dl> <dt>**LVIS \_ DROPHILITED**</dt> </dl>          | O item é realçado como um destino do tipo "arrastar e soltar".<br/>                                                                                                        |
| <span id="LVIS_FOCUSED"></span><span id="lvis_focused"></span><dl> <dt>**LVIS com \_ foco**</dt> </dl>                      | O item tem o foco, portanto, está circundado por um retângulo de foco padrão. Embora mais de um item possa ser selecionado, somente um item pode ter o foco.<br/> |
| <span id="LVIS_SELECTED"></span><span id="lvis_selected"></span><dl> <dt>**LVIS \_ selecionado**</dt> </dl>                   | O item está selecionado. A aparência de um item selecionado depende de se ele tem o foco e também das cores do sistema usadas para seleção.<br/>             |
| <span id="LVIS_OVERLAYMASK"></span><span id="lvis_overlaymask"></span><dl> <dt>**LVIS \_ OVERLAYMASK**</dt> </dl>          | Use essa máscara para recuperar o índice de imagem de sobreposição do item.<br/>                                                                                                 |
| <span id="LVIS_STATEIMAGEMASK"></span><span id="lvis_stateimagemask"></span><dl> <dt>**LVIS \_ STATEIMAGEMASK**</dt> </dl> | Use essa máscara para recuperar o índice de imagem de estado do item.<br/>                                                                                                   |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o estado atual do item especificado. Os únicos bits válidos no valor de retorno são aqueles que correspondem aos bits definidos no parâmetro *lParam* .

## <a name="remarks"></a>Comentários

As informações de estado de um item incluem um conjunto de sinalizadores de bit, bem como índices de lista de imagens que indicam a imagem de estado e a imagem de sobreposição do item.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**GetItemState do LVM \_**](lvm-setitemstate.md)
</dt> </dl>

 

 





