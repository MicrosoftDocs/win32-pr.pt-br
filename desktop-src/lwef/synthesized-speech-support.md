---
title: Suporte a fala sintetizada
description: Suporte a fala sintetizada
ms.assetid: 38172e04-a5b6-41e4-9d7c-539d9d4117be
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c31fcb655ccb5a8fbb2ffbbb8d01d1da317209fbfa3e270a76d92208c06777df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118475318"
---
# <a name="synthesized-speech-support"></a>Suporte a fala sintetizada

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

Se você usar fala sintetizada, seu caractere terá a capacidade de dizer quase tudo, o que fornece a maior flexibilidade. Com o áudio gravado, você pode dar ao caractere uma voz específica ou exclusiva. Para especificar a saída, forneça o texto falado como um parâmetro do [**método Speak.**](speak-method.md)

Como a arquitetura do Microsoft Agent usa o Microsoft SAPI para saída de fala sintetizada, você pode usar qualquer mecanismo que esteja em conformidade com essa especificação e dá suporte à saída do IPA (Alfabeto Fonético Internacional) usando o método [**Visual**](https://www.bing.com/search?q=**Visual**) da interface [**ITTSNotifySinkW.**](ittsnotifysinkw.md) Para obter mais informações sobre o mecanismo necessário, consulte [Requisitos de suporte do Mecanismo de Fala](requirements-for-text-to-speech-engines.md).

A configuração de ID de idioma de um caractere determina sua saída do TTS. Se um cliente não especificar uma ID de idioma para o caractere, a ID de idioma do caractere será definida como a ID de idioma padrão do usuário. Se a definição do caractere incluir um mecanismo específico e esse mecanismo puder ser carregado e ele corresponde à configuração de idioma do caractere, esse mecanismo será usado. Caso contrário, o Microsoft Agent enumera os outros mecanismos disponíveis e solicita uma melhor combinação de SAPI com base em idioma, gênero e idade (nessa ordem). Se não houver nenhum mecanismo correspondente disponível, não haverá nenhuma saída TTS para o uso do caractere pelo cliente. O Agent tenta carregar o mecanismo TTS na primeira chamada [**speak**](speak-method.md) ou ao consultar ou definir com êxito sua ID de modo.

Um aplicativo cliente também pode especificar um mecanismo TTS para seu caractere (usando a [**propriedade TTSModeID).**](ttsmodeid-property.md) Isso substitui a tentativa do servidor de encontrar automaticamente um mecanismo correspondente com base na ID de modo TTS preferencial do caractere ou na configuração de ID de idioma atual do caractere. No entanto, se esse mecanismo não estiver instalado (ou não puder ser carregado de outra forma), a chamada falhará (e gera um erro no controle ). Em seguida, o servidor tenta carregar outro mecanismo com base na ID da linguagem, na configuração de TTS de caractere compilado e nos mecanismos TTS disponíveis. Se ainda não houver nenhuma combinação, o TTS não estará disponível para esse cliente, mas o caractere ainda poderá falar em seu balão de palavra.

Somente os mecanismos TTS em uso por qualquer cliente permanecem carregados. Por exemplo, se um caractere tiver uma preferência definida para um mecanismo específico e esse mecanismo estiver disponível, mas seu aplicativo cliente tiver especificado um mecanismo diferente (definindo a ID de idioma de um caractere de forma diferente do mecanismo ou especificando uma ID de modo diferente), somente o mecanismo especificado pelo aplicativo permanecerá carregado. O mecanismo que corresponde à preferência definida do caractere para uma configuração de TTS é descarregado (a menos que outro cliente esteja usando a configuração do mecanismo compilado do caractere).

 

 




