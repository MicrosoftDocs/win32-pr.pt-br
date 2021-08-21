---
title: Objeto Propriedades da Mídia de Saída
description: Objeto Propriedades da Mídia de Saída
ms.assetid: 96fa7c66-59a0-4eb3-ace4-a827b139f978
keywords:
- Windows SDK de Formato de Mídia, objetos de propriedades de mídia de saída
- FORMATO DE SISTEMAS Avançados (ASF), objetos de propriedades de mídia de saída
- ASF (Formato de Sistemas Avançados), objetos de propriedades de mídia de saída
- objetos, objetos de propriedades de mídia de saída
- objetos de propriedades de mídia de saída
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6848270147a1a191faf93830f062cf7768a19ccd38a77598d15617197a1967a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119084624"
---
# <a name="output-media-properties-object"></a>Objeto Propriedades da Mídia de Saída

Um objeto de propriedades de mídia de saída é usado para recuperar e definir uma propriedade de saída. Os objetos de propriedades de mídia de saída são criados para formatos de saída com suporte de fluxos em um arquivo carregado em um objeto de leitor. Para fluxos compactados, as propriedades de saída são determinadas pelas possíveis saídas do codec descompactando.

Um objeto de propriedades de mídia de saída é criado por [**IWMReader::GetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputprops) Esse método cria um objeto de propriedades de mídia de saída que contém as propriedades do formato de saída padrão. Outros formatos podem ter suporte para uma saída. Para obter formatos de saída adicionais, você pode chamar [**IWMReader::GetOutputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformatcount) para obter o número de formatos de saída com suporte e, em seguida, fazer um loop usando chamadas para [**IWMReader::GetOutputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat). **GetOutputFormat cria** um objeto de propriedades de mídia de saída populado com os dados para o formato de saída selecionado.

Os objetos de propriedades de mídia de saída também podem ser criados com o leitor síncrono. Todos os nomes de método são idênticos aos do leitor e todos eles são expostos pela interface [**IWMSyncReader.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)

**GetOutputProps** e **GetOutputFormat configuram** um ponteiro para uma interface [**IWMOutputMediaProps.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) As outras interfaces do objeto de propriedades de mídia de saída podem ser obtidas chamando **o método QueryInterface.**

As interfaces a seguir têm suporte em cada objeto de propriedades de mídia de saída.



| Interface                                          | Descrição                                                                                                |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**IWMMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)             | Usado como a interface base para outras interfaces de propriedade de mídia (entrada, saída e vídeo).             |
| [**IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) | Recupera as propriedades de uma saída.                                                                     |
| [**IWMVideoMediaProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nn-wmsdkidl-iwmvideomediaprops)   | Gerencia as propriedades de um fluxo de vídeo. Essa é uma interface opcional, disponível somente para fluxos de vídeo. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Objetos**](objects.md)
</dt> <dt>

[**Objeto de leitor**](reader-object.md)
</dt> </dl>

 

 




