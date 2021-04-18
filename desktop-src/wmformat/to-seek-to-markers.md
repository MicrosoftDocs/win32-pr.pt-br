---
title: Para buscar marcadores
description: Para buscar marcadores
ms.assetid: 2d5efebf-dcbd-4fb8-933e-cc6d3a99adf8
keywords:
- ASF (Advanced Systems Format), buscando marcadores
- ASF (formato de sistemas avançados), buscando marcadores
- ASF (Advanced Systems Format), leitores assíncronos
- ASF (formato de sistemas avançados), leitores assíncronos
- ASF (Advanced Systems Format), marcadores
- ASF (formato de sistemas avançados), marcadores
- leitores assíncronos, buscando marcadores
- leitores assíncronos, marcadores
- marcadores, buscando
- marcadores, leitores assíncronos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a16cb4fef99a5c735a12f03f8d2e962d6caf9c2a
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2020
ms.locfileid: "105807882"
---
# <a name="to-seek-to-markers"></a>Para buscar marcadores

Um marcador é um local nomeado em um arquivo ASF. Você só pode iniciar a reprodução do local de um marcador usando o leitor assíncrono. Você pode começar a reprodução em um marcador seguindo estas etapas.

1.  Chame **IWMReader:: QueryInterface** para obter um ponteiro para a interface [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) .
2.  Recupere o número total de marcadores no arquivo chamando [**IWMHeaderInfo:: GetMarkerCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getmarkercount).
3.  Faça um loop pelos marcadores, usando a contagem de marcadores recuperada na etapa 2. Recupere o nome e a hora de cada marcador chamando [**IWMHeaderInfo:: Getmarkr**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getmarker) para cada. Salve o índice do marcador desejado.
4.  Chame **IWMReader:: QueryInterface** para obter um ponteiro para a interface [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) .
5.  Especifique o marcador no qual iniciar a reprodução chamando [**IWMReaderAdvanced2:: StartAtMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-startatmarker). Você deve passar o índice do marcador desejado, que você salvou na etapa 3.
6.  Manipule os exemplos como faria normalmente em sua implementação do método [**IWMReaderCallback:: onsample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Marcadores**](markers.md)
</dt> <dt>

[**Lendo arquivos com o leitor assíncrono**](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[**Trabalhando com índices**](working-with-indexes.md)
</dt> </dl>

 

 




