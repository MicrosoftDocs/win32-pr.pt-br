---
description: Marca um ponto no fluxo. Essa mensagem se aplica somente a MFTs assíncronos.
ms.assetid: eae1d066-64af-45e2-b8bb-eddf9147ad8b
title: MFT_MESSAGE_COMMAND_MARKER (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc55a96ae9680b37d83ec776c66848ed04f4a30b62d1d0378035c88823d2c19d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117872166"
---
# <a name="mft_message_command_marker"></a>MARCADOR DE COMANDO \_ \_ DE MENSAGEM \_ MFT

Marca um ponto no fluxo. Essa mensagem se aplica somente a [MFTs assíncronos.](asynchronous-mfts.md)

## <a name="message-parameter"></a>Parâmetro message

Um valor arbitrário. O MFT retorna o valor para o cliente no [evento METransformMarker.](metransformmarker.md)

## <a name="remarks"></a>Comentários

Para enviar essa mensagem, chame [**IMFTransform::P rocessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).

A MFT responde a esta mensagem da seguinte forma:

1.  O MFT gera o máximo de amostras de saída possível dos dados de entrada existentes, enviando um [evento METransformHaveOutput](metransformhaveoutput.md) para cada exemplo de saída.
2.  Depois que toda a saída é gerada, o MFT envia um [evento METransformMarker.](metransformmarker.md) Esse evento deve ser enviado após todos os eventos [METransformHaveOutput.](metransformhaveoutput.md)

O cliente não é necessário para enviar essa mensagem e deve enviar essa mensagem somente para MFTs assíncronos. Um MFT síncrono não enviará um [evento METransformMarker](metransformmarker.md) em resposta a essa mensagem.

### <a name="implementation"></a>Implementação

Os MFTs assíncronos devem responder a essa mensagem, conforme descrito. Os MFTs síncronos devem ignorar essa mensagem.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do Server 2008 R2 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**TIPO DE \_ MENSAGEM \_ MFT**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




