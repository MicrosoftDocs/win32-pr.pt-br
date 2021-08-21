---
title: Estados do agente
description: Estados do agente
ms.assetid: 8c3c5b12-81af-4ba5-b834-9f0a7ff5d075
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbfb927cbe9ad703e733caa827df7c5a63bac67b93d49edbb8f59884c89b6ee7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976796"
---
# <a name="agent-states"></a>Estados do agente

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

Os serviços de animação do Microsoft Agent reproduzem automaticamente determinadas animações para você. Por exemplo, quando você usa comandos [**MoveTo**](moveto-method.md) ou [**GestureAt,**](gestureat-method.md) os serviços de animação reproduzem uma animação apropriada. Da mesma forma, após o tempo de ociosidade, os serviços reproduzem animações automaticamente. Para dar suporte a esses estados, você pode definir animações apropriadas e atribuí-las aos estados. Você ainda pode reproduzir qualquer animação que definir diretamente usando o [**método Play,**](play-method.md) mesmo se atribuí-lo a um estado.

Você pode atribuir várias animações ao mesmo estado e os serviços de animação escolherão aleatoriamente uma de suas animações. Isso permite que seu caractere extiver uma variedade muito mais natural em seu comportamento.

Embora as animações que você atribui aos estados possam incluir quadros de ramificação, evite fazer loop de animações (animações que se ramificam para sempre). Caso contrário, você terá que usar o [**método Stop**](play-method.md) antes de reproduzir outra animação.

É importante definir e atribuir pelo menos uma animação para cada estado que ocorre para o caractere. Se você não fornecer essas animações e atribuições de estado, seu caractere poderá não parecer se comportar adequadamente para o usuário. No entanto, se um estado não ocorrer para um caractere específico, você não precisará atribuir uma animação a esse estado. Por exemplo, se o aplicativo host nunca chamar o [**método MoveTo,**](moveto-method.md) você poderá ignorar a criação e a atribuição de **Animações** de estado de movimentação.



| Estado              | Exemplo de uso                                                                         |
|--------------------|----------------------------------------------------------------------------------------|
| **GesturingDown**  | Quando o [**método de animação GestureAt**](gestureat-method.md) é processado.          |
| **GesturingLeft**  | Quando o [**método de animação GestureAt**](gestureat-method.md) é processado.          |
| **GesturingRight** | Quando o [**método de animação GestureAt**](gestureat-method.md) é processado.          |
| **GesturingUp**    | Quando o [**método de animação GestureAt**](gestureat-method.md) é processado.          |
| **Audição**        | Quando o início da entrada falada é detectado.                                        |
| **Escondendo**         | Quando o usuário ou o aplicativo oculta o caractere.                                  |
| **IdlingLevel1**   | Quando o caractere inicia o **estado de Idling.**                                        |
| **IdlingLevel2**   | Quando o caractere inicia o segundo **estado de nível de Idling.**                           |
| **IdlingLevel3**   | Quando o caractere inicia o estado final **do nível de Idling.**                            |
| **Ouvir**      | Quando o caractere começa a escutar (o usuário pressiona pela primeira vez a tecla de tecla de entrada de fala). |
| **MovingDown**     | Quando o [**método de animação MoveTo**](moveto-method.md) é processado.                |
| **MovingLeft**     | Quando o [**método de animação MoveTo**](moveto-method.md) é processado.                |
| **MovingRight**    | Quando o [**método de animação MoveTo**](moveto-method.md) é processado.                |
| **MovingUp**       | Quando o [**método de animação MoveTo**](moveto-method.md) é processado.                |
| **Mostrando**        | Quando o usuário ou o aplicativo mostra o caractere.                                  |
| **Falando**       | Quando o [**método de**](speak-method.md) animação Speak é processado.                  |



 

### <a name="the-hearing-and-listening-states"></a>Os estados auditivos e de escuta

A animação que você atribui ao **estado** De escuta é reproduzindo quando o usuário pressiona a tecla de tecla quente push-to-talk para entrada de fala. Crie e atribua uma animação curta que faça com que o caractere pareça insuntente. Da mesma forma, defina sua **animação** Return para  ter uma duração curta para que o caractere reproduza sua animação de estado auditivo quando o usuário fala. Uma **animação** de estado auditivo também deve ser breve e projetada para permitir que o usuário saiba que o caractere está escutando ativamente o que o usuário diz. Inclinações de cabeça ou outros gestos pequenos são apropriados. Para fornecer variabilidade natural, forneça várias **animações de** estado auditivo.

### <a name="the-gesturing-states"></a>Os estados de gestação

