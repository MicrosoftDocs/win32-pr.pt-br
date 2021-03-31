---
title: Estados do agente
description: Estados do agente
ms.assetid: 8c3c5b12-81af-4ba5-b834-9f0a7ff5d075
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c371b1a2126129c03f16ce7fc7c2f95cca955a2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159469"
---
# <a name="agent-states"></a>Estados do agente

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

Os serviços de animação do Microsoft Agent executam automaticamente determinadas animações para você. Por exemplo, quando você usa comandos [**MoveTo**](moveto-method.md) ou [**GestureAt**](gestureat-method.md) , os serviços de animação desempenham uma animação apropriada. Da mesma forma, após o tempo limite ocioso, os serviços executam animações automaticamente. Para dar suporte a esses Estados, você pode definir animações apropriadas e, em seguida, atribuí-las aos Estados. Você ainda pode reproduzir qualquer animação que definir diretamente usando o método [**Play**](play-method.md) , mesmo se você atribuí-lo a um estado.

Você pode atribuir várias animações ao mesmo estado e os serviços de animação escolherão aleatoriamente uma das suas animações. Isso permite que seu caractere exiba uma variedade muito mais natural em seu comportamento.

Embora as animações que você atribui a Estados possam incluir quadros de ramificação, evite fazer loops de animações (animações que ramificam para sempre). Caso contrário, você precisará usar o método [**Stop**](play-method.md) antes de poder reproduzir outra animação.

É importante definir e atribuir pelo menos uma animação para cada Estado que ocorre para o caractere. Se você não fornecer essas animações e atribuições de estado, talvez seu caractere não pareça se comportar adequadamente ao usuário. No entanto, se um estado não ocorrer para um caractere específico, você não precisará atribuir uma animação a esse estado. Por exemplo, se o aplicativo host nunca chamar o método [**MoveTo**](moveto-method.md) , você poderá ignorar a criação e a atribuição de animações de estado de **movimentação** .



| Estado              | Exemplo de uso                                                                         |
|--------------------|----------------------------------------------------------------------------------------|
| **GesturingDown**  | Quando o método de animação [**GestureAt**](gestureat-method.md) é processado.          |
| **GesturingLeft**  | Quando o método de animação [**GestureAt**](gestureat-method.md) é processado.          |
| **GesturingRight** | Quando o método de animação [**GestureAt**](gestureat-method.md) é processado.          |
| **GesturingUp**    | Quando o método de animação [**GestureAt**](gestureat-method.md) é processado.          |
| **Audição**        | Quando o início da entrada falada é detectado.                                        |
| **Ocultar**         | Quando o usuário ou o aplicativo oculta o caractere.                                  |
| **IdlingLevel1**   | Quando o caractere começa o estado **deixar** .                                        |
| **IdlingLevel2**   | Quando o caractere começa o segundo estado de nível **deixar** .                           |
| **IdlingLevel3**   | Quando o caractere inicia o estado de nível de **deixar** final.                            |
| **Detecta**      | Quando o caractere começa a escutar (o usuário primeiro pressiona a tecla de acesso de entrada de fala). |
| **MovingDown**     | Quando o método de animação [**MoveTo**](moveto-method.md) é processado.                |
| **MovingLeft**     | Quando o método de animação [**MoveTo**](moveto-method.md) é processado.                |
| **MovingRight**    | Quando o método de animação [**MoveTo**](moveto-method.md) é processado.                |
| **MovingUp**       | Quando o método de animação [**MoveTo**](moveto-method.md) é processado.                |
| **Mostrando**        | Quando o usuário ou o aplicativo mostra o caractere.                                  |
| **Língua**       | Quando o método de animação de [**fala**](speak-method.md) é processado.                  |



 

### <a name="the-hearing-and-listening-states"></a>Os Estados de audição e de escuta

