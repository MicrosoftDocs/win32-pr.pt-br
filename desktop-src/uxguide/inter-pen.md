---
title: Caneta
description: Todos os aplicativos do Microsoft Windows devem estar habilitados para a caneta. E fazer isso é mais fácil do que você imagina.
ms.assetid: 45635d5a-c9ff-47d0-89ef-a9c48ac67594
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 35994f345306bd3a270f8d8cf9760e7d07183941
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "103837571"
---
# <a name="pen"></a>Caneta

> [!NOTE]
> Este guia de design foi criado para o Windows 7 e não foi atualizado para versões mais recentes do Windows. Grande parte da orientação ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais](/windows/uwp/design/).

Todos os aplicativos do Microsoft Windows devem estar habilitados para a caneta. E fazer isso é mais fácil do que você imagina.

A entrada à caneta se refere à maneira como o Windows permite interagir diretamente com um computador usando uma caneta. Uma caneta pode ser usada para apontar e também para gestos, entrada de texto simples e captura de ideias de forma livre em tinta digital.

A caneta usada para entrada tem uma dica suave e tranqüila que dá suporte ao ponto, gravação ou desenho preciso na tinta. A caneta também pode ter um botão de caneta opcional (usado para executar cliques com o botão direito do mouse) e borracha (usado para apagar a tinta). A maioria das canetas dá suporte ao mouse.

![Figura de uma caneta típica ](images/inter-pen-image1.png)

Uma caneta típica.

Quando a caneta é usada para manuscrito, os traços do usuário podem ser convertidos em texto usando o reconhecimento de manuscrito. Os traços podem ser mantidos exatamente como foram escritos, com o reconhecimento realizado em segundo plano para dar suporte à pesquisa e cópia como texto. Esses traços não convertidos são chamados de tinta digital.

![captura de tela de manuscrito na página do OneNote ](images/inter-pen-image2.png)

Um exemplo de entrada de tinta.

A maioria dos programas do Windows já é amigável para a caneta, pois uma caneta pode ser usada em vez de um mouse, a caneta funciona tranqüilamente para as tarefas e interações mais importantes e o programa responde aos gestos. Um programa torna-se fácil de escrever quando ajuda na entrada de texto manuscrito. Um programa torna-se habilitado para tinta quando pode lidar diretamente com a tinta, em vez de exigir que os traços de caneta sejam convertidos em texto ou em movimentos equivalentes do mouse. Isso permite que os usuários escrevam, desenhem e adicionem comentários em tinta digital de alta qualidade e de fluxo livre. A coleta de tinta é diferente da coleta de eventos do mouse, pois a tinta requer uma resolução mais alta e uma taxa de amostra mais alta, e também pode adicionar nuances com pressão e inclinação. Para obter informações sobre a criação de programas manuscritos e habilitados para tinta, consulte [integrando tinta](/previous-versions/windows/desktop/ms700674(v=vs.85)) e [entrada de texto usando a caneta](/previous-versions/windows/desktop/ms695501(v=vs.85)).

Ao posicionar uma caneta, há menos necessidade de um cursor porque a dica representa a si mesma. No entanto, para obter assistência para direcionar, o Windows fornece um pequeno cursor de caneta que indica o local da caneta atual. Ao contrário do ponteiro do mouse que ele substitui, o cursor da caneta não é necessário, a menos que a caneta esteja próxima da exibição, portanto, ela desaparece após alguns segundos de inatividade para permitir uma exibição inobstruída das informações.

A maioria dos programas amigáveis dá suporte a gestos. Um gesto é um movimento rápido da caneta em uma tela que o computador interpreta como um comando, em vez de um movimento de mouse, gravação ou desenho. Um dos gestos mais rápidos e fáceis de executar é um movimento. Um movimento é um gesto simples que resulta na navegação ou em um comando de edição. Os movimentos de navegação incluem arrastar para cima, arrastar para baixo, voltar e avançar, enquanto os movimentos de edição incluem copiar, colar, desfazer e excluir.

Todos os ponteiros, exceto o ponteiro ocupado, têm um ponto de acesso de pixel único que define o local exato da tela do ponteiro. O ponto de acesso determina qual objeto é afetado pela interação. Os objetos definem uma zona de acesso, que é a área em que o ponto de acesso é considerado sobre o objeto. Normalmente, a zona quente coincide com as bordas de um objeto, mas pode ser maior para facilitar a interação.

