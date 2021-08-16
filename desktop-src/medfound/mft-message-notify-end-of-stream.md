---
description: Notifica uma Media Foundation transformação (MFT) que um fluxo de entrada terminou.
ms.assetid: 2d6cdf45-1bb4-4915-bd27-efa041089100
title: MFT_MESSAGE_NOTIFY_END_OF_STREAM (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 951337fb91a26f1498b2aa82d42754fb2954ab649b4a021d37d42047be331ab4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117872156"
---
# <a name="mft_message_notify_end_of_stream"></a>\_ \_ \_ fim \_ da notificação de \_ mensagem MFT

Notifica uma Media Foundation transformação (MFT) que um fluxo de entrada terminou.

## <a name="message-parameter"></a>Parâmetro de mensagem

O parâmetro *ulParam* contém o identificador do fluxo de entrada, especificado como um valor **DWORD** . Em aplicativos de 64 bits, coloque esse valor no menor 32 bits do **ULONG \_ PTR**.

## <a name="remarks"></a>Comentários

Para enviar esta mensagem, chame [**IMFTransform::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).

O cliente não é necessário para enviar esta mensagem.

Depois que um fluxo termina, o cliente pode chamar [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) novamente para enviar novos dados para esse fluxo. Nesse caso, o cliente deve definir o atributo de descontinuidade (atributo de [**\_ descontinuidade MFSampleExtension**](mfsampleextension-discontinuity-attribute.md) ) no primeiro exemplo de entrada após o término do fluxo. (O cliente sempre deve definir esse atributo no primeiro exemplo novo após o término de um fluxo, independentemente de o cliente ter enviado a mensagem **\_ \_ \_ de fim \_ de notificação de fim de \_ transmissão da mensagem do MFT** . Para obter mais informações sobre como tratar descontinuidades, consulte [modelo básico de processamento de MFT](basic-mft-processing-model.md).)

Depois de enviar essa mensagem para cada fluxo de entrada, o cliente normalmente envia um comando de **\_ dreno de \_ comando \_ de mensagem MFT** e, em seguida, coleta a saída restante. No entanto, o cliente não precisa drenar o MFT. Se o cliente não drenar o MFT, o MFT normalmente descartará os dados não processados na próxima chamada para [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput), quando detectar a descontinuidade do fluxo. Como alternativa, o cliente pode liberar o MFT antes de chamar **ProcessInput**.

Essa mensagem não remove o fluxo de entrada ou redefine o tipo de mídia.

### <a name="implementation"></a>Implementação

Um MFT não é necessário para responder a esta mensagem.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                     |
| Cabeçalho<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_tipo de mensagem MFT \_**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




