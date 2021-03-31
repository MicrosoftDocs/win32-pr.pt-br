---
description: Esta seção descreve como usar a API de transcodificação para codificar novamente os arquivos de mídia. A API de transcodificação foi introduzida no Windows 7.
ms.assetid: 24bf68a8-39bf-4302-b28c-71bb23b63469
title: API de transcodificação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9783c6f99a25ba6835171dcc7f7555a1f747c72b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827801"
---
# <a name="transcode-api"></a>API de transcodificação

Esta seção descreve como usar a API de transcodificação para codificar novamente os arquivos de mídia. A API de transcodificação foi introduzida no Windows 7.

*Transcodificação* é a conversão de um arquivo de mídia digital de um formato para outro. A API de transcodificação foi projetada para ser usada com a [sessão de mídia](media-session.md). Ele simplifica o uso da sessão de mídia para determinados tipos de aplicativos de transcodificação:

-   Codificação de taxa de bits constante (CBR), em que a taxa de bits de destino é conhecida com antecedência.
-   No máximo um fluxo de áudio e um fluxo de vídeo.
-   Codificação de e para um arquivo.

A API de transcodificação não oferece suporte ao seguinte:

-   Taxa de bits variável (VBR) ou codificação de passagem múltipla.
-   Vários fluxos de áudio ou vários fluxos de vídeo.
-   Conteúdo protegido por DRM diferente dos arquivos ASF protegidos com WMDRM.
-   Transmissão ao vivo, como streaming de Live-to-file ou Live-to-Live streaming.

Se o aplicativo de codificação se ajustar a essas restrições, a API transcodificará um modelo de programação mais simples do que usar a sessão de mídia sozinha.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                          | Descrição                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Sobre a API de transcodificação](about-the-transcode-api.md)<br/>                              | Fornece uma visão geral da API de transcodificação.<br/>                                                                                                                                                                |
| [Usando a API de transcodificação](fast-transcode-objects.md)<br/>                               | Descreve como um aplicativo usa a API de transcodificação.<br/>                                                                                                                                                             |
| [Tutorial: codificando um arquivo MP4](tutorial--encoding-an-mp4-file-.md)<br/>               | Um tutorial passo a passo que mostra como usar a API de transcodificação para codificar um arquivo MP4.<br/>                                                                                                                           |
| [Tutorial: codificando um arquivo WMA](tutorial--converting-an-mp3-file-to-a-wma-file.md)<br/> | Mostra como usar a API de transcodificação para codificar um arquivo WMA. Este tutorial modifica o código mostrado no [tutorial: codificando um arquivo MP4](tutorial--encoding-an-mp4-file-.md), portanto, você deve ler o tutorial primeiro.<br/> |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Codificando e criando arquivos](encoding-and-file-authoring.md)
</dt> <dt>

[Media Foundation: conceitos essenciais](media-foundation-programming--essential-concepts.md)
</dt> <dt>

[Visão geral da codificação no Media Foundation](overview-of-encoding-in-media-foundation.md)
</dt> </dl>

 

 




