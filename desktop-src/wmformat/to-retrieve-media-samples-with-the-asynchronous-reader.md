---
title: Para recuperar amostras de mídia com o leitor assíncrono
description: Para recuperar amostras de mídia com o leitor assíncrono
ms.assetid: 0d8c3099-f068-4074-b717-2f5b9ed9eeb8
keywords:
- ASF (Advanced Systems Format), recuperando amostras de mídia
- ASF (formato de sistemas avançados), recuperando amostras de mídia
- ASF (Advanced Systems Format), leitores assíncronos
- ASF (formato de sistemas avançados), leitores assíncronos
- leitores assíncronos, recuperando amostras de mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 896fa4a023dc0cbcce3db6e0b0fc5101347f12fd65a4294a608823e511a55e77
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118699117"
---
# <a name="to-retrieve-media-samples-with-the-asynchronous-reader"></a>Para recuperar amostras de mídia com o leitor assíncrono

Depois de receber a mensagem de \_ status aberta do WMT em sua implementação de [**IWMStatusCallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus), você pode começar a receber exemplos chamando [**IWMReader:: Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start). O leitor assíncrono fornece amostras para sua implementação de [**IWMReaderCallback:: onsample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample). Os exemplos são entregues em ordem de tempo de apresentação.

**Start** é uma chamada assíncrona. Ele será retornado quase imediatamente e continuará a ser executado em threads separados. O leitor assíncrono usa vários threads ao decodificar conteúdo e fornecer exemplos. Quando o final do arquivo é atingido, o leitor envia uma mensagem de \_ status de EOF WMT para sua implementação do retorno de chamada **OnStatus** . Quando WMT \_ EOF é enviado, o leitor interrompe seu próprio processamento; você não precisa responder a WMT \_ EOF com uma chamada para [**IWMReader:: Stop**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-stop).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Interface IWMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[**Para implementar mensagens de leitor no retorno de chamada OnStatus**](to-implement-reader-messages-in-the-onstatus-callback.md)
</dt> <dt>

[**Para implementar o retorno de chamada onsample**](to-implement-the-onsample-callback.md)
</dt> </dl>

 

 




