---
description: Introdução ao DirectShow
ms.assetid: 39a701b3-2633-426f-9733-2172ad3ea372
title: Introdução ao DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51cd4dc2a75233c519c4ca3d5db213451b097c0528ab782109da611b6e35aca7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952575"
---
# <a name="introduction-to-directshow"></a>Introdução ao DirectShow

o microsoft® DirectShow® é uma arquitetura para streaming de mídia na plataforma Microsoft Windows®. o DirectShow fornece a captura de alta qualidade e a reprodução de fluxos de multimídia. Ele dá suporte a uma ampla variedade de formatos, incluindo ASF (Advanced System Format), MPEG (Motion Picture Experts Group), Audio-Video intercalado (AVI), MPEG Audio Layer-3 (MP3) e arquivos de som WAV. ele dá suporte à captura de dispositivos digitais e analógicos com base no Windows Driver Model (WDM) ou vídeo para Windows. Ele detecta e usa automaticamente o hardware de aceleração de vídeo e áudio quando disponível, mas também oferece suporte a sistemas sem aceleração de hardware.

o DirectShow é baseado no Component Object Model (com). para escrever um aplicativo ou componente DirectShow, você deve entender a programação de cliente COM. Para a maioria dos aplicativos, você não precisa implementar seus próprios objetos COM. DirectShow fornece os componentes de que você precisa. no entanto, se você quiser estender DirectShow escrevendo seus próprios componentes, você deve implementá-los como objetos COM.

DirectShow é projetado para C++. A Microsoft não fornece uma API gerenciada para DirectShow.

DirectShow simplifica a reprodução de mídia, a conversão de formato e as tarefas de captura. Ao mesmo tempo, ele fornece acesso à arquitetura de controle de fluxo subjacente para aplicativos que exigem soluções personalizadas. você também pode criar seus próprios componentes DirectShow para dar suporte a novos formatos ou efeitos personalizados.

exemplos dos tipos de aplicativo que você pode escrever com DirectShow incluem players de arquivos, TV e players de DVD, aplicativos de edição de vídeo, conversores de formato de arquivo, aplicativos de captura de vídeo de áudio, codificadores e decodificadores, processadores de sinal digital e muito mais.

Esta seção contém os seguintes tópicos:

-   [O que há de novo no DirectShow](whats-new-in-directshow.md)
-   [Formatos com suporte no DirectShow](supported-formats-in-directshow.md)
-   [DirectShow PERGUNTAS FREQÜENTES](directshow-faq.yml)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Introdução](getting-started.md)
</dt> <dt>

[Usando DirectShow](using-directshow.md)
</dt> </dl>

 

 



