---
description: Este tópico é uma visão geral das APIs de codificação de arquivo fornecidas no Microsoft Media Foundation.
ms.assetid: 69dbef63-e272-4ad2-8d04-ae9366f79b33
title: Visão geral da codificação no Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81882bd6da43f4040614347b662d988844c7b7a6
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104558069"
---
# <a name="overview-of-encoding-in-media-foundation"></a>Visão geral da codificação no Media Foundation

Este tópico é uma visão geral das APIs de codificação de arquivo fornecidas no Microsoft Media Foundation.

## <a name="terminology"></a>Terminologia

A *codificação* é um termo geral que abrange vários processos distintos:

1.  Codificação de um fluxo de áudio ou vídeo em formatos compactados. Por exemplo, codificar um fluxo de vídeo para o vídeo H. 264.
2.  Multiplexação ("muxing") de um ou mais fluxos em um único fluxo de bytes. Normalmente, os fluxos de entrada são codificados primeiro. Essa etapa pode envolver o pacote de fluxos codificados.
3.  Gravar um fluxo de bytes multiplexados em um arquivo, como um arquivo MP4 ou um formato de sistema avançado (ASF). Como alternativa, o fluxo multiplexado pode ser enviado pela rede.

O diagrama a seguir mostra esses três processos:

![diagrama mostrando os processos de codificação e multiplexação](images/encoding03.png)

As variações desse processo incluem transcodificação e remuxing:

-   *Transcodificação* significa decodificar um arquivo existente, codificar novamente os fluxos e remultiplexar os fluxos codificados. A transcodificação pode ser feita para converter um arquivo de um tipo de codificação para outro; por exemplo, para converter o vídeo H. 264 no vídeo do Windows Media (WMV). Também pode ser feito para alterar a taxa de bits codificada; o tamanho do quadro do vídeo; a taxa de quadros; ou outros parâmetros de formato.
-   A *remultiplexação* ou *remuxing* significa demultiplexar um arquivo e remultiplexar os fluxos, sem nenhuma etapa de decodificação/codificação. Isso pode ser feito para alterar como os pacotes de áudio/vídeo são multiplexados, para remover um fluxo ou para combinar fluxos de dois arquivos de origem diferentes.
-   A *transclassificação* é um caso especial de transcodificação, em que a taxa de bits é alterada sem alterar o tipo de compactação. Por exemplo, você pode converter um arquivo de alta taxa de bits em uma taxa de bits inferior. Um cenário típico no qual a transclassificação pode ser usada é ao sincronizar o conteúdo de mídia de um PC para um dispositivo portátil. Se o dispositivo portátil não oferecer suporte a uma taxa de bits alta, o arquivo poderá ser transformado antes de ser copiado para o dispositivo portátil.

O diagrama de bloco a seguir mostra o processo de transcodificação.

![diagrama mostrando o processo de transcodificação](images/encoding05.png)

O diagrama de bloco a seguir mostra o processo remuxing.

![diagrama mostrando o processo remuxing](images/encoding06.png)

Essa documentação às vezes usa a *codificação* de termo para incluir transcodificação e remuxing. Quando for importante distinguir entre eles, a documentação notará a diferença.

Consulte também: [Media Foundation: conceitos essenciais](media-foundation-programming--essential-concepts.md).

## <a name="media-foundation-encoding-architecture"></a>Arquitetura de codificação de Media Foundation

Na camada mais baixa da arquitetura de Media Foundation, os seguintes tipos de componente são usados para codificação:

-   Para transcodificação, as [fontes de mídia](media-sources.md) são usadas para demultiplexar o arquivo de origem.
-   Para o processo de codificação, [Media Foundation transformações](media-foundation-transforms.md) são usadas para decodificar e codificar fluxos.
-   Para o processo de multiplexação, os [coletores de mídia](media-sinks.md) são usados para multiplexar os fluxos e gravar o fluxo multiplexado em um arquivo ou rede.

O diagrama a seguir mostra o fluxo de dados entre esses componentes em um cenário de transcodificação:

![diagrama mostrando os componentes usados na transcodificação](images/encoding04.png)

A maioria dos aplicativos não usará esses componentes diretamente. Em vez disso, um aplicativo usará APIs de nível superior que gerenciam esses componentes de nível inferior. Media Foundation fornece duas APIs de nível superior para codificação:

<dl> <dt>

<span id="Media_Session"></span><span id="media_session"></span><span id="MEDIA_SESSION"></span>[Sessão de mídia](media-session.md)
</dt> <dd>

A sessão de mídia fornece um pipeline de ponta a ponta que move dados da origem de mídia, por meio dos codecs e, por fim, para o coletor de mídia. O aplicativo controla a sessão de mídia e recebe eventos de status da sessão de mídia.

</dd> <dt>

<span id="Source_Reader_plus_Sink_Writer"></span><span id="source_reader_plus_sink_writer"></span><span id="SOURCE_READER_PLUS_SINK_WRITER"></span>[Leitor de origem](source-reader.md) mais [gravador de coletor](sink-writer.md)
</dt> <dd>

O leitor de origem encapsula a fonte de mídia e, opcionalmente, os decodificadores. Ele fornece amostras codificadas ou decodificadas do aplicativo. O gravador do coletor encapsula o coletor de mídia e, opcionalmente, os codificadores. O aplicativo passa amostras para o gravador do coletor.

</dd> </dl>

O diagrama a seguir mostra a sessão de mídia:

![diagrama mostrando como a sessão de mídia executa transcodificação](images/encoding01.png)

A [API de transcodificação](transcode-api.md) (a caixa sombreada azul) é um conjunto de APIs introduzidas no Windows 7, que facilitam a configuração da sessão de mídia para codificação.

O próximo diagrama mostra o leitor de fonte e o gravador de coletor:

![diagrama mostrando transcodificação com o leitor de fonte e o gravador de coletor](images/encoding02.png)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Codificando e criando arquivos](encoding-and-file-authoring.md)
</dt> <dt>

[Programação de Media Foundation: conceitos essenciais](media-foundation-programming--essential-concepts.md)
</dt> </dl>

 

 



