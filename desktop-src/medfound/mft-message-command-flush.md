---
description: MFT_MESSAGE_COMMAND_FLUSH-solicita uma Media Foundation transformação (MFT) para liberar todos os dados armazenados.
ms.assetid: c799a962-da79-46df-a37f-4016c8c1701e
title: MFT_MESSAGE_COMMAND_FLUSH (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f34959303a2835e67202256341b0f5998b63d16b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108092734"
---
# <a name="mft_message_command_flush"></a>\_liberação de \_ comando de mensagem MFT \_

Solicita uma Media Foundation transformação (MFT) para liberar todos os dados armazenados.

## <a name="message-parameter"></a>Parâmetro de mensagem

Nenhum.

## <a name="remarks"></a>Comentários

Para enviar esta mensagem, chame [**IMFTransform::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).

Depois que essa mensagem é enviada, o MFT pode aceitar novos exemplos de entrada. Os tipos de mídia atuais não são invalidados.

### <a name="implementation"></a>Implementação

Todos os MFTs devem implementar essa mensagem. Quando ele recebe essa mensagem, o MFT deve descartar qualquer amostra de mídia que esteja segurando.

[MFTs assíncrona](asynchronous-mfts.md): o MFT não envia outro evento [METransformNeedInput](metransformneedinput.md) até receber uma [**mensagem de \_ MFT \_ notificar \_ início \_ da \_**](mft-message-notify-start-of-stream.md) mensagem de fluxo do cliente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                     |
| parâmetro<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**\_tipo de mensagem MFT \_**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




