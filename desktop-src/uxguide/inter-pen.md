---
title: Caneta
description: Todos os aplicativos Windows Microsoft devem ser habilitados para caneta. E fazer isso é mais fácil do que você pensa.
ms.assetid: 45635d5a-c9ff-47d0-89ef-a9c48ac67594
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 90c953fe1c287741bec266bfe6516a6a8922692b213292d2f17cccebf561cb0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117853347"
---
# <a name="pen"></a>Caneta

> [!NOTE]
> Este guia de design foi criado para Windows 7 e não foi atualizado para versões mais recentes do Windows. Grande parte das diretrizes ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais.](/windows/uwp/design/)

Todos os aplicativos Windows Microsoft devem ser habilitados para caneta. E fazer isso é mais fácil do que você pensa.

Entrada de caneta refere-se à maneira Windows permite interagir diretamente com um computador usando uma caneta. Uma caneta pode ser usada para apontar e também para gestos, entrada de texto simples e captura de ideias de forma livre em tinta digital.

A caneta usada para entrada tem uma dica fina e suave que dá suporte a apontar, escrever ou desenhar com precisão em tinta. A caneta também pode ter um botão de caneta opcional (usado para executar cliques com o botão direito do mouse) e borracha (usado para apagar tinta). A maioria das canetas suporta o foco.

![figura de uma caneta típica ](images/inter-pen-image1.png)

Uma caneta típica.

Quando a caneta é usada para manuscrito, os traços do usuário podem ser convertidos em texto usando o reconhecimento de manuscrito. Os traços podem ser mantidos da mesma forma que foram gravados, com o reconhecimento executado em segundo plano para dar suporte à pesquisa e à cópia como texto. Esses traços não convertidos são chamados de tinta digital.

![captura de tela de manuscrito na página onenote ](images/inter-pen-image2.png)

Um exemplo de entrada de tinta.

A maioria Windows programas já são amigáveis com caneta, pois uma caneta pode ser usada em vez de um mouse, a caneta funciona perfeitamente para tarefas e interações mais importantes e o programa responde a gestos. Um programa se torna amigável para manuscrito quando auxilia na entrada de texto manuscrito. Um programa se torna habilitado para tinta quando pode manipular tinta diretamente, em vez de exigir que os traços de caneta sejam convertidos em texto ou movimentos equivalentes do mouse. Isso permite que os usuários escrevam, desenhem e adicionem comentários em tinta digital de fluxo livre e de alta qualidade. A coleta de tinta é diferente da coleta de eventos do mouse, pois a tinta requer uma resolução mais alta e uma taxa de amostra mais alta e também pode adicionar nuances com pressão e inclinação. Para obter informações sobre como criar programas amigáveis e habilitados para tinta, consulte [Integrando](/previous-versions/windows/desktop/ms700674(v=vs.85)) entrada de tinta e [texto usando a caneta](/previous-versions/windows/desktop/ms695501(v=vs.85)).

Ao posicionar uma caneta, há menos necessidade de um cursor porque a dica se representa. No entanto, para direcionar a assistência, Windows fornece um cursor de caneta minúscula que indica o local da caneta atual. Ao contrário do ponteiro do mouse que ele substitui, o cursor de caneta não é necessário, a menos que a caneta esteja próxima à exibição, portanto, ele desaparece após alguns segundos de inatividade para permitir uma exibição desobstruída das informações.

A maioria dos programas amigáveis com canetas suporta gestos. Um gesto é um movimento rápido da caneta em uma tela que o computador interpreta como um comando, em vez de como um movimento, escrita ou desenho do mouse. Um dos gestos mais rápidos e fáceis de executar é um movimento. Um movimento é um gesto simples que resulta na navegação ou em um comando de edição. Os movimento de navegação incluem arrastar para cima, arrastar para baixo, voltar e avançar, enquanto editar os movimento inclui copiar, colar, desfazer e excluir.

