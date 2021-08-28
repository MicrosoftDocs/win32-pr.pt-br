---
description: MFT_MESSAGE_COMMAND_DRAIN - solicita uma transformação Media Foundation (MFT) para liberar todos os dados armazenados.
ms.assetid: c48f3a88-a007-4f30-ac60-9e5a8c24e1ee
title: MFT_MESSAGE_COMMAND_DRAIN (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c8faf20ca1169d87370a7dc1b5a128b11c9f17937a514f4aaea37631aee4d83
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012616"
---
# <a name="mft_message_command_drain"></a>DRENO DO \_ COMANDO \_ DE MENSAGEM \_ MFT

Solicita uma transformação Media Foundation (MFT) para liberar todos os dados armazenados.

## <a name="message-parameter"></a>Parâmetro message

Nenhum.

## <a name="remarks"></a>Comentários

Para enviar essa mensagem, chame [**IMFTransform::P rocessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).

Depois que essa mensagem é enviada, o fluxo de entrada especificado não aceita entrada até que o MFT processe todos os dados de chamadas anteriores para [**IMFTransform::P rocessInput.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput)

O processo de esgotamento varia ligeiramente entre MFTs síncronos e MFTs assíncronos:

**MFTs síncronos**

1.  Depois que o cliente envia essa mensagem, ele chama [**IMFTransform::P rocessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) em um loop, até que **ProcessOutput** retorne o código de erro **MF \_ E TRANSFORM NEED MORE \_ \_ \_ \_ INPUT**.
2.  Desde que o MFT ainda tenha dados para processar, outras chamadas para [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) falharão. O MFT continua a produzir a saída até usar todos os dados armazenados. O MFT descarta todos os dados que não podem ser processados em um exemplo de saída completo. (Por exemplo, ele deve soltar um quadro de vídeo parcial.)

**MFTs assíncronos**

1.  O MFT continua a enviar [eventos METransformHaveOutput](metransformhaveoutput.md) até que não tenha mais dados a processar. Ele não envia eventos [METransformNeedInput](metransformneedinput.md) durante esse tempo.
2.  Depois que o MFT envia o último [evento METransformHaveOutput,](metransformhaveoutput.md) ele envia um [evento METransformDhaveComplete.](metransformdraincomplete.md)
3.  Após a conclusão do esgotamento, o MFT não envia outro evento [METransformNeedInput](metransformneedinput.md) até receber uma mensagem NOTIFICAÇÃO DE MENSAGEM MFT DE INÍCIO [**\_ DO \_ \_ \_ \_ FLUXO**](mft-message-notify-start-of-stream.md) do cliente.

Depois que o cliente esvaziar o MFT, o cliente poderá enviar mais dados de entrada. O primeiro exemplo após a operação de dreno deve ter o atributo de descontinuidade ([**atributo MFSampleExtension \_ Discontinuity).**](mfsampleextension-discontinuity-attribute.md)

> [!Note]  
> Versões anteriores desta documentação declaram que o parâmetro de evento *ulParam* é membro da enumeração [**\_ MFT \_ DRAIN \_ TYPE.**](/windows/win32/api/mftransform/ne-mftransform-_mft_drain_type) Incorreto. O *ulParam contém* um identificador de fluxo.

 

### <a name="implementation"></a>Implementação

Um MFT assíncrono sempre deve retornar [METransformDrainComplete](metransformdraincomplete.md) depois que ele tiver sido esvaziado.

Uma MFT síncrona pode ignorar essa mensagem e retornar S \_ OK se as seguintes condições são verdadeiras:

-   O MFT nunca armazena mais de uma amostra de entrada por vez.
-   Cada exemplo de entrada produz um único exemplo de saída.

Caso contrário, uma MFT síncrona deverá implementar essa mensagem.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                     |
| Cabeçalho<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**TIPO DE \_ MENSAGEM \_ MFT**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> <dt>

[MFTs assíncronos](asynchronous-mfts.md)
</dt> </dl>

 

 