**Como uma caneta pode apontar com mais precisão do que um dedo, se a interface do usuário funcionar bem para toque, ela também funcionará bem para uma caneta.** Consequentemente, este artigo se concentra principalmente em adicionar suporte à caneta a programas que já foram projetados para toque.

**Observação:** As diretrizes relacionadas ao [mouse](inter-mouse.md), à [acessibilidade](inter-accessibility.md)e ao [Touch](inter-touch.md) são apresentadas em artigos separados.

## <a name="design-concepts"></a>Conceitos de design

O uso de uma caneta para entrada tem as seguintes características:

-   **Natural e intuitiva.** Todos sabem como apontar e tocar com uma caneta. As interações de objeto são projetadas para corresponder a como os usuários interagem com objetos no mundo real de maneira consistente.
-   **Expressividade.** Os traços de uma caneta são fáceis de controlar, de escrever, desenhar, esboçar, pintar e anotar mais facilmente do que com um mouse.
-   **Mais pessoal.** Assim como uma nota ou assinatura manuscrita é mais pessoal do que uma digitada, usar uma nota ou assinatura digitalmente manuscrita também é mais pessoal.
-   **Menos invasivo.** Usar uma caneta é silencioso e, consequentemente, menos confuso do que digitar ou clicar, especialmente em situações sociais, como reuniões.
-   **Portátil.** Um computador com um recurso de caneta pode ser mais compacto, pois a maioria das tarefas pode ser concluída sem teclado, mouse ou touchpad. Pode ser mais flexível porque não requer uma superfície de trabalho. Ele permite novos locais e cenários para usar um computador.
-   **Direto e envolvente.** Usar uma caneta faz você sentir como você está interagindo diretamente com os objetos na tela, enquanto o uso de um mouse ou Touchpad sempre exige que você coordene os movimentos da mão com movimentos de ponteiros na tela separados que se sentem indiretos por comparação.

**Todos os programas do Windows devem ter uma boa experiência de caneta.** Os usuários devem ser capazes de executar as tarefas mais importantes do seu programa com eficiência usando uma caneta. Algumas tarefas, como digitação ou manipulação de pixels detalhadas, não são apropriadas para uma caneta, mas devem, pelo menos, ser possíveis.

Felizmente, se o seu programa já estiver bem projetado e for compatível com toque, é fácil fornecer um bom suporte à caneta. Para essa finalidade, um programa bem projetado:

-   **Tem um bom suporte ao mouse.** Os controles interativos têm capacidades claros, visíveis e têm Estados de foco para comentários de ponteiro. Os objetos têm comportamentos padrão para as interações padrão do mouse (simples e duplo clique com o botão direito, clique, arraste e focalize). A [forma do ponteiro](inter-mouse.md) muda conforme apropriado para indicar o tipo de manipulação direta.
-   **Tem um bom suporte de teclado.** O programa torna os usuários eficientes fornecendo atribuições de teclas de atalho padrão, especialmente para comandos de navegação e edição que também podem ser gerados por meio de gestos.
-   **Tem controles grandes o suficiente para toque.** Os controles têm um tamanho mínimo de 23x23 pixels (unidades de caixa de diálogo 13x13 \[ DLUs \] ) e os controles usados com mais frequência são pelo menos 40x40 pixels (23x22 DLUs). Para evitar o comportamento sem resposta, não deve haver nenhum intervalo pequeno entre os destinos que os elementos da interface do usuário devem ter espaçados para que os destinos adjacentes estejam tocando ou tenham pelo menos 5 pixels (3 DLUs) de espaço entre eles.
-   **Está acessível.** Usa o Microsoft Acessibilidade Ativa (MSAA) para fornecer acesso programático à interface do usuário para tecnologias assistenciais. O programa responde adequadamente às alterações de métricas de tema e do sistema.
-   **Funciona bem e parece bom em 120 DPI (pontos por polegada),** que é a resolução de vídeo padrão recomendada para computadores habilitados para Pen.
-   **Usa controles comuns.** Os controles mais comuns são projetados para dar suporte a uma boa experiência de caneta. Se necessário, o programa usa controles personalizados bem implementados que são projetados para dar suporte ao direcionamento fácil e à manipulação interativa.
-   **Usa controles restritos.** Quando projetado para direcionamento fácil, controles restritos como listas e controles deslizantes podem ser melhores do que controles irrestrito, como caixas de texto, porque reduzem a necessidade de entrada de texto.
-   **Fornece valores padrão apropriados.** O programa seleciona o mais seguro (para evitar a perda de dados ou acesso ao sistema) e a opção mais segura por padrão. Se não houver fatores de segurança e segurança, o programa selecionará a opção mais provável ou conveniente, eliminando assim a interação desnecessária.
-   **Fornece preenchimento automático de texto.** Fornece uma lista de valores de entrada mais prováveis ou mais recentes para tornar a entrada de texto muito mais fácil.

