---
title: Atribuindo formatos de saída
description: Atribuindo formatos de saída
ms.assetid: 47697ffb-51cb-44cd-a0b0-7d85625a38f9
keywords:
- Windows SDK de Formato de Mídia, atribuindo formatos de saída
- ASF (Advanced Systems Format), atribuindo formatos de saída
- ASF (Formato de Sistemas Avançados), atribuindo formatos de saída
- FORMATO AVANÇADO de Sistemas (ASF), números de saída e formatos
- ASF (Formato de Sistemas Avançados), números de saída e formatos
- números de saída e formatos, atribuindo
- codecs, números de saída e formatos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80672419a032b2fff779259ffc6dcebfbe9e9a569f9d4b7afbb75ae5a84fac2c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119659366"
---
# <a name="assigning-output-formats"></a>Atribuindo formatos de saída

Alguns codecs podem descompactar dados de mídia digital em vários formatos descompactados. Você pode encontrar todos os formatos com suporte para uma saída específica usando o leitor assíncrono ou o leitor síncrono.

Para examinar todos os formatos disponíveis para uma saída, execute as etapas a seguir. Esses procedimentos são idênticos para o leitor assíncrono e o leitor síncrono. Quando os nomes de interface variam, os métodos de leitor síncronos são listados entre parênteses após os métodos do leitor assíncrono.

1.  Crie um objeto de leitor e carregue um arquivo para leitura. Para obter mais informações, [consulte Para criar](to-create-a-reader-and-open-a-file.md) um leitor e abrir um arquivo (ou Para criar um leitor [síncrono e abrir um arquivo](to-create-a-synchronous-reader-and-open-a-file.md)).
2.  Determine a saída para a qual você deseja encontrar os formatos disponíveis. Se você ainda não sabe qual saída deseja usar, poderá identificar as saídas no arquivo usando os procedimentos em Para [identificar números de saída.](to-identify-output-numbers.md)
3.  Recupere o número total de formatos disponíveis para a saída desejada chamando [**IWMReader::GetOutputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformatcount) (ou [**IWMSyncReader::GetOutputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputformatcount)).
4.  Loop pelos formatos disponíveis um de cada vez, executando as seguintes etapas para cada um:
    -   Recupere a interface [**IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) para o formato de saída atual chamando [**IWMReader::GetOutputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat) (ou [**IWMSyncReader::GetOutputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputformat)).
    -   Recupere a [**estrutura WM \_ MEDIA \_ TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) para o formato de saída fazendo duas chamadas para [**IWMMediaProps::GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype). Faça a primeira chamada para obter o tamanho da estrutura e, em seguida, aloce memória para ela e passe um ponteiro para a memória alocada na segunda chamada.
    -   Encontre o subtipo de mídia do formato de saída em **WM \_ MEDIA \_ TYPE.subtype**.
    -   Para o vídeo, se o subtipo atual for o formato que você deseja usar para a saída, saia do loop. Caso contrário, vá para a próxima iteração.

        Para áudio, você deve verificar os valores na estrutura **WAVEFORMATEX** em relação aos seus requisitos. **WM \_ MEDIA \_ TYPE.pbFormat** aponta para a estrutura **WAVEFORMATEX** para saídas de áudio.

5.  Quando você encontrar a saída desejada, depure-a para uso com o leitor chamando [**IWMReader::SetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-setoutputprops) (ou [**IWMSyncReader::SetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setoutputprops)). Você deve passar um ponteiro para a interface **IWMOutputMediaProps** obtida na primeira etapa do loop.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IWMMediaProps Interface**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)
</dt> <dt>

[**IWMOutputMediaProps Interface**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops)
</dt> <dt>

[**IWMReader Interface**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[**IWMSyncReader Interface**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[**Trabalhando com saídas**](working-with-outputs.md)
</dt> </dl>

 

 




