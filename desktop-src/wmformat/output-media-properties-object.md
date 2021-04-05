---
title: Objeto de propriedades de mídia de saída
description: Objeto de propriedades de mídia de saída
ms.assetid: 96fa7c66-59a0-4eb3-ace4-a827b139f978
keywords:
- SDK do Windows Media Format, objetos de propriedades de mídia de saída
- ASF (Advanced Systems Format), objetos de propriedades de mídia de saída
- ASF (formato de sistemas avançados), objetos de propriedades de mídia de saída
- objetos, objetos de propriedades de mídia de saída
- objetos de propriedades de mídia de saída
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61490464381a0b4e58be7994dfaeb0dfec2baa76
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2020
ms.locfileid: "104007244"
---
# <a name="output-media-properties-object"></a>Objeto de propriedades de mídia de saída

Um objeto de propriedades de mídia de saída é usado para recuperar e definir uma propriedade de saída. Os objetos de propriedades de mídia de saída são criados para formatos de saída com suporte de fluxos em um arquivo que é carregado em um objeto leitor. Para fluxos compactados, as propriedades de saída são determinadas pelas saídas possíveis do codec de descompactação.

Um objeto de propriedades de mídia de saída é criado por [**IWMReader:: GetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputprops) esse método cria um objeto de propriedades de mídia de saída que contém as propriedades do formato de saída padrão. Outros formatos podem ter suporte para uma saída. Para obter formatos de saída adicionais, você pode chamar [**IWMReader:: GetOutputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformatcount) para obter o número de formatos de saída com suporte e, em seguida, fazer um loop através deles usando chamadas para [**IWMReader:: GetOutputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat). **GetOutputFormat** cria um objeto de propriedades de mídia de saída populado com os dados para o formato de saída selecionado.

Os objetos de propriedades de mídia de saída também podem ser criados com o leitor síncrono. Todos os nomes de método são idênticos aos do leitor e são todos expostos pela interface [**IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader) .

**GetOutputProps** e **GetOutputFormat** definem um ponteiro para uma interface [**IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) . As outras interfaces do objeto de propriedades de mídia de saída podem ser obtidas chamando o método **QueryInterface** .

As interfaces a seguir têm suporte em cada objeto de propriedades de mídia de saída.



| Interface                                          | Descrição                                                                                                |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**IWMMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)             | Usado como interface base para as outras interfaces de propriedade de mídia (entrada, saída e vídeo).             |
| [**IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) | Recupera as propriedades de uma saída.                                                                     |
| [**IWMVideoMediaProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nn-wmsdkidl-iwmvideomediaprops)   | Gerencia as propriedades de um fluxo de vídeo. Essa é uma interface opcional, disponível apenas para fluxos de vídeo. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Objetos**](objects.md)
</dt> <dt>

[**Objeto de leitor**](reader-object.md)
</dt> </dl>

 

 




