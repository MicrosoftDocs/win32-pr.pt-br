---
title: Para fornecer exemplos compactados com o Leitor Assíncrono
description: Para fornecer exemplos compactados com o Leitor Assíncrono
ms.assetid: 488baa3c-8863-4afc-89b2-fe55823e5db9
keywords:
- ASF (Advanced Systems Format), fornecendo amostras compactadas
- ASF (Formato de Sistemas Avançados), fornecendo exemplos compactados
- ASF (Advanced Systems Format), leitores assíncronos
- ASF (Formato de Sistemas Avançados), leitores assíncronos
- ASF (Advanced Systems Format), amostras compactadas
- ASF (Formato de Sistemas Avançados), amostras compactadas
- leitores assíncronos, fornecendo amostras compactadas
- leitores assíncronos, exemplos compactados
- amostras compactadas, entregando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd9199fb1deefdd3c7408bc9039639bd723b06c380c03d249c9c71a1d792c1e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118699926"
---
# <a name="to-deliver-compressed-samples-with-the-asynchronous-reader"></a>Para fornecer exemplos compactados com o Leitor Assíncrono

O leitor assíncrono pode fornecer amostras compactadas de fluxos em arquivos ASF. Os aplicativos geralmente entregam exemplos compactados ao copiar um fluxo de um arquivo para outro. Não é aconselhável recompactar dados que foram reconstruídos de um fluxo compactado, pois os dados são perdidos no processo de codificação. A mídia digital que foi compactada mais de uma vez terá uma diminuição perceptível na qualidade.

O Windows SDK de Formato de Mídia não fornece nenhum método para decodificar dados depois que eles são extraídos de um arquivo ASF. Se você receber amostras compactadas e, posteriormente, quiser descompactá-las, será preciso fornecer seu próprio código para fazer isso. Uma maneira de obter essa limitação é gravar as amostras compactadas em um novo arquivo ASF e, em seguida, lê-las em exemplos normais e descompactados.

Para receber exemplos compactados com o leitor assíncrono, execute as etapas a seguir.

1.  Implemente [**o retorno de chamada IWMReaderCallbackAdvanced::OnStreamSample.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-onstreamsample) Esse retorno de chamada é basicamente idêntico em função a [**IWMReaderCallback::OnSample,**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) exceto que ele fornece exemplos por número de fluxo e os exemplos ainda são compactados.
2.  Antes de iniciar a reprodução, obtenha um ponteiro para a interface [**IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced) do objeto de leitor chamando **IWMReader::QueryInterface**.
3.  Configure o leitor para fornecer amostras compactadas para o fluxo desejado chamando [**IWMReaderAdvanced::SetReceiveStreamSamples.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setreceivestreamsamples)
4.  Repita a etapa 3 para cada fluxo para o qual a entrega de amostra compactada é desejada.

> [!Note]  
> Os fluxos de imagem não são válidos para entrega de fluxo compactado. Se você copiar um fluxo de imagem de um arquivo para outro, ele não funcionará no novo arquivo. Para copiar um fluxo de imagem de arquivo para arquivo, recupere os exemplos de fluxo de imagem por número de saída e inclua-os no novo arquivo como se estivesse incluindo um novo fluxo de imagem.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IWMReaderCallbackAdvanced Interface**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallbackadvanced)
</dt> <dt>

[**Lendo arquivos com o Leitor Assíncrono**](reading-files-with-the-asynchronous-reader.md)
</dt> </dl>

 

 




