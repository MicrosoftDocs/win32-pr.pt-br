---
title: Mensagem de LVM_SETCALLBACKMASK (commctrl. h)
description: Altera a máscara de retorno de chamada para um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a \_ macro SetCallbackMask do ListView.
ms.assetid: d7828bab-9897-408c-99ca-fad42b431be8
keywords:
- Controles de LVM_SETCALLBACKMASK de mensagens do Windows
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
ms.openlocfilehash: ef6dd46228c4e4aeada30f469a77f9e67aff3a37
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085405"
---
# <a name="lvm_setcallbackmask-message"></a>\_Mensagem SETCALLBACKMASK LVM

Altera a máscara de retorno de chamada para um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ SetCallbackMask do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setcallbackmask) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor da máscara de retorno de chamada. Os bits da máscara indicam os Estados do item ou as imagens para as quais o aplicativo armazena os dados de estado atuais. Esse valor pode ser qualquer combinação das seguintes constantes:



| Valor                                                                                                                                                                           | Significado                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <span id="LVIS_CUT"></span><span id="lvis_cut"></span><dl> <dt>**LVIS \_ recortar**</dt> </dl>                                  | O item é marcado para uma operação de recortar e colar.<br/>                                       |
| <span id="LVIS_DROPHILITED"></span><span id="lvis_drophilited"></span><dl> <dt>**LVIS \_ DROPHILITED**</dt> </dl>          | O item é realçado como um destino do tipo "arrastar e soltar".<br/>                                      |
| <span id="LVIS_FOCUSED"></span><span id="lvis_focused"></span><dl> <dt>**LVIS com \_ foco**</dt> </dl>                      | O item tem o foco.<br/>                                                                 |
| <span id="LVIS_SELECTED"></span><span id="lvis_selected"></span><dl> <dt>**LVIS \_ selecionado**</dt> </dl>                   | O item está selecionado. <br/>                                                                  |
| <span id="LVIS_OVERLAYMASK"></span><span id="lvis_overlaymask"></span><dl> <dt>**LVIS \_ OVERLAYMASK**</dt> </dl>          | O aplicativo armazena o índice da lista de imagens da imagem de sobreposição atual para cada item.<br/> |
| <span id="LVIS_STATEIMAGEMASK"></span><span id="lvis_stateimagemask"></span><dl> <dt>**LVIS \_ STATEIMAGEMASK**</dt> </dl> | O aplicativo armazena o índice da lista de imagens da imagem de estado atual para cada item. <br/>  |



 

</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.

## <a name="remarks"></a>Comentários

A *máscara de retorno de chamada* de um controle de exibição de lista é um conjunto de sinalizadores de bits que especificam os Estados de item para os quais o aplicativo, em vez do controle, armazena os dados atuais. A máscara de retorno de chamada aplica-se a todos os itens do controle, diferentemente da designação do item de retorno de chamada, que se aplica a um item específico. A máscara de retorno de chamada é zero por padrão, o que significa que o controle List-View armazena todas as informações de estado do item. Depois de criar um controle de exibição de lista e inicializar seus itens, você pode enviar a mensagem **LVM \_ SETCALLBACKMASK** para alterar a máscara de retorno de chamada. Para recuperar a máscara de retorno de chamada atual, envie a mensagem [**LVM \_ GETCALLBACKMASK**](lvm-getcallbackmask.md) .

Para obter mais informações sobre imagens de sobreposição e imagens de estado, consulte [adicionando List-View listas](using-list-view-controls.md)de imagens.

Para obter mais informações sobre retornos de chamada de exibição de lista, consulte [itens de retorno de chamada e a máscara de retorno de chamada](list-view-controls-overview.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**LVN \_ GETDISPINFO**](lvn-getdispinfo.md)
</dt> </dl>

 

 





