---
title: Como funciona o Gerenciador de Compactação de Áudio
description: Como funciona o Gerenciador de Compactação de Áudio
ms.assetid: 7f1c3f21-262f-42a1-b9f7-069fb13b9d8f
keywords:
- audio multimídia, gerenciador de compactação de áudio (ACM)
- audio, gerenciador de compactação de áudio (ACM)
- gerenciador de compactação de áudio (ACM), sobre
- ACM (gerenciador de compactação de áudio),sobre
- gerenciador de compactação de áudio (ACM), drivers codec
- ACM (gerenciador de compactação de áudio), drivers codec
- gerenciador de compactação de áudio (ACM), drivers de conversor de formato
- ACM (gerenciador de compactação de áudio), drivers de conversor de formato
- gerenciador de compactação de áudio (ACM), drivers de filtro
- ACM (gerenciador de compactação de áudio), drivers de filtro
- gerenciador de compactação de áudio (ACM), drivers de drivers de drivers
- ACM (gerenciador de compactação de áudio), drivers de drivers de drivers
- gerenciador de compactação de áudio (ACM), drivers descompactador
- ACM (gerenciador de compactação de áudio), drivers descompactador
- drivers codec
- drivers de conversor de formato
- drivers de filtro
- drivers de drivers de drivers
- drivers descompactador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bacb3d94feee3da290bf9c1cc90cab92f2aade083effd8a01cb17906c22e0f4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118140991"
---
# <a name="how-the-audio-compression-manager-works"></a>Como funciona o Gerenciador de Compactação de Áudio

O ACM usa ganchos de interface de driver existentes para substituir o algoritmo de mapeamento padrão para dispositivos waveform-audio. Isso permite que o ACM intercepte chamadas abertas do dispositivo. Depois que uma chamada é interceptada, o ACM pode executar uma variedade de tarefas para processar os dados de áudio, como inserir um grupo externo ou descompactador na sequência.

O ACM gerencia os seguintes tipos de drivers:

-   Drivers Descompactador e Descompactador (codec)
-   Drivers de conversor de formato
-   Filtrar drivers

Os descompactores e os descompactores alteram um tipo de formato para outro. Por exemplo, um grupo ou descompactador pode alterar um arquivo PCM (Pulse Code Modulartion) para um arquivo ADPCM (Modularidade de Código de Pulso Diferencial Adaptável). Os conversores de formato alteram o formato, mas não o tipo de dados. Por exemplo, um conversor pode alterar dados de 44 kHz de 16 bits para dados de 44 kHz e 8 bits. Os filtros não alteram o formato de dados, mas alteram os dados waveform-audio de alguma maneira. Por exemplo, um filtro pode combinar um fluxo de dados e um eco de si mesmo. Um único driver ACM, ou uma marca de filtro ou marca de formato em um driver, também pode dar suporte a combinações dos tipos anteriores.

Para a saída waveform-audio, o ACM passa cada buffer de dados para o conversor conforme ele chega. O conversor descompacta os dados e retorna os dados descompactados para o ACM em um buffer de "sombra". Em seguida, o ACM passa o buffer de sombra descompactado para o driver waveform-audio. O ACM aloca os buffers de sombra sempre que recebe uma mensagem de preparação.

Para a entrada waveform-audio, o ACM passa buffers de sombra vazios para o driver. Ele usa uma tarefa em segundo plano para receber uma notificação depois que o driver tiver preenchido o buffer de sombra. Em seguida, o ACM passa os buffers para o driver para compactação. Após a compactação ser concluída, o driver passa os dados para o aplicativo.

 

 




