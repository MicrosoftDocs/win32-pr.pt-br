---
title: Para fornecer amostras compactadas com o leitor assíncrono
description: Para fornecer amostras compactadas com o leitor assíncrono
ms.assetid: 488baa3c-8863-4afc-89b2-fe55823e5db9
keywords:
- ASF (Advanced Systems Format), fornecendo amostras compactadas
- ASF (formato de sistemas avançados), fornecendo amostras compactadas
- ASF (Advanced Systems Format), leitores assíncronos
- ASF (formato de sistemas avançados), leitores assíncronos
- ASF (Advanced Systems Format), amostras compactadas
- ASF (formato de sistemas avançados), amostras compactadas
- leitores assíncronos, fornecendo amostras compactadas
- leitores assíncronos, amostras compactadas
- amostras compactadas, entregando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4ce835075f5bd760014a3b1b776ba3627adb076
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103640155"
---
# <a name="to-deliver-compressed-samples-with-the-asynchronous-reader"></a>Para fornecer amostras compactadas com o leitor assíncrono

O leitor assíncrono pode fornecer amostras compactadas de fluxos em arquivos ASF. Normalmente, os aplicativos fornecem amostras compactadas ao copiar um fluxo de um arquivo para outro. Não é aconselhável recompactar os dados que foram reconstruídos a partir de um fluxo compactado, pois os dados são perdidos no processo de codificação. A mídia digital que foi compactada mais de uma vez terá uma diminuição perceptível na qualidade.

O Windows Media Format SDK não fornece nenhum método para decodificar dados depois que ele foi extraído de um arquivo ASF. Se você receber amostras compactadas e, posteriormente, quiser descompactá-las, precisará fornecer seu próprio código para fazer isso. Uma maneira de contornar essa limitação é escrever os exemplos compactados em um novo arquivo ASF e, em seguida, lê-los novamente em amostras normais e descompactadas.

Para receber amostras compactadas com o leitor assíncrono, execute as etapas a seguir.

1.  Implemente o retorno de chamada [**IWMReaderCallbackAdvanced:: OnStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-onstreamsample) . Esse retorno de chamada é basicamente idêntico na função para [**IWMReaderCallback:: onsample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) , exceto pelo fato de que ele fornece exemplos por número de fluxo e os exemplos ainda são compactados.
2.  Antes de iniciar a reprodução, obtenha um ponteiro para a interface [**IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced) do objeto leitor chamando **IWMReader:: QueryInterface**.
3.  Configure o leitor para fornecer amostras compactadas para o fluxo desejado chamando [**IWMReaderAdvanced:: SetReceiveStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setreceivestreamsamples).
4.  Repita a etapa 3 para cada fluxo para o qual a entrega de amostra compactada é desejada.

> [!Note]  
> Fluxos de imagem não são válidos para entrega de fluxo compactado. Se você copiar um fluxo de imagem de um arquivo para outro, ele não funcionará no novo arquivo. Para copiar um fluxo de imagem do arquivo para o arquivo, recupere os exemplos de fluxo de imagem por número de saída e inclua-os no novo arquivo como se incluir um novo fluxo de imagem.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Interface IWMReaderCallbackAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallbackadvanced)
</dt> <dt>

[**Lendo arquivos com o leitor assíncrono**](reading-files-with-the-asynchronous-reader.md)
</dt> </dl>

 

 




