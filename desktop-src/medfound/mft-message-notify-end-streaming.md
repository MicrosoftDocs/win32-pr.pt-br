---
description: Solicita uma Media Foundation transformação (MFT) para que o streaming esteja prestes a terminar.
ms.assetid: df313a66-e80f-499c-a9f2-a7cbaaf0a7d4
title: MFT_MESSAGE_NOTIFY_END_STREAMING (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad2f13635b97db0c6d7751d9648f42b2b4ed8acc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502276"
---
# <a name="mft_message_notify_end_streaming"></a>\_fim da \_ notificação de mensagem \_ de MFT \_

Solicita uma Media Foundation transformação (MFT) para que o streaming esteja prestes a terminar.

## <a name="message-parameter"></a>Parâmetro de mensagem

Nenhum.

## <a name="remarks"></a>Comentários

Para enviar esta mensagem, chame [**IMFTransform::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).

Não é necessário que o cliente envie essa mensagem, mesmo que o cliente tenha enviado anteriormente a mensagem de **\_ início de notificação de \_ \_ \_ transmissão de mensagem de MFT** .

### <a name="implementation"></a>Implementação

O MFT pode responder a essa mensagem liberando buffers e outros recursos. O MFT não libera dados de entrada nem redefine os tipos de mídia em resposta a essa mensagem. Um MFT não é necessário para responder a esta mensagem.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                     |
| parâmetro<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_tipo de mensagem MFT \_**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




