---
description: O leitor de origem é uma alternativa ao uso da sessão de mídia e do Microsoft Media Foundation pipeline para processar dados de mídia.
ms.assetid: 8a17a754-53ef-4c05-9189-7978d864b17a
title: Leitor de origem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81527392c97aae039de8b8cdbd76b1251e03842b6b66c22cc224118d4f428620
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119101805"
---
# <a name="source-reader"></a>Leitor de origem

O leitor de origem é uma alternativa ao uso da [sessão de mídia](media-session.md) e do Microsoft Media Foundation pipeline para processar dados de mídia.

## <a name="why-use-the-source-reader"></a>Por que usar o leitor de origem?

Media Foundation fornece um pipeline otimizado para reprodução. O pipeline é de ponta a ponta, o que significa que ele lida com o fluxo de dados da fonte (como um arquivo de vídeo) até o destino (como a exibição de gráficos). No entanto, se você quiser ler ou modificar os dados conforme eles passam pelo pipeline, deverá escrever um plug-in personalizado. Isso requer um conhecimento bastante profundo do pipeline de Media Foundation. Para determinadas tarefas, a criação de um novo plug-in é muita sobrecarga. O leitor de origem foi projetado para esse tipo de situação, quando você deseja obter os dados brutos de uma fonte sem a sobrecarga de todo o pipeline.

Internamente, o leitor de origem mantém um ponteiro para uma fonte de mídia. Uma *origem de mídia* é um objeto Media Foundation que gera dados de mídia de uma fonte externa, como um arquivo de mídia ou dispositivo de captura de vídeo. O leitor de origem gerencia todas as chamadas de método para a origem de mídia. (Para obter mais informações sobre fontes de mídia, consulte [fontes de mídia](media-sources.md).)

Se a origem da mídia fornecer dados compactados, você poderá usar o leitor de origem para decodificar os dados. Nesse caso, o leitor de origem carregará o decodificador correto e gerenciará o fluxo de dados entre a origem e o decodificador de mídia. O leitor de origem também pode executar algum processamento de vídeo limitado: conversão de cores de YUV para RGB-32 e desentrelaçamento de software, embora essas operações não sejam recomendadas para renderização de vídeo em tempo real. A imagem a seguir ilustra esse processo.

![diagrama do leitor de origem](images/sourcereader.png)

O leitor de origem não envia os dados para um destino; cabe ao aplicativo consumir os dados. Por exemplo, o leitor de origem pode ler um arquivo de vídeo, mas ele não renderizará o vídeo na tela. Além disso, o leitor de origem não gerencia um relógio de apresentação, manipula problemas de tempo ou sincroniza vídeo com áudio.

Considere usar o leitor de origem quando:

-   Você deseja obter dados de um arquivo de mídia sem se preocupar com a estrutura de arquivos subjacente.
-   Você deseja obter dados de um dispositivo de captura de áudio ou vídeo.
-   Suas tarefas de processamento de dados não são sensíveis a tempo ou você não precisa de um relógio de apresentação.
-   Você já tem um pipeline de mídia que não é baseado em Media Foundation e você deseja incorporar as fontes de mídia de Media Foundation em seu próprio pipeline.

O leitor de origem não é recomendado nas seguintes situações:

-   Para conteúdo protegido. O leitor de origem não dá suporte ao DRM (gerenciamento de direitos digitais).
-   Se você se preocupa com os detalhes da estrutura de arquivos subjacente. O leitor de origem oculta esse tipo de detalhe.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                                        | Descrição                                                                                                                       |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [Usando o leitor de origem para processar dados de mídia](processing-media-data-with-the-source-reader.md)<br/> | Este tópico descreve como usar o leitor de origem para processar dados de mídia.<br/>                                               |
| [Usando o leitor de origem no modo assíncrono](using-the-source-reader-in-asynchronous-mode.md)<br/>  | Este tópico descreve como usar o leitor de origem no modo assíncrono.<br/>                                                |
| [Tutorial: decodificando áudio](tutorial--decoding-audio.md)<br/>                                          | Este tutorial mostra como usar o leitor de origem para decodificar áudio de um arquivo de mídia e gravar o áudio em um arquivo WAVE.<br/> |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Arquitetura Media Foundation](media-foundation-architecture.md)
</dt> <dt>

[Guia de programação Media Foundation](media-foundation-programming-guide.md)
</dt> <dt>

[**IMFSourceReader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader)
</dt> </dl>

 

 




