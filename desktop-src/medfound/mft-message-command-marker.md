---
description: Marca um ponto no fluxo. Essa mensagem se aplica somente a MFTs assíncronas.
ms.assetid: eae1d066-64af-45e2-b8bb-eddf9147ad8b
title: MFT_MESSAGE_COMMAND_MARKER (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3802cb94c9183d4f392fbcedcf48c0c01071298e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105765023"
---
# <a name="mft_message_command_marker"></a>\_marcador de \_ comando de mensagem MFT \_

Marca um ponto no fluxo. Essa mensagem se aplica somente a [MFTs assíncronas](asynchronous-mfts.md).

## <a name="message-parameter"></a>Parâmetro de mensagem

Um valor arbitrário. O MFT retorna o valor para o cliente no evento [METransformMarker](metransformmarker.md) .

## <a name="remarks"></a>Comentários

Para enviar esta mensagem, chame [**IMFTransform::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).

O MFT responde a estas mensagens da seguinte maneira:

1.  O MFT gera tantas amostras de saída quanto possível dos dados de entrada existentes, enviando um evento [METransformHaveOutput](metransformhaveoutput.md) para cada exemplo de saída.
2.  Depois que toda a saída é gerada, o MFT envia um evento [METransformMarker](metransformmarker.md) . Esse evento deve ser enviado após todos os eventos [METransformHaveOutput](metransformhaveoutput.md) .

O cliente não é necessário para enviar essa mensagem e deve enviar essa mensagem somente para MFTs assíncronas. Um MFT síncrono não enviará um evento [METransformMarker](metransformmarker.md) em resposta a essa mensagem.

### <a name="implementation"></a>Implementação

O MFTs assíncrono deve responder a essa mensagem, conforme descrito. O MFTs síncrono deve ignorar esta mensagem.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                               |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_tipo de mensagem MFT \_**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