Todos os ponteiros, exceto o ponteiro ocupado, têm um único ponto de acesso de pixel que define o local exato da tela do ponteiro. O ponto de contato determina qual objeto é afetado pela interação. Os objetos definem uma zona quente, que é a área em que o ponto de acesso é considerado sobre o objeto. Normalmente, a zona quente coincide com as bordas de um objeto, mas pode ser maior para facilitar a interação.

**Como uma caneta pode apontar mais precisamente do que um dedo, se a interface do usuário funcionar bem para toque, ela também funcionará bem para uma caneta.** Consequentemente, este artigo se concentra principalmente em adicionar suporte à caneta a programas que já foram projetados para toque.

**Observação:** As diretrizes relacionadas [ao mouse,](inter-mouse.md) [acessibilidade](inter-accessibility.md)e [toque](inter-touch.md) são apresentadas em artigos separados.

## <a name="design-concepts"></a>Conceitos de design

O uso de uma caneta para entrada tem as seguintes características:

-   **Natural e intuitivo.** Todos sabem como apontar e tocar com uma caneta. As interações de objeto são projetadas para corresponder a como os usuários interagem com objetos no mundo real de maneira consistente.
-   **Expressivo.** Traços de uma caneta são fáceis de controlar, tornando a escrita, o desenho, o esboço, a pintura e a anotação mais fáceis do que fazer isso com um mouse.
-   **Mais pessoal.** Assim como uma anotação ou assinatura manuscrita é mais pessoal do que uma digitada, usar uma assinatura ou uma nota digitalmente manuscrito também é mais pessoal.
-   **Menos invasivo.** O uso de uma caneta é silencioso e, consequentemente, muito menos distração do que digitar ou clicar, especialmente em situações sociais, como reuniões.
-   **Portátil.** Um computador com uma funcionalidade de caneta pode ser mais compacto porque a maioria das tarefas pode ser concluída sem teclado, mouse ou touchpad. Ele pode ser mais flexível porque não requer uma superfície de trabalho. Ele permite novos locais e cenários para usar um computador.
-   **Direta e envolvente.** Usar uma caneta faz com que você sinta que está interagindo diretamente com os objetos na tela, enquanto o uso de um mouse ou touchpad sempre exige que você coordene movimentos de mão com movimentos de ponteiro separados na tela que parecem indiretos por comparação.

**Todos Windows programas devem ter uma boa experiência de caneta.** Os usuários devem ser capazes de executar as tarefas mais importantes do programa com eficiência usando uma caneta. Algumas tarefas, como digitação ou manipulação detalhada de pixels, não são apropriadas para uma caneta, mas devem pelo menos ser possíveis.

Felizmente, se o programa já foi bem projetado e é amigável para toque, fornecer um bom suporte à caneta é fácil de fazer. Para essa finalidade, um programa bem projetado:

