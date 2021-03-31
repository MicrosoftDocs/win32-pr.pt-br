---
description: .
ms.assetid: BE89E2E0-711F-4BD5-BB86-AA4CCA2D3E7F
title: Usando o gravador do coletor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e46157eae6fe851468515f9d9653adb33918ebb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921348"
---
# <a name="using-the-sink-writer"></a>Usando o gravador do coletor

## <a name="overview"></a>Visão geral

### <a name="file-container-types"></a>Tipos de contêiner de arquivo

O gravador do coletor tem suporte interno para vários tipos de contêineres de arquivos. Para obter uma lista completa, confira o [ \_ \_ contêiner de codificação MF](mf-transcode-containertype.md). Você pode dar suporte a tipos de contêineres adicionais escrevendo um [coletor de mídia](media-sinks.md)personalizado. O contêiner de arquivo é especificado quando você cria uma nova instância do gravador de coletor.

### <a name="stream-formats"></a>Formatos de fluxo

Para cada fluxo, o aplicativo deve especificar o seguinte.

-   O *formato de entrada* é o formato que o aplicativo envia para o gravador do coletor.
-   O *formato de saída* é o formato que será gravado no arquivo.

Os formatos de entrada e saída podem ser compactados ou descompactados. O gravador do coletor dá suporte às seguintes combinações:

-   Entrada não compactada com saída compactada. Esse é o caso típico e é usado para cenários de codificação ou transcodificação. Um codificador de Microsoft Media Foundation deve estar disponível para aceitar o tipo de entrada e codificar para o tipo de saída.
-   Entrada compactada com saída idêntica. Use essa combinação para remux um arquivo sem transcodificação.
-   Entrada não compactada com saída idêntica. Use essa combinação para gravar áudio ou vídeo não compactado em um contêiner de arquivo.

O gravador de coletor não dá suporte ao redimensionamento de vídeo, conversão de taxa de quadros ou reamostragem de áudio, a menos que essas funções sejam fornecidas pelo codificador. Caso contrário, o aplicativo pode usar [processadores de sinal digital](windowsmediadigitalsignalprocessors.md) para converter os dados de entrada, antes de enviar os dados para o

## <a name="creating-the-sink-writer"></a>Criando o gravador do coletor

Há duas funções que criam o gravador de coletor:

-   [**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl) Obtém a URL de um arquivo de saída ou um ponteiro para um fluxo de bytes. Essa função cria o coletor de mídia internamente.
-   [**MFCreateSinkWriterFromMediaSink**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink) usa um ponteiro para um coletor de mídia que já foi criado pelo aplicativo.

Se você estiver usando um dos coletores de mídia internos, a função [**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl) é preferível, pois o chamador não precisa configurar o coletor de mídia.

O método [**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl) fornece várias opções para especificar o tipo de contêiner de arquivo. No caso mais simples, a função usa a extensão de nome de arquivo na URL para selecionar o contêiner de arquivo. Para obter detalhes, consulte a página de referência da função.

Por exemplo, o código a seguir especifica o nome do arquivo "output. wmv" para a URL. Com base na extensão de nome de arquivo, o gravador de coletor carregará o [coletor de mídia ASF](asf-media-sinks.md) para criar um arquivo ASF (Advanced Systems Format).


```C++
    HRESULT hr = MFCreateSinkWriterFromURL(L"output.wmv", NULL, NULL, &pSinkWriter);
```



No caso do [**MFCreateSinkWriterFromMediaSink**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink), o tipo de arquivo é determinado pelo coletor de mídia.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gravador do coletor](sink-writer.md)
</dt> </dl>

 

 



