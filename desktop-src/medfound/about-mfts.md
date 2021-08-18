---
description: Sobre o MFTs
ms.assetid: ca9cef70-b897-4fd5-9a13-8bf1c2b84b00
title: Sobre o MFTs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f04bfc09cbd17e5f0810f46eb6e42b230010348e89040b3cd407e98ee069c8f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035694"
---
# <a name="about-mfts"></a>Sobre o MFTs

Transformações de Media Foundation (MFTs) fornecem um modelo genérico para o processamento de dados de mídia. MFTs são usados para decodificadores, codificadores e processadores de sinais digitais (DSPs). Em suma, tudo que fica no pipeline de mídia entre a origem da mídia e o coletor de mídia é uma MFT.

Para a maioria dos aplicativos, os detalhes do processamento de dados de MFT ficam ocultos por camadas mais altas da arquitetura de Media Foundation. Muitos aplicativos Media Foundation nunca farão uma chamada direta para um MFT. No entanto, é certamente possível hospedar um MFT diretamente em seu aplicativo.

MFTs são uma evolução do modelo de transformação introduzido pela primeira vez com o DirectX Media Objects (DMOs). Na verdade, é relativamente fácil criar uma transformação que dê suporte a ambos os modelos. Em comparação com DMOs, os comportamentos necessários de MFTs são mais claramente especificados, o que facilita a gravação de uma implementação correta. Além disso, o MFTs pode dar suporte ao processamento de vídeo acelerado por hardware.

Este tópico fornece uma breve visão geral do modelo de processamento de MFT, com foco no design geral, em vez de chamadas de método específicas. Para obter uma descrição mais detalhada e passo a passo, consulte [modelo básico de processamento de MFT](basic-mft-processing-model.md).

## <a name="streams"></a>Fluxos

Uma MFT tem fluxos de entrada e fluxos de saída. Os fluxos de entrada recebem dados e os fluxos de saída produzem dados. Por exemplo, um decodificador tem um fluxo de entrada, que recebe os dados codificados e um fluxo de saída, que produz os dados decodificados.

Os fluxos em uma MFT não são representados como objetos COM distintos. Em vez disso, cada fluxo tem um identificador de fluxo designado e os métodos na interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) usam identificadores de fluxo como parâmetros de entrada.

Alguns MFTs têm um número fixo de fluxos. Por exemplo, decodificadores e codificadores normalmente têm exatamente uma entrada e uma saída. Outros MFTs têm um número dinâmico de fluxos. Se uma MFT oferecer suporte a fluxos dinâmicos, o cliente poderá adicionar novos fluxos de entrada. O cliente não pode adicionar fluxos de saída, mas o MFT pode adicionar ou remover fluxos de saída durante o processamento. Por exemplo, os multiplexadores geralmente permitem que o cliente adicione fluxos de entrada e tenha uma saída para o fluxo multiplexado. Os demultiplexadores são o inverso, com uma entrada, mas um número dinâmico de fluxos de saída, dependendo do conteúdo do fluxo de entrada. A ilustração a seguir mostra a diferença entre o multiplexador e o demultiplexador.

![diagrama mostrando um codificador/decodificador (1 entrada, 1 saída), um multiplexador (2 entradas, 1 saída) e um demultiplexador (1 entrada, 2 saídas)](images/f2b95bd5-f862-4d66-9d75-550a90f6cc97.gif)

## <a name="media-types"></a>Tipos de mídia

Quando um MFT é criado pela primeira vez, nenhum dos fluxos tem um formato estabelecido. Antes que o MFT possa processar dados, o cliente deve definir os formatos para os fluxos. Por exemplo, com um decodificador, o formato de entrada é o formato de compactação usado no arquivo de origem original, e o formato de saída é um formato descompactado, como áudio PCM ou vídeo RGB. Os formatos de fluxo são descritos usando [tipos de mídia](media-types.md).