Infelizmente, o inverso também será verdadeiro se o programa não estiver bem projetado, suas limitações serão especialmente óbvias para os usuários que usam uma caneta.

### <a name="model-for-pen-interaction"></a>Modelo para interação com a caneta

Se você não tiver experiência com o uso de uma caneta, a melhor introdução será aprender fazendo isso. Obtenha um computador habilitado para caneta, coloque o mouse e o teclado à parte e faça as tarefas que normalmente faz usando apenas uma caneta. Certifique-se de experimentar os programas habilitados para tinta, como o diário do Windows, e os programas que não são habilitados para tinta. Se você tiver um Tablet PC, experimente tê-lo em posições diferentes, como no seu colo, de acordo com o plano de uma mesa ou em seus braços enquanto estiver em pé. Tente usá-lo na orientação Retrato e paisagem e segure a caneta para escrever e apenas para o ponto à esquerda, bem como para a direita.

Ao experimentar o uso de uma caneta, você descobrirá que:

-   **Pequenos controles são difíceis de usar.** O tamanho dos controles afeta muito sua capacidade de interagir com eficiência. Os controles que são pixels 10x10 funcionam razoavelmente para uma caneta, mas controles maiores são ainda mais confortáveis para uso. Por exemplo, [controles de rotação](ctrl-spin-controls.md) (15x11 pixels) são muito pequenos para usar com uma caneta facilmente.
-   **Destromente é um fator.** A mão às vezes aborda as coisas que você pode querer ver ou interagir com elas. Por exemplo, para usuários da mão direita, os menus de contexto são difíceis de usar se aparecerem à direita do ponto de clique, portanto, é melhor se eles aparecerem à esquerda. O Windows permite que os usuários indiquem suas destros no item do painel de controle configurações do Tablet PC.
-   **A localidade da tarefa ajuda.** Embora você possa mover o ponteiro em uma tela de 14 polegadas com um movimento de um mouse de 3 polegadas, usar uma caneta exige que você mova a sua mão o total de 14 polegadas. Mover repetidamente entre os destinos que estão muito distantes pode ser entediante, portanto, é muito melhor manter as interações de tarefas dentro do intervalo de uma mão sempre que possível. Menus de contexto são convenientes porque não exigem movimento à mão.
-   **A entrada e a seleção de texto são difíceis.** A entrada de texto demorada é especialmente difícil de usar uma caneta, portanto, os valores de texto padrão aceitáveis e de preenchimento automático podem realmente simplificar as tarefas. A seleção de texto também pode ser muito difícil, portanto, as tarefas são mais fáceis quando não exigem posicionamento preciso do cursor.
-   **Pequenos destinos próximos à borda da exibição podem ser muito difíceis de tocar.** Alguns dos chanfros de tela estão em uma região e algumas tecnologias de tela touch são menos sensíveis às bordas, tornando os controles próximos à borda mais difíceis de usar. Por exemplo, os botões minimizar, maximizar/restaurar e fechar na barra de título podem ser mais difíceis de usar quando uma janela é maximizada.

### <a name="control-location"></a>Local do controle

A localidade da tarefa reduz movimentos de tela de repetição entediantes. Para minimizar os movimentos da mão, localize controles próximos de onde eles serão mais provavelmente usados.

**Incorreto:**

![captura de tela da paleta de cores separada das ferramentas ](images/inter-pen-image3.png)

Neste exemplo do Windows XP, a paleta de cores está muito longe de onde é provável que seja usada.

Considere que o local atual do usuário é o mais próximo que um destino pode ser, tornando-o trivial de adquirir. Portanto, os menus de contexto aproveitam totalmente a [lei de Fitts](inter-mouse.md), assim como as mini barras de ferramentas usadas pelo Microsoft Office.

![captura de tela de ponteiros próximos de menus ](images/inter-pen-image4.png)

O local do ponteiro atual é sempre o mais fácil de adquirir.

