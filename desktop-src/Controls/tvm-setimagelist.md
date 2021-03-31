---
title: Mensagem de TVM_SETIMAGELIST (commctrl. h)
description: Define a lista de imagens normal ou de estado para um controle de exibição em árvore e redesenha o controle usando as novas imagens. Você pode enviar essa mensagem explicitamente ou usando a macro do \_ Defaultimagelist de árvore.
ms.assetid: 1a7bf2f8-c7db-44a8-b234-0ffc498e9000
keywords:
- Controles de TVM_SETIMAGELIST de mensagens do Windows
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
ms.openlocfilehash: 8f308cb8a56b2e74a5703af144bac03c271efc95
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644663"
---
# <a name="tvm_setimagelist-message"></a>\_Mensagem TVM SETimagelist

Define a lista de imagens normal ou de estado para um controle de exibição em árvore e redesenha o controle usando as novas imagens. Você pode enviar essa mensagem explicitamente ou usando a macro [**do \_ defaultimagelist de árvore**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setimagelist) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Tipo de lista de imagens a ser definida. Esse parâmetro pode ser um dos seguintes valores:



| Valor                                                                                                                                                      | Significado                                                                                                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TVSIL_NORMAL"></span><span id="tvsil_normal"></span><dl> <dt>**TVSIL \_ normal**</dt> </dl> | Indica a lista de imagens normal, que contém imagens selecionadas, não selecionadas e sobreposição para os itens de um controle de exibição de árvore.<br/>                                                          |
| <span id="TVSIL_STATE"></span><span id="tvsil_state"></span><dl> <dt>**\_estado TVSIL**</dt> </dl>    | Indica a lista de imagens de estado. Você pode usar imagens de estado para indicar os Estados de itens definidos pelo aplicativo. Uma imagem de estado é exibida à esquerda da imagem selecionada ou não marcada de um item.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador para a lista de imagens. Se *lParam* for **NULL**, a mensagem removerá a lista de imagens especificada do controle de exibição de árvore.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o identificador para a lista de imagens anterior, se houver, ou **NULL** de outra forma.

## <a name="remarks"></a>Comentários

O controle de exibição de árvore não destruirá a lista de imagens especificada com esta mensagem. Seu aplicativo deve destruir a lista de imagens quando ela não for mais necessária.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**TVM \_ GETimagelist**](tvm-getimagelist.md)
</dt> </dl>

 

 





