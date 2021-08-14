---
title: TVM_CREATEDRAGIMAGE mensagem (Commctrl.h)
description: Cria um bitmap de arrastar para o item especificado em um controle de exibição de árvore.
ms.assetid: fbe97921-c9d3-473c-933c-d6bc0599e24d
keywords:
- TVM_CREATEDRAGIMAGE controles de Windows mensagem
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
ms.openlocfilehash: a18a00b2225749b30b8dcd9a928fd73e3ffabcfd4a4f9512cd2332d98cc08a79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118408656"
---
# <a name="tvm_createdragimage-message"></a>Mensagem TVM \_ CREATEDRAGIMAGE

Cria um bitmap de arrastar para o item especificado em um controle de exibição de árvore. A mensagem também cria uma lista de imagens para o bitmap e adiciona o bitmap à lista de imagens. Um aplicativo pode exibir a imagem ao arrastar o item usando as funções de lista de imagens. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ TreeView CreateDragImage.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_createdragimage)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Lidar com o item que recebe o novo bitmap de arrastar.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna o alça para a lista de imagens à qual o bitmap de arrastar foi adicionado se for bem-sucedido ou **NULL** caso contrário.

## <a name="remarks"></a>Comentários

Se você criar um controle de exibição de árvore sem uma lista de imagens associada, não poderá usar a mensagem **TVM \_ CREATEDRAGIMAGE** para criar a imagem a ser exibida durante uma operação de arrastar. Você deve implementar seu próprio método de criação de um cursor de arrastar.

Seu aplicativo é responsável por destruir a lista de imagens quando ela não é mais necessária.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