Pequenos destinos próximos à borda de exibição podem ser difíceis de direcionar, portanto, evite colocar pequenos controles próximos às bordas da janela. Para garantir que os controles sejam fáceis de direcionar quando uma janela for maximizada, torne-as pelo menos 23x23 pixels (13x13 DLUs) ou coloque-as fora da borda da janela.

### <a name="pen-interactions"></a>Interações com a caneta

**Gestos do sistema**

Os gestos do sistema são definidos e manipulados pelo Windows. Como resultado, todos os programas do Windows têm acesso a eles. Esses gestos têm mensagens de comando equivalentes do mouse, do teclado e do aplicativo:



| Gesto do sistema                                                           | Mensagem equivalente sintetizada                                              |
|------------------------------------------------------------|-----------------------------------------------|
| Focalizar (quando houver suporte)<br/>                          | Mouse em foco<br/>                        |
| Toque (para baixo e para cima)<br/>                               | Clique com o botão esquerdo do mouse<br/>                   |
| Toque duplo (para baixo e para cima duas vezes)<br/>                  | Clique com o botão esquerdo do mouse<br/>            |
| Pressionar e manter pressionado (inoperante, pausar, verticalmente)<br/>                | Clique com o botão direito do mouse<br/>                  |
| Arrastar (para baixo, mover, para cima)<br/>                           | Mouse à esquerda-arrastar<br/>                    |
| Pressione, mantenha pressionado e arraste (para baixo, pause, mova, para cima)<br/>   | Arrastar com o botão direito do mouse<br/>                   |
| Selecionar (inativo, mover sobre objetos selecionáveis, para cima)<br/> | Seleção do mouse<br/>                       |



 

**Desenvolvedores:** Para obter mais informações, consulte [Enumeração SystemGesture](/previous-versions/ms552724(v=vs.100)).

**Movimentos**

Os movimentos são gestos simples que são aproximadamente o equivalente a atalhos de teclado. Os movimentos de navegação incluem arrastar para cima, arrastar para baixo, mover para trás e avançar. Os movimentos de edição incluem copiar, colar, desfazer e excluir. Para usar movimentos, seu programa só precisa responder aos comandos de teclas relacionadas.

![Diagrama que mostra gestos de movimento e suas atribuições padrão no Windows 7.](images/inter-pen-image5.png)

Os oito gestos de movimento e suas atribuições padrão no Windows 7. Os movimentos de navegação foram alterados para corresponder ao movimento panorâmico (onde o objeto se move com o gesto) em vez de rolar (onde o objeto se move na direção oposta do gesto).

![Figura de gestos de movimento, como o gesto de movimentação ](images/inter-pen-image6.png)

Os oito gestos de movimento e suas atribuições padrão no Windows Vista.

Os movimentos de navegação têm um mapeamento natural, portanto, são fáceis de aprender e de se lembrar. Os movimentos de edição são diagonais que exigem mais precisão e seus mapeamentos não são tão naturais (movimento para a lixeira para exclusão, movimento na direção da seta voltar para desfazer) e, portanto, eles não são habilitados por padrão. Todas as ações de movimento podem ser personalizadas usando o item do painel de controle caneta e dispositivos de entrada.



| Flick                                     | Mensagem equivalente sintetizada                                                            |
|--------------------------------------|-------------------------------------------------------------|
| Mover para a esquerda<br/>                | Comando encaminhar (comando voltar para o Windows Vista)<br/> |
| Mover para a direita<br/>               | Comando voltar (comando encaminhar para o Windows Vista)<br/> |
| Mover para cima<br/>                  | Rolagem do teclado para baixo<br/>                             |
| Mover para baixo<br/>                | Rolagem do teclado para cima<br/>                               |
| Mover para cima-diagonal para a esquerda<br/>    | Exclusão de teclado<br/>                                  |
| Mover para baixo-diagonal esquerda<br/>  | Desfazer teclado<br/>                                    |
| Mover para cima-diagonal direita<br/>   | Cópia do teclado<br/>                                    |
| Mover para baixo-diagonal direita<br/> | Colar teclado<br/>                                   |



 

**Gestos de aplicativo**

Os aplicativos também podem definir e lidar com outros gestos. O reconhecedor de gestos da Microsoft pode reconhecer mais de [40 gestos](../tablet/application-gestures-and-semantic-behavior.md). Para usar gestos de aplicativo, seu programa deve definir os gestos que ele reconhece e, em seguida, manipular os eventos resultantes.

**Capacidade de resposta e consistência**