-   **Tem bom suporte para mouse.** Os controles interativos têm recursos claros e visíveis e têm estados de foco para comentários de ponteiro. Os objetos têm comportamentos padrão para as interações padrão do mouse (clique com o botão esquerdo único e duplo, clique com o botão direito do mouse, arraste e passe o mouse). A [forma do ponteiro](inter-mouse.md) muda conforme apropriado para indicar o tipo de manipulação direta.
-   **Tem bom suporte ao teclado.** O programa torna os usuários eficientes fornecendo atribuições de tecla de atalho padrão, especialmente para comandos de navegação e edição que também podem ser gerados por meio de gestos.
-   **Tem controles grandes o suficiente para toque.** Os controles têm um tamanho mínimo de 23x23 pixels (DLUs de unidades de diálogo 13x13) e os controles mais usados são pelo menos \[ \] 40 x 40 pixels (23x22 DLUs). Para evitar um comportamento sem resposta, não deve haver intervalos pequenos entre destinos, os elementos da interface do usuário devem ser espainhados para que os destinos adjacentes sejam tocados ou tenham pelo menos 5 pixels (3 DLUs) de espaço entre eles.
-   **É acessível.** Usa Microsoft Active Accessibility (MSAA) para fornecer acesso programático à interface do usuário para tecnologias adaptativas. O programa responde adequadamente às alterações de tema e métrica do sistema.
-   **Funciona bem e parece bom em 120 dpi (pontos** por polegada), que é a resolução de exibição padrão recomendada para computadores habilitados para caneta.
-   **Usa controles comuns.** Os controles mais comuns são projetados para dar suporte a uma boa experiência de caneta. Se necessário, o programa usa controles personalizados bem implementados que são projetados para dar suporte a direcionamento fácil e manipulação interativa.
-   **Usa controles restritos.** Quando projetados para direcionamento fácil, controles restritos, como listas e controles deslizantes, podem ser melhores do que controles irr pouco restritos, como caixas de texto, pois eles reduzem a necessidade de entrada de texto.
-   **Fornece valores padrão apropriados.** O programa seleciona o mais seguro (para evitar perda de dados ou acesso ao sistema) e a opção mais segura por padrão. Se segurança e segurança não são fatores, o programa seleciona a opção mais provável ou conveniente, eliminando a interação desnecessária.
-   **Fornece preenchimento automático de texto.** Fornece uma lista dos valores de entrada mais prováveis ou recentes para facilitar muito a entrada de texto.

Infelizmente, o inverso também será verdadeiro se o programa não for bem projetado, suas deficiências serão especialmente óbvias para os usuários que usam uma caneta.

### <a name="model-for-pen-interaction"></a>Modelo para interação com caneta

Se você não tiver experiência com o uso de uma caneta, a melhor introdução será aprender fazendo isso. Obter um computador habilitado para caneta, colocar o mouse e o teclado de lado e realizar as tarefas que você normalmente faz usando apenas uma caneta. Experimente programas habilitados para tinta, como o Windows Journal, e programas que não estão habilitados para tinta. Se você tiver um Tablet PC, experimente segurando-o em posições diferentes, como no seu colo, em uma tabela ou em seus braços enquanto estiver em pé. Tente usá-lo na orientação retrato e paisagem e mantenha a caneta para escrita e apenas para apontar, à esquerda, bem como à direita.

Ao experimentar o uso de uma caneta, você descobrirá que:

-   **Controles pequenos são difíceis de usar.** O tamanho dos controles afeta muito sua capacidade de interagir com eficiência. Controles com 10 x 10 pixels funcionam razoavelmente para uma caneta, mas controles maiores são ainda mais confortável de usar. Por exemplo, [controles de rotação](ctrl-spin-controls.md) (15x11 pixels) são muito pequenos para usar com uma caneta facilmente.
-   **A mão é um fator.** Às vezes, sua mão aborda coisas com as que você talvez queira ver ou interagir. Por exemplo, para usuários de direita, os menus de contexto são difíceis de usar se aparecerem à direita do ponto de clique, portanto, será melhor se eles aparecerem à esquerda. Windows permite que os usuários indiquem suas mãos no item do painel de Configurações tablet.
-   **A localidade da tarefa ajuda.** Embora você possa mover o ponteiro em uma tela de 14 polegadas com um movimento do mouse de 3 polegadas, usar uma caneta exige que você mova a mão por 14 polegadas inteiras. Mover-se repetidamente entre destinos distantes pode ser entediante, portanto, é muito melhor manter as interações de tarefas dentro do intervalo de uma mão mesmada sempre que possível. Os menus de contexto são convenientes porque não exigem movimentação da mão.
-   **A entrada e a seleção de texto são difíceis.** A entrada de texto longa é especialmente difícil de usar uma caneta, portanto, o preenchimento automático e os valores de texto padrão aceitáveis podem realmente simplificar as tarefas. A seleção de texto também pode ser bastante difícil, portanto, as tarefas são mais fáceis quando não exigem um posicionamento preciso do cursor.
-   **Destinos pequenos próximos à borda da exibição podem ser muito difíceis de tocar.** Algumas telas de exibição são protrutivas e algumas tecnologias touchscreen são menos sensíveis às bordas, tornando os controles próximos à borda mais difíceis de usar. Por exemplo, os botões Minimizar, Maximizar/Restaurar e Fechar na barra de título podem ser mais difíceis de usar quando uma janela é maximizada.

