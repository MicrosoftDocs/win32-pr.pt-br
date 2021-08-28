---
title: Mensagem de LVM_SETIMAGELIST (commctrl. h)
description: Atribui uma lista de imagens a um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a \_ macro Defaultimagelist de ListView.
ms.assetid: 5241065b-85e4-412e-9868-fd5b15ff7c17
keywords:
- controles de Windows de mensagem de LVM_SETIMAGELIST
topic_type:
- apiref
api_name:
- LVM_SETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4151f7d6e3736e6fe28faa28bc258fb4f85bfb57622b1ec77c02ed83ea187941
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119919956"
---
# <a name="lvm_setimagelist-message"></a>Mensagem do LVM \_ SETimagelist

Atribui uma lista de imagens a um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ defaultimagelist de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setimagelist) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Tipo de lista de imagens. Esse parâmetro pode ser um dos seguintes valores:



| Valor                                                                                                                                                                     | Significado                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <span id="LVSIL_NORMAL"></span><span id="lvsil_normal"></span><dl> <dt>**LVSIL \_ normal**</dt> </dl>                | Lista de imagens com ícones grandes.<br/>  |
| <span id="LVSIL_SMALL"></span><span id="lvsil_small"></span><dl> <dt>**LVSIL \_ pequeno**</dt> </dl>                   | Lista de imagens com ícones pequenos.<br/>  |
| <span id="LVSIL_STATE"></span><span id="lvsil_state"></span><dl> <dt>**\_estado LVSIL**</dt> </dl>                   | Lista de imagem com imagens de estado.<br/> |
| <span id="LVSIL_GROUPHEADER"></span><span id="lvsil_groupheader"></span><dl> <dt>**\_GROUPHEADER LVSIL**</dt> </dl> | Lista de imagens para cabeçalho de grupo.<br/>  |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador para a lista de imagens a ser atribuída.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna o identificador para a lista de imagens associada anteriormente ao controle, se for bem-sucedido, ou **NULL** de outra forma.

## <a name="remarks"></a>Comentários

A lista de imagens atual será destruída quando o controle de exibição de lista for destruído, a menos que o estilo [**LVS \_ SHAREIMAGELISTS**](list-view-window-styles.md) seja definido. Se você usar essa mensagem para substituir uma lista de imagens por outra, seu aplicativo deverá destruir explicitamente todas as listas de imagens diferentes da atual.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





