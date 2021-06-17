---
title: Acessando serviços de fala (controle do Microsoft Agent)
description: Saiba mais sobre como acessar os serviços de fala com o controle do Microsoft Agent. O Microsoft Agent foi preterido a partir do Windows 7.
ms.assetid: c6c10f2a-a433-4a8e-a069-48e3c2032fb8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 035bde03d18b77ce43c47375f2075bba02416c39
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262708"
---
# <a name="accessing-speech-services-microsoft-agent-control"></a>Acessando serviços de fala (controle do Microsoft Agent)

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

Embora os serviços do Microsoft Agent incluam suporte para entrada de fala, um mecanismo de reconhecimento de fala de comando e controle compatível deve ser instalado para acessar os serviços de entrada de fala do agente. Da mesma forma, se você quiser usar os serviços de fala do Microsoft Agent para dar suporte à saída de fala sintetizada para um caractere, deverá instalar um mecanismo de fala compatível com conversão de texto em fala (TTS) para seu caractere.

Para habilitar o suporte de entrada de fala em seu aplicativo, defina um objeto de [**comando**](https://www.bing.com/search?q=**Command**) e defina sua propriedade de [**voz**](https://www.bing.com/search?q=**Voice**) . O Agent carregará automaticamente os serviços de fala, de modo que quando o usuário pressionar a tecla de escuta ou chamar [**Listen**](https://www.bing.com/search?q=**Listen**), o mecanismo de reconhecimento de fala será carregado. Por padrão, o [**LanguageID**](https://www.bing.com/search?q=**LanguageID**) do caractere determinará qual mecanismo está carregado. O Agent tenta carregar o primeiro mecanismo que o SAPI (Microsoft Speech API) retorna como correspondente a esse idioma. Use [**SRModeID**](https://www.bing.com/search?q=**SRModeID**) se você quiser carregar um mecanismo específico.

Para habilitar a saída de conversão de texto em fala, use o método [**Speak**](https://www.bing.com/search?q=**Speak**) . O Agent tentará automaticamente carregar um mecanismo que corresponda à [**LanguageID**](https://www.bing.com/search?q=**LanguageID**)do caractere. Se a definição do caractere incluir uma ID de modo de mecanismo TTS específica e esse mecanismo estiver disponível e corresponder à **LanguageID** do caractere, o Agent carregará esse mecanismo para o caractere. Se não estiver, ele carregará o primeiro mecanismo de TTS que o SAPI retorna como correspondente à configuração de idioma do caractere. Você também pode usar o [**TTSModeID**](https://www.bing.com/search?q=**TTSModeID**) para carregar um mecanismo específico.

Normalmente, o Agent carrega o reconhecimento de fala quando o modo de escuta é iniciado e um mecanismo de conversão de texto em fala quando a [**fala**](https://www.bing.com/search?q=**Speak**) é chamada pela primeira vez. No entanto, se você quiser pré-carregar o mecanismo de fala, consulte as propriedades relacionadas às interfaces de fala. Por exemplo, consultar [**SRModeID**](https://www.bing.com/search?q=**SRModeID**) ou [**TTSModeID**](https://www.bing.com/search?q=**TTSModeID**) tentará carregar esse tipo de mecanismo.

Como os serviços de fala do Microsoft Agent são baseados no Microsoft Speech API, você pode usar qualquer mecanismo que ofereça suporte às interfaces de fala necessárias.

 

 