Você precisará criar e atribuir **animações de estado de gestação** somente se planeja usar o [**método GestureAt.**](gestureat-method.md) **Animações de** estado de gestão são reproduzidas quando o Microsoft Agent processa uma chamada para o **método GestureAt.** Se você definir sobreposições de boca para suas animações de estado de **Gestação,** o caractere poderá falar conforme ele faz gestos.

Os serviços de animação determinam o local do caractere e sua relação com o local das coordenadas especificadas no método e reproduzem uma animação apropriada. A direção de gestação é sempre em relação ao caractere; por exemplo, **GestureRight** deve ser um gesto à direita do caractere.

### <a name="the-showing-and-hiding-states"></a>Os estados de exibição e ocultação

Os **estados Mostrando** e **Ocultando** reproduzem as animações atribuídas quando o usuário ou o aplicativo host solicita para mostrar ou ocultar o caractere. Esses estados também configuram adequadamente o estado Visível **do quadro de** caracteres. Ao definir animações para esses estados, tenha em mente que um caractere pode aparecer ou sair em qualquer local da tela. Como o usuário pode mostrar ou ocultar qualquer caractere, sempre dá suporte a pelo menos uma animação para esses estados.

Animações que você atribui ao **estado** Mostrando normalmente terminam com um quadro que contém a imagem de posição neutra do caractere. Por outro lado, **Ocultar** animações de estado normalmente começa com a posição neutra. **Exibir** e **ocultar** animações de estado pode incluir um quadro vazio no início ou no fim, respectivamente, para fornecer uma transição do estado atual do caractere.

### <a name="the-idling-states"></a>Os estados de Idling

Os **estados de Idling** são progressivos. Os serviços de animação começam a usar as atribuições de Nível 1 para o primeiro período ocioso e usam as animações de Nível 2 para o segundo. Depois disso, o ciclo ocioso progride para as animações atribuídas ao Nível 3 e permanece nesse estado até ser cancelado, como quando uma nova solicitação de animação é iniciada.

Projete animações para os **estados de Idling** comunicarem o estado do caractere, mas não para desviar o usuário. As animações devem refletir adequadamente a capacidade de resposta do caractere de maneiras sutis, mas claras. Por exemplo, olhar ao redor ou piscar são boas animações para atribuir ao **estado IdlingLevel1.** A leitura de animações funciona bem para o **estado IdlingLevel2.** Adormecendo ou escutando música com fones de ouvido são bons exemplos de animações a atribuir ao **estado IdlingLevel3.** Animações que incluem muitos ou grandes movimentos não são adequadas para animações ociosas porque chamam a atenção do usuário. Como as animações de estado de **Idling** são tocadas com frequência, forneça várias animações de estado de **Idling,** especialmente para os estados **IdlingLevel1** e **IdlingLevel2.**

Observe que um aplicativo pode desativar o processamento ocioso automático de um caractere e gerenciar o próprio estado **de Idling do** caractere. Os estados **de Idling do** Agente foram projetados para ajudá-lo a evitar qualquer situação em que o caractere não tenha animação para reproduzir. Uma imagem de caractere que não muda após um breve período de tempo é como um aplicativo exibindo um ponteiro de espera por um longo tempo, o que diminui a noção de inatividade e interatividade. Manter a ilusão não leva muito tempo: às vezes, apenas um piscar animado, um rosto visível ou uma mudança no corpo.

### <a name="the-speaking-state"></a>O estado de fala

Os serviços de animação usam **o estado De** fala quando uma animação de fala não pode ser encontrada para a animação atual. Atribua uma animação de fala simples a esse estado. Por exemplo, você pode usar um único quadro que consiste na posição neutra do caractere com sobreposições de boca.

### <a name="the-moving-states"></a>Os estados de movimentação

Os **estados De** movimentação são reproduzidas quando um aplicativo chama o método [**MoveTo.**](moveto-method.md) Os serviços de animação determinam qual animação reproduzir com base no local atual do caractere e nas coordenadas especificadas. A direção de movimento é baseada na posição do caractere. Portanto, a animação que você atribui à **animação MovingLeft** deve ser baseada na esquerda do caractere. Se você não usar o método **MoveTo,** poderá ignorar a criação e a atribuição de uma animação.

**Mover** animações de estado deve animar o caractere para sua posição móvel. O último quadro dessa animação é exibido à medida que o quadro do caractere é movido na tela. Não há suporte para animar o caractere enquanto seu quadro se move.

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
| **Pesquisar**                       | Quando o caractere procura algo.                                                                   | O caractere embaralha na gaveta do arquivo ou em outro contêiner procurando por algo.                                                                                                                                       |
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



 

 

 





