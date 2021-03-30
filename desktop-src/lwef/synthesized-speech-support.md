---
title: Suporte a fala sintetizado
description: Suporte a fala sintetizado
ms.assetid: 38172e04-a5b6-41e4-9d7c-539d9d4117be
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8a89610a912cf601724bc9a2153cba8343e6feb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005493"
---
# <a name="synthesized-speech-support"></a>Suporte a fala sintetizado

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

Se você usar a fala sintetizada, seu caractere terá a capacidade de dizer quase tudo, o que fornece a maior flexibilidade. Com o áudio gravado, você pode dar ao caractere uma voz específica ou exclusiva. Para especificar a saída, forneça o texto falado como um parâmetro do método [**Speak**](speak-method.md) .

Como a arquitetura do Microsoft Agent usa o Microsoft SAPI para saída de fala sintetizada, você pode usar qualquer mecanismo que esteja em conformidade com essa especificação e dá suporte à saída do alfabeto fonético internacional (IPA) usando o método [**Visual**](https://www.bing.com/search?q=**Visual**) da interface [**ITTSNotifySinkW**](ittsnotifysinkw.md) . Para obter mais informações sobre o mecanismo necessário, consulte [requisitos de suporte do mecanismo de fala](requirements-for-text-to-speech-engines.md).

A configuração de ID de idioma de um caractere determina sua saída de TTS. Se um cliente não especificar uma ID de idioma para o caractere, a ID de idioma do caractere será definida como a ID de idioma padrão do usuário. Se a definição do caractere incluir um mecanismo específico e esse mecanismo puder ser carregado e corresponder à configuração de idioma do caractere, esse mecanismo será usado. Caso contrário, o Microsoft Agent enumera os outros mecanismos disponíveis e solicita uma melhor correspondência SAPI com base no idioma, sexo e idade (nessa ordem). Se não houver nenhum mecanismo correspondente disponível, não haverá nenhuma saída de TTS para o uso desse cliente do caractere. O Agent tenta carregar o mecanismo de TTS na primeira chamada de [**fala**](speak-method.md) ou quando você consulta ou define com êxito sua ID de modo.

Um aplicativo cliente também pode especificar um mecanismo de TTS para seu caractere (usando a propriedade [**TTSModeID**](ttsmodeid-property.md) ). Isso substitui a tentativa do servidor de localizar automaticamente um mecanismo de correspondência com base na ID do modo TTS preferencial do caractere ou na configuração da ID de idioma atual do caractere. No entanto, se esse mecanismo não estiver instalado (ou não puder ser carregado de outra forma), a chamada falhará (e gerará um erro no controle). Em seguida, o servidor tenta carregar outro mecanismo com base na ID do idioma, na configuração de TTS do caractere compilado e nos mecanismos de TTS disponíveis. Se ainda não houver correspondência, a TTS não estará disponível para esse cliente, mas o caractere ainda poderá falar em seu balão de palavra.

Somente os mecanismos de TTS em uso por qualquer cliente permanecem carregados. Por exemplo, se um caractere tiver uma preferência definida para um mecanismo específico e esse mecanismo estiver disponível, mas o aplicativo cliente tiver especificado um mecanismo diferente (definindo a ID de idioma de um caractere diferentemente do mecanismo ou especificando uma ID de modo diferente), somente o mecanismo especificado pelo seu aplicativo permanecerá carregado. O mecanismo que corresponde à preferência definida pelo caractere para uma configuração de TTS é descarregado (a menos que outro cliente esteja usando a configuração do mecanismo compilado do caractere).

 

 




