---
description: O sink writer é um componente para codificar arquivos de áudio ou vídeo.
ms.assetid: 23AF25B8-B94C-48BC-83D8-5863ACFFD4CA
title: Sink Writer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a1cfa60abb9b107030aba18e30175592d637c7676ff44781d62b3f5c1509351
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119887346"
---
# <a name="sink-writer"></a>Sink Writer

O sink writer é um componente para codificar arquivos de áudio ou vídeo.

O diagrama a seguir mostra, em um alto nível, como um aplicativo usa o autor do sink para codificar e o arquivo de áudio/vídeo.

![um diagrama que mostra o autor do sink.](images/encoding09.png)

O autor do sink hospeda um sink de mídia e, opcionalmente, um ou mais codificadores. Os codificadores convertem dados de áudio ou vídeo descompactados em bitstreams codificados. O sink de mídia saídas de bitstreams para um arquivo. O autor do sink executa as seguintes tarefas:

-   Carrega o sink de mídia.
-   Localiza e carrega os codificadores.
-   Gerencia o fluxo de dados para os codificadores e o sink de mídia.

O aplicativo passa dados de áudio/vídeo para o autor do sink como entrada. Não importa como o aplicativo obtém ou gera os dados de entrada. Uma opção é usar o [Leitor de Origem](source-reader.md), conforme mostrado no diagrama a seguir. No entanto, o autor do sink não exige o uso do leitor de origem. Esses dois componentes são independentes.

![um diagrama que mostra o leitor de origem e o autor do sink.](images/encoding02.png)

## <a name="in-this-section"></a>Nesta seção

-   [Usando o Sink Writer](using-the-sink-writer.md)
-   [Tutorial: Usando o Sink Writer para codificar vídeo](tutorial--using-the-sink-writer-to-encode-video.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Codificando e criando arquivos](encoding-and-file-authoring.md)
</dt> <dt>

[Visão geral da codificação em Media Foundation](overview-of-encoding-in-media-foundation.md)
</dt> </dl>

 

 



