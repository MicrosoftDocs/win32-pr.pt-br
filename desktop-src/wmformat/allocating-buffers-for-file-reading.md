---
title: Alocando buffers para leitura de arquivo
description: Alocando buffers para leitura de arquivo
ms.assetid: da66ef5b-ec92-445c-90ba-5ee89e0def36
keywords:
- SDK do Windows Media Format, lendo arquivos ASF
- ASF (Advanced Systems Format), lendo arquivos
- ASF (formato de sistemas avançados), lendo arquivos
- SDK do Windows Media Format, alocando buffers
- ASF (Advanced Systems Format), alocando buffers
- ASF (formato de sistemas avançados), alocando buffers
- ASF (Advanced Systems Format), alocação de buffer
- ASF (formato de sistemas avançados), alocação de buffer
- alocação de buffer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecdf9ba0a333bbe25c94ec087911237b68f38f74
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104365525"
---
# <a name="allocating-buffers-for-file-reading"></a>Alocando buffers para leitura de arquivo

No cenário de leitura de arquivos mais básico, os buffers usados para fornecer exemplos são alocados pelo objeto de leitura (o objeto leitor ou o objeto leitor síncrono). No entanto, você pode alocar buffers por conta própria. Para obter mais informações sobre os benefícios de alocar seus próprios buffers, consulte [suporte de exemplo alocado pelo usuário](user-allocated-sample-support.md).

Para usar seus próprios buffers para leitura de arquivos, execute as etapas a seguir.

1.  Implemente um retorno de chamada ou retornos de chamada para o leitor chamar quando ele precisar de um buffer. Se você estiver lendo exemplos de saída, use [**IWMReaderAllocatorEx:: AllocateForOutputEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforoutputex). Se você estiver lendo exemplos de fluxo, use [**IWMReaderAllocatorEx:: AllocateForStreamEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforstreamex). Inclua qualquer lógica para o gerenciamento de buffers que atendam ao seu aplicativo.
2.  Aloque um pool de buffers que será usado para a leitura de arquivos.
    -   Localize o tamanho necessário para seus buffers chamando [**IWMReaderAdvanced:: GetMaxOutputSampleSize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getmaxoutputsamplesize) ou [**IWMReaderAdvanced:: GetMaxStreamSampleSize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getmaxstreamsamplesize) para cada saída e/ou fluxo para o qual o buffer é usado. Se estiver usando o leitor síncrono, use [**IWMSyncReader:: GetMaxOutputSampleSize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getmaxoutputsamplesize) ou [**IWMSyncReader:: GetMaxStreamSampleSize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getmaxstreamsamplesize) em vez disso.
    -   Crie cada buffer para o pool.
3.  Configure o leitor ou leitor síncrono para leitura. Para obter mais informações, consulte [lendo arquivos com o leitor assíncrono](reading-files-with-the-asynchronous-reader.md) ou [lendo arquivos com o leitor síncrono](reading-files-with-the-synchronous-reader.md).
4.  Antes de começar a gravar, chame [**IWMReaderAdvanced:: SetAllocateForOutput**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setallocateforoutput) ou [**IWMReaderAdvanced:: SetAllocateForStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setallocateforstream) para cada saída e fluxo para o qual você está alocando buffers usando o objeto leitor. Para o leitor síncrono, chame [**IWMSyncReader2:: SetAllocateForOutput**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader2-setallocateforoutput) ou [**IWMSyncReader2:: SetAllocateForStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader2-setallocateforstream) em vez disso.
5.  Comece a ler o arquivo.

O objeto de leitura fará chamadas para o retorno de chamada de alocador apropriado e obterá exemplos de seu aplicativo. A lógica de gerenciamento de buffer deve incluir uma maneira de sinalizar que um buffer está livre para ser usado novamente. Normalmente, um buffer é colocado de volta no pool quando seu conteúdo é renderizado. Dependendo do seu aplicativo, talvez você precise de apenas alguns buffers no pool ou muitos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Lendo arquivos ASF**](reading-asf-files.md)
</dt> </dl>

 

 




