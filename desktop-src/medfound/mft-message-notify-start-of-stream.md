---
description: Notifica uma Media Foundation (MFT) de que a primeira amostra está prestes a ser processada.
ms.assetid: 579df695-02c4-4332-b1b4-c7bd9da50c0f
title: MFT_MESSAGE_NOTIFY_START_OF_STREAM (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20ed40d9d3514dfa6223d4e20f2eb411caec497e16f2e97c456f16e14442c407
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973025"
---
# <a name="mft_message_notify_start_of_stream"></a>INÍCIO DO FLUXO \_ \_ DE \_ NOTIFICAÇÃO DE MENSAGEM \_ MFT \_

Notifica uma Media Foundation (MFT) de que a primeira amostra está prestes a ser processada.

## <a name="message-parameter"></a>Parâmetro message

Nenhum.

## <a name="remarks"></a>Comentários

Para enviar essa mensagem, chame [**IMFTransform::P rocessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).

Para MFTs síncronos, é opcional enviar essa mensagem.

Para MFTs assíncronos, o cliente deve enviar essa mensagem.

### <a name="implementation"></a>Implementação

Uma MFT síncrona não é necessária para responder à mensagem.

Um MFT assíncrono deve implementar essa mensagem, conforme descrito em [MFTs assíncronos.](asynchronous-mfts.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                     |
| Cabeçalho<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**TIPO DE \_ MENSAGEM \_ MFT**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