A animação que você atribui ao estado de **escuta** é reproduzida quando o usuário pressiona a tecla de acesso Push a Talk para entrada de fala. Crie e atribua uma breve animação que torne a aparência do caractere cuidadosa. Da mesma forma, defina sua animação de **retorno** para ter uma duração curta para que o caractere reproduza sua animação de estado de **audição** quando o usuário fala. Uma animação de estado **audição** também deve ser breve e projetada para permitir que o usuário saiba que o caractere está ouvindo ativamente o que o usuário diz. As inclinações de cabeçalho ou outros pequenos gestos são apropriados. Para fornecer variabilidade natural, forneça várias animações de estado **auditivas** .

### <a name="the-gesturing-states"></a>Os Estados gesturing

Você precisa criar e atribuir animações de estado **gesturing** somente se planeja usar o método [**GestureAt**](gestureat-method.md) . Animações de estado **gesturing** são executadas quando o Microsoft Agent processa uma chamada para o método **GestureAt** . Se você definir sobreposições de boca para suas animações de estado **gesturing** , o caractere poderá falar como gestos de ti.

Os serviços de animação determinam o local do caractere e sua relação com o local das coordenadas especificadas no método e executam uma animação apropriada. A direção do gesturing é sempre em relação ao caractere; por exemplo, **GestureRight** deve ser um gesto para o direito do caractere.

### <a name="the-showing-and-hiding-states"></a>Os Estados mostrando e ocultando

Os Estados **mostrando** e **ocultação** desempenham as animações atribuídas quando o usuário ou o aplicativo host solicita a exibição ou ocultação do caractere. Esses Estados também definem adequadamente o estado **visível** do quadro de caracteres. Ao definir animações para esses Estados, tenha em mente que um caractere pode aparecer ou ser departe em qualquer local da tela. Como o usuário pode mostrar ou ocultar qualquer caractere, sempre há suporte para pelo menos uma animação para esses Estados.

As animações que você atribui ao estado de **exibição** normalmente terminam com um quadro que contém a imagem de posição neutra do caractere. Por outro lado, **ocultar** animações de estado normalmente começa com a posição neutra. **Mostrar** e **ocultar** animações de estado pode incluir um quadro vazio no início ou no final, respectivamente, para fornecer uma transição do estado atual do caractere.

### <a name="the-idling-states"></a>Os Estados deixar

Os Estados **deixar** são progressivos. Os serviços de animação começam a usar as atribuições de nível 1 para o primeiro período ocioso e usam as animações de nível 2 para a segunda. Depois disso, o ciclo de ociosidade progride para as animações de nível 3 atribuídas e permanece nesse estado até ser cancelado, como quando uma nova solicitação de animação é iniciada.

Crie animações para os Estados **deixar** para comunicar o estado do caractere, mas sem distrair o usuário. As animações devem refletir adequadamente a capacidade de resposta do caractere de maneiras sutis, mas claras. Por exemplo, glancing ou piscando são boas animações para atribuir ao estado **IdlingLevel1** . A leitura de animações funciona bem para o estado **IdlingLevel2** . Suspender ou ouvir música com fones de ouvido são bons exemplos de animações para atribuir ao estado **IdlingLevel3** . As animações que incluem muitos ou grandes movimentos não são adequadas para animações ociosas porque desenham a atenção do usuário. Como as animações de estado **deixar** são reproduzidas com frequência, forneça várias animações de estado **deixar** , especialmente para os Estados **IdlingLevel1** e **IdlingLevel2** .

Observe que um aplicativo pode desativar o processamento de ociosidade automático para um caractere e gerenciar o próprio estado de **deixar** do caractere. Os Estados **deixar** do agente são projetados para ajudá-lo a evitar qualquer situação em que o caractere não tenha animação para reproduzir. Uma imagem de caractere que não é alterada após um breve período de tempo é como um aplicativo que exibe um ponteiro de espera por um longo tempo, o que se reduz da sensação de believability e interatividade. Manter a ilusão não leva muito: às vezes, apenas uma intermitência animada, uma respire visível ou uma mudança de corpo.

