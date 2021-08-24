---
title: Para buscar marcadores
description: Para buscar marcadores
ms.assetid: 2d5efebf-dcbd-4fb8-933e-cc6d3a99adf8
keywords:
- ASF (Advanced Systems Format), buscando marcadores
- ASF (Formato de Sistemas Avançados), buscando marcadores
- ASF (Advanced Systems Format), leitores assíncronos
- ASF (Formato de Sistemas Avançados), leitores assíncronos
- ASF (Advanced Systems Format), marcadores
- ASF (Formato de Sistemas Avançados), marcadores
- leitores assíncronos, buscando marcadores
- leitores assíncronos, marcadores
- marcadores, buscando
- marcadores, leitores assíncronos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3361546f4087e0c2104809435d9d75e8711560ec4f3c55855d14b05ef4dfb8dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807346"
---
# <a name="to-seek-to-markers"></a>Para buscar marcadores

Um marcador é um local nomeado em um arquivo ASF. Você só pode iniciar a reprodução no local de um marcador usando o leitor assíncrono. Você pode começar a reprodução em um marcador seguindo estas etapas.

1.  Chame **IWMReader::QueryInterface para** obter um ponteiro para a interface [**IWMHeaderInfo.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)
2.  Recupere o número total de marcadores no arquivo chamando [**IWMHeaderInfo::GetMarkerCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getmarkercount).
3.  Loop pelos marcadores, usando a contagem de marcadores recuperada na etapa 2. Recupere o nome e a hora de cada marcador chamando [**IWMHeaderInfo::GetMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getmarker) para cada um. Salve o índice do marcador desejado.
4.  Chame **IWMReader::QueryInterface** para obter um ponteiro para a interface [**IWMReaderAdvanced2.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)
5.  Especifique o marcador no qual iniciar a reprodução chamando [**IWMReaderAdvanced2::StartAtMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-startatmarker). Você deve passar o índice do marcador desejado, que você salvou na etapa 3.
6.  Manipular os exemplos como faria normalmente em sua implementação do [**método IWMReaderCallback::OnSample.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Marcadores**](markers.md)
</dt> <dt>

[**Lendo arquivos com o Leitor Assíncrono**](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[**Trabalhando com índices**](working-with-indexes.md)
</dt> </dl>

 

 




