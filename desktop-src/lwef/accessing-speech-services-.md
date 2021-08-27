---
title: Acessando os Serviços de Fala (Controle do Microsoft Agent)
description: Saiba mais sobre como acessar serviços de fala com o Controle do Microsoft Agent. O Microsoft Agent foi preterido a partir Windows 7.
ms.assetid: c6c10f2a-a433-4a8e-a069-48e3c2032fb8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 617da522912e2fbae361fb3addf569d5164894fc2b98a901686b2458d4d0a8e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120114936"
---
# <a name="accessing-speech-services-microsoft-agent-control"></a>Acessando os Serviços de Fala (Controle do Microsoft Agent)

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

Embora os serviços do Microsoft Agent incluam suporte para entrada de fala, um mecanismo de reconhecimento de fala de comando e controle compatível deve ser instalado para acessar os serviços de entrada de fala do Agent. Da mesma forma, se você quiser usar os serviços de fala do Microsoft Agent para dar suporte à saída de fala sintetizada para um caractere, deverá instalar um mecanismo de fala TTS (texto em fala) compatível para seu caractere.

Para habilitar o suporte à entrada de fala em seu aplicativo, defina [**um objeto Command**](https://www.bing.com/search?q=**Command**) e defina sua propriedade [**Voice.**](https://www.bing.com/search?q=**Voice**) O Agent carregará automaticamente os serviços de fala, de modo que quando o usuário pressionar a tecla Listening ou você chamar [**Escutar**](https://www.bing.com/search?q=**Listen**), o mecanismo de reconhecimento de fala será carregado. Por padrão, a [**LanguageID**](https://www.bing.com/search?q=**LanguageID**) do caractere determinará qual mecanismo é carregado. O Agent tenta carregar o primeiro mecanismo que o SAPI (Microsoft Speech API) retorna como correspondente a esse idioma. Use [**SRModeID**](https://www.bing.com/search?q=**SRModeID**) se quiser carregar um mecanismo específico.

Para habilitar a saída de texto em fala, use o [**método Speak.**](https://www.bing.com/search?q=**Speak**) O Agent tentará carregar automaticamente um mecanismo que corresponde ao LanguageID do [**caractere.**](https://www.bing.com/search?q=**LanguageID**) Se a definição do caractere incluir uma ID de modo de mecanismo TTS específica e esse mecanismo estiver disponível e corresponde ao **LanguageID** do caractere, o Agent carregará esse mecanismo para o caractere. Se não estiver, ele carregará o primeiro mecanismo TTS que o SAPI retorna como correspondente à configuração de idioma do caractere. Você também pode usar o [**TTSModeID**](https://www.bing.com/search?q=**TTSModeID**) para carregar um mecanismo específico.

Normalmente, o Agent carrega o reconhecimento de fala quando o modo de escuta é iniciado e um mecanismo de texto em fala quando [**o Speak**](https://www.bing.com/search?q=**Speak**) é chamado pela primeira vez. No entanto, se você quiser pré-carregar o mecanismo de fala, consulte as propriedades relacionadas às interfaces de fala. Por exemplo, consultar [**SRModeID**](https://www.bing.com/search?q=**SRModeID**) ou [**TTSModeID**](https://www.bing.com/search?q=**TTSModeID**) tentará carregar esse tipo de mecanismo.

Como os serviços de fala do Microsoft Agent são baseados no Microsoft Speech API, você pode usar todos os mecanismos que deem suporte às interfaces de fala necessárias.

 

 




