---
title: Mensagem de TVM_GETIMAGELIST (commctrl. h)
description: Recupera o identificador para a lista de imagens normal ou de estado associada a um controle de exibição de árvore. Você pode enviar essa mensagem explicitamente ou usando a macro do TreeView \_ GetImageList.
ms.assetid: bcf5eac8-cb07-4cf8-ad93-47319fc915a5
keywords:
- Controles de TVM_GETIMAGELIST de mensagens do Windows
topic_type:
- apiref
api_name:
- TVM_GETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e4e2503d9c6d57743059ee1da3049a36ed17f2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645122"
---
# <a name="tvm_getimagelist-message"></a>\_Mensagem TVM GETimagelist

Recupera o identificador para a lista de imagens normal ou de estado associada a um controle de exibição de árvore. Você pode enviar essa mensagem explicitamente ou usando a macro do [**TreeView \_ GetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getimagelist) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Tipo de lista de imagens a recuperar. Esse parâmetro pode ser um dos seguintes valores:



| Valor                                                                                                                                                      | Significado                                                                                                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TVSIL_NORMAL"></span><span id="tvsil_normal"></span><dl> <dt>**TVSIL \_ normal**</dt> </dl> | Indica a lista de imagens normal, que contém imagens selecionadas, não selecionadas e sobreposição para os itens de um controle de exibição de árvore.<br/>                                                          |
| <span id="TVSIL_STATE"></span><span id="tvsil_state"></span><dl> <dt>**\_estado TVSIL**</dt> </dl>    | Indica a lista de imagens de estado. Você pode usar imagens de estado para indicar os Estados de itens definidos pelo aplicativo. Uma imagem de estado é exibida à esquerda da imagem selecionada ou não marcada de um item.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um identificador HIMAGELIST para a lista de imagens especificada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**TVM \_ SETimagelist**](tvm-setimagelist.md)
</dt> </dl>

 

 





