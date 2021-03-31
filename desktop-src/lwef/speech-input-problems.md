---
title: Problemas de entrada de fala
description: Problemas de entrada de fala
ms.assetid: b42664a2-9615-4e15-97a6-115e9556096b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a7b29a85c79996eb0c01260c8e2b738fcd926f2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916167"
---
# <a name="speech-input-problems"></a>Problemas de entrada de fala

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

### <a name="the-character-does-not-respond-to-my-spoken-input"></a>O caractere não responde à minha entrada falada.

Esse sintoma pode ser causado por vários problemas. Tente o seguinte para isolar o problema:

-   Verifique se o microfone está conectado corretamente. É uma boa ideia testá-lo com outro aplicativo de entrada de som para garantir que ele funcione corretamente.
-   Verifique se um mecanismo de fala compatível está instalado. Em Windows 95, Windows 98 e Windows NT 4,0, abra o painel de controle. Se você encontrar o objeto de fala, abra-o e ele listará os mecanismos de fala disponíveis e instalados no sistema.
-   Verifique se a placa de som é compatível com o Microsoft Windows 95, Windows 98 ou Windows NT.

    A melhor maneira de fazer isso é executar o aplicativo de gravador de som que vem com o Windows. Em geral, ele pode ser encontrado no menu iniciar. Clique no botão Iniciar, em programas, em acessórios, em multimídia e em gravador de som. Quando a janela gravador de som for exibida, clique no botão **gravar** e fale com o microfone. A linha na janela deve ser animada em resposta à entrada de voz.

    Se o aplicativo gravador de som não funcionar no seu sistema, entre em contato com o departamento de suporte técnico do fabricante da placa de som para obter assistência. Sua placa de som pode não ser compatível com o Windows ou pode haver um problema com os drivers de software para a placa de som.

-   Verifique se a entrada de som para entrada de fala está definida corretamente.
    1.  Abra o objeto de entrada de fala no painel de controle. Se o objeto de fala não estiver presente, instale um.
    2.  Selecione o mecanismo de entrada de fala que você instalou.
    3.  Escolha o botão Assistente de configurações de microfone. Se esse botão aparecer desabilitado, um mecanismo de fala compatível não será instalado ou o mecanismo de fala que você instalou poderá não dar suporte ao ajuste automático.
-   Verifique se o aplicativo habilitado para agente ou a página da Web dá suporte à entrada de fala. Nem todas as páginas (ou aplicativos) dão suporte à entrada de fala. Pressione e segure a tecla de escuta. Normalmente, essa será a chave de bloqueio de rolagem, a menos que você a tenha alterado. Uma janela pop-up deve aparecer sob o caractere. O texto na dica informará o estado de escuta do caractere. Se nenhuma gorjeta for exibida, o aplicativo ou a página da Web não oferece suporte à entrada de fala ou você não tem um mecanismo de fala compatível instalado. Se a dica aparecer e indicar que o caractere está escutando, fale um dos comandos de voz do caractere. Se você não souber quais comandos de voz estão disponíveis, libere a chave de escuta e clique com o botão direito do mouse no caractere. Em seguida, escolha abrir janela de comandos de voz no menu pop-up. Se o comando não for exibido, o suporte a fala não estará disponível para o aplicativo ou a página da Web que você está usando. Se ele for exibido, pressione e segure a tecla de escuta novamente. Se a dica de escuta aparecer abaixo do caractere e indicar que o caractere está escutando, fale um dos comandos listados na janela. Se o caractere não responder, vá para a próxima etapa.
-   Verifique se nenhum outro aplicativo está usando o dispositivo de saída de áudio no momento.
-   Verifique se o uso do MIDI do Microsoft Agent não está bloqueando o canal de áudio (consulte [aplicativos que executam MIDI sem saída de áudio quando o Microsoft Agent está em execução](output-problems.md)"na seção problemas de saída).
-   Se você seguiu as etapas acima, mas ainda tiver problemas com a entrada de fala, verifique se a placa de som e o software do driver são compatíveis com o mecanismo de fala que você está usando. Verifique com o suporte técnico de sua placa de som e seu fabricante de mecanismo de fala.

### <a name="the-midi-tone-seems-to-disrupts-speech-input"></a>O tom de MIDI parece interromper a entrada de fala.

Reduza o volume MIDI usando as etapas a seguir.

1.  Abra a janela de controle de volume clicando com o botão direito do mouse no ícone do orador na barra de tarefas ou abrindo o objeto multimídia no painel de controle. Clique no botão volume na seção reprodução da página áudio.
2.  Diminua o volume de MIDI movendo o controle deslizante para baixo.

### <a name="the-character-does-not-respond-to-voice-input-but-i-can-hear-my-voice-through-my-speakers-when-i-talk-into-my-microphone"></a>O caractere não responde à entrada de voz, mas posso ouvir minha voz por meio de meus alto-falantes quando falo com meu microfone.

Sua placa de som não está configurada corretamente para uso com o Microsoft Agent. Escolha o assistente de configurações de microfone na folha de propriedades do objeto de fala no painel de controle. Consulte as etapas para "[o caractere não responde à minha entrada falada](#the-character-does-not-respond-to-my-spoken-input)" para obter informações sobre como acessar esse botão.

 

 




