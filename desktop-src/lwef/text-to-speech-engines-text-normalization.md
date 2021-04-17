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
# <a name="text-to-speech-engines-text-normalization"></a><span data-ttu-id="bd9ce-103">Normalização de texto em mecanismos de conversão de texto em fala</span><span class="sxs-lookup"><span data-stu-id="bd9ce-103">Text-to-Speech Engines Text Normalization</span></span>

<span data-ttu-id="bd9ce-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="bd9ce-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="bd9ce-105">A normalização é o processo de identificar números, abreviações, acrônimos e idiomatics e transformá-los em texto completo conforme necessário, geralmente com base no contexto da sentença.</span><span class="sxs-lookup"><span data-stu-id="bd9ce-105">Normalization is the process of identifying numbers, abbreviations, acronyms and idiomatics and transforming them into full text as needed, usually based on the context of the sentence.</span></span>

<span data-ttu-id="bd9ce-106">Por exemplo, usando o mecanismo de TTS L&H TruVoice American Inglês, a frase:</span><span class="sxs-lookup"><span data-stu-id="bd9ce-106">For example, using the L&H TruVoice American English TTS Engine, the sentence:</span></span>

<span data-ttu-id="bd9ce-107">King George VI da Inglaterra morreu em 6 de fevereiro de 1952.</span><span class="sxs-lookup"><span data-stu-id="bd9ce-107">King George VI of England died on Feb 6, 1952.</span></span>

<span data-ttu-id="bd9ce-108">será lido no **contexto normal** como:</span><span class="sxs-lookup"><span data-stu-id="bd9ce-108">will be read under **normal context** as:</span></span>

   <span data-ttu-id="bd9ce-109">King George V I da Inglaterra, morreu em seis de fevereiro de 19 52.</span><span class="sxs-lookup"><span data-stu-id="bd9ce-109">King George V I of England, died on February six, nineteen fifty-two.</span></span>

<span data-ttu-id="bd9ce-110">Mas, em **contexto de email**, ele será lido como:</span><span class="sxs-lookup"><span data-stu-id="bd9ce-110">But under **E-mail context**, it will be read as:</span></span>

   <span data-ttu-id="bd9ce-111">King George The sexta-Inglaterra, morreu em sexto de fevereiro de 19 52.</span><span class="sxs-lookup"><span data-stu-id="bd9ce-111">King George the sixth of England, died on February sixth, nineteen fifty-two.</span></span>

<span data-ttu-id="bd9ce-112">Informações sobre como usar a marca de fala de **contexto** podem ser encontradas na documentação de programação do agente [marcas de saída de fala do Microsoft Agent](microsoft-agent-speech-output-tags.md).</span><span class="sxs-lookup"><span data-stu-id="bd9ce-112">Information about using the **Context** speech tag can be found in the Agent programming documentation [Microsoft Agent Speech Output Tags](microsoft-agent-speech-output-tags.md).</span></span>

 

 




