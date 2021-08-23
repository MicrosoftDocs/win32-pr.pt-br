---
title: Animando um caractere
description: Animando um caractere
ms.assetid: ed42de30-acac-41e8-bacb-4caaff254724
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 937b970f1cdc9de9c973d298bbe963bfa70e4de3733869292e54d5d32742c722
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976776"
---
# <a name="animating-a-character"></a>Animando um caractere

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

Depois que um caractere é carregado, você pode usar vários dos métodos do Microsoft Agent para animar o caractere. O primeiro que você usa normalmente é o [**método Show.**](show-method.md) **Mostrar** torna o quadro do caractere visível e reproduz a animação atribuída ao estado Mostrando **do** caractere.

Depois que o quadro do caractere ficar visível, você poderá usar o método [**Play,**](play-method.md) especificando o nome de uma animação, para reproduzir essa animação. Os nomes de animação são específicos para uma definição de caractere. Conforme uma animação é reproduzida, a forma de sua janela muda para corresponder à imagem no quadro. Isso resulta em uma imagem gráfica móvel, ou *sprite*, exibida na parte superior da área de trabalho e em todas as janelas, ou *na ordem z.*

Se o arquivo do caractere for armazenado localmente, você poderá simplesmente chamar o [**método**](play-method.md) Play. Em outros casos, como quando você carregou um . Caractere ACF de um servidor HTTP, você deve usar o [**método Get**](get-method.md) (ou [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare)) para primeiro recuperar os dados de animação. Isso fará com que o Agent solicite o arquivo de animação do servidor e armazene-o no buffer do navegador no computador local.

O [**método Speak**](speak-method.md) permite que você programe o caractere para falar, sincronizando automaticamente a saída. Mais detalhes são abordados na seção Saída deste documento.

Você pode usar o [**método MoveTo**](moveto-method.md) para posicionar o caractere em um novo local. Quando você chama o **método MoveTo,** o Microsoft Agent reproduz automaticamente a animação apropriada com base no local atual do caractere e, em seguida, move o quadro do caractere. Da mesma forma, quando você chama [**GestureAt**](gestureat-method.md), o Microsoft Agent reproduz a animação de gestação apropriada com base no local do caractere e no local especificado na chamada.

Para ocultar o caractere, chame o [método Hide.](hide-method.md) Isso reproduz automaticamente o caractere associado  ao estado Ocultando do caractere e, em seguida, oculta o quadro do caractere. No entanto, você também pode ocultar ou mostrar um caractere definindo a propriedade [**Visible do**](visible-property.md) caractere.

O Microsoft Agent processa todas as chamadas de *animação ou solicita*, de forma assíncrona. Isso permite que o código do aplicativo continue manipulando outros eventos enquanto a solicitação está sendo processada. Por exemplo, chamadas para o método [**Play**](play-method.md) agem a animação em uma fila para o caractere para que as animações possam ser reproduzidas sequencialmente. No entanto, isso significa que você não pode assumir que uma chamada para outras funções será necessariamente executada após uma animação que segue em seu código. Por exemplo, normalmente, uma instrução após uma chamada para **Reproduzir** ou [**MoverTo**](moveto-method.md) será executada antes que a animação seja terminada.

Você pode sincronizar seu código com animações na fila de um caractere criando uma referência de objeto para [](the-request-object.md) a solicitação de animação e, quando a animação é iniciada ou concluída, monitorando os eventos de solicitação que o servidor usa para notificar os clientes do caractere. Por exemplo, se você quiser que uma caixa de mensagem apareça quando o caractere concluir uma animação, poderá colocar a chamada da caixa de mensagem na sub-rotina de manipulação de eventos [**RequestComplete,**](requestcomplete-event.md) verificando a ID de solicitação específica.

Quando um caractere está oculto, o servidor não reproduz animações; no entanto, ele ainda enfileia e processa a solicitação de animação (reproduz a animação) e passa um status de solicitação de volta para o cliente. No estado oculto, o caractere não pode se tornar input-active. No entanto, se o usuário falar o nome do caractere (quando a entrada de fala estiver habilitada), o servidor mostrará automaticamente o caractere.

Quando o aplicativo cliente carrega vários caracteres ao mesmo tempo, os serviços de animação do Microsoft Agent permitem animar caracteres independentemente ou usar os métodos [**Wait**](wait-method.md), [**Interrupt**](interrupt-method.md)ou [**Stop**](stop-method.md) para sincronizar a animação entre si.

O Microsoft Agent também reproduz outras animações automaticamente para você. Por exemplo, se o estado do caractere não tiver sido alterado por vários segundos, o Agent começará a reprodução de animações atribuídas às animações de **Idling** do caractere. Da mesma forma, quando a entrada de fala  está habilitada, o Agent reproduz as animações de Escuta do caractere e, em seguida, escuta animações quando um enunciado é detectado.  Essas animações gerenciadas pelo servidor são chamadas *de estados* e são definidas quando um caractere é criado. Para obter mais informações, consulte [Projetando caracteres para o Microsoft Agent.](agent-states.md)

 

 