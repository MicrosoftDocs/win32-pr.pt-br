---
title: Mensagem de LVM_SETIMAGELIST (commctrl. h)
description: Atribui uma lista de imagens a um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a \_ macro Defaultimagelist de ListView.
ms.assetid: 5241065b-85e4-412e-9868-fd5b15ff7c17
keywords:
- Controles de LVM_SETIMAGELIST de mensagens do Windows
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
ms.openlocfilehash: 779d31fd781a72dbdfbc4738e091482ca4a08528
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103917991"
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

## <a name="return-value"></a>Retornar valor

Retorna o identificador para a lista de imagens associada anteriormente ao controle, se for bem-sucedido, ou **NULL** de outra forma.

## <a name="remarks"></a>Comentários

A lista de imagens atual será destruída quando o controle de exibição de lista for destruído, a menos que o estilo [**LVS \_ SHAREIMAGELISTS**](list-view-window-styles.md) seja definido. Se você usar essa mensagem para substituir uma lista de imagens por outra, seu aplicativo deverá destruir explicitamente todas as listas de imagens diferentes da atual.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





