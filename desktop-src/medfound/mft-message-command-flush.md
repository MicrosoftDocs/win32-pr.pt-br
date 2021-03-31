---
description: Solicita uma Media Foundation transformação (MFT) para liberar todos os dados armazenados.
ms.assetid: c799a962-da79-46df-a37f-4016c8c1701e
title: MFT_MESSAGE_COMMAND_FLUSH (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd68f5e52cda9cca3470fb1dd903b5083a0cbc4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661494"
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



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_tipo de mensagem MFT \_**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




