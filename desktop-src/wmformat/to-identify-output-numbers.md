---
title: Para identificar números de saída
description: Para identificar números de saída
ms.assetid: a2135a71-52e6-4f62-8be8-b9886be9b37c
keywords:
- Windows SDK de Formato de Mídia, identificando números de saída
- ASF (Advanced Systems Format), identificando números de saída
- ASF (Formato de Sistemas Avançados), identificando números de saída
- FORMATO AVANÇADO de Sistemas (ASF), números de saída e formatos
- ASF (Formato de Sistemas Avançados), números de saída e formatos
- números de saída e formatos, identificando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c601481520632806ac56e12e16e1474336897d1be341c9d19df8e235d6355ab1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118699376"
---
# <a name="to-identify-output-numbers"></a>Para identificar números de saída

Para identificar os números de saída de um arquivo carregado, execute as etapas a seguir. Esses procedimentos são idênticos para o leitor assíncrono e o leitor síncrono. Quando os nomes de interface variam, os métodos de leitor síncronos são listados entre parênteses após os métodos do leitor assíncrono.

1.  Crie um objeto de leitor e carregue um arquivo para leitura. Para obter mais informações, [consulte Para criar](to-create-a-reader-and-open-a-file.md) um leitor e abrir um arquivo (ou Para criar um leitor [síncrono e abrir um arquivo](to-create-a-synchronous-reader-and-open-a-file.md)).
2.  Recupere o número total de saídas para o arquivo chamando [**IWMReader::GetOutputCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputcount) (ou [**IWMSyncReader::GetOutputCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputcount)).
3.  Executar um loop pelas saídas uma de cada vez, executando as seguintes etapas para cada uma:
    -   Recupere a interface [**IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) para a saída atual com uma chamada para [**IWMReader::GetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputprops) (ou [**IWMSyncReader::GetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputprops)).
    -   Recupere a [**estrutura WM \_ MEDIA \_ TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) para a saída fazendo duas chamadas para [**IWMMediaProps::GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype). Faça a primeira chamada para obter o tamanho da estrutura e, em seguida, aloce memória para ela e passe um ponteiro para a memória alocada na segunda chamada. Como alternativa, você pode chamar [**IWMMediaProps::GetType,**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-gettype)que fornece o tipo principal sem exigir que você aloce memória para a estrutura **WM MEDIA \_ \_ TYPE.** Você pode ignorar saídas do tipo principal errado.
    -   Recupere o tipo de mídia principal e o subtipo de mídia da estrutura **WM \_ MEDIA \_ TYPE.** Esses valores são armazenados em membros de **dados majortype** e **subtipo,** respectivamente.
    -   Verifique o valor de **WM \_ MEDIA \_ TYPE.formattype**. Isso especifica o tipo de estrutura contida no buffer em **WM \_ MEDIA \_ TYPE.pbFormat.** Para obter mais informações sobre tipos de formato, consulte [Tipos de mídia](media-types.md).
    -   Alocar memória para manter a estrutura do tipo identificado na etapa anterior. Copie a estrutura para a memória alocada. Para áudio e vídeo, essa estrutura fornece informações essenciais sobre como os dados devem ser renderizados.

O leitor síncrono também fornece métodos para recuperar associações entre números de saída e números de fluxo. Para obter mais informações, consulte [Para encontrar números de fluxo e números de saída](to-find-stream-numbers-and-output-numbers.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Entradas, Fluxos e saídas**](inputs-streams-and-outputs.md)
</dt> <dt>

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

 

 




