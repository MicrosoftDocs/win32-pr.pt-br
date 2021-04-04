---
title: Animando um caractere
description: Animando um caractere
ms.assetid: ed42de30-acac-41e8-bacb-4caaff254724
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ed47b30a9bcfcdb5e305b87ced5f02526ae0056
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007425"
---
# <a name="animating-a-character"></a>Animando um caractere

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

Depois que um caractere é carregado, você pode usar vários métodos do Microsoft Agent para animar o caractere. O primeiro que você usa é normalmente o método [**show**](show-method.md) . **Mostrar** torna o quadro do caractere visível e reproduz a animação atribuída ao estado de **exibição** do caractere.

Depois que o quadro do caractere estiver visível, você poderá usar o método [**Play**](play-method.md) , especificando o nome de uma animação para reproduzir essa animação. Os nomes de animação são específicos de uma definição de caractere. Conforme uma animação é reproduzida, a forma de sua janela é alterada para corresponder à imagem no quadro. Isso resulta em uma imagem gráfica móvel, ou *Sprite*, exibida na parte superior da área de trabalho e de todas as janelas ou *ordem z*.

Se o arquivo do caractere for armazenado localmente, você poderá simplesmente chamar o método [**Play**](play-method.md) . Em outros casos, como quando você carregou um. Caractere de ACF de um servidor HTTP, você deve usar o método [**Get**](get-method.md) (ou [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare)) para recuperar primeiro os dados da animação. Isso fará com que o Agent solicite o arquivo de animação do servidor e o armazene no buffer do navegador no computador local.

O método [**Speak**](speak-method.md) permite que você programe o caractere para falar, automaticamente sincronizando a saída. Mais detalhes são abordados na seção de saída deste documento.

Você pode usar o método [**MoveTo**](moveto-method.md) para posicionar o caractere em um novo local. Quando você chamar o método **MoveTo** , o Microsoft Agent reproduzirá automaticamente a animação apropriada com base na localização atual do caractere e moverá o quadro do caractere. Da mesma forma, quando você chama [**GestureAt**](gestureat-method.md), o Microsoft Agent reproduz a animação gesturing apropriada com base na localização do caractere e no local especificado na chamada.

Para ocultar o caractere, chame o método [Hide](hide-method.md) . Isso reproduz automaticamente o caractere associado ao estado **oculto** do caractere e, em seguida, oculta o quadro do caractere. No entanto, você também pode ocultar ou mostrar um caractere definindo a propriedade [**Visible**](visible-property.md) do caractere.

O Microsoft Agent processa todas as chamadas de animação, ou *solicitações*, de forma assíncrona. Isso permite que o código do aplicativo continue a lidar com outros eventos enquanto a solicitação está sendo processada. Por exemplo, as chamadas para o método [**Play**](play-method.md) colocam a animação em uma fila para o caractere de forma que as animações possam ser reproduzidas sequencialmente. No entanto, isso significa que você não pode supor que uma chamada para outras funções será necessariamente executada Depois de uma animação que segue em seu código. Por exemplo, normalmente, uma instrução após uma chamada para **Play** ou [**MoveTo**](moveto-method.md) será executada antes de a animação ser concluída.

Você pode sincronizar seu código com animações na fila de um caractere criando uma referência de objeto para a solicitação de animação e, quando a animação for iniciada ou concluída, monitorando os eventos de [solicitação](the-request-object.md) que o servidor usa para notificar os clientes do caractere. Por exemplo, se desejar que uma caixa de mensagem apareça quando o caractere terminar uma animação, você poderá colocar a chamada de caixa de mensagem em sua sub-rotina de manipulação de eventos [**RequestComplete**](requestcomplete-event.md) , verificando a ID de solicitação específica.

Quando um caractere é ocultado, o servidor não reproduz animações; no entanto, ele ainda enfileira e processa a solicitação de animação (desempenha a animação) e passa um status de solicitação de volta para o cliente. No estado oculto, o caractere não pode se tornar entrada-ativo. No entanto, se o usuário fala o nome do caractere (quando a entrada de fala está habilitada), o servidor mostra automaticamente o caractere.

Quando o aplicativo cliente carrega vários caracteres ao mesmo tempo, os serviços de animação do Microsoft Agent permitem que você anime os caracteres de forma independente ou use os métodos de [**espera**](wait-method.md), [**interrupção**](interrupt-method.md)ou [**parada**](stop-method.md) para sincronizar suas animações entre si.

O Microsoft Agent também desempenha outras animações automaticamente para você. Por exemplo, se o estado do caractere não for alterado por vários segundos, o Agent começará a reproduzir animações atribuídas às animações de **deixar** do caractere. Da mesma forma, quando a entrada de fala está habilitada, o Agent desempenha as animações de **escuta** do caractere e, em seguida, **ouve** animações quando um expressão é detectado. Essas animações gerenciadas por servidor são chamadas de *Estados* e são definidas quando um caractere é criado. Para obter mais informações, consulte [criando caracteres para o Microsoft Agent](agent-states.md).

 

 