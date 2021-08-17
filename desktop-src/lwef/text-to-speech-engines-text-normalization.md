---
title: Normalização de texto em mecanismos de conversão de texto em fala
description: Normalização de texto em mecanismos de conversão de texto em fala
ms.assetid: 1974d47b-4877-47e3-89d8-fd70967e7605
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cd195212d52d9107aa8112c156bfd8dd6b33d00d2161bec624d182f0f12f78e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119347916"
---
# <a name="text-to-speech-engines-text-normalization"></a>Normalização de texto em mecanismos de conversão de texto em fala

\[o Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

A normalização é o processo de identificar números, abreviações, acrônimos e idiomatics e transformá-los em texto completo conforme necessário, geralmente com base no contexto da sentença.

Por exemplo, usando o mecanismo de TTS L&H TruVoice American Inglês, a frase:

King George VI da Inglaterra morreu em 6 de fevereiro de 1952.

será lido no **contexto normal** como:

   King George V I da Inglaterra, morreu em seis de fevereiro de 19 52.

Mas, em **contexto de email**, ele será lido como:

   King George The sexta-Inglaterra, morreu em sexto de fevereiro de 19 52.

Informações sobre como usar a marca de fala de **contexto** podem ser encontradas na documentação de programação do agente [marcas de saída de fala do Microsoft Agent](microsoft-agent-speech-output-tags.md).

 

 




