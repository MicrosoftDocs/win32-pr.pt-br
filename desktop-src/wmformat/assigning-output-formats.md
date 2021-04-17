---
title: Atribuindo formatos de saída
description: Atribuindo formatos de saída
ms.assetid: 47697ffb-51cb-44cd-a0b0-7d85625a38f9
keywords:
- Windows Media Format SDK, atribuindo formatos de saída
- ASF (Advanced Systems Format), atribuindo formatos de saída
- ASF (formato de sistemas avançados), atribuindo formatos de saída
- ASF (Advanced Systems Format), formatos e números de saída
- ASF (formato de sistemas avançados), números e formatos de saída
- números e formatos de saída, atribuindo
- codecs, números e formatos de saída
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 633673053a2b34a2f7aed5ed3f6ae66457a7ee13
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/21/2020
ms.locfileid: "105755454"
---
# <a name="assigning-output-formats"></a>Atribuindo formatos de saída

Alguns codecs podem descompactar dados de mídia digital em vários formatos descompactados. Você pode encontrar todos os formatos com suporte para uma saída específica usando o leitor assíncrono ou o leitor síncrono.

Para examinar todos os formatos disponíveis para uma saída, execute as etapas a seguir. Esses procedimentos são idênticos tanto para o leitor assíncrono quanto para o leitor síncrono. Quando os nomes de interface variam, os métodos de leitor síncronos são listados entre parênteses após os métodos do leitor assíncrono.

1.  Crie um objeto leitor e carregue um arquivo para leitura. Para obter mais informações, consulte [para criar um leitor e abrir um arquivo](to-create-a-reader-and-open-a-file.md) (ou [criar um leitor síncrono e abrir um arquivo](to-create-a-synchronous-reader-and-open-a-file.md)).
2.  Determine a saída para a qual você deseja encontrar os formatos disponíveis. Se você ainda não souber qual saída deseja usar, poderá identificar as saídas no arquivo usando os procedimentos em [para identificar os números de saída](to-identify-output-numbers.md).
3.  Recupere o número total de formatos disponíveis para a saída desejada chamando [**IWMReader:: GetOutputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformatcount) (ou [**IWMSyncReader:: GetOutputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputformatcount)).
4.  Faça um loop pelos formatos disponíveis, um de cada vez, executando as seguintes etapas para cada um:
    -   Recupere a interface [**IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) para o formato de saída atual chamando [**IWMReader:: GetOutputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat) (ou [**IWMSyncReader:: GetOutputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputformat)).
    -   Recupere a estrutura do [**\_ \_ tipo de mídia do WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) para o formato de saída fazendo duas chamadas para [**IWMMediaProps:: GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype). Faça a primeira chamada para obter o tamanho da estrutura e, em seguida, aloque memória para ela e passe um ponteiro para a memória alocada na segunda chamada.
    -   Localize o subtipo de mídia do formato de saída no **arquivo de mídia do WM \_ \_ tipo. subtipo**.
    -   Para vídeo, se o subtipo atual for o formato que você deseja usar para a saída, interrompa o loop. Caso contrário, vá para a próxima iteração.

        Para áudio, você deve verificar os valores na estrutura **WAVEFORMATEX** em seus requisitos. **WM \_ MEDIA \_ Type. pbFormat** aponta para a estrutura **WAVEFORMATEX** para saídas de áudio.

5.  Quando você encontrar a saída desejada, defina-a para uso com o leitor chamando [**IWMReader:: SetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-setoutputprops) (ou [**IWMSyncReader:: SetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setoutputprops)). Você deve passar um ponteiro para a interface **IWMOutputMediaProps** obtida na primeira etapa do loop.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Interface IWMMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)
</dt> <dt>

[**Interface IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops)
</dt> <dt>

[**Interface IWMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[**Interface IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[**Trabalhando com saídas**](working-with-outputs.md)
</dt> </dl>

 

 




