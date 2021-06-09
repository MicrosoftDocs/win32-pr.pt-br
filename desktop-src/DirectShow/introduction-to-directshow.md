---
description: Introdução ao DirectShow
ms.assetid: 39a701b3-2633-426f-9733-2172ad3ea372
title: Introdução ao DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5706ff0dec34c5db3762f5782f96804e5c85e889
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/09/2021
ms.locfileid: "111827220"
---
# <a name="introduction-to-directshow"></a>Introdução ao DirectShow

Microsoft® DirectShow® é uma arquitetura para mídia de streaming na plataforma microsoft Windows®. O DirectShow fornece captura de alta qualidade e reprodução de fluxos multimídia. Ele dá suporte a uma ampla variedade de formatos, incluindo ASF (Advanced Systems Format), MPEG (Motion Picture Experts Group), Audio-Video INTERleaved (AVI), MPEG Audio Layer-3 (MP3) e arquivos de som WAV. Ele dá suporte à captura de dispositivos digitais e análogos com base Windows Driver Model (WDM) ou Vídeo para Windows. Ele detecta e usa automaticamente o hardware de aceleração de áudio e vídeo quando disponível, mas também dá suporte a sistemas sem hardware de aceleração.

O DirectShow é baseado no COM (Component Object Model). Para escrever um aplicativo ou componente do DirectShow, você deve entender a programação do cliente COM. Para a maioria dos aplicativos, você não precisa implementar seus próprios objetos COM. O DirectShow fornece os componentes necessários. No entanto, se você quiser estender o DirectShow escrevendo seus próprios componentes, deverá implementá-los como objetos COM.

O DirectShow foi projetado para C++. A Microsoft não fornece uma API gerenciada para o DirectShow.

O DirectShow simplifica as tarefas de reprodução de mídia, conversão de formato e captura. Ao mesmo tempo, ele fornece acesso à arquitetura de controle de fluxo subjacente para aplicativos que exigem soluções personalizadas. Você também pode criar seus próprios componentes do DirectShow para dar suporte a novos formatos ou efeitos personalizados.

Exemplos dos tipos de aplicativo que você pode escrever com o DirectShow incluem players de arquivos, players de TV e DVD, aplicativos de edição de vídeo, conversores de formato de arquivo, aplicativos de captura de áudio e vídeo, codificadores e decodificadores, processadores de sinal digital e muito mais.

Esta seção contém os seguintes tópicos:

-   [Novidades no DirectShow](whats-new-in-directshow.md)
-   [Formatos com suporte no DirectShow](supported-formats-in-directshow.md)
-   [Perguntas frequentes sobre o DirectShow](directshow-faq.yml)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Introdução](getting-started.md)
</dt> <dt>

[Usando o DirectShow](using-directshow.md)
</dt> </dl>

 

 



