---
description: Introdução ao DirectShow
ms.assetid: 39a701b3-2633-426f-9733-2172ad3ea372
title: Introdução ao DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01733db5f8168a67871ec1797f79cd10a90c6c22
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087550"
---
# <a name="introduction-to-directshow"></a>Introdução ao DirectShow

O Microsoft® DirectShow® é uma arquitetura para streaming de mídia na plataforma Microsoft Windows®. O DirectShow fornece captura de alta qualidade e reprodução de fluxos de multimídia. Ele dá suporte a uma ampla variedade de formatos, incluindo ASF (Advanced System Format), MPEG (Motion Picture Experts Group), Audio-Video intercalado (AVI), MPEG Audio Layer-3 (MP3) e arquivos de som WAV. Ele dá suporte à captura de dispositivos digitais e analógicos com base no Windows Driver Model (WDM) ou vídeo para Windows. Ele detecta e usa automaticamente o hardware de aceleração de vídeo e áudio quando disponível, mas também oferece suporte a sistemas sem aceleração de hardware.

O DirectShow é baseado na Component Object Model (COM). Para escrever um aplicativo ou componente do DirectShow, você deve entender a programação de cliente COM. Para a maioria dos aplicativos, você não precisa implementar seus próprios objetos COM. O DirectShow fornece os componentes de que você precisa. No entanto, se você quiser estender o DirectShow escrevendo seus próprios componentes, você deve implementá-los como objetos COM.

O DirectShow foi projetado para C++. A Microsoft não fornece uma API gerenciada para o DirectShow.

O DirectShow simplifica a reprodução de mídia, a conversão de formato e as tarefas de captura. Ao mesmo tempo, ele fornece acesso à arquitetura de controle de fluxo subjacente para aplicativos que exigem soluções personalizadas. Você também pode criar seus próprios componentes do DirectShow para dar suporte a novos formatos ou efeitos personalizados.

Exemplos dos tipos de aplicativo que você pode escrever com o DirectShow incluem players de arquivos, TV e DVD players, aplicativos de edição de vídeo, conversores de formato de arquivo, aplicativos de captura de vídeo de áudio, codificadores e decodificadores, processadores de sinais digitais e muito mais.

Esta seção contém os seguintes tópicos:

-   [O que há de novo no DirectShow](whats-new-in-directshow.md)
-   [Formatos com suporte no DirectShow](supported-formats-in-directshow.md)
-   [Perguntas frequentes do DirectShow](directshow-faq.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Introdução](getting-started.md)
</dt> <dt>

[Usando o DirectShow](using-directshow.md)
</dt> </dl>

 

 



