---
description: MFT_MESSAGE_COMMAND_DRAIN-solicita uma Media Foundation transformação (MFT) para liberar todos os dados armazenados.
ms.assetid: c48f3a88-a007-4f30-ac60-9e5a8c24e1ee
title: MFT_MESSAGE_COMMAND_DRAIN (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 907bfbd888b1eccbe7336c0d8f386d3266fd8e9b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108092744"
---
# <a name="mft_message_command_drain"></a>\_ \_ drenagem de comando de mensagem MFT \_

Solicita uma Media Foundation transformação (MFT) para liberar todos os dados armazenados.

## <a name="message-parameter"></a>Parâmetro de mensagem

Nenhum.

## <a name="remarks"></a>Comentários

Para enviar esta mensagem, chame [**IMFTransform::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).

Depois que essa mensagem é enviada, o fluxo de entrada especificado não aceita a entrada até que o MFT processe todos os dados das chamadas anteriores para [**IMFTransform::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput).

O processo de descarga varia ligeiramente entre MFTs síncronos e MFTs assíncronas:

**MFTs síncrono**

1.  Depois que o cliente envia essa mensagem, ele chama [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) em um loop, até que **ProcessOutput** retorne o código de erro **MF \_ E \_ Transform \_ precise de \_ mais \_ entradas**.
2.  Desde que o MFT ainda tenha dados a serem processados, outras chamadas para [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) falharão. O MFT continua a produzir saída até que use todos os dados armazenados. O MFT descarta todos os dados que não podem ser processados em um exemplo de saída completa. (Por exemplo, ele deve remover um quadro de vídeo parcial.)

**MFTs assíncrona**

1.  O MFT continua enviando eventos [METransformHaveOutput](metransformhaveoutput.md) até que não haja mais dados a serem processados. Ele não envia eventos [METransformNeedInput](metransformneedinput.md) durante esse tempo.
2.  Depois que o MFT envia o último evento [METransformHaveOutput](metransformhaveoutput.md) , ele envia um evento [METransformDrainComplete](metransformdraincomplete.md) .
3.  Após a conclusão do descarregamento, o MFT não enviará outro evento [METransformNeedInput](metransformneedinput.md) até receber uma [**mensagem \_ MFT \_ \_ início \_ da mensagem de \_ fluxo**](mft-message-notify-start-of-stream.md) do cliente.

Depois que o cliente drena o MFT, o cliente pode enviar mais dados de entrada. O primeiro exemplo após a operação de descarga deve ter o atributo de descontinuidade (atributo de descontinuidade [**MFSampleExtension \_**](mfsampleextension-discontinuity-attribute.md) ).

> [!Note]  
> As versões anteriores desta documentação afirmaram que o parâmetro de evento *ulParam* é um membro da enumeração de [**\_ \_ \_ tipo de drenagem de MFT**](/windows/win32/api/mftransform/ne-mftransform-_mft_drain_type) . Incorreto. O *ulParam* contém um identificador de fluxo.

 

### <a name="implementation"></a>Implementação

Uma MFT assíncrona sempre deve retornar [METransformDrainComplete](metransformdraincomplete.md) depois que ela for descarregada.

Um MFT síncrono pode ignorar essa mensagem e retornar S \_ OK se as seguintes condições forem verdadeiras:

-   O MFT nunca armazena mais de uma amostra de entrada por vez.
-   Cada amostra de entrada produz um único exemplo de saída.

Caso contrário, um MFT síncrono deve implementar essa mensagem.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                     |
| parâmetro<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**\_tipo de mensagem MFT \_**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> <dt>

[MFTs assíncrona](asynchronous-mfts.md)
</dt> </dl>

 

 




