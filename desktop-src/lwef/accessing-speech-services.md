---
title: Acessando os serviços de fala (interface do servidor do Microsoft Agent)
description: Acessando serviços de fala
ms.assetid: 99cf630d-3bd1-403a-833a-9173a84fe3c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9eeb4afb2b05ca13c52d49508c3c25b7e02da676
ms.sourcegitcommit: 59ec383331366f8a62c94bb88468ca03e95c43f8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/13/2021
ms.locfileid: "107380800"
---
# <a name="accessing-speech-services-microsoft-agent-server-interface"></a>Acessando os serviços de fala (interface do servidor do Microsoft Agent)

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

Embora os serviços do Microsoft Agent incluam suporte para entrada de fala, um mecanismo de reconhecimento de fala de comando e controle compatível deve ser instalado para acessar os serviços de entrada de fala do agente. Da mesma forma, se você quiser usar os serviços de fala do Microsoft Agent para dar suporte à saída de fala sintetizada para um caractere, deverá instalar um mecanismo de fala compatível com conversão de texto em fala (TTS) para seu caractere. Como os serviços de fala do Microsoft Agent se baseiam no Microsoft Speech API (SAPI), você pode usar qualquer mecanismo que dos suporte às interfaces de fala necessárias.

Para habilitar o suporte de entrada de fala em seu aplicativo, defina um objeto de [**comando**](https://www.bing.com/search?q=**Command**) e defina sua propriedade de [**voz**](https://www.bing.com/search?q=**Voice**) . O Microsoft Agent carregará automaticamente os serviços de fala, de modo que quando o usuário pressionar a tecla de escuta ou chamar [**Listen**](https://www.bing.com/search?q=**Listen**), o mecanismo de reconhecimento de fala será carregado. Por padrão, a ID de idioma do caractere determinará qual mecanismo está carregado. O Agent tenta carregar o primeiro mecanismo que o SAPI retorna como correspondente a esse idioma. Use **IAgentCharacterEx:: SetSRModeID** se você quiser carregar um mecanismo específico.

Para habilitar a saída de conversão de texto em fala, use o método [**Speak**](https://www.bing.com/search?q=**Speak**) . O Microsoft Agent tentará automaticamente carregar um mecanismo que corresponda à ID de idioma do caractere. Se a definição do caractere incluir uma ID de modo de mecanismo TTS específica e esse mecanismo estiver disponível e corresponder à ID de idioma do caractere, o Agent carregará esse mecanismo para o caractere. Caso contrário, o Agent carrega o primeiro mecanismo de TTS que o SAPI retorna como correspondente à configuração de idioma do caractere. Você também pode usar **IAgentCharacterEx:: SetTTSModeID** para carregar um mecanismo específico.

Normalmente, o Microsoft Agent carrega um mecanismo de reconhecimento de fala quando o modo de escuta é iniciado e carrega um mecanismo de conversão de texto em fala quando a [**fala**](https://www.bing.com/search?q=**Speak**) é chamada pela primeira vez. No entanto, se você quiser pré-carregar o mecanismo de fala, poderá fazer isso consultando as propriedades relacionadas às interfaces de fala. Por exemplo, chamar **IAgentCharacterEx:: GetSRModeID** ou **IAgentCharacterEx:: GetTTSModeID** tentará carregar esse tipo de mecanismo.

 

 




