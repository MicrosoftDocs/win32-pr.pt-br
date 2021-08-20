---
title: Reizing de vídeo
description: Reizing de vídeo
ms.assetid: 38ecb729-68eb-4452-8389-cabe987fb8b6
keywords:
- Windows SDK de Formato de Mídia, reizing de vídeo
- Windows SDK de Formato de Mídia, reizing video
- ASF (Advanced Systems Format), resizing de vídeo
- ASF (Formato de Sistemas Avançados), reizing de vídeo
- FORMATO DE SISTEMAS Avançados (ASF), reizing video
- ASF (Formato de Sistemas Avançados), reizing video
- reizing de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7a3261b5b78b386a0589e2e5554b52793d478f052765cb9caa63cf7e399d90e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027174"
---
# <a name="video-resizing"></a>Reizing de vídeo

Ao definir as configurações para um fluxo de vídeo, você deve especificar uma largura e altura para os quadros de vídeo. Esse tamanho de vídeo determina o tamanho dos quadros de vídeo codificados na seção de dados do arquivo. No entanto, o tamanho do vídeo em um perfil não determina ou limita o tamanho da mídia de entrada que você fornece ao autor ou o tamanho da mídia de saída que você recebe do leitor. O autor pode reorganizar os quadros de vídeo para atender às necessidades do seu aplicativo.

O tamanho da imagem de vídeo pode ser pensado como passando por três estágios: tamanho do vídeo de entrada, tamanho do vídeo de fluxo e tamanho do vídeo de saída.

O tamanho do vídeo de entrada é o tamanho dos quadros que você passa como exemplos para o objeto de gravação. Você define esse tamanho como uma das propriedades de entrada de vídeo necessárias. Para obter mais informações sobre propriedades de entrada, [consulte Para enumerar formatos de entrada.](to-enumerate-input-formats.md)

O tamanho do vídeo de fluxo é o tamanho dos quadros na seção de dados do arquivo ASF. Você define esse tamanho como uma das definições de configuração de fluxo necessárias no perfil. Se você estiver escrevendo um arquivo e o tamanho do vídeo de entrada for diferente do tamanho do vídeo de fluxo, o autor resize os quadros durante a codificação. Para obter mais informações sobre propriedades de fluxo de vídeo, consulte [Configuring Video Fluxos](configuring-video-streams.md).

O tamanho do vídeo de saída é o tamanho dos quadros entregues pelo leitor ou pelo leitor síncrono. Você define esse tamanho como uma das propriedades de saída de vídeo necessárias. Se você estiver lendo um arquivo e o tamanho do vídeo de saída for diferente do tamanho do vídeo de fluxo, o leitor resize os quadros durante a decodificação.

Não é possível definir um tamanho de vídeo de fluxo para um número ímpar de pixels de largura. Se você definir a largura de um fluxo de vídeo com um valor ímpar, o perfil não será aceito pelo autor ou o vídeo resultante será codificado com uma linha preta em um lado para fazer a diferença.

Você deve tomar cuidado ao reizing video. As imagens tendem a ter a melhor aparência em sua resolução original. O reizing de imagens geralmente pode causar distorção e tornar o texto ilegível. Se você estiver compactando o vídeo para uma taxa de bits baixa, também encontrará que o reizing de distorções pode levar a artefatos de compactação graves.

O codec Windows de tela do Vídeo de Mídia 9 não dá suporte ao re tamanho.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Recursos de escrita de arquivo**](file-writing-features.md)
</dt> <dt>

[**Trabalhando com entradas**](working-with-inputs.md)
</dt> <dt>

[**Trabalhando com saídas**](working-with-outputs.md)
</dt> </dl>

 

 




