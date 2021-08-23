---
description: Se você for novo na mídia digital, este tópico apresentará alguns conceitos que você precisará entender antes de escrever um Media Foundation aplicativo.
ms.assetid: d76d655e-23f3-407c-97a1-be015b0de37d
title: 'Media Foundation: conceitos essenciais'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 825e84b3c7ad3060cae0a2530bc9a7af3155fd9113c490ce2c42f69771c1f9b8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119357246"
---
# <a name="media-foundation-essential-concepts"></a>Media Foundation: conceitos essenciais

Se você for novo na mídia digital, este tópico apresentará alguns conceitos que você precisará entender antes de escrever um Media Foundation aplicativo.

-   [Fluxos](#streams)
-   [Compactação](#compression)
-   [Contêineres de mídia](#media-containers)
-   [Formatos](#formats)
-   [Tópicos relacionados](#related-topics)

## <a name="streams"></a>Fluxos

Um *fluxo* é uma sequência de dados de mídia com um tipo uniforme. Os tipos mais comuns são áudio e vídeo, mas um fluxo pode conter quase qualquer tipo de dados, incluindo texto, comandos de script e imagens ainda. O termo *fluxo* nesta documentação não implica entrega em uma rede. Um arquivo de mídia destinado à reprodução local também contém fluxos.

Normalmente, um arquivo de mídia contém um único fluxo de áudio ou exatamente um fluxo de vídeo e um fluxo de áudio. No entanto, um arquivo de mídia pode conter vários fluxos do mesmo tipo. Por exemplo, um arquivo de vídeo pode conter fluxos de áudio em vários idiomas diferentes. Em tempo de executar, o aplicativo selecionaria qual fluxo usar.

## <a name="compression"></a>Compactação

*Compactação* refere-se a qualquer processo que reduz o tamanho de um fluxo de dados removendo informações redundantes. Os algoritmos de compactação se enquadram em duas categorias amplas:

-   *Compactação sem* perda. Usando um algoritmo sem perda, os dados reconstruídos são idênticos ao original.
-   *Compactação com* perda. Usando um algoritmo de perda, os dados reconstruídos são uma aproximação do original, mas não são uma combinação exata.

Na maioria dos outros domínios, a compactação com perda não é aceitável. (Imagine uma "aproximação" de uma planilha!) Mas os esquemas de compactação com perda são adequados para áudio e vídeo, por alguns motivos.

O primeiro motivo tem a ver com a física da percepção humana. Quando escutamos um som complexo, como uma gravação de música, algumas das informações contidas nesse som não são perceptíveis para o ouvido. Com a ajuda da teoria do processamento de sinais, é possível analisar e separar as frequências que não podem ser percebidas. Essas frequências podem ser removidas sem nenhum efeito perceptivo. Embora o áudio reconstruído não corresponderá exatamente ao original, ele *soará* o mesmo para o ouvinte. Princípios semelhantes se aplicam ao vídeo.

Em segundo lugar, alguma degradação na qualidade do som ou da imagem pode ser aceitável, dependendo da finalidade pretendido. Em telefonia, por exemplo, o áudio geralmente é altamente compactado. O resultado é bom o suficiente para uma conversa por telefone, mas você não gostaria de escutar uma orquestra de orquestração em um telefone.

A compactação também *é chamada de codificação* e um dispositivo que codifica é chamado de *codificador*. O processo reverso *está decodificando* e o dispositivo é naturalmente chamado *de decodificador*. O termo geral para codificadores e decodificadores é *codec*. Os codecs podem ser implementados em hardware ou software.

A tecnologia de compactação mudou rapidamente desde o advento da mídia digital e um grande número de esquemas de compactação está em uso atualmente. Esse fato é um dos principais desafios para programação de mídia digital.

## <a name="media-containers"></a>Contêineres de mídia

É raro armazenar um fluxo de áudio ou vídeo bruto como um arquivo de computador ou enviar um diretamente pela rede. Por um lado, seria impossível decodificar esse fluxo, sem saber com antecedência qual codec usar. Portanto, os arquivos de mídia geralmente contêm pelo menos alguns dos seguintes elementos:

-   Os headers de arquivo que descrevem o número de fluxos, o formato de cada fluxo e assim por diante.
-   Um índice que permite acesso aleatório ao conteúdo.
-   Metadados que descrevem o conteúdo (por exemplo, o artista ou título).
-   Os headers de pacote, para habilitar a transmissão de rede ou o acesso aleatório.

Esta documentação usa o *termo contêiner* para descrever todo o pacote de fluxos, headers, índices, metadados e assim por diante. O motivo para usar o termo *contêiner em* vez *de arquivo* é que alguns formatos de contêiner são projetados para transmissão ao vivo. Um aplicativo pode gerar o contêiner em tempo real, nunca o armazenar em um arquivo.

Um exemplo inicial de um contêiner de mídia é o formato de arquivo AVI. Outros exemplos incluem MP4 e ASF (Advanced Systems Format). Os contêineres podem ser identificados pela extensão de nome de arquivo (por exemplo, .mp4) ou pelo tipo MIME.

O diagrama a seguir mostra uma estrutura típica para um contêiner de mídia. O diagrama não representa nenhum formato específico; os detalhes de cada formato variam muito.

![diagrama mostrando um contêiner de mídia típico](images/concepts01.png)

Observe que a estrutura mostrada no diagrama é hierárquica, com informações de header aparecendo no início do contêiner. Essa estrutura é típica de muitos (mas não todos) formatos de contêiner. Observe também que a seção de dados contém pacotes intercalados de áudio e vídeo. Esse tipo de intercalação é comum em contêineres de mídia.

O termo *multiplexação* refere-se ao processo de pacotes dos fluxos de áudio e vídeo e da intercalação dos pacotes no contêiner. O processo reverso, remontando os fluxos dos dados em pacotes, é chamado *de demultiplexing*.

## <a name="formats"></a>Formatos

Na mídia digital, o formato *do termo* é ambíguo. Um formato pode se referir ao tipo de codificação *,* como vídeo H.264 ou o *contêiner*, como MP4. Essa distinção geralmente é confusa para usuários comuns. Os nomes dados aos formatos de mídia nem sempre ajudam. Por exemplo, *MP3* refere-se a um formato de codificação (MPEG-1 Camada de Áudio 3) e a um formato de arquivo.

No entanto, a distinção é importante, pois a leitura de um arquivo de mídia envolve, na verdade, dois estágios:

1.  Primeiro, o contêiner deve ser analisado. Na maioria dos casos, o número de fluxos e o formato de cada fluxo não podem ser conhecidos até que esta etapa seja concluída.
2.  Em seguida, se os fluxos são compactados, eles devem ser decodificados usando os decodificadores apropriados.

Esse fato leva naturalmente a um design de software em que componentes separados são usados para analisar contêineres e decodificar fluxos. Além disso, essa abordagem se presta a um modelo de plug-in, para que terceiros possam fornecer seus próprios analisadores e codecs. No Windows, o COM (Component Object Model) fornece uma maneira padrão de separar uma API de sua implementação, que é um requisito para qualquer modelo de plug-in. Por esse motivo (entre outros), o Media Foundation usa interfaces COM.

O diagrama a seguir mostra os componentes usados para ler um arquivo de mídia:

![diagrama mostrando os componentes para ler um arquivo de mídia](images/concepts02.png)

A escrita de um arquivo de mídia também requer duas etapas:

1.  Codificando os dados de áudio/vídeo descompactados.
2.  Colocar os dados compactados em um formato de contêiner específico.

O diagrama a seguir mostra os componentes usados para gravar um arquivo de mídia:

![diagrama mostrando os componentes para gravar um arquivo de mídia.](images/concepts03.png)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Guia Media Foundation programação do Media Foundation](media-foundation-programming-guide.md)
</dt> </dl>

 

 



