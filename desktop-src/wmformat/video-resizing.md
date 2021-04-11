---
title: Redimensionamento de vídeo
description: Redimensionamento de vídeo
ms.assetid: 38ecb729-68eb-4452-8389-cabe987fb8b6
keywords:
- SDK do Windows Media Format, redimensionamento de vídeo
- SDK do Windows Media Format, redimensionando vídeo
- ASF (Advanced Systems Format), redimensionamento de vídeo
- ASF (formato de sistemas avançados), redimensionamento de vídeo
- ASF (Advanced Systems Format), redimensionando vídeo
- ASF (formato de sistemas avançados), redimensionando vídeo
- redimensionamento de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b200496b1dead3abacfbfad7674519e0cf7ce4f7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159591"
---
# <a name="video-resizing"></a>Redimensionamento de vídeo

Ao definir as configurações para um fluxo de vídeo, você deve especificar uma largura e uma altura para os quadros de vídeo. Esse tamanho de vídeo determina o tamanho dos quadros de vídeo codificados na seção de dados do arquivo. No entanto, o tamanho do vídeo em um perfil não determina ou limita o tamanho da mídia de entrada que você entrega ao gravador ou o tamanho da mídia de saída que você recebe do leitor. O gravador pode redimensionar os quadros de vídeo para atender às necessidades do seu aplicativo.

O tamanho da imagem de vídeo pode ser pensado como passar por três estágios: tamanho do vídeo de entrada, tamanho do vídeo de fluxo e tamanho do vídeo de saída.

O tamanho do vídeo de entrada é o tamanho dos quadros que você passa como amostras para o objeto do gravador. Você define esse tamanho como uma das propriedades de entrada de vídeo necessárias. Para obter mais informações sobre propriedades de entrada, consulte [para enumerar formatos de entrada](to-enumerate-input-formats.md).

O tamanho do vídeo do fluxo é o tamanho dos quadros na seção de dados do arquivo ASF. Você define esse tamanho como uma das definições de configuração de fluxo necessárias no perfil. Se você estiver gravando um arquivo e o tamanho do vídeo de entrada for diferente do tamanho do vídeo do fluxo, o gravador redimensionará os quadros durante a codificação. Para obter mais informações sobre as propriedades de fluxo de vídeo, consulte [Configuring Video Streams](configuring-video-streams.md).

Tamanho do vídeo de saída é o tamanho dos quadros entregues pelo leitor ou leitor síncrono. Você define esse tamanho como uma das propriedades de saída de vídeo necessárias. Se você estiver lendo um arquivo e o tamanho do vídeo de saída for diferente do tamanho do vídeo do fluxo, o leitor redimensionará os quadros durante a decodificação.

Não é possível definir um tamanho de vídeo de fluxo para um número ímpar de pixels de largura. Se você definir a largura de um fluxo de vídeo com um valor ímpar, o perfil não será aceito pelo gravador ou o vídeo resultante será codificado com uma linha preta de um lado para fazer a diferença.

Você deve tomar cuidado ao redimensionar o vídeo. As imagens tendem a ter a melhor aparência em sua resolução original. O redimensionamento de imagens pode muitas vezes causar distorção e tornar o texto ilegível. Se você estiver compactando o vídeo em uma taxa de bits baixa, também verá que o redimensionamento de distorções pode levar a artefatos de compactação graves.

O codec de tela do Windows Media Video 9 não dá suporte ao redimensionamento.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Recursos de gravação de arquivo**](file-writing-features.md)
</dt> <dt>

[**Trabalhando com entradas**](working-with-inputs.md)
</dt> <dt>

[**Trabalhando com saídas**](working-with-outputs.md)
</dt> </dl>

 

 




