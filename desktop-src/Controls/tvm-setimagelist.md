---
title: TVM_SETIMAGELIST mensagem (Commctrl.h)
description: Define a lista de imagens normais ou de estado para um controle de exibição de árvore e redesenha o controle usando as novas imagens. Você pode enviar essa mensagem explicitamente ou usando a macro TreeView \_ SetImageList.
ms.assetid: 1a7bf2f8-c7db-44a8-b234-0ffc498e9000
keywords:
- TVM_SETIMAGELIST controles Windows mensagem
topic_type:
- apiref
api_name:
- TVM_SETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df79089c7a2071c6af702da9ef862178738ede3dccff312c3fbae7dbefe4de56
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018674"
---
# <a name="tvm_setimagelist-message"></a>Mensagem TVM \_ SETIMAGELIST

Define a lista de imagens normais ou de estado para um controle de exibição de árvore e redesenha o controle usando as novas imagens. Você pode enviar essa mensagem explicitamente ou usando a [**macro TreeView \_ SetImageList.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setimagelist)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Tipo de lista de imagens a ser definida. Esse parâmetro pode ser um dos seguintes valores:



| Valor                                                                                                                                                      | Significado                                                                                                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TVSIL_NORMAL"></span><span id="tvsil_normal"></span><dl> <dt>**TVSIL \_ NORMAL**</dt> </dl> | Indica a lista de imagens normais, que contém imagens selecionadas, não selecionadas e sobreposição para os itens de um controle de exibição de árvore.<br/>                                                          |
| <span id="TVSIL_STATE"></span><span id="tvsil_state"></span><dl> <dt>**ESTADO DE \_ TVSIL**</dt> </dl>    | Indica a lista de imagens de estado. Você pode usar imagens de estado para indicar estados de item definidos pelo aplicativo. Uma imagem de estado é exibida à esquerda da imagem selecionada ou não selecionada de um item.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Lidar com a lista de imagens. Se *lParam* for **NULL,** a mensagem removerá a lista de imagens especificada do controle de exibição de árvore.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna o alça para a lista de imagens anterior, se for o caso, ou **NULL, caso** contrário.

## <a name="remarks"></a>Comentários

O controle de exibição de árvore não destruirá a lista de imagens especificada com essa mensagem. Seu aplicativo deve destruir a lista de imagens quando ela não for mais necessária.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**TVM \_ GETIMAGELIST**](tvm-getimagelist.md)
</dt> </dl>

 

 