### <a name="the-speaking-state"></a>O estado de fala

Os serviços de animação usam o estado de **fala** quando uma animação de fala não pode ser encontrada para a animação atual. Atribua uma animação de fala simples a esse estado. Por exemplo, você pode usar um único quadro que consiste na posição neutra do caractere com sobreposições de boca.

### <a name="the-moving-states"></a>Os Estados de movimentação

Os Estados de **movimentação** são executados quando um aplicativo chama o método [**MoveTo**](moveto-method.md) . Os serviços de animação determinam qual animação deve ser reproduzida com base no local atual do caractere e nas coordenadas especificadas. A direção do movimento é baseada na posição do caractere. Portanto, a animação que você atribui à animação **MovingLeft** deve ser baseada na esquerda do caractere. Se você não usar o método **MoveTo** , poderá ignorar a criação e a atribuição de uma animação.

**Mover** animações de Estado deve animar o caractere em sua posição de movimentação. O último quadro dessa animação é exibido, pois o quadro do caractere é movido na tela. Não há suporte para animar o caractere enquanto seu quadro se move.

### <a name="standard-animation-set"></a>Conjunto de animações padrão

Embora você possa criar um caractere personalizado para ter as animações que deseja usar, o Microsoft Agent define um conjunto de animações padrão. Os caracteres que estão em conformidade com essa definição podem ser selecionados como um caractere padrão.

A tabela a seguir lista as animações incluídas no conjunto de animações padrão. Mesmo que você esteja criando um caractere personalizado, talvez queira usar a lista como um guia para criar seus próprios caracteres. Os caracteres que dão suporte ao conjunto de animações padrão devem dar suporte a pelo menos as animações a seguir.



