---
description: Codificação de vídeo com compactação temporal
ms.assetid: df363017-97c5-45b0-b8a5-44ac73b7a0e7
title: Codificação de vídeo com compactação temporal (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10d663b0101353d9ce72dab45f0b85e594afcacf4aa8b8a99a6d61d2db0ae07d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119721346"
---
# <a name="video-encoding-with-temporal-compression-microsoft-media-foundation"></a>Codificação de vídeo com compactação temporal (Microsoft Media Foundation)

para obter as maiores taxas de compactação possíveis, os codecs de vídeo de mídia Windows usam a *compactação temporal*. A compactação temporal é uma técnica para reduzir o tamanho do vídeo compactado não codificando cada quadro como uma imagem completa. Os quadros codificados completamente (como uma imagem estática) são chamados de *quadros-chave*. Todos os outros quadros do vídeo são representados por dados que especificam a alteração desde o último quadro. Esses quadros são chamados de *quadros Delta*.

A quantidade de compactação que pode ser obtida usando a compactação temporal depende do conteúdo. Se o vídeo for estático, sem muito movimento ou outras alterações na imagem, muitos quadros Delta poderão ser criados para cada quadro-chave. Quanto mais quadros Delta forem usados, menor será o fluxo de vídeo codificado. No entanto, se o vídeo for dinâmico, com muitas cores de movimento ou alteração, o benefício de usar a compactação temporal será menor.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Trabalhando com vídeo](workingwithvideo.md)
</dt> </dl>

 

 



