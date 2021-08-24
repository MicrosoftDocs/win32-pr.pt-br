---
title: Mensagem de TVM_GETIMAGELIST (commctrl. h)
description: Recupera o identificador para a lista de imagens normal ou de estado associada a um controle de exibição de árvore. Você pode enviar essa mensagem explicitamente ou usando a macro do TreeView \_ GetImageList.
ms.assetid: bcf5eac8-cb07-4cf8-ad93-47319fc915a5
keywords:
- controles de Windows de mensagem de TVM_GETIMAGELIST
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
ms.openlocfilehash: 2b7536f21757d5ad03446654d9eed17444e4e07570c3f4bf032b7d32f0009208
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119293276"
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

## <a name="return-value"></a>Valor retornado

Retorna um identificador HIMAGELIST para a lista de imagens especificada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**TVM \_ SETimagelist**](tvm-setimagelist.md)
</dt> </dl>

 

 





