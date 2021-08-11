---
title: Problemas de entrada de fala
description: Problemas de entrada de fala
ms.assetid: b42664a2-9615-4e15-97a6-115e9556096b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d135ac8a098f52066854c6003c22caa7290efbd01c8038bda116cd843b21a2e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118246225"
---
# <a name="speech-input-problems"></a>Problemas de entrada de fala

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

### <a name="the-character-does-not-respond-to-my-spoken-input"></a>O caractere não responde à minha entrada falada.

Esse sintoma pode ser causado por vários problemas. Tente o seguinte para isolar o problema:

-   Verifique se o microfone está conectado corretamente. É uma boa ideia testá-lo com outro aplicativo de entrada de som para garantir que ele funcione corretamente.
-   Verifique se um mecanismo de fala compatível está instalado. Em Windows 95, Windows 98 e Windows NT 4.0, abra o Painel de Controle. Se você encontrar o objeto Speech, abra-o e ele lista os mecanismos de fala disponíveis e instalados em seu sistema.
-   Verifique se sua placa de som é compatível com o Microsoft Windows 95, Windows 98 ou Windows NT.

    A melhor maneira de fazer isso é executar o aplicativo de Gravador de Som que vem com Windows. Normalmente, ele pode ser encontrado no menu Iniciar. Clique no botão Iniciar, clique em Programas, em Acessórios, em Multimídiae em Gravador de Som. Quando a janela Gravador de Som for exibida, clique **no botão Gravar** e fale com o microfone. A linha na janela deve ser animada em resposta à sua entrada de voz.

    Se o aplicativo Gravador de Som não funcionar em seu sistema, entre em contato com o departamento de suporte técnico do fabricante da placa de som para saber mais. Sua placa de som pode não ser compatível com Windows ou pode haver um problema com os drivers de software para sua placa de som.

-   Verifique se a entrada de som para entrada de fala está definida corretamente.
    1.  Abra o objeto de entrada De fala no Painel de Controle. Se o objeto Speech não estiver presente, instale um.
    2.  Selecione o mecanismo de entrada de fala que você instalou.
    3.  Escolha o botão Assistente Configurações Microfone. Se esse botão aparecer desabilitado, um mecanismo de fala compatível não será instalado ou o mecanismo de fala instalado poderá não dar suporte ao ajuste automático.
-   Verifique se o aplicativo habilitado para Agente ou a página da Web dá suporte à entrada de fala. Nem todas as páginas (ou aplicativos) suportam a entrada de fala. Pressione e segure a tecla Listening. Normalmente, essa será a tecla Scroll Lock, a menos que você a tenha alterado. Uma janela pop-up deve aparecer sob o caractere . O texto na dica lhe dirá o estado de escuta do caractere. Se nenhuma dica for exibida, o aplicativo ou a página da Web não dá suporte à entrada de fala ou você não tem um mecanismo de fala compatível instalado. Se a dica aparecer e indicar que o caractere está escutando, fale um dos comandos de voz do caractere. Se você não sabe quais comandos de voz estão disponíveis, libere a tecla Listening e clique com o botão direito do mouse no caractere. Em seguida, escolha Abrir Janela Comandos de Voz no menu pop-up. Se o comando não aparecer, o suporte à fala não estará disponível para o aplicativo ou a página da Web que você está usando. Se ele aparecer, pressione e mantenha a tecla Escuta novamente. Se a dica Escuta aparecer sob o caractere e indicar que o caractere está escutando, fale um dos comandos listados na janela. Se o caractere não responder, vá para a próxima etapa.
-   Verifique se nenhum outro aplicativo está usando o dispositivo de saída de áudio no momento.
-   Verifique se o uso do MIDI pelo Microsoft Agent não está bloqueando o canal de áudio (consulte Aplicativos que reproduzem [MIDI](output-problems.md)não têm saída de áudio quando o Microsoft Agent está em execução " na seção Problemas de saída).
-   Se você seguiu as etapas acima, mas ainda tem problemas com a entrada de fala, verifique se a placa de som e o software do driver são compatíveis com o mecanismo de fala que você está usando. Verifique com o suporte técnico para sua placa de som e o fabricante do mecanismo de fala.

### <a name="the-midi-tone-seems-to-disrupts-speech-input"></a>O tom MIDI parece interromper a entrada de fala.

Reduza o volume MIDI usando as etapas a seguir.

1.  Abra a janela Controle de Volume clicando com o botão direito do mouse no ícone do locutor na barra de tarefas ou abrindo o objeto Multimídia no Painel de Controle. Clique no botão Volume na seção Reprodução da página Áudio.
2.  Diminua o volume MIDI movendo o controle deslizante para baixo.

### <a name="the-character-does-not-respond-to-voice-input-but-i-can-hear-my-voice-through-my-speakers-when-i-talk-into-my-microphone"></a>O caractere não responde à entrada de voz, mas posso ouvir minha voz por meio de meus alto-falantes quando converso com meu microfone.

Sua placa de som não está configurada corretamente para uso com o Microsoft Agent. Escolha o Assistente Configurações microfone na folha de propriedades do objeto Speech no Painel de Controle. Consulte as etapas para " O caractere não responde à minha entrada[falada](#the-character-does-not-respond-to-my-spoken-input)" para obter informações sobre como acessar esse botão.

 

 