| Animação                        | Exemplo de uso                                                                                           | Animação de exemplo                                                                                                                                                                                                      |
|----------------------------------|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Reconhecer**                  | Quando o caractere reconhece a solicitação do usuário.                                                      | O caractere nós nesta ou pisca no gesto da mão "OK". Observe que essa animação deve retornar o caractere para sua posição neutra.<br/>                                                                                  |
| **Alerta**<sup>1, 2</sup>          | Quando o caractere está aguardando instruções, normalmente são reproduzidos depois que o usuário ativa o modo de escuta. | O caractere é voltado para frente, respiração, piscando ocasionalmente, mas aguardando claramente a instrução.                                                                                                                             |
| **Anúncio**<sup>1, 2</sup>       | Quando o caractere encontrar informações para o usuário.                                                   | Os gestos de caractere levantam os eyebrows e a mão ou abrem um envelope.                                                                                                                                                  |
| **Blink**                        | Quando o caractere termina de falar ou ocioso.                                                            | O caractere naturalmente pisca nos olhos.                                                                                                                                                                                       |
| **Confuso**<sup>1, 2</sup>       | Quando o caractere não entende o que fazer.                                                        | Cabeça de rabiscos de caracteres.                                                                                                                                                                                              |
| **Congratulações**<sup>1, 2</sup>   | Quando o caractere ou usuário conclui uma tarefa (uma forma mais forte da animação de **reconhecimento** ).          | O caractere executa o gesto de parabenização, transmite "Sim!"                                                                                                                                                              |
| **Recusar**<sup>1, 2</sup>        | Quando o caractere não pode ou recusa a solicitação do usuário.                                             | O caractere agita a cabeça, transmite "não pode fazer."                                                                                                                                                                            |
| **DoMagic1**                     | O caractere se prepara para exibir algo.                                                                 | Viva-ondas de caracteres ou varinha.                                                                                                                                                                                         |
| **DoMagic2**                     | O caractere conclui a exibição de algo.                                                                | O caractere conclui o gesto mágico.                                                                                                                                                                                     |
| **DontRecognize**<sup>1, 2</sup>  | Quando o caractere não reconheceu a solicitação do usuário.                                                  | O caractere tem a mão para a Ear.                                                                                                                                                                                           |
| **Explicar**<sup>1, 2</sup>        | Quando o caractere explica algo ao usuário.                                                       | Gestos de caractere como se estiver explicando algo.                                                                                                                                                                         |
| **GestureDown**<sup>1, 2</sup>    | Quando o caractere precisa apontar para algo abaixo dele.                                                 | Pontos de caractere para baixo.                                                                                                                                                                                                 |
| **GestureLeft**<sup>1, 2</sup>    | Quando o caractere precisa apontar para algo à esquerda.                                              | Pontos de caracteres com à esquerda ou Metamorfoses em uma seta apontando para a esquerda.                                                                                                                                                 |
| **GestureRight**<sup>1, 2</sup>   | Quando o caractere precisa apontar para algo à direita.                                             | Pontos de caracteres com direita ou transformar em uma seta apontando para a direita.                                                                                                                                               |
| **GestureUp**<sup>1, 2</sup>      | Quando o caractere precisa apontar para algo acima dele.                                                 | O caractere aponta para cima.                                                                                                                                                                                                   |
| **Getatenção**                 | Quando o caractere precisa notificar o usuário sobre algo importante.                                   | As ondas de caractere imvivam ou saltam para cima e para baixo.                                                                                                                                                                            |
| **GetAttentionContinued**        | Para enfatizar a importância da notificação.                                                         | Uma continuação ou repetição do gesto inicial.                                                                                                                                                                       |
| **GetAttentionReturn**           | Quando o caractere concluir a animação **getattention** ou **GetAttentionContinued** .                | O caractere retorna para sua posição neutra.                                                                                                                                                                             |
| **Saudação**<sup>1, 2</sup>          | Quando o usuário inicia o sistema.                                                                      | Caracteres sorrisos e ondas.                                                                                                                                                                                            |
| **Hearing1**                     | Quando o caractere ouve o início de um expressão falado (ouvindo ativamente).                           | O caractere é revertida para frente e nós nesta ou transforma o cabeçalho mostrando a resposta à entrada de fala. Observação: essa animação faz um loop para algum quadro intermediário que ocorre depois que o caractere se move para uma posição apropriada.<br/>   |
| **Hearing2**                     | Quando o caractere ouve o início de um expressão falado (ouvindo ativamente).                           | Outra variação do tipo de animação usada em **Hearing1** Observação: essa animação faz um loop para algum quadro intermediário que ocorre depois que o caractere se move para uma posição apropriada.<br/>                      |
| **Ocultar**                         | Quando o usuário ignora o caractere.                                                                   | O caractere remove Self da tela.                                                                                                                                                                                    |
| **Idle1 \_ 1**                     | Quando o caractere não tem nenhuma tarefa e o usuário não está interagindo com o caractere.                       | O caractere pisca ou procura, permanece em ou retornando para a posição neutra.                                                                                                                                   |
| **Idle1 \_ 2**                     | Quando o caractere não tem nenhuma tarefa e o usuário não está interagindo com o caractere.                       | Outra variação do tipo de animação usada no **Idle1 \_ 1**.                                                                                                                                                       |
| **Idle2 \_ 1**                     | Quando o caractere esteve ocioso por algum tempo.                                                          | O caractere bocejos ou a revista de leitura permaneceu ou retornando para a posição neutra.                                                                                                                                   |
| **Idle2 \_ 2**                     | Quando o caractere esteve ocioso por algum tempo.                                                          | Outra variação do tipo de animação usada no **Idle2 \_ 1**.                                                                                                                                                       |
| **Idle3 \_ 1**                     | Quando o caractere ficar ocioso por muito tempo.                                                        | Bocejos de caracteres.                                                                                                                                                                                                       |
| **Idle3 \_ 2**                     | Quando o caractere ficar ocioso por muito tempo.                                                        | O caractere é suspenso ou coloca os fones de ouvido para escutar música. Observação: essa animação faz um loop para algum quadro intermediário que ocorre depois que o caractere se move para uma posição apropriada.<br/>                          |
| **LookDown**                     | Quando o caractere precisa ser examinado.                                                                   | A aparência do caractere é inativa.                                                                                                                                                                                                  |
| **LookLeft**                     | Quando o caractere precisa ser exibido à esquerda.                                                                   | O caractere é exibido à esquerda.                                                                                                                                                                                           |
| **LookRight**                    | Quando o caractere precisa ser examinado à direita.                                                                  | O caractere é semelhante à direita.                                                                                                                                                                                          |
| **Busca**                       | Quando o caractere precisa ser pesquisado.                                                                     | O caractere é pesquisado.                                                                                                                                                                                                    |
| **MoveDown**                     | Quando o caractere se prepara para a movimentação para baixo.                                                                | A transição de caracteres para uma posição de movimentação/vôo.                                                                                                                                                               |
| **MoveLeft**                     | Quando o caractere se prepara para mover para a esquerda.                                                                | As transições de caractere para uma posição esquerda de movimentação/vôo.                                                                                                                                                               |
| **MoveRight**                    | Quando o caractere se prepara para mover para a direita.                                                               | As transições de caractere para uma posição direita de cima para cima/caminhada.                                                                                                                                                              |
| **MoveUp**                       | Quando o caractere se prepara para mover para cima.                                                                  | A transição de caracteres para uma posição de movimentação/vôo.                                                                                                                                                                 |
| 1 com **prazer**<sup>, 2</sup>        | Quando o caractere está satisfeito com a solicitação ou a opção do usuário.                                         | Sorrisos de caracteres.                                                                                                                                                                                                      |
| **Processo**                      | Quando o caractere executa algum tipo de tarefa genérica.                                                   | Caractere pressiona botões ou usa algum tipo de ferramenta.                                                                                                                                                                   |
| **Processing**                   | Quando o caractere está ocupado trabalhando em uma tarefa genérica.                                                    | O caractere rabiscos no painel de papel ou usa algum tipo de ferramenta. Observação: essa animação faz um loop para algum quadro intermediário que ocorre depois que o caractere se move para uma posição apropriada.<br/>                      |
| **Ler**                         | Quando o caractere lê algo para o usuário.                                                          | Caractere exibe livro ou papel, lê e olha de volta ao usuário.                                                                                                                                                       |
| **ReadContinued**                | Quando o caractere lê mais para o usuário.                                                            | O caractere lê novamente e, em seguida, procura novamente no usuário.                                                                                                                                                                        |
| **ReadReturn**                   | Quando o caractere concluir a animação de **leitura** ou **ReadContinued** .                                | O caractere retorna para sua posição neutra.                                                                                                                                                                             |
| **Lendo**                      | Quando o caractere lê algo, mas não pode aceitar entrada.                                              | As leituras de caractere de um pedaço de papel. Observação: essa animação faz um loop para alguns quadros intermediários que ocorrem depois que o caractere se move para uma posição apropriada.<br/>                                           |
| **RestPose**                     | Quando o caractere se fala de sua posição neutra.                                                     | O caractere representa uma postura relaxada, mas cuidadosa.                                                                                                                                                                   |
| 1º **triste**<sup>, 2</sup>            | Quando o caractere está desapontado com a opção do usuário.                                               | Caracteres tristes ou parecem desapontados.                                                                                                                                                                                |
| **Pesquisa**                       | Quando o caractere procura algo.                                                                   | O caractere embaralha na gaveta do arquivo ou em outro contêiner procurando por algo.                                                                                                                                       |
| **Procurar**                    | Quando o caractere está procurando informações especificadas pelo usuário.                                              | O caractere embaralha na gaveta do arquivo ou em outro contêiner procurando por algo. Observação: essa animação faz um loop para alguns quadros intermediários que ocorrem depois que o caractere se move para uma posição apropriada.<br/> |
| **Mostrar**                         | Quando o caractere é iniciado ou retorna depois de ser Summoned.                                            | O caractere é exibido em uma assoprar de fumaça, passa ou percorre a tela.                                                                                                                                                    |
| **StartListening**<sup>1, 2</sup> | Quando o caractere está ouvindo.                                                                         | O caractere é colocado em Ear.                                                                                                                                                                                            |
| **StopListening**<sup>1, 2</sup>  | Quando o caractere para de escutar.                                                                      | O caractere coloca as mãos sobre ouvidos.                                                                                                                                                                                        |
| **Sugerir**<sup>1, 2</sup>        | Quando o caractere tem uma dica ou sugestão para o usuário.                                                 | A lâmpada aparece ao lado de caractere.                                                                                                                                                                                  |
| **Surpreso**<sup>1, 2</sup>      | Quando o caractere é surpreso pela ação ou opção do usuário.                                          | O caractere amplia os olhos, abre a boca.                                                                                                                                                                                    |
| **Considere**<sup>1, 2</sup>          | Quando o caractere está pensando em algo.                                                          | O caractere procura e tem mão no cabeçalho.                                                                                                                                                                             |
| **Definido** como <sup>1, 2</sup>      | Quando o caractere precisa que o usuário confirme uma solicitação.                                                  | O caractere parece ser testado, é transmitido ("tem certeza?")                                                                                                                                                                   |
| **Onda**<sup>1, 2</sup>           | Quando o usuário opta por desligar o servidor ou o sistema.                                                 | Ondas de caractere de boa ou Olá.                                                                                                                                                                                     |
| **Gravar**                        | Quando o caractere estiver ouvindo instruções do usuário.                                          | Character exibe papel, escreve e olha de volta ao usuário.                                                                                                                                                              |
| **WriteContinued**               | Quando o caractere continuar ouvindo as instruções do usuário.                                   | O caractere grava em um pedaço de papel e olha de volta ao usuário.                                                                                                                                                           |
| **WriteReturn**                  | Quando o caractere conclui a animação **Write** ou **WriteContinued** .                              | O caractere retorna para sua posição neutra.                                                                                                                                                                             |
| **Gravando**                      | Quando o caractere grava informações para o usuário.                                                  | Gravações de caracteres em um pedaço de papel. Observação: essa animação faz um loop.<br/>                                                                                                                                             |



 

  A animação requer sobreposições de boca e um quadro de fala definido.

  A animação requer uma animação de retorno atribuída com base em sua ramificação de saída ou em uma animação de retorno explícita.

Além disso, um caractere deve ter as atribuições de estado a seguir.



| Estado          | Animações necessárias                           |
|----------------|-----------------------------------------------|
| GesturingDown  | GestureDown                                   |
| GesturingLeft  | GestureLeft                                   |
| GesturingRight | GestureRight                                  |
| GesturingUp    | GestureUp                                     |
| Audição        | Hearing1, Hearing2                            |
| Ocultar         | Ocultar                                          |
| IdlingLevel1   | Piscar, Idle1 \_ 1, Idle1 \_ 2                     |
| IdlingLevel2   | Piscar, Idle1 \_ 1, Idle1 \_ 2, Idle2 \_ 1, Idle2 \_ 2 |
| IdlingLevel3   | Idle3 \_ 1, Idle3 \_ 2                            |
| Detecta      | Alerta                                         |
| MovingDown     | MoveDown                                      |
| MovingLeft     | MoveLeft                                      |
| MovingRight    | MoveRight                                     |
| MovingUp       | MoveUp                                        |
| Mostrando        | Mostrar                                          |
| Língua       | RestPose                                      |



 

 

 





