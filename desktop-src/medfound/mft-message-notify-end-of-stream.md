---
description: Notifica uma Media Foundation (MFT) de que um fluxo de entrada foi encerrado.
ms.assetid: 2d6cdf45-1bb4-4915-bd27-efa041089100
title: MFT_MESSAGE_NOTIFY_END_OF_STREAM (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 951337fb91a26f1498b2aa82d42754fb2954ab649b4a021d37d42047be331ab4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117872156"
---
# <a name="mft_message_notify_end_of_stream"></a>FIM DO FLUXO \_ \_ DE \_ NOTIFICAÇÃO DE MENSAGEM \_ MFT \_

Notifica uma Media Foundation (MFT) de que um fluxo de entrada foi encerrado.

## <a name="message-parameter"></a>Parâmetro message

O *parâmetro ulParam* contém o identificador do fluxo de entrada, especificado como um **valor DWORD.** Em aplicativos de 64 bits, coloque esse valor nos 32 bits inferiores do **\_ PTR ULONG.**

## <a name="remarks"></a>Comentários

Para enviar essa mensagem, chame [**IMFTransform::P rocessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).

O cliente não é necessário para enviar essa mensagem.

Depois que um fluxo termina, o cliente pode chamar [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) novamente para enviar novos dados para esse fluxo. Nesse caso, o cliente deve definir o atributo de descontinuidade ( atributo [**MFSampleExtension \_ Discontinuity)**](mfsampleextension-discontinuity-attribute.md) no primeiro exemplo de entrada após o fim do fluxo. (O cliente sempre deve definir esse atributo no primeiro novo exemplo após o término de um fluxo, independentemente de o cliente ter enviado a mensagem NOTIFICAÇÃO DE MENSAGEM MFT DO FIM **\_ \_ \_ \_ DO \_** FLUXO. Para obter mais informações sobre como lidar com descontinuidades, consulte [Modelo básico de processamento MFT](basic-mft-processing-model.md).)

Depois de enviar essa mensagem para cada fluxo de entrada, o cliente normalmente envia um comando **MFT \_ MESSAGE COMMAND \_ \_ DRAIN** e, em seguida, coleta a saída restante. No entanto, o cliente não é necessário para esvaziar o MFT. Se o cliente não esvaziar o MFT, o MFT normalmente descartará todos os dados não processados na próxima chamada para [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput)quando detectar a descontinuidade do fluxo. Como alternativa, o cliente pode liberar o MFT antes de **chamar ProcessInput.**

Essa mensagem não remove o fluxo de entrada nem redefine o tipo de mídia.

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

 

 




