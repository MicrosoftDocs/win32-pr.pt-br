---
title: Para usar a exibição do gravador
description: Para usar a exibição do gravador
ms.assetid: 9da3c749-f6bd-43b5-9eff-3a637ddef048
keywords:
- Formato de sistema avançado (ASF), modo de exibição de gravador
- ASF (formato de sistemas avançados), modo de exibição de gravador
- Formato de sistema avançado (ASF), visualização
- ASF (formato de sistemas avançados), visualização
- visualização do gravador
- visualização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abb3c1c83ebd38ff04c2022e529693d3d43b8b35
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2020
ms.locfileid: "104499004"
---
# <a name="to-use-writer-postview"></a>Para usar a exibição do gravador

O objeto Writer fornece recursos de visualização para que você possa verificar o conteúdo escrito sem precisar configurar o objeto leitor. O objeto gravador não oferece suporte à visualização de conteúdo de áudio.

O gravador de gravação funciona praticamente da mesma forma que o objeto leitor assíncrono, apenas com menos recursos. Para obter informações detalhadas sobre como ler mídia digital, consulte [lendo arquivos ASF](reading-asf-files.md).

Para implementar o revisor, execute as etapas a seguir.

1.  Implemente o retorno de chamada [**IWMWriterPostViewCallback:: OnPostViewSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostviewcallback-onpostviewsample) . Esse método é essencialmente o mesmo que [**IWMReaderCallback:: onsample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) , exceto que ele especifica números de fluxo em vez de saídas.
2.  Configure para escrever como de costume.
3.  Obtenha um ponteiro para a interface [**IWMWriterPostView**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpostview) do objeto gravador chamando **IWMWriter:: QueryInterface**.
4.  Defina o retorno de chamada para o revisor a ser usado chamando [**IWMWriterPostView:: SetPostViewCallback**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostview-setpostviewcallback).
5.  Para cada fluxo para o qual você deseja receber exemplos de exibição prévia, chame [**IWMWriterPostView:: SetReceivePostViewSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostview-setreceivepostviewsamples). Você pode verificar se um fluxo está definido para receber exemplos de exibição prévia chamando [**IWMWriterPostView:: GetReceivePostViewSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostview-getreceivepostviewsamples).
6.  Você pode manipular os formatos de exemplo, assim como faria com os formatos de saída no objeto leitor ou no objeto leitor síncrono.
7.  Ao começar a gravar o arquivo, você começará a receber exemplos em sua implementação do método de retorno de chamada **OnPostViewSample** .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Interface IWMWriterPostViewCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpostviewcallback)
</dt> <dt>

[**Gravando arquivos ASF**](writing-asf-files.md)
</dt> </dl>

 

 




