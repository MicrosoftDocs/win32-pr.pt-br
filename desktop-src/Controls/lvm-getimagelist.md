---
title: Mensagem de LVM_GETIMAGELIST (commctrl. h)
description: Recupera o identificador para uma lista de imagens usada para desenhar itens de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a \_ macro GetImageList de ListView.
ms.assetid: dd48d8b5-6dbd-48ab-95c3-0fcf1e8c24f0
keywords:
- Controles de LVM_GETIMAGELIST de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_GETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0abc68c5e5dd9a18c3ec203ad7fe3db97a542845
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085813"
---
# <a name="lvm_getimagelist-message"></a>Mensagem do LVM \_ GETimagelist

Recupera o identificador para uma lista de imagens usada para desenhar itens de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ GetImageList de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getimagelist) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Lista de imagens a recuperar. Esse parâmetro pode ser um dos seguintes valores:



| Valor                                                                                                                                                                     | Significado                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <span id="LVSIL_NORMAL"></span><span id="lvsil_normal"></span><dl> <dt>**LVSIL \_ normal**</dt> </dl>                | Lista de imagens com ícones grandes.<br/>  |
| <span id="LVSIL_SMALL"></span><span id="lvsil_small"></span><dl> <dt>**LVSIL \_ pequeno**</dt> </dl>                   | Lista de imagens com ícones pequenos.<br/>  |
| <span id="LVSIL_STATE"></span><span id="lvsil_state"></span><dl> <dt>**\_estado LVSIL**</dt> </dl>                   | Lista de imagem com imagens de estado.<br/> |
| <span id="LVSIL_GROUPHEADER"></span><span id="lvsil_groupheader"></span><dl> <dt>**\_GROUPHEADER LVSIL**</dt> </dl> | Lista de imagens para cabeçalho de grupo.<br/>  |



 

</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o identificador para a lista de imagens especificada, se for bem-sucedido, ou **NULL** caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





