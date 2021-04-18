---
description: Codificação de vídeo com compactação temporal
ms.assetid: df363017-97c5-45b0-b8a5-44ac73b7a0e7
title: Codificação de vídeo com compactação temporal (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ee107d8bf6b1ef6b1700abff105b0bdb79f72f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105791556"
---
# <a name="video-encoding-with-temporal-compression-microsoft-media-foundation"></a>Codificação de vídeo com compactação temporal (Microsoft Media Foundation)

Para obter as maiores taxas de compactação possíveis, os codecs de vídeo do Windows Media usam a *compactação temporal*. A compactação temporal é uma técnica para reduzir o tamanho do vídeo compactado não codificando cada quadro como uma imagem completa. Os quadros codificados completamente (como uma imagem estática) são chamados de *quadros-chave*. Todos os outros quadros do vídeo são representados por dados que especificam a alteração desde o último quadro. Esses quadros são chamados de *quadros Delta*.

A quantidade de compactação que pode ser obtida usando a compactação temporal depende do conteúdo. Se o vídeo for estático, sem muito movimento ou outras alterações na imagem, muitos quadros Delta poderão ser criados para cada quadro-chave. Quanto mais quadros Delta forem usados, menor será o fluxo de vídeo codificado. No entanto, se o vídeo for dinâmico, com muitas cores de movimento ou alteração, o benefício de usar a compactação temporal será menor.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Trabalhando com vídeo](workingwithvideo.md)
</dt> </dl>

 

 



