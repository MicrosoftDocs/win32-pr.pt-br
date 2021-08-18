---
title: Para usar o Postview do Writer
description: Para usar o Postview do Writer
ms.assetid: 9da3c749-f6bd-43b5-9eff-3a637ddef048
keywords:
- ASF (Advanced Systems Format), postview de writer
- ASF (Formato de Sistemas Avançados), postview do autor
- ASF (Advanced Systems Format), postviewing
- ASF (Formato de Sistemas Avançados), postviewing
- postview do writer
- postviewing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7800f3ba50f9f1d61793a0d2ada2db0c03d6b88551ac1147e17872aa8e428c39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118196400"
---
# <a name="to-use-writer-postview"></a>Para usar o Postview do Writer

O objeto writer fornece recursos de pós-visualização para que você possa verificar o conteúdo gravado sem precisar configurar o objeto de leitor. O objeto writer não dá suporte à postviewing para conteúdo de áudio.

O postviewer do autor funciona da mesma maneira que o objeto de leitor assíncrono, apenas com menos recursos. Para obter informações detalhadas sobre como ler mídia digital, consulte [Lendo arquivos ASF](reading-asf-files.md).

Para implementar o postviewer, execute as etapas a seguir.

1.  Implemente [**o retorno de chamada IWMWriterPostViewCallback::OnPostViewSample.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostviewcallback-onpostviewsample) Esse método é essencialmente o mesmo que [**IWMReaderCallback::OnSample,**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) exceto que especifica números de fluxo em vez de saídas.
2.  Configurar para escrever como de costume.
3.  Obtenha um ponteiro para a interface [**IWMWriterPostView**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpostview) do objeto de autor chamando **IWMWriter::QueryInterface**.
4.  De definir o retorno de chamada para o postviewer a ser usado chamando [**IWMWriterPostView::SetPostViewCallback**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostview-setpostviewcallback).
5.  Para cada fluxo para o qual você deseja receber exemplos de postview, chame [**IWMWriterPostView::SetReceivePostViewSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostview-setreceivepostviewsamples). Você pode verificar se um fluxo está definido para receber exemplos de postview chamando [**IWMWriterPostView::GetReceivePostViewSamples.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostview-getreceivepostviewsamples)
6.  Você pode manipular os formatos de exemplo, assim como faria com os formatos de saída no objeto de leitor ou objeto de leitor síncrono.
7.  Ao começar a escrever o arquivo, você começará a receber exemplos em sua implementação do método de retorno de chamada **OnPostViewSample.**

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IWMWriterPostViewCallback Interface**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpostviewcallback)
</dt> <dt>

[**Escrevendo arquivos ASF**](writing-asf-files.md)
</dt> </dl>

 

 