Dependendo do estado interno do MFT, ele pode fornecer uma lista de possíveis tipos de mídia para cada fluxo. Você pode usar essa lista como uma dica ao definir os tipos de mídia. Definir o tipo de mídia em um fluxo pode alterar a lista de tipos possíveis para um outro fluxo. Por exemplo, um decodificador normalmente não pode fornecer tipos de saída até que o cliente defina o tipo de entrada. O tipo de entrada contém as informações de que o decodificador precisa para retornar uma lista de possíveis tipos de saída.

Para definir o tipo de mídia em um fluxo, chame [**IMFTransform:: SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) ou [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype). Para obter a lista de possíveis tipos de mídia para um fluxo, chame [**IMFTransform:: GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) ou [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype).

## <a name="processing-data"></a>Processando dados

Depois que o cliente define os tipos de mídia nos fluxos, o MFT está pronto para processar dados. Para fazer isso acontecer, o cliente alterna entre fornecer dados de entrada para o MFT e obter dados de saída do MFT:

-   Para fornecer dados de entrada para o MFT, chame [**IMFTransform::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput).
-   Para efetuar pull de dados de saída do MFT, chame [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput).

O método [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) usa um ponteiro para um exemplo de mídia alocado pelo cliente. O exemplo de mídia contém um ou mais buffers, e cada buffer contém dados de entrada para o MFT processar.

O método [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) dá suporte a dois modelos de alocação diferentes: ou o MFT aloca os buffers de saída ou o cliente aloca os buffers de saída. Alguns MFTs dão suporte a ambos os modelos de alocação, mas não são necessários para que um MFT dê suporte a ambos. Por exemplo, um MFT pode exigir que o cliente aloque os buffers de saída. O método [**IMFTransform:: GetOutputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo) retorna informações sobre um fluxo de saída, incluindo a qual modelo de alocação o MFT dá suporte.

MFTs são projetados para armazenar em buffer o mínimo possível de dados, a fim de minimizar a latência no pipeline. Portanto, a qualquer momento, o MFT pode sinalizar uma das seguintes condições:

-   O MFT requer mais dados de entrada. Nesse estado, o MFT não pode produzir saída até que o cliente chame [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) pelo menos uma vez.
-   O MFT não aceitará mais nenhuma entrada até que o cliente chame [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) pelo menos uma vez.

Por exemplo, suponha que você esteja usando um decodificador de vídeo para decodificar um fluxo de vídeo que contém uma mistura de quadros-chave e quadros Delta. Inicialmente, o MFT requer alguma entrada antes de poder decodificar qualquer quadro. O cliente chama [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) para entregar o primeiro quadro. Suponha que o primeiro quadro seja um quadro Delta (mostrado no diagrama a seguir como "P" para o quadro previsto). O decodificador se mantém nesse quadro, mas não pode produzir nenhuma saída até obter o próximo quadro chave.

![diagrama mostrando o MFT que precisa de entrada, apontando para um quadro previsto](images/f5a88ac6-24da-40e5-b356-649aa6f811c3.gif)

O cliente continua a chamar [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) e, eventualmente, atinge o próximo quadro-chave (mostrado no próximo diagrama como ' I ' para o quadro embutido). Agora, o decodificador tem quadros suficientes para iniciar a decodificação. Neste ponto, ele deixa de aceitar a entrada e o cliente deve chamar [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) para obter os quadros decodificados.

![diagrama mostrando um MFT que não está aceitando entrada, apontando para um quadro embutido e três quadros previstos](images/ae014a1a-9d03-4cfa-a04d-4a63bdc83f73.gif)

A abordagem mais simples para o cliente é simplesmente para chamadas alternativas para [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) e [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput). Um algoritmo mais sofisticado é descrito no tópico [modelo de processamento de MFT básico](basic-mft-processing-model.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Transformações de Media Foundation](media-foundation-transforms.md)
</dt> </dl>

 

 



