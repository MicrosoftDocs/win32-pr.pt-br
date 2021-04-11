---
title: Problemas de saída
description: Problemas de saída
ms.assetid: 45423b7e-f648-408c-9cff-f7cf1affc42a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d909052feb2463637a8eab6343353f0af617c06
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104293812"
---
# <a name="output-problems"></a>Problemas de saída

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

### <a name="the-character-leaves-images-or-trails-behind-when-it-moves"></a>O caractere deixa imagens ou trilhas para trás quando ela se move.

Quando um caractere de agente é animado, ele exige que as janelas de aplicativo por trás do caractere sejam atualizadas em tempo hábil. Quando o caractere se move pela tela, é normal, às vezes, ver algumas imagens residuais que desaparecem rapidamente (dependendo da velocidade do seu PC e dos aplicativos que você está executando). Se não forem, a causa pode ser a seguinte:

-   O sistema não atende aos requisitos mínimos do sistema para o Agent.
-   A janela do aplicativo por trás do caractere não processa atualizações em tempo hábil. Tente arrastar o caractere pela janela da área de trabalho ou de uma pasta ou desligue alguns dos seus aplicativos. Se você vir um aperfeiçoamento perceptível, o problema poderá ser inevitável.
-   Talvez você não tenha o lançamento oficial do Microsoft Internet Explorer 4,0 (ou posterior) instalado. As versões anteriores de pré-lançamento do Internet Explorer 4,0 não trataram corretamente a atualização da tela. Isso resultaria em imagens residuais do caractere restante na tela. Para corrigir o problema, instale a versão oficial mais recente do Internet Explorer ( [https://www.microsoft.com/windows/ie/](https://www.microsoft.com/windows/internet-explorer/default.aspx) ).
-   Pode haver um problema com os drivers de tela do sistema ou o hardware. Certifique-se de que você tenha os drivers mais recentes para seu hardware gráfico. Se o problema persistir, talvez você queira entrar em contato com o fornecedor do seu PC.

### <a name="the-character-doesnt-produce-any-audio-output-when-it-speaks"></a>O caractere não produz nenhuma saída de áudio quando fala.

Esse sintoma pode ter várias causas. Tente o seguinte para isolar o problema:

-   Verifique se os alto-falantes estão conectados e se a placa de som é compatível com o Windows. É uma boa ideia testá-los com outro aplicativo de som para confirmar se a saída de áudio está funcionando corretamente.
-   Verifique se o aplicativo habilitado para agente ou a página da Web dá suporte à entrada de fala. Nem todas as páginas de exemplo dão suporte à entrada de fala. Pressione e segure a chave de escuta (normalmente, essa será a chave Scroll Lock, a menos que você a tenha alterado). Uma janela pop-up deve aparecer sob o caractere. O texto na dica informará o estado de escuta do caractere. Se nenhuma gorjeta for exibida, o aplicativo ou a página da Web não oferecerá suporte à entrada de fala ou você não tem um mecanismo de fala compatível instalado. Se a dica aparecer e indicar que o caractere está escutando, fale um dos comandos de voz do caractere. Se você não souber quais comandos de voz estão disponíveis: Libere a chave de escuta e clique com o botão direito do mouse no caractere e, em seguida, escolha abrir janela de comandos de voz no menu pop-up. Se o comando não for exibido, o suporte a fala não estará disponível para o aplicativo ou a página da Web que você está usando. Se ele for exibido, pressione e segure a tecla de escuta novamente. Se a dica de escuta aparecer abaixo do caractere e indicar que o caractere está escutando, fale um dos comandos listados na janela. Se o caractere não responder, vá para a próxima etapa.
-   Verifique se nenhum outro aplicativo está usando o dispositivo de saída de áudio no momento.
-   Verifique se o caractere que você está usando foi configurado para saída falada. (Talvez seja necessário verificar com o site ou o fornecedor do aplicativo.)
-   Verifique se as configurações do Microsoft Agent estão habilitadas para saída falada
-   Se o caractere usar um mecanismo de conversão de texto em fala (TTS) para produzir uma saída falada, verifique se você instalou um mecanismo de TTS compatível. Por exemplo, quando instalado como um componente de complemento do Internet Explorer 4,0, somente os componentes principais do Microsoft Agent são instalados. Os componentes principais não incluem um mecanismo de conversão de texto em fala. Sem esse mecanismo de TTS (um mecanismo compatível com o Microsoft Speech API), os caracteres de exemplo do Microsoft Agent não produzirão uma saída falada.
-   Verifique se o uso do MIDI do Microsoft Agent não está bloqueando o canal de áudio (consulte o próximo tópico, os aplicativos que executam o MIDI não têm nenhuma saída de áudio quando o Microsoft Agent está em execução).

### <a name="applications-that-play-midi-have-no-audio-output-when-microsoft-agent-is-running"></a>Os aplicativos que executam MIDI não têm nenhuma saída de áudio quando o Microsoft Agent está em execução.

O Microsoft Agent usa MIDI para tocar um tom quando você pressiona a tecla de escuta. Se você achar que isso interfere em outros aplicativos que reproduzem MIDI ou interferem na entrada de fala, você pode desativar o tom de reprodução quando você pode falar com a opção em Propriedades do Microsoft Agent.

### <a name="i-get-the-following-message-an-outgoing-call-cannot-be-made-since-the-application-is-dispatching-an-input-synchronous-call"></a>Recebo a seguinte mensagem: não é possível fazer uma chamada de saída, pois o aplicativo está expedindo uma chamada de entrada síncrona.

Essa mensagem pode ocorrer nas seguintes circunstâncias:

Quando uma página da Web que inclui o Microsoft Agent é fechada (clicando com o botão direito do mouse na entrada da barra de tarefas da página e escolhendo fechar no menu pop-up), isso pode ocorrer. Isso ocorre devido a um problema de tempo entre o agente e o navegador quando eles estão sendo desligados ao mesmo tempo. O erro é inofensivo. Clique em OK para ignorar a mensagem.

O que ocorreu porque a página da Web (ou aplicativo) habilitada para agente tentou solicitar um mecanismo de conversão de texto em fala (TTS) específico. O Speechapi.dll não foi instalado.

### <a name="the-speech-engines-dont-seem-to-work-with-microsoft-agent-in-windows-xp"></a>Os mecanismos de fala não parecem funcionar com o Microsoft Agent no Windows XP?

O Microsoft Agent usa o SAPI 4,0 para fornecer serviços de fala. No entanto, o Windows XP agora é fornecido com o SAPI 5,0, que não fornece suporte à compatibilidade com versões anteriores para seu antecessor. Felizmente, o SAPI 4,0 e o SAPI 5,0 podem coexistir juntos no mesmo computador com Windows XP.

Para fazer com que os mecanismos de fala funcionem com o Microsoft Agent no Windows XP, primeiro instale os [binários de tempo de execução SAPI 4,0](https://activex.microsoft.com/activex/controls/sapi/spchapi.exe)e, em seguida, instale os mecanismos de fala específicos.

### <a name="the-speech-engines-used-to-work-with-microsoft-agent-until-i-upgraded-to-windows-xp-what-happened"></a>Os mecanismos de fala usados para trabalhar com o Microsoft Agent até que eu tenha atualizado para o Windows XP. O que aconteceu?

Consulte a pergunta e a resposta anteriores. O processo de atualização do Windows XP pode ter removido o suporte a SAPI 4,0 já existente no computador. Basta reinstalar o tempo de execução do SAPI 4,0 e os mecanismos de fala do SAPI 4,0 novamente após a atualização para o Windows XP.

### <a name="i-installed-the-tts3000-text-to-speech-engines-onto-my-computer-that-runs-windows-xp-or-windows-2000-and-correctly-edited-my-programming-accordingly-for-their-use-the-microsoft-agent-characters-speak-audibly-using-these-tts3000-text-to-speech-engines-when-i-or-other-local-administrators-are-logged-in-but-not-when-other-users-without-administrator-privileges-are-logged-into-this-computer-on-windows-98-and-windows-me-these-tts3000-text-to-speech-engines-work-correctly-for-both-sets-of-users-how-can-i-fix-this"></a>Instalei os mecanismos de conversão de texto em fala do TTS3000 em meu computador que executa o Windows XP (ou o Windows 2000) e editei corretamente minha programação de acordo com seu uso. Os caracteres do Microsoft Agent falam forma audível usando esses mecanismos de conversão de texto em fala quando eu ou outros administradores locais estão conectados, mas não quando outros usuários *sem privilégios de administrador* estão conectados a este computador. No Windows 98 e no Windows me, esses mecanismos de conversão de texto em fala TTS3000 funcionam corretamente para ambos os conjuntos de usuários. Como posso corrigir isso?

Você precisará configurar as permissões de segurança para algumas das chaves do registro dos mecanismos de conversão de texto em fala do TTS3000 para habilitar seu uso por contas de usuário sem privilégios de administrador. Isso pode ser feito com o editor do registro do sistema operacional.

### <a name="i-followed-the-procedure-described-as-a-solution-to-the-problem-stated-in-the-previous-question-this-worked-fine-so-that-the-microsoft-agent-characters-could-speak-audibly-using-these-tts3000-text-to-speech-engines-when-users-without-administrator-privileges-were-logged-into-the-windows-xp-or-windows-2000-computer-now-months-later-these-same-tts3000-text-to-speech-engines-have-stopped-working-again-what-happened"></a>Segui o procedimento descrito como uma solução para o problema indicado na pergunta anterior. Isso funcionou bem para que os caracteres do Microsoft Agent pudessem falar forma audível usando esses mecanismos de conversão de texto em fala quando os usuários *sem privilégios de administrador* eram registrados no computador com Windows XP (ou Windows 2000). Agora, meses mais tarde, esses mesmos mecanismos de conversão de texto em fala TTS3000 pararam de funcionar novamente. O que aconteceu?

Quando você seguiu o procedimento descrito fornecido para a pergunta anterior, isso forneceu as contas de usuário não administrador com permissões de controle total para as chaves de Registro necessárias. É possível que um desses usuários tenha editado os valores de forma desconhecida ou inconsciente, alterado as permissões novamente ou até mesmo excluída totalmente a chave do registro.

Verifique se essas chaves do registro e suas permissões foram editadas, excluídas ou alteradas de outra forma desde o. Se necessário, altere essas chaves do registro e suas permissões novamente ou reinstale a conversão de texto em fala do TTS3000.

 

 




