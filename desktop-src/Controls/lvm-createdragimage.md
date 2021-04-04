---
title: Mensagem de LVM_CREATEDRAGIMAGE (commctrl. h)
description: Cria uma lista de imagens de arrastar para o item especificado. Você pode enviar essa mensagem explicitamente ou usando a \_ macro CreateDragImage do ListView.
ms.assetid: face4c8f-01ff-4f5a-a468-e306a50dae35
keywords:
- Controles de LVM_CREATEDRAGIMAGE de mensagens do Windows
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
ms.openlocfilehash: ace975b178fee85e2794b518a78b40b375c65ae7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085176"
---
# <a name="lvm_createdragimage-message"></a>\_Mensagem CREATEDRAGIMAGE LVM

Cria uma lista de imagens de arrastar para o item especificado. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ CreateDragImage do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_createdragimage) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O índice do item.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma estrutura de [**ponto**](/previous-versions//dd162805(v=vs.85)) que recebe o local inicial do canto superior esquerdo da imagem, em Exibir coordenadas.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o identificador para a lista de imagens de arrastar, se for bem-sucedido, ou **NULL** caso contrário.

## <a name="remarks"></a>Comentários

Seu aplicativo é responsável por destruir a lista de imagens quando ela não é mais necessária.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

