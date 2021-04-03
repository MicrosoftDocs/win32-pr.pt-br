---
title: Para implementar mensagens de leitor no retorno de chamada OnStatus
description: Para implementar mensagens de leitor no retorno de chamada OnStatus
ms.assetid: f0535e02-a283-48bf-9242-ebcc17a6fb66
keywords:
- ASF (Advanced Systems Format), implementando mensagens de leitor
- ASF (formato de sistemas avançados), implementando mensagens de leitor
- ASF (Advanced Systems Format), retorno de chamada OnStatus
- ASF (formato de sistemas avançados), retorno de chamada OnStatus
- ASF (Advanced Systems Format), leitores assíncronos
- ASF (formato de sistemas avançados), leitores assíncronos
- leitores assíncronos, implementando mensagens de leitor
- Método de retorno de chamada OnStatus, implementando mensagens de leitor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 384cf8df8628efa9bd2cc17920dc6b1303655691
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104007100"
---
# <a name="to-implement-reader-messages-in-the-onstatus-callback"></a>Para implementar mensagens de leitor no retorno de chamada OnStatus

Para usar o leitor assíncrono para fornecer conteúdo de um arquivo ASF, você deve implementar um mínimo de dois métodos de retorno de chamada, [**IWMStatusCallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) e [**IWMReaderCallback:: onsample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample). Esta seção descreve como implementar **IWMStatusCallback:: OnStatus** para receber e responder a mensagens de status enviadas pelo leitor. **OnStatus** é usado por outros objetos no SDK do Windows Media Format. Para obter informações gerais sobre **OnStatus**, consulte [usando o retorno de chamada OnStatus](using-the-onstatus-callback.md).

Ao usar o leitor assíncrono, você deve interceptar as seguintes mensagens em **IWMStatusCallback:: OnStatus**.



| Mensagem de status | Descrição                                     |
|----------------|-------------------------------------------------|
| WMT \_ aberto    | Enviado quando as operações de abertura de arquivo são concluídas. |
| WMT \_ fechado    | Enviado quando as operações de fechamento de arquivo são concluídas. |



 

Você deve usar as mensagens de status listadas acima para controlar a execução do seu aplicativo de leitura. Por exemplo, você deve aguardar até receber a mensagem **\_ aberta WMT** para iniciar o leitor ou chamar outros métodos que exigem que o leitor tenha um arquivo pronto. Frequentemente, os aplicativos criados com o leitor assíncrono usam um evento para sinalizar a conclusão de chamadas assíncronas e prosseguir com o processamento. Para obter mais informações sobre como usar eventos para sinalizar a conclusão de operações, consulte [usando eventos com chamadas assíncronas](using-events-with-asynchronous-calls.md).

Muitas outras mensagens são enviadas ao **OnStatus** pelo objeto leitor para permitir que o aplicativo responda ao status das operações de leitura. Os valores de mensagem de status possíveis são definidos no tipo de enumeração [**\_ status WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IWMStatusCallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus)
</dt> <dt>

[**Lendo arquivos com o leitor assíncrono**](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[**Usando o retorno de chamada OnStatus**](using-the-onstatus-callback.md)
</dt> </dl>

 

 




