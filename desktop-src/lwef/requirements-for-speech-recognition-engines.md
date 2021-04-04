---
title: Requisitos para mecanismos de reconhecimento de fala
description: Requisitos para mecanismos de reconhecimento de fala
ms.assetid: 41aca5da-c680-41c1-b070-af291cb0c8e1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9214f13b11a071ec8d8599f0b6dd542884ae05f8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916523"
---
# <a name="requirements-for-speech-recognition-engines"></a><span data-ttu-id="44121-103">Requisitos para mecanismos de reconhecimento de fala</span><span class="sxs-lookup"><span data-stu-id="44121-103">Requirements for Speech Recognition Engines</span></span>

<span data-ttu-id="44121-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="44121-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="44121-105">Um mecanismo de reconhecimento de fala também deve ser um mecanismo de comando e controle (C&C) totalmente compatível de acordo com o SAPI 4,0.</span><span class="sxs-lookup"><span data-stu-id="44121-105">A speech recognition engine must also be a fully compliant Command and Control (C&C) engine according to SAPI 4.0.</span></span> <span data-ttu-id="44121-106">Ele deve dar suporte a várias gramáticas no formato binário descrito na especificação e permitir que essas gramáticas sejam ativadas ou desativadas em tempo real.</span><span class="sxs-lookup"><span data-stu-id="44121-106">It must support multiple grammars in the binary format described in the specification and allow those grammars to be activated or deactivated in real time.</span></span>

<span data-ttu-id="44121-107">Observe que o SAPI 4,0 exige que os mecanismos de reconhecimento de fala ofereçam suporte ao caractere largo, interfaces Unicode.</span><span class="sxs-lookup"><span data-stu-id="44121-107">Note that SAPI 4.0 requires that speech recognition engines support the wide character, Unicode interfaces.</span></span> <span data-ttu-id="44121-108">No entanto, no suporte a essas interfaces, o mecanismo não deve depender da conversão de dados Unicode para ANSI, pois o mecanismo pode não funcionar corretamente em alguns sistemas.</span><span class="sxs-lookup"><span data-stu-id="44121-108">However, in supporting these interfaces, the engine should not depend on converting Unicode data to ANSI, as the engine may not function correctly on some systems.</span></span> <span data-ttu-id="44121-109">Por exemplo, um mecanismo japonês que converte Unicode em ANSI pode não funcionar em um sistema em inglês do Microsoft Windows 95.</span><span class="sxs-lookup"><span data-stu-id="44121-109">For example, a Japanese engine that converts Unicode to ANSI may not work on an English-language Microsoft Windows 95 system.</span></span>

<span data-ttu-id="44121-110">Além disso, para ser considerado compatível com o Microsoft Agent, o mecanismo deve retornar objetos de resultados após o reconhecimento bem-sucedido de uma frase (por meio de ISRGramNotifySinkW::P hraseFinish).</span><span class="sxs-lookup"><span data-stu-id="44121-110">In addition, to be considered Microsoft Agent-compliant, the engine must return results objects upon the successful recognition of a phrase (through ISRGramNotifySinkW::PhraseFinish).</span></span> <span data-ttu-id="44121-111">Esses objetos de resultados devem dar suporte a ISRResBasic, conforme a especificação exige.</span><span class="sxs-lookup"><span data-stu-id="44121-111">These results objects must support ISRResBasic, as the specification requires.</span></span> <span data-ttu-id="44121-112">Além disso, eles devem dar suporte a ISRResScore.</span><span class="sxs-lookup"><span data-stu-id="44121-112">In addition, they should support ISRResScore.</span></span> <span data-ttu-id="44121-113">Embora o Microsoft Agent seja executado com um mecanismo que dá suporte apenas a ISRResBasic, ou mesmo com um mecanismo que não retorna nenhum objeto de resultados, o desempenho geralmente será significativamente mais fraco com esses mecanismos.</span><span class="sxs-lookup"><span data-stu-id="44121-113">Although Microsoft Agent will run with an engine that supports only ISRResBasic, or even with an engine that returns no results objects whatsoever, performance will usually be significantly poorer with such engines.</span></span> <span data-ttu-id="44121-114">Muitos aplicativos usam os valores de confiança fornecidos pelo mecanismo para controlar como eles respondem a vários comandos.</span><span class="sxs-lookup"><span data-stu-id="44121-114">Many applications use the confidence values provided by the engine to control how they respond to various commands.</span></span>

 

 




