---
title: Normalização de texto em mecanismos de conversão de texto em fala
description: Normalização de texto em mecanismos de conversão de texto em fala
ms.assetid: 1974d47b-4877-47e3-89d8-fd70967e7605
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb7bda7cb8041e31ef8e741df4d3f5d807610f1f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105765771"
---
# <a name="text-to-speech-engines-text-normalization"></a>Normalização de texto em mecanismos de conversão de texto em fala

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

A normalização é o processo de identificar números, abreviações, acrônimos e idiomatics e transformá-los em texto completo conforme necessário, geralmente com base no contexto da sentença.

Por exemplo, usando o mecanismo de TTS L&H TruVoice American Inglês, a frase:

King George VI da Inglaterra morreu em 6 de fevereiro de 1952.

será lido no **contexto normal** como:

   King George V I da Inglaterra, morreu em seis de fevereiro de 19 52.

Mas, em **contexto de email**, ele será lido como:

   King George The sexta-Inglaterra, morreu em sexto de fevereiro de 19 52.

Informações sobre como usar a marca de fala de **contexto** podem ser encontradas na documentação de programação do agente [marcas de saída de fala do Microsoft Agent](microsoft-agent-speech-output-tags.md).

 

 