**A capacidade de resposta é essencial para a criação de experiências de caneta que se sentem diretas e envolventes.** Para se sentir direto, os gestos devem entrar em vigor imediatamente e os pontos de contato de um objeto devem permanecer sob a caneta suavemente ao longo do gesto. Qualquer retardo, resposta instável, perda de contato ou resultados imprecisos destrói a percepção da manipulação direta e também da qualidade.

**A consistência é essencial para a criação de experiências de caneta que se sentem naturais e intuitivas.** Depois que os usuários aprendem um gesto padrão, eles esperam que o gesto tenha o mesmo efeito em todos os programas aplicáveis. Para evitar confusão e frustração, nunca atribua significados não padrão a gestos padrão. Em vez disso, use gestos personalizados para interações exclusivas para seu programa.

**Editando a tinta e o texto**

A edição de tinta e texto está entre as interações mais desafiadoras ao usar uma caneta. O uso de controles restritos, valores padrão apropriados e preenchimento automático elimina ou reduz a necessidade de inserir texto. Mas se o seu programa envolver a edição de texto ou tinta, **você poderá tornar os usuários mais produtivos ao aplicar zoom automaticamente na interface do usuário de entrada até 150 por padrão quando uma caneta for usada.**

Por exemplo, um programa de email poderia exibir a interface do usuário em tamanho normal, mas aplicar zoom à interface do usuário de entrada para 150% para compor mensagens.

![captura de tela da mensagem do Outlook em fonte grande ](images/inter-pen-image7.png)

Neste exemplo, a interface do usuário de entrada é ampliada para 150 por cento.

**Se você fizer apenas quatro coisas...**

1.  1. Faça com que seus programas do Windows tenham uma boa experiência de caneta! Os usuários devem ser capazes de executar as tarefas mais importantes do seu programa com eficiência usando uma caneta (pelo menos as tarefas que não envolvem muita digitação ou manipulação de pixel detalhada).
2.  2. Considere adicionar suporte para escrever, desenhar e adicionar comentários diretamente usando tinta nos cenários mais relevantes.
3.  3. Para criar uma experiência direta e envolvente, os gestos entram em vigor imediatamente, mantêm os pontos de contato sob a caneta do usuário suavemente ao longo do gesto e têm o efeito do mapa de gestos diretamente para o movimento do usuário.
4.  4. Para criar uma experiência natural e intuitiva, dê suporte a gestos padrão apropriados e atribua a eles seus significados padrão. Use gestos personalizados para interações exclusivas para seu programa.

## <a name="guidelines"></a>Diretrizes

### <a name="control-usage"></a>Uso do controle

-   **Prefira usar controles comuns.** Os controles mais comuns são projetados para dar suporte a uma boa experiência de caneta.
-   **Prefira controles restritos.** Use controles restritos como listas e controles deslizantes sempre que possível, em vez de controlar unrestrição como caixas de texto, para reduzir a necessidade de entrada de texto.
-   **Forneça os valores padrão apropriados.** Selecione a opção mais segura (para evitar perda de dados ou acesso ao sistema) e a mais segura por padrão. Se não houver fatores de segurança e segurança, selecione a opção mais provável ou conveniente, eliminando assim a interação desnecessária.
-   **Forneça preenchimento automático de texto.** Forneça uma lista de valores de entrada mais prováveis ou mais recentes para tornar a entrada de texto muito mais fácil.
-   **Para tarefas importantes que usam seleção múltipla, se uma lista de seleção múltipla padrão for normalmente usada, forneça uma opção para usar uma lista de caixas de seleção em vez disso.**
-   **Respeitar as métricas do sistema.** O uso de métricas do sistema para todos os tamanhos não tem tamanhos de fisicamente. Se necessário, os usuários podem alterar as métricas ou o DPI do sistema para acomodar suas necessidades. No entanto, trate isso como um último recurso, pois os usuários normalmente não precisam ajustar as configurações do sistema para tornar a interface do usuário utilizável.

![captura de tela de menus com dimensionamento normal e grande ](images/inter-pen-image8.png)

Neste exemplo, a métrica do sistema para a altura do menu foi alterada.

### <a name="control-sizing-layout-and-spacing"></a>Controle de dimensionamento, layout e espaçamento

