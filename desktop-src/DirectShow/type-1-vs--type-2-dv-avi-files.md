---
description: Digite-1 vs.
ms.assetid: 3f1cf981-f678-46a6-9784-ffb389438b6d
title: Tipos-1 vs. tipo-2 arquivos AVI de DV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0000b81e94e25749b5590287145a88a28280e16d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103921920"
---
# <a name="type-1-vs-type-2-dv-avi-files"></a>Tipos-1 vs. tipo-2 arquivos AVI de DV

Câmeras de DV produzem áudio-vídeo intercalado; cada quadro de vídeo também contém as informações de áudio. Se você salvar dados DV em um arquivo AVI, terá uma opção:

-   Armazene os dados intercalados como um fluxo no arquivo AVI. Isso é conhecido como um arquivo de tipo 1.
-   Divida os dados intercalados em fluxos de áudio e vídeo separados. Isso é conhecido como um arquivo de tipo 2.

Para captura de vídeo, em que a taxa de transferência máxima é crucial, é melhor usar um arquivo Type-1, pois os arquivos de tipo 2 contêm dados de áudio redundantes. (O fluxo de vídeo ainda tem os dados de áudio. O áudio é simplesmente ocultado ao rotular o fluxo como vídeo.) Além disso, gravar um arquivo de tipo 2 requer um tempo de processador adicional para dividir o fluxo intercalado.

Por outro lado, os arquivos Type-1 são menos eficientes para a edição em tempo real. O aplicativo deve extrair o áudio do fluxo intercalado, fazer as edições e intercalar os dados novamente. Além disso, o formato Type-1 não é compatível com o Microsoft® Video for Windows® (VFW). O DirectShow pode lidar com os dois tipos de arquivos.

Um arquivo de tipo 2 pode ser convertido para o tipo 1 usando o filtro [DV Muxer](dv-muxer-filter.md) . Um arquivo Type-1 pode ser convertido para o tipo 2 usando o filtro de [Splitter de DV](dv-splitter-filter.md) . O diagrama a seguir ilustra a diferença entre os dois formatos.

![conversão entre o tipo-1 e o tipo-2 DV](images/dv-filters3.png)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Vídeo digital no DirectShow](digital-video-in-directshow.md)
</dt> <dt>

[Dados de DV no formato de arquivo AVI](dv-data-in-the-avi-file-format.md)
</dt> </dl>

 

 



