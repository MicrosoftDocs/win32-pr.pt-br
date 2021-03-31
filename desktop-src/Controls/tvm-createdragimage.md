---
title: Mensagem de TVM_CREATEDRAGIMAGE (commctrl. h)
description: Cria um bitmap de arrastar para o item especificado em um controle de exibição de árvore.
ms.assetid: fbe97921-c9d3-473c-933c-d6bc0599e24d
keywords:
- Controles de TVM_CREATEDRAGIMAGE de mensagens do Windows
topic_type:
- apiref
api_name:
- TVM_CREATEDRAGIMAGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 189b37affc6a4382541faea13199cacfcb9b7df5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085630"
---
# <a name="tvm_createdragimage-message"></a>\_Mensagem TVM CREATEDRAGIMAGE

Cria um bitmap de arrastar para o item especificado em um controle de exibição de árvore. A mensagem também cria uma lista de imagens para o bitmap e adiciona o bitmap à lista de imagens. Um aplicativo pode exibir a imagem ao arrastar o item usando as funções de lista de imagens. Você pode enviar essa mensagem explicitamente ou usando a macro [**TreeView \_ CreateDragImage**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_createdragimage) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Identificador para o item que recebe o novo bitmap de arrastar.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o identificador para a lista de imagens para a qual o bitmap de arrastar foi adicionado, se for bem-sucedido, ou **NULL** de outra forma.

## <a name="remarks"></a>Comentários

Se você criar um controle de exibição de árvore sem uma lista de imagens associada, não poderá usar a mensagem **TVM \_ CREATEDRAGIMAGE** para criar a imagem a ser exibida durante uma operação de arrastar. Você deve implementar seu próprio método de criação de um cursor de arrastar.

Seu aplicativo é responsável por destruir a lista de imagens quando ela não é mais necessária.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