-   **Para controles comuns, use os tamanhos de controle recomendados.** Elas são grandes o suficiente para uma boa experiência de caneta, exceto para controles de rotação (que não podem ser usados com uma caneta, mas são redundantes).
-   **Escolha um layout que coloque controles próximos de onde eles serão usados com mais probabilidade.** Mantenha as interações entre tarefas em uma pequena área sempre que possível. Evite movimentações de longa distância, especialmente para tarefas comuns e para arrastar.
-   **Use o espaçamento recomendado.** O espaçamento recomendado é amigável para a caneta.
-   **Os controles interativos devem ser tocados ou, de preferência, têm pelo menos 5 pixels (3 DLUs) de espaço entre eles.** Isso evita confusão quando os usuários tocam fora do destino pretendido.
-   **Considere adicionar mais do que o espaçamento vertical recomendado em grupos de controles,** como links de comando, caixas de seleção e botões de opção, bem como entre os grupos. Isso facilita a diferenciação.

### <a name="interaction"></a>Interação

-   **Para programas criados para aceitar manuscrito, habilite a tinta padrão.** A entrada de tinta padrão permite que os usuários insiram tinta apenas começando a escrever, sem precisar tocar, dar um comando ou fazer algo especial. Isso permite a experiência mais natural com uma caneta. Para programas não projetados para aceitar manuscrito, manipule a entrada de caneta em caixas de texto como seleção.
-   **Permitir que os usuários apliquem zoom na interface de usuário do conteúdo** se o programa tiver tarefas que exijam a edição de texto. Considere aplicar zoom automaticamente a 150 por cento quando uma caneta for usada.
-   **Como os gestos são memorizados, atribua-os aos significados que são consistentes entre os programas.** Não dê diferentes significados a gestos com semântica fixa. Em vez disso, use um gesto apropriado específico do programa.

### <a name="handedness"></a>Direção

-   **Se uma janela for contextual, sempre a exibirá perto do objeto do qual foi iniciada.** Coloque-o fora do caminho para que o objeto de origem não seja coberto pela janela.
    -   Se for exibido usando o mouse, quando possível, coloque a janela contextual deslocada para baixo e para a direita.

        ![figura da janela contextual posicionada à direita do objeto ](images/inter-pen-image9.png)

        Mostrar janelas contextuais próximo ao objeto do qual ele foi iniciado.

    -   Se for exibido usando uma caneta, quando possível, coloque a janela contextual para que não seja coberta pela mão do usuário. Para usuários da mão direita, exiba à esquerda; caso contrário, exiba à direita.

        ![figura da janela contextual posicionada à esquerda do objeto ](images/inter-pen-image10.png)

        Ao usar uma caneta, também mostrar janelas contextuais para que elas não sejam cobertas pela mão do usuário.

-   **Desenvolvedores:** Você pode distinguir entre eventos de mouse e eventos de caneta usando a API [GetMessageExtraInfo](../tablet/system-events-and-mouse-messages.md) . Você pode determinar a [destro/canhoto](/previous-versions/ms819495(v=msdn.10)) do usuário usando a API [SystemParametersInfo](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) com SPI \_ GETMENUDROPALIGNMENT.

### <a name="forgiveness"></a>Forgiveness

-   **Forneça um comando desfazer.** O ideal é que você forneça desfazer para todos os comandos, mas o programa pode ter alguns comandos cujo efeito não possa ser desfeito.
-   **Forneça comentários de bom foco.** Indique claramente quando a caneta está sobre um destino clicável. Esses comentários são uma ótima maneira de evitar a manipulação acidental.
-   **Sempre que for prático, forneça bons comentários sobre a caneta, mas não execute ações até uma movimentação ou caneta para cima.** Isso permite que os usuários corrijam os erros antes que eles os façam.
-   **Sempre que for prático, permita que os usuários corrijam os erros facilmente.** Se uma ação entrar em vigor na caneta, permita que os usuários corrijam os erros deslizando enquanto a caneta ainda estiver inoperante.

## <a name="documentation"></a>Documentação

Ao fazer referência à entrada de caneta:

-   Consulte um dispositivo de entrada de caneta em forma de caneta como uma caneta. Na primeira menção, use caneta eletrônica.
-   Consulte o botão no lado de uma caneta como botão de caneta, não o botão de cilindro.
-   Consulte genericamente o teclado, o mouse, o trackball, a caneta ou o dedo como um dispositivo de entrada.
-   Use tocar (e toque duplo) em vez de clicar ao documentar procedimentos específicos ao uso de uma caneta. Toque em significa pressionar a tela e, em seguida, levantar antes de um tempo de espera. Ele pode ou não ser usado para gerar um clique do mouse. Para interações que não envolvem a caneta, continue a usar clique.

