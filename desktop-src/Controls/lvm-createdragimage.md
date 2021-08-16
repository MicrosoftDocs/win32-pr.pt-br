---
title: LVM_CREATEDRAGIMAGE mensagem (Commctrl.h)
description: Cria uma lista de imagens de arrastar para o item especificado. Você pode enviar essa mensagem explicitamente ou usando a \_ macro CreateDragImage listView.
ms.assetid: face4c8f-01ff-4f5a-a468-e306a50dae35
keywords:
- LVM_CREATEDRAGIMAGE controles de Windows mensagem
topic_type:
- apiref
api_name:
- LVM_CREATEDRAGIMAGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d551dfa7b14ecff8c9fd1efe015e173403c1b5981f294a18b3180a42cc03de63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118411991"
---
# <a name="lvm_createdragimage-message"></a>Mensagem LVM \_ CREATEDRAGIMAGE

Cria uma lista de imagens de arrastar para o item especificado. Você pode enviar essa mensagem explicitamente ou usando a [**macro \_ CreateDragImage listView.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_createdragimage)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O índice do item.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma [**estrutura POINT**](/previous-versions//dd162805(v=vs.85)) que recebe o local inicial do canto superior esquerdo da imagem, em coordenadas de exibição.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna o alça para a lista de imagens de arrastar se for bem-sucedido ou **NULL** caso contrário.

## <a name="remarks"></a>Comentários

Seu aplicativo é responsável por destruir a lista de imagens quando ela não é mais necessária.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

