---
description: Notifica uma Media Foundation (MFT) de que o streaming está prestes a começar.
ms.assetid: a7f02e92-a747-4ac6-aa83-60897acb2bc5
title: MFT_MESSAGE_NOTIFY_BEGIN_STREAMING (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 491f84ee2dee752cccc251187c43bd497723a64ae6601954051f2aebab34ef85
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119848056"
---
# <a name="mft_message_notify_begin_streaming"></a>NOTIFICAÇÃO DE \_ MENSAGEM MFT \_ INICIAR \_ \_ STREAMING

Notifica uma Media Foundation (MFT) de que o streaming está prestes a começar.

## <a name="message-parameter"></a>Parâmetro message

Nenhum.

## <a name="remarks"></a>Comentários

Para enviar essa mensagem, chame [**IMFTransform::P rocessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).

O cliente não é necessário para enviar essa mensagem. Se o cliente enviar essa mensagem, ele deverá fazer isso depois de definir todos os tipos de mídia no MFT e antes de chamar [**ProcessInput.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) O MFT pode responder alocando buffers ou outros recursos. Se o cliente não enviar essa mensagem, o MFT alocará recursos na primeira chamada para **ProcessInput.** Portanto, enviar essa mensagem pode reduzir a latência inicial quando o streaming começa.

### <a name="implementation"></a>Implementação

Uma MFT não é necessária para responder a essa mensagem.

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

 

 




