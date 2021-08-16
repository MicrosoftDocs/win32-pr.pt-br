---
title: Mensagem de BCM_GETIMAGELIST (commctrl. h)
description: Obtém a estrutura de IMAGELIST do botão \_ que descreve a lista de imagens atribuída a um controle de botão. Você pode enviar essa mensagem explicitamente ou usar a \_ macro GetImageList do botão.
ms.assetid: 79383758-53d4-4955-b472-befd338cbec6
keywords:
- controles de Windows de mensagem de BCM_GETIMAGELIST
topic_type:
- apiref
api_name:
- BCM_GETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba74f358e80871ffad4822fd8088ca6aeb58521d8878254ed920356db5a6daf2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117833907"
---
# <a name="bcm_getimagelist-message"></a>Mensagem do BCM \_ GETimagelist

Obtém a estrutura de [**\_ IMAGELIST do botão**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) que descreve a lista de imagens atribuída a um controle de botão. Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ GetImageList do botão**](/windows/desktop/api/Commctrl/nf-commctrl-button_getimagelist) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Não usado; deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma estrutura de [**botão \_ IMAGELIST**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) que contém informações da lista de imagens.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a mensagem tiver sucesso, retornará **true**. Caso contrário, retornará **false**.

## <a name="remarks"></a>Comentários

> [!Note]  
> Para usar essa mensagem, você deve fornecer um manifesto especificando Comclt32.dll versão 6,0. Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





