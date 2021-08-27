---
title: LVM_SETCALLBACKMASK mensagem (Commctrl.h)
description: Altera a máscara de retorno de chamada para um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a \_ macro ListView SetCallbackMask.
ms.assetid: d7828bab-9897-408c-99ca-fad42b431be8
keywords:
- LVM_SETCALLBACKMASK controles de Windows mensagem
topic_type:
- apiref
api_name:
- LVM_SETCALLBACKMASK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79e33b106eb0c59f83e40b9f170dd017fcdda412072ed51a26572fcf368f5215
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088846"
---
# <a name="lvm_setcallbackmask-message"></a>Mensagem LVM \_ SETCALLBACKMASK

Altera a máscara de retorno de chamada para um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a [**macro \_ ListView SetCallbackMask.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setcallbackmask)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor da máscara de retorno de chamada. Os bits da máscara indicam os estados ou imagens do item para os quais o aplicativo armazena os dados de estado atuais. Esse valor pode ser qualquer combinação das seguintes constantes:



| Valor                                                                                                                                                                           | Significado                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <span id="LVIS_CUT"></span><span id="lvis_cut"></span><dl> <dt>**LVIS \_ CUT**</dt> </dl>                                  | O item é marcado para uma operação de recortar e colar.<br/>                                       |
| <span id="LVIS_DROPHILITED"></span><span id="lvis_drophilited"></span><dl> <dt>**LVIS \_ DROPHILITED**</dt> </dl>          | O item é realçada como um destino do tipo "arrastar e soltar".<br/>                                      |
| <span id="LVIS_FOCUSED"></span><span id="lvis_focused"></span><dl> <dt>**LVIS \_ FOCALIZADO**</dt> </dl>                      | O item tem o foco.<br/>                                                                 |
| <span id="LVIS_SELECTED"></span><span id="lvis_selected"></span><dl> <dt>**LVIS \_ SELECTED**</dt> </dl>                   | O item está selecionado. <br/>                                                                  |
| <span id="LVIS_OVERLAYMASK"></span><span id="lvis_overlaymask"></span><dl> <dt>**SOBREPOSIÇÃO DE \_ LVISMASK**</dt> </dl>          | O aplicativo armazena o índice da lista de imagens da imagem de sobreposição atual para cada item.<br/> |
| <span id="LVIS_STATEIMAGEMASK"></span><span id="lvis_stateimagemask"></span><dl> <dt>**LVIS \_ STATEIMAGEMASK**</dt> </dl> | O aplicativo armazena o índice da lista de imagens da imagem de estado atual para cada item. <br/>  |



 

</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna **TRUE se** for bem-sucedido ou FALSE **caso** contrário.

## <a name="remarks"></a>Comentários

A *máscara de retorno de* chamada de um controle de exibição de lista é um conjunto de sinalizadores de bits que especificam os estados de item para os quais o aplicativo, em vez do controle, armazena os dados atuais. A máscara de retorno de chamada se aplica a todos os itens do controle, ao contrário da designação de item de retorno de chamada, que se aplica a um item específico. A máscara de retorno de chamada é zero por padrão, o que significa que o controle de exibição de lista armazena todas as informações de estado do item. Depois de criar um controle de exibição de lista e inicializar seus itens, você pode enviar a mensagem **LVM \_ SETCALLBACKMASK** para alterar a máscara de retorno de chamada. Para recuperar a máscara de retorno de chamada atual, envie a [**mensagem \_ GETCALLBACKMASK LVM.**](lvm-getcallbackmask.md)

Para obter mais informações sobre imagens de sobreposição e imagens de estado, [consulte Adicionando List-View de imagens](using-list-view-controls.md).

Para obter mais informações sobre retornos de chamada de exibição de lista, consulte [Itens de retorno de chamada e Máscara de Retorno de Chamada](list-view-controls-overview.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**LVN \_ GETDISPINFO**](lvn-getdispinfo.md)
</dt> </dl>

 

 





