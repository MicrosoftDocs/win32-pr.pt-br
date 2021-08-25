---
title: Problemas de saída
description: Problemas de saída
ms.assetid: 45423b7e-f648-408c-9cff-f7cf1affc42a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f19afb705e1d71b3b47bc44c35a51cb83029932287c582b0481ff6a5b078049
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961046"
---
# <a name="output-problems"></a>Problemas de saída

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

### <a name="the-character-leaves-images-or-trails-behind-when-it-moves"></a>O caractere deixa imagens ou trilhas para trás quando se move.

Quando um caractere do Agent é animado, ele requer que as janelas do aplicativo atrás do caractere se atualizem em tempo há tempo. Quando o caractere se move pela tela, às vezes é normal ver algumas imagens residuais que desaparecem rapidamente (dependendo da velocidade do computador e dos aplicativos que você está executando). Se não o fazem, o seguinte pode ser a causa:

-   Seu sistema não atendem aos requisitos mínimos do sistema para o Agent.
-   A janela do aplicativo por trás do caractere não processa atualizações em tempo hábil. Tente arrastar o caractere pela área de trabalho ou uma janela de pasta ou desligue alguns de seus aplicativos. Se você vir uma melhoria perceptível, o problema poderá ser inevitável.
-   Talvez você não tenha a versão oficial do Microsoft Internet Explorer 4.0 (ou posterior) instalada. As versões de pré-lançamento Internet Explorer 4.0 não trataram da atualização da tela corretamente. Isso resultaria em imagens residuais do caractere restante na tela. Para corrigir o problema, instale a versão oficial mais recente do Internet Explorer ( [https://www.microsoft.com/windows/ie/](https://www.microsoft.com/windows/internet-explorer/default.aspx) ).
-   Pode haver um problema com drivers de tela ou hardware do sistema. Certifique-se de que você tenha os drivers mais recentes para seu hardware gráfico. Se o problema persistir, talvez você queira entrar em contato com o fornecedor do computador.

### <a name="the-character-doesnt-produce-any-audio-output-when-it-speaks"></a>O caractere não produz nenhuma saída de áudio quando ele fala.

Esse sintoma pode ter várias causas. Tente o seguinte para isolar o problema:

-   Verifique se os alto-falantes estão conectados e se a placa de som é compatível com Windows. É uma boa ideia testá-los com outro aplicativo de som para confirmar se a saída de áudio está funcionando corretamente.
-   Verifique se o aplicativo habilitado para Agente ou a página da Web dá suporte à entrada de fala. Nem todas as páginas de exemplo são suportadas pela entrada de fala. Pressione e mantenha pressionada a tecla Listening (normalmente, essa será a tecla Scroll Lock, a menos que você a tenha alterado). Uma janela pop-up deve aparecer sob o caractere . O texto na dica lhe dirá o estado de escuta do caractere. Se nenhuma dica for exibida, o aplicativo ou a página da Web não dá suporte à entrada de fala ou você não tem um mecanismo de fala compatível instalado. Se a dica aparecer e indicar que o caractere está escutando, fale um dos comandos de voz do caractere. Se você não sabe quais comandos de voz estão disponíveis: libere a tecla Listening e clique com o botão direito do mouse no caractere e escolha Abrir Janela Comandos de Voz no menu pop-up. Se o comando não aparecer, o suporte à fala não estará disponível para o aplicativo ou a página da Web que você está usando. Se ele aparecer, pressione e mantenha a tecla Escuta novamente. Se a dica De escuta aparecer sob o caractere e indicar que o caractere está escutando, fale um dos comandos listados na janela. Se o caractere não responder, vá para a próxima etapa.
-   Verifique se nenhum outro aplicativo está usando o dispositivo de saída de áudio no momento.
-   Verifique se o caractere que você está usando foi configurado para a saída falada. (Talvez seja necessário verificar com o site ou o fornecedor do aplicativo.)
-   Verifique se as configurações do Microsoft Agent estão habilitadas para saída falada
-   Se o caractere usar um mecanismo de TTS (texto em fala) para produzir saída falada, verifique se você instalou um mecanismo TTS compatível. Por exemplo, quando instalado como um Internet Explorer complemento do Internet Explorer 4.0, somente os componentes principais do Microsoft Agent são instalados. Os componentes principais não incluem um mecanismo de texto em fala. Sem esse mecanismo TTS (um mecanismo compatível Speech API Microsoft), os caracteres de exemplo do Microsoft Agent não produzirão a saída falada.
-   Verifique se o uso do MIDI pelo Microsoft Agent não está bloqueando o canal de áudio (consulte o próximo tópico, Aplicativos que reproduzem MIDI não têm saída de áudio quando o Microsoft Agent está em execução).

### <a name="applications-that-play-midi-have-no-audio-output-when-microsoft-agent-is-running"></a>Aplicativos que reproduzem MIDI não têm saída de áudio quando o Microsoft Agent está em execução.

O Microsoft Agent usa MIDI para reproduzir um tom quando você pressiona a tecla Listening. Se você achar que isso interfere em outros aplicativos que reproduzem MIDI ou interferem na entrada de fala, você pode desativar a opção Reproduzir Tom Quando Você Pode Falar nas propriedades do Microsoft Agent.

### <a name="i-get-the-following-message-an-outgoing-call-cannot-be-made-since-the-application-is-dispatching-an-input-synchronous-call"></a>Eu vejo a seguinte mensagem: Não é possível fazer uma chamada de saída, pois o aplicativo está enviando uma chamada síncrona de entrada.

Essa mensagem pode ocorrer nas seguintes circunstâncias:

Quando uma página da Web, incluindo o Microsoft Agent, é fechada (clicando com o botão direito do mouse na entrada da barra de tarefas da página e escolhendo Fechar no menu pop-up), isso pode ocorrer. Isso ocorre devido a um problema de tempo entre o Agent e o navegador quando eles estão sendo desligados ao mesmo tempo. O erro é inofensivo. Clique em OK para descartar a mensagem.

O que ocorreu foi que a página da Web (ou aplicativo) habilitada para Agente tentou solicitar um mecanismo TTS (texto em fala) específico. Speechapi.dll não foi instalado.

### <a name="the-speech-engines-dont-seem-to-work-with-microsoft-agent-in-windows-xp"></a>Os mecanismos de fala parecem não funcionar com o Microsoft Agent no Windows XP?

O Microsoft Agent usa o SAPI 4.0 para fornecer serviços de fala. Windows No entanto, o XP agora é compatível com o SAPI 5.0, que não oferece suporte à compatibilidade com compatibilidade com backward para seu antecessor. Felizmente, o SAPI 4.0 e o SAPI 5.0 podem existir juntos no mesmo computador Windows XP.

Para fazer com que os mecanismos de fala funcionem com o Microsoft Agent no Windows XP, primeiro instale os binários de runtime do [SAPI 4.0](https://activex.microsoft.com/activex/controls/sapi/spchapi.exe)e, em seguida, instale os mecanismos de fala específicos.

### <a name="the-speech-engines-used-to-work-with-microsoft-agent-until-i-upgraded-to-windows-xp-what-happened"></a>Os mecanismos de fala costumavam trabalhar com o Microsoft Agent até que eu atualizava para Windows XP. O que aconteceu?

Consulte a pergunta e a resposta anteriores. O processo de atualização Windows XP pode ter removido o suporte do SAPI 4.0 já existente no computador. Basta instalar novamente o runtime do SAPI 4.0 e os mecanismos de fala do SAPI 4.0 novamente após a atualização para o Windows XP.

### <a name="i-installed-the-tts3000-text-to-speech-engines-onto-my-computer-that-runs-windows-xp-or-windows-2000-and-correctly-edited-my-programming-accordingly-for-their-use-the-microsoft-agent-characters-speak-audibly-using-these-tts3000-text-to-speech-engines-when-i-or-other-local-administrators-are-logged-in-but-not-when-other-users-without-administrator-privileges-are-logged-into-this-computer-on-windows-98-and-windows-me-these-tts3000-text-to-speech-engines-work-correctly-for-both-sets-of-users-how-can-i-fix-this"></a>Instalei os mecanismos de texto em fala TTS3000 em meu computador que executa o Windows XP (ou Windows 2000) e editei corretamente minha programação de acordo com seu uso. Os caracteres do Microsoft Agent falam de forma audível usando esses mecanismos de texto em fala TTS3000 quando eu ou outros administradores locais estão conectados, mas não quando outros usuários sem privilégios de Administrador são conectados neste computador.  No Windows 98 e Windows Me, esses mecanismos de texto em fala TTS3000 funcionam corretamente para ambos os conjuntos de usuários. Como posso corrigir isso?

Você precisará configurar as permissões de segurança para algumas das chaves do Registro dos mecanismos de texto em fala TTS3000 para habilitar seu uso por contas de usuário sem privilégios de Administrador. Isso pode ser feito com o Editor do Registro do sistema operacional.

### <a name="i-followed-the-procedure-described-as-a-solution-to-the-problem-stated-in-the-previous-question-this-worked-fine-so-that-the-microsoft-agent-characters-could-speak-audibly-using-these-tts3000-text-to-speech-engines-when-users-without-administrator-privileges-were-logged-into-the-windows-xp-or-windows-2000-computer-now-months-later-these-same-tts3000-text-to-speech-engines-have-stopped-working-again-what-happened"></a>Segui o procedimento descrito como uma solução para o problema declarado na pergunta anterior. Isso funcionou bem para que os caracteres do Microsoft Agent pudessem falar de forma audível usando esses mecanismos de texto em fala TTS3000 quando usuários sem privilégios de Administrador estavam *conectados* ao computador Windows XP (ou Windows 2000). Agora, meses depois, esses mesmos mecanismos de texto em fala TTS3000 param de funcionar novamente. O que aconteceu?

Quando você seguiu o procedimento descrito fornecido para a pergunta anterior, isso forneceu às contas de usuário não Administrador permissões de Controle Total para as chaves do Registro necessárias. É possível que um desses usuários tenha editado os valores de forma intencional ou não, alterado as permissões novamente ou até mesmo excluído totalmente a chave do Registro.

Verifique se essas chaves do Registro e suas permissões foram editadas, excluídas ou alteradas desde então. Se necessário, altere essas chaves do Registro e suas permissões novamente ou instale novamente o texto em fala do TTS3000.

 

 




