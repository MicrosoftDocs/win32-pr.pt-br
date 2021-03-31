---
title: Lendo de um fluxo
description: Lendo de um fluxo
ms.assetid: be961f06-cf5f-4093-9b31-7d1d69e62fec
keywords:
- Função AVIStreamInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cc7ecd606a33503557e7c7209bff68015756523
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103917301"
---
# <a name="reading-from-a-stream"></a>Lendo de um fluxo

Você pode recuperar informações sobre um fluxo aberto usando a função [**AVIStreamInfo**](/windows/desktop/api/Vfw/nf-vfw-avistreaminfoa) . Essa função preenche a estrutura [**AVISTREAMINFO**](/windows/desktop/api/Vfw/ns-vfw-avistreaminfoa) com informações como o tipo de dados no fluxo, o método de compactação usado ao gravar dados de fluxo, o tamanho sugerido do buffer, a taxa de reprodução e uma descrição de texto do fluxo.

Alguns membros da estrutura [**AVISTREAMINFO**](/windows/desktop/api/Vfw/ns-vfw-avistreaminfoa) também estão presentes na estrutura [**AVIFILEINFO**](/windows/desktop/api/Vfw/ns-vfw-avifileinfoa) . As informações na estrutura **AVIFILEINFO** se aplicam a todo o arquivo. As informações na estrutura **AVISTREAMINFO** são específicas para o fluxo acessado e têm precedência sobre as informações na estrutura **AVIFILEINFO** .

Se um fluxo tiver informações complementares associadas a ele, você poderá recuperar essas informações usando a função [**AVIStreamReadData**](/windows/desktop/api/Vfw/nf-vfw-avistreamreaddata) . Essa função retorna as informações em um buffer fornecido pelo aplicativo. As informações de fluxo suplementares podem incluir definições de configuração para os métodos de compactação e descompactação usados em um fluxo. Você pode obter o tamanho de buffer necessário usando a macro [**AVIStreamDataSize**](/windows/desktop/api/Vfw/nf-vfw-avistreamdatasize) .

Você pode recuperar informações de formatação sobre um fluxo usando a função [**AVIStreamReadFormat**](/windows/desktop/api/Vfw/nf-vfw-avistreamreadformat) . Essa função retorna uma estrutura específica de fluxo em um buffer fornecido pelo aplicativo. Para um fluxo de vídeo, o buffer contém informações de formatação em uma estrutura [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) . Para um fluxo de áudio, o buffer contém informações de formatação em uma estrutura [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) ou [**PCMWAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-pcmwaveformat) . Para outros tipos de fluxo, o manipulador de fluxo retorna informações específicas para o fluxo. Você pode determinar o tamanho do buffer necessário usando **AVIStreamReadFormat** e especificando um endereço de buffer **nulo** ou usando a macro [**AVIStreamFormatSize**](/windows/desktop/api/Vfw/nf-vfw-avistreamformatsize) .

Você pode recuperar o conteúdo multimídia em um fluxo usando a função [**AVIStreamRead**](/windows/desktop/api/Vfw/nf-vfw-avistreamread) . Essa função copia dados brutos do fluxo para um buffer fornecido pelo aplicativo. Para fluxos de vídeo, essa função recupera as imagens de bitmap que compõem o conteúdo do quadro. Para fluxos de áudio, essa função recupera amostras de wave-áudio que compõem o conteúdo do som. Você pode determinar o tamanho do buffer necessário usando **AVIStreamRead** e especificando um endereço de buffer **nulo** ou usando a macro [**AVIStreamSampleSize**](/windows/desktop/api/Vfw/nf-vfw-avistreamsamplesize) .

Alguns manipuladores de fluxo AVI introduzem atrasos associados à inicialização ou à coordenação de software e hardware. Você pode informar esses manipuladores para se preparar para o streaming de dados usando a função [**AVIStreamBeginStreaming**](/windows/desktop/api/Vfw/nf-vfw-avistreambeginstreaming) . Essa função permite que o manipulador de fluxo aloque e inicialize os recursos de que precisa. Para informar esses manipuladores quando o streaming terminar, use a função [**AVIStreamEndStreaming**](/windows/desktop/api/Vfw/nf-vfw-avistreamendstreaming) . Essa função permite que o manipulador de fluxo desaloque os recursos alocados para **AVIStreamBeginStreaming**.

A função [**AVIStreamRead**](/windows/desktop/api/Vfw/nf-vfw-avistreamread) não fornece serviços de descompactação. Para obter informações sobre como compactar e descompactar fluxos de áudio, consulte [Gerenciador de compactação de áudio](audio-compression-manager.md). Para obter informações sobre como compactar e descompactar fluxos de vídeo, consulte [Gerenciador de compactação de vídeo](video-compression-manager.md). Para obter informações sobre como compactar e descompactar quadros individuais em um fluxo de vídeo, consulte [trabalhando com dados de vídeo compactados em um fluxo](working-with-compressed-video-data-in-a-stream.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Operações de fluxo](stream-operations.md)
</dt> </dl>

 

 