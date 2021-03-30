---
title: Mensagem de BCM_GETIMAGELIST (commctrl. h)
description: Obtém a estrutura de IMAGELIST do botão \_ que descreve a lista de imagens atribuída a um controle de botão. Você pode enviar essa mensagem explicitamente ou usar a \_ macro GetImageList do botão.
ms.assetid: 79383758-53d4-4955-b472-befd338cbec6
keywords:
- Controles de BCM_GETIMAGELIST de mensagens do Windows
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
ms.openlocfilehash: 5b0c28e997e23d6df63150fe2283d04be1a8c0d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455239"
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

## <a name="return-value"></a>Retornar valor

Se a mensagem tiver sucesso, retornará **true**. Caso contrário, retornará **false**.

## <a name="remarks"></a>Comentários

> [!Note]  
> Para usar essa mensagem, você deve fornecer um manifesto especificando Comclt32.dll versão 6,0. Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