### <a name="control-location"></a>Local do controle

A localidade da tarefa reduz a repetição entediante de movimentos entre telas. Para minimizar os movimentos de mão, localize controles próximos de onde eles provavelmente serão usados.

**Incorreto:**

![captura de tela da paleta de cores separada das ferramentas ](images/inter-pen-image3.png)

Neste exemplo do Windows XP, a paleta de cores está muito longe de onde é provável que ela seja usada.

Considere que o local atual do usuário é o mais próximo que um destino pode ser, tornando trivial adquirir. Assim, os menus de contexto aproveitam ao máximo a Lei do [Fitts,](inter-mouse.md)assim como as minibaras de ferramentas usadas pelo Microsoft Office.

![captura de tela de ponteiros próximos a menus ](images/inter-pen-image4.png)

O local do ponteiro atual é sempre o mais fácil de adquirir.

Destinos pequenos próximos à borda de exibição podem ser difíceis de serem destinados, portanto, evite colocar controles pequenos próximos às bordas da janela. Para garantir que os controles sejam fáceis de direcionar quando uma janela é maximizada, faça-os pelo menos 23x23 pixels (DLUs 13x13) ou coloque-os fora da borda da janela.

### <a name="pen-interactions"></a>Interações com caneta

**Gestos do sistema**

Os gestos do sistema são definidos e tratados Windows. Como resultado, todos Windows programas têm acesso a eles. Esses gestos têm mensagens equivalentes de mouse, teclado e comando de aplicativo:



| Gesto do sistema                                                           | Mensagem equivalente sintetizada                                              |
|------------------------------------------------------------|-----------------------------------------------|
| Passar o mouse (quando há suporte)<br/>                          | Passar o mouse sobre o mouse<br/>                        |
| Toque (para baixo e para cima)<br/>                               | Clique com o mouse com o botão esquerdo do mouse<br/>                   |
| Toque duas vezes (para baixo e para cima duas vezes)<br/>                  | Clique duas vezes com o botão esquerdo do mouse<br/>            |
| Pressione e mantenha pressionado (para baixo, pausar, para cima)<br/>                | Clique com o botão direito do mouse<br/>                  |
| Arrastar (para baixo, mover, para cima)<br/>                           | Arrastar para a esquerda do mouse<br/>                    |
| Pressione, segure e arraste (para baixo, pausar, mover, para cima)<br/>   | Arrastar o mouse para a direita<br/>                   |
| Selecione (para baixo, mover objetos selecionáveis, para cima)<br/> | Selecionar o mouse<br/>                       |



 

**Desenvolvedores:** Para obter mais informações, consulte [Enumeração SystemGesture](/previous-versions/ms552724(v=vs.100)).

**Movimentos**

Os gestos são gestos simples que são aproximadamente equivalentes aos atalhos de teclado. Os movimento de navegação incluem arrastar para cima, arrastar para baixo, voltar e avançar. A edição de movimento inclui copiar, colar, desfazer e excluir. Para usar os movimento, seu programa só precisa responder aos comandos de teclas relacionados.

![Diagrama que mostra gestos de movimento e suas atribuições padrão Windows 7.](images/inter-pen-image5.png)

Os oito gestos de movimento e suas atribuições padrão Windows 7. Os movimentos de navegação foram alterados para corresponder ao panorâmico (em que o objeto se move com o gesto) em vez de rolar (em que o objeto se move na direção oposta do gesto).

