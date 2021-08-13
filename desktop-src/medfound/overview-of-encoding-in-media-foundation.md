---
description: Este tópico é uma visão geral das APIs de codificação de arquivo fornecidas no Microsoft Media Foundation.
ms.assetid: 69dbef63-e272-4ad2-8d04-ae9366f79b33
title: Visão geral da codificação no Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a663260d92aad4eb23902ec35721c252f15fbba64c3404ff97bfb60f0622c674
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118239725"
---
# <a name="overview-of-encoding-in-media-foundation"></a>Visão geral da codificação no Media Foundation

Este tópico é uma visão geral das APIs de codificação de arquivo fornecidas no Microsoft Media Foundation.

## <a name="terminology"></a>Terminologia

*A codificação é* um termo geral que abrange vários processos distintos:

1.  Codificando um fluxo de áudio ou vídeo em formatos compactados. Por exemplo, codificar um fluxo de vídeo para o vídeo H.264.
2.  Multiplexação ("muxing") um ou mais fluxos em um único fluxo de byte. Normalmente, os fluxos de entrada são codificados primeiro. Esta etapa pode envolver o packetizing dos fluxos codificados.
3.  Escrevendo um fluxo de byte multiplexado em um arquivo, como um arquivo MP4 ou ASF (Advanced Systems Format). Como alternativa, o fluxo multiplexado pode ser enviado pela rede.

O diagrama a seguir mostra estes três processos:

![diagrama mostrando os processos de codificação e multiplexação](images/encoding03.png)

Variações desse processo incluem transcodificação e remuxing:

-   *Transcodificação* significa decodificar um arquivo existente, codificar os fluxos e re-multiplexar os fluxos codificados. A transcodificação pode ser feita para converter um arquivo de um tipo de codificação para outro; por exemplo, para converter vídeo H.264 em Windows vídeo de mídia (WMV). Também pode ser feito para alterar a taxa de bits codificada; o tamanho do quadro de vídeo; a taxa de quadros; ou outros parâmetros de formato.
-   *Remultiplexing* ou *remuxing* significa demultiplexar um arquivo e re multiplexar os fluxos, sem nenhuma etapa de decodificar/codificar. Isso pode ser feito para alterar como os pacotes de áudio/vídeo são multiplexados, para remover um fluxo ou combinar fluxos de dois arquivos de origem diferentes.
-   *Transgravação* é um caso especial de transcodificação, em que a taxa de bits é alterada sem alterar o tipo de compactação. Por exemplo, você pode converter um arquivo de alta taxa de bits em uma taxa de bits mais baixa. Um cenário típico no qual a transratação pode ser usada é ao sincronizar o conteúdo de mídia de um computador para um dispositivo portátil. Se o dispositivo portátil não dá suporte a uma alta taxa de bits, o arquivo pode ser transrated antes de ser copiado para o dispositivo portátil.

O diagrama de bloco a seguir mostra o processo de transcodificação.

![diagrama mostrando o processo de transcodificação](images/encoding05.png)

O diagrama de bloco a seguir mostra o processo de remuxing.

![diagrama mostrando o processo de remuxing](images/encoding06.png)

Essa documentação às vezes usa *o termo codificação* para incluir transcodificação e remuxing. Quando for importante distinguir entre eles, a documentação observará a diferença.

Confira também: [Media Foundation: Conceitos Essenciais.](media-foundation-programming--essential-concepts.md)

## <a name="media-foundation-encoding-architecture"></a>Media Foundation de codificação

Na camada mais baixa da arquitetura Media Foundation, os seguintes tipos de componente são usados para codificação:

-   Para transcodificação, [as Fontes de](media-sources.md) Mídia são usadas para demultiplexar o arquivo de origem.
-   Para o processo de codificação, [as Media Foundation são usadas](media-foundation-transforms.md) para decodificar e codificar fluxos.
-   Para o processo de multiplexação, os [Sinks](media-sinks.md) de Mídia são usados para multiplexar os fluxos e gravar o fluxo multiplexado em um arquivo ou rede.

O diagrama a seguir mostra o fluxo de dados entre esses componentes em um cenário de transcodificação:

![diagrama mostrando os componentes usados na transcodificação](images/encoding04.png)

A maioria dos aplicativos não usará esses componentes diretamente. Em vez disso, um aplicativo usará APIs de nível superior que gerenciam esses componentes de nível inferior. Media Foundation fornece duas APIs de nível superior para codificação:

<dl> <dt>

<span id="Media_Session"></span><span id="media_session"></span><span id="MEDIA_SESSION"></span>[Sessão de mídia](media-session.md)
</dt> <dd>

A Sessão de Mídia fornece um pipeline de ponta a ponta que move dados da fonte de mídia, por meio dos codecs e, por fim, para o sink de mídia. O aplicativo controla a Sessão de Mídia e recebe eventos de status da Sessão de Mídia.

</dd> <dt>

<span id="Source_Reader_plus_Sink_Writer"></span><span id="source_reader_plus_sink_writer"></span><span id="SOURCE_READER_PLUS_SINK_WRITER"></span>[Leitor de Origem](source-reader.md) mais [o Sink Writer](sink-writer.md)
</dt> <dd>

O Leitor de Origem envolve a origem da mídia e, opcionalmente, os decodificadores. Ele fornece amostras codificadas ou decodificadas do aplicativo. O Sink Writer envolve o sink de mídia e, opcionalmente, os codificadores. O aplicativo passa amostras para o Sink Writer.

</dd> </dl>

O diagrama a seguir mostra a Sessão de Mídia:

![diagrama mostrando como a sessão de mídia executa a transcodificação](images/encoding01.png)

A [API transcodificar](transcode-api.md) (a caixa sombreada azul) é um conjunto de APIs introduzidas no Windows 7, o que facilita a configuração da Sessão de Mídia para codificação.

O diagrama a seguir mostra o Leitor de Origem e o Sink Writer:

![diagrama mostrando a transcodificação com o leitor de origem e o autor do sink](images/encoding02.png)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Codificando e criando arquivos](encoding-and-file-authoring.md)
</dt> <dt>

[Media Foundation programação: conceitos essenciais](media-foundation-programming--essential-concepts.md)
</dt> </dl>

 

 



