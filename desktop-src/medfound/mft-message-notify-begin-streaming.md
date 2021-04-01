---
description: Notifica uma Media Foundation transformação (MFT) que o streaming está prestes a começar.
ms.assetid: a7f02e92-a747-4ac6-aa83-60897acb2bc5
title: MFT_MESSAGE_NOTIFY_BEGIN_STREAMING (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1aa67f58c7246b50292f4b34711e0149eb8f3377
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164912"
---
# <a name="mft_message_notify_begin_streaming"></a>notificação de mensagem de MFT \_ \_ \_ Iniciar \_ streaming

Notifica uma Media Foundation transformação (MFT) que o streaming está prestes a começar.

## <a name="message-parameter"></a>Parâmetro de mensagem

Nenhum.

## <a name="remarks"></a>Comentários

Para enviar esta mensagem, chame [**IMFTransform::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).

O cliente não é necessário para enviar esta mensagem. Se o cliente enviar essa mensagem, ele deverá fazer isso depois de definir todos os tipos de mídia no MFT e antes de chamar [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput). O MFT pode responder alocando buffers ou outros recursos. Se o cliente não enviar essa mensagem, o MFT alocará recursos na primeira chamada para **ProcessInput**. Portanto, o envio dessa mensagem pode reduzir a latência inicial quando o streaming começa.

### <a name="implementation"></a>Implementação

Um MFT não é necessário para responder a esta mensagem.

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

 

 