![figura de gestos de movimento, como o gesto de movimentação ](images/inter-pen-image6.png)

Os oito gestos de movimento e suas atribuições padrão no Windows Vista.

Os movimento de navegação têm mapeamento natural, portanto, são fáceis de aprender e lembrar. Os movimento de edição são diagonais que exigem mais precisão e seus mapeamentos não são tão naturais (movimento em direção ao Lixeira a ser excluído, movimento na direção da seta para voltar para desfazer), portanto, eles não são habilitados por padrão. Todas as ações de movimento podem ser personalizadas usando o item do painel de controle Caneta e Dispositivos de Entrada.



| Flick                                     | Mensagem equivalente sintetizada                                                            |
|--------------------------------------|-------------------------------------------------------------|
| Movimento à esquerda<br/>                | Comando Encaminhar (comando Voltar para Windows Vista)<br/> |
| Movimento à direita<br/>               | Comando Voltar (comando Encaminhar para Windows Vista)<br/> |
| Movimento para cima<br/>                  | Rolagem do teclado para baixo<br/>                             |
| Movimento para baixo<br/>                | Rolagem do teclado para cima<br/>                               |
| Diagonal para cima e para a esquerda<br/>    | Exclusão de teclado<br/>                                  |
| Diagonal para baixo e para baixo<br/>  | Desfazer teclado<br/>                                    |
| Fazer movimento diagonal para cima e para a direita<br/>   | Cópia do teclado<br/>                                    |
| Diagonal da direita para baixo<br/> | Colar teclado<br/>                                   |



 

**Gestos de aplicativo**

Os aplicativos também podem definir e manipular outros gestos. O Microsoft Gesture Recognizer pode reconhecer mais [de 40 gestos.](../tablet/application-gestures-and-semantic-behavior.md) Para usar gestos de aplicativo, seu programa deve definir os gestos que reconhece e, em seguida, manipular os eventos resultantes.

**Capacidade de resposta e consistência**

**A capacidade de resposta é essencial para criar experiências de caneta que se sintam diretas e envolvente.** Para se sentir direto, os gestos devem entrar em vigor imediatamente e os pontos de contato de um objeto devem permanecer na caneta sem problemas durante o gesto. Qualquer retardo, resposta mesiva, perda de contato ou resultados imprecisos destrói a percepção da manipulação direta e também da qualidade.

**A consistência é essencial para criar experiências de caneta que se sintam naturais e intuitivas.** Depois que os usuários aprendem um gesto padrão, eles esperam que esse gesto tenha o mesmo efeito em todos os programas aplicáveis. Para evitar confusão e frustração, nunca atribua significados não padrão a gestos padrão. Em vez disso, use gestos personalizados para interações exclusivas ao seu programa.

**Editando tinta e texto**

Editar tinta e texto está entre as interações mais desafiadoras ao usar uma caneta. Usar controles restritos, valores padrão apropriados e preenchimento automático elimina ou reduz a necessidade de inserir texto. Mas se seu programa envolver a edição de texto ou tinta, você poderá tornar os usuários mais produtivos ampliando automaticamente a interface do usuário de entrada até **150%** por padrão quando uma caneta é usada.

Por exemplo, um programa de email pode exibir a interface do usuário em tamanho normal, mas ampliar a interface do usuário de entrada para 150% para compor mensagens.

![captura de tela da mensagem do Outlook em uma fonte grande ](images/inter-pen-image7.png)

Neste exemplo, a interface do usuário de entrada é ampliada para 150%.

**Se você fizer apenas quatro coisas...**

1.  1. Faça com que Windows programas de programação tenham uma boa experiência de caneta! Os usuários devem ser capazes de executar as tarefas mais importantes do programa com eficiência usando uma caneta (pelo menos essas tarefas que não envolvem muita digitação ou manipulação de pixel detalhada).
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

