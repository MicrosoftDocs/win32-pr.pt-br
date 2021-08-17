---
title: Lista de verificação de experiência do usuário para aplicativos da área de trabalho
description: Aqui está uma coleção de algumas das diretrizes importantes no Guia de UX. Você pode usar isso como uma lista de verificação para garantir que a interface do usuário do programa tenha esses itens importantes corretos.
ms.assetid: 4705a807-5949-4957-8ea6-70871beaf8e0
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 712b31a7a5166e41e590470aea48f60a1f159850da3ea6917b36ece9ada80fa0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119332466"
---
# <a name="ux-checklist-for-desktop-applications"></a>Lista de verificação de experiência do usuário para aplicativos da área de trabalho

> [!NOTE]
> Este guia de design foi criado para Windows 7 e não foi atualizado para versões mais recentes do Windows. Grande parte das diretrizes ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais.](/windows/uwp/design/)

Aqui está uma coleção de algumas das diretrizes importantes no Guia de UX. Você pode usar isso como uma lista de verificação para garantir que a interface do usuário do programa tenha esses itens importantes corretos.

## <a name="windows"></a>Windows

-   **Dar suporte à resolução Windows efetiva mínima de 800 x 600 pixels.** Para UIs (interfaces de usuário) críticas que devem funcionar no modo de segurança, suporte [a](glossary.md) uma resolução efetiva de 640 x 480 pixels. Certifique-se de levar em conta o espaço usado pela barra de tarefas reservando 48 [pixels relativos verticais para janelas exibidas](glossary.md) com a barra de tarefas.
-   **Otimize layouts de janela reizáveis para uma resolução efetiva de 1024 x 768 pixels.** Reorganize automaticamente essas janelas para resoluções de tela inferior de uma maneira que ainda seja funcional.
-   **Teste suas janelas em 96 pontos por polegada (dpi) (a 800 x 600 pixels), 120 dpi (em 1024 x 768 pixels) e 144 dpi (a 1200 x 900 pixels).** Verifique se há problemas de layout, como recorte de controles, texto e janelas e alongamento de ícones e bitmaps.
-   **Para programas com cenários de uso móvel e de toque, otimize para 120 dpi.** Atualmente, as telas de alto dpi são predominantes em PCs móveis e de toque.
-   **Se uma janela for uma janela de propriedade, inicialmente a exibirá "centralizada" na parte superior da janela do proprietário.** Nunca abaixo. Para exibição subsequente, considere exibi-lo em seu último local (em relação à janela do proprietário) se for provável que isso seja mais conveniente.
-   **Se uma janela for contextual, sempre a exibirá perto do objeto do qual ela foi lançada.** No entanto, coloque-o fora do caminho (preferencialmente deslocamento para baixo e para a direita) para que o objeto não seja coberto pela janela.

## <a name="layout"></a>Layout

-   **Controles de tamanho e painéis dentro de uma janela para corresponder ao conteúdo típico.** Evite texto truncado e suas reellips associadas. Os usuários nunca devem ter que interagir com uma janela para exibir seu conteúdo típico– reservar reizing e rolagem para conteúdo incomummente grande. Verifique especificamente:
    -   **Tamanhos de controle.** Controles de tamanho para seu conteúdo típico, tornando os controles mais largos, mais altos ou de várias linhas, se necessário. Controles de tamanho para eliminar ou reduzir a rolagem em janelas que têm muito espaço disponível. Além disso, nunca deve haver rótulos truncados ou texto truncado em janelas que tenham muito espaço disponível. No entanto, para facilitar a leitura do texto, considere limitar as larguras de linha a 65 caracteres.
    -   **Larguras de coluna.** Certifique-se de que as colunas de exibição de lista tenham um tamanho padrão, mínimo e máximo adequado. Escolha larguras de coluna padrão de exibições de lista que não resultam em texto truncado, especialmente se houver espaço disponível na exibição de lista.
    -   **Saldo de layout.** O layout de uma janela deve ser aproximadamente equilibrado. Se o layout for pesado para a esquerda, considere tornar os controles mais largos e mover alguns controles mais para a direita.
    -   **Resize de layout.** Quando uma janela é resizável e os dados são truncados, certifique-se de que tamanhos de janela maiores mostrem mais dados. Quando os dados são truncados, os usuários esperam reizing de janelas para mostrar mais informações.
-   **Definir um tamanho mínimo da janela se houver um tamanho abaixo do qual o conteúdo não é mais acessível.** Para controles reizáveis, de definir tamanhos mínimos de elementos reizáveis para seus menores tamanhos funcionais, como larguras mínimas de coluna funcional em exibições de lista.

## <a name="text"></a>Texto

-   **Use termos comuns e conversacionais quando possível.** Concentre-se nas metas do usuário, não na tecnologia. Isso é especialmente eficaz se você estiver explicando um conceito técnico complexo ou uma ação. Imagine você mesmo olhando sobre o responsabilidade do usuário e explicando como realizar a tarefa.
-   **Seja cortês, reatêm e incentivador.** O usuário nunca deve se sentir desaixado, responsabilizado ou descarado.
-   **Remova texto redundante.** Procure texto redundante em títulos de janela, instruções principais, instruções complementares, áreas de conteúdo, links de comando e botões de commit. Em geral, deixe o texto completo nas instruções principais e controles interativos e remova qualquer redundância de outros locais.
-   **Use a capitalização de estilo de título para títulos e a capitalização de estilo de frase para todos os outros elementos da interface do usuário.** Fazer isso é mais apropriado para o Windows tom.
    -   **Exceção:** Para aplicativos herdado, você pode usar a capitalização de estilo de título para botões de comando, menus e títulos de coluna, se necessário, para evitar a combinação de estilos de capitalização.
-   **Para nomes de recursos e tecnologias, seja conservadora na capitalização.** Normalmente, somente os componentes principais devem ser em maiúsculas (usando a capitalização de estilo de título).
-   **Para nomes de recursos e tecnologias, seja consistente na capitalização.** Se o nome aparecer mais de uma vez em uma tela de interface do usuário, ele sempre deverá aparecer da mesma maneira. Da mesma forma, em todas as telas da interface do usuário no programa, o nome deve ser apresentado consistentemente.
-   **Não use maiúsculas os nomes** de elementos de interface do usuário genéricos, como barra de ferramentas, menu, barra de rolagem, botão e ícone.
    -   **Exceções:** Barra de endereços, Barra de links, faixa de opções.
-   **Não use todas as letras maiúsculas para teclas de teclado.** Em vez disso, siga a capitalização usada por teclados padrão ou minúsculas se a tecla não estiver rotulada no teclado.
-   **As re elipses significam a incompleta.** Use re elipses no texto da interface do usuário da seguinte forma:
    -   **Comandos.** Indique que um comando precisa de informações adicionais. Não use reellipses sempre que uma ação exibir outra janela — somente quando informações adicionais são necessárias. Comandos cujo verbo implícito é mostrar outra janela não têm reellipses, como Avançado, Ajuda, Opções, Propriedades ou Configurações.
    -   **Dados.** Indique que o texto está truncado.
    -   **Rótulos.** Indique que uma tarefa está em andamento (por exemplo, "Pesquisando...").

**Dica:** Texto truncado em uma janela ou página com espaço nãoutilado indica um layout ruim ou um tamanho de janela padrão muito pequeno. Busque layouts e tamanhos de janela padrão que eliminam ou reduzem a quantidade de texto truncado. Veja [Layout](vis-layout.md) para obter mais informações.

-   **Não use texto azul que não seja um link, pois os usuários podem presumir que se trata de um link.** Use negrito ou um tom de cinza em que, de outra forma, você usaria texto colorido.
-   **Use negrito com moderação para chamar a atenção para o texto que os usuários devem ler.**
-   **Use a instrução principal para explicar concisamente o que os usuários devem fazer em uma determinada janela ou página.** Boas instruções principais comunicam o objetivo do usuário em vez de se concentrar apenas na manipulação da interface do usuário.
-   **Expresse a instrução principal na forma de uma direção imperativa ou pergunta específica.**
-   **Não coloque pontos no final dos rótulos de controle ou instruções principais.**
-   **Use um espaço entre frases.** Não dois.

## <a name="controls"></a>Controles

-   **Geral**
    -   **Rotule cada controle ou grupo de controles. Exceções:**
        -   Caixas de texto e listas listadas podem ser rotuladas usando prompts.
        -   Os controles subordinados usam o rótulo de seu controle associado. Controles de rotação são sempre controles subordinados.
    -   **Para todos os controles, selecione o mais seguro (para evitar a perda de dados ou acesso ao sistema), o valor mais seguro por padrão.** Se segurança e segurança não são fatores, selecione o valor mais provável ou conveniente.
    -   **Prefira controles restritos.** Use controles restritos, como listas e controles deslizantes sempre que possível, em vez de controles irrados, como caixas de texto, para reduzir a necessidade de entrada de texto.
    -   **Reavaliar controles desabilitados.** Controles desabilitados podem ser difíceis de usar porque os usuários precisam deduzir literalmente por que estão desabilitados. Desabilite um controle quando os usuários esperam que eles se apliquem e podem facilmente deduzir por que o controle está desabilitado. Remova o controle quando não há nenhuma maneira para os usuários habilitá-lo ou se eles não esperam que ele seja aplicado, ou deixe-o habilitado, mas forneça uma mensagem de erro quando ele for usado incorretamente.
        -   **Dica:** Se você não tiver certeza se deve desabilitar um controle ou fornecer uma mensagem de erro, comece compondo a mensagem de erro que você pode fornecer. Se a mensagem de erro contiver informações úteis que os usuários de destino não têm probabilidade de deduzir rapidamente, deixe o controle habilitado e forneça o erro. Caso contrário, desabilite o controle.
-   **Botões de comando**
    -   **Prefira rótulos específicos sobre aqueles genéricos.** Idealmente, os usuários não precisam ler mais nada para entender o rótulo. Os usuários têm muito mais probabilidade de ler rótulos de botão de comando do que texto estático.
        -   **Exceção:** Não renomeie o botão cancelar se o significado de Cancel não for ambíguo. Os usuários não devem ler todos os botões para determinar qual botão cancela uma ação. No entanto, renomeie cancelar se não estiver claro qual ação está sendo cancelada, como quando há várias ações pendentes.
    -   **Ao fazer uma pergunta, use rótulos que correspondam à pergunta.** Por exemplo, forneça respostas Sim e não para uma pergunta Sim ou não.
    -   **Não use os botões aplicar em caixas de diálogo que não sejam folhas de propriedades ou itens do painel de controle.** O botão Aplicar significa aplicar as alterações pendentes, mas deixar a janela aberta. Isso permite que os usuários avaliem as alterações antes de fechar a janela. No entanto, somente as folhas de propriedades e os itens do painel de controle têm essa necessidade.
    -   Rotular um botão cancelar se cancelar retornar o ambiente para seu estado anterior (não deixando nenhum efeito colateral); caso contrário, Rotule o botão fechar (se a operação estiver concluída) ou pare (se a operação estiver em andamento) para indicar que ele deixa o estado alterado atual intacto.
-   **Links de comando**
    -   **Sempre apresente links de comando em um conjunto de dois ou mais.** Logicamente, não há motivo para fazer uma pergunta que tenha apenas uma resposta.
    -   **Forneça um botão de cancelamento explícito.** Não use um link de comando para essa finalidade. Com muita frequência, os usuários percebem que não querem executar uma tarefa. O uso de um link de comando para cancelar exigiria que os usuários leiam todos os links de comandos com cuidado para determinar qual deles significa cancelar. Ter um botão de cancelamento explícito permite que os usuários cancelem uma tarefa com eficiência.
    -   **Se fornecer um botão de cancelamento explícito deixar um único link de comando, forneça um link de comando para cancelar e um botão de cancelamento.** Isso torna claro que os usuários têm uma opção. Frase este link de comando em termos de como ele difere da primeira resposta, em vez de apenas "Cancelar" ou de alguma variação.
-   **Caixas de seleção "não mostrar \<item\> novamente"**
    -   **Considere usar uma opção "não mostrar isso \<item\> novamente" para permitir que os usuários suprimem uma caixa de diálogo recorrente, somente se não houver uma alternativa melhor.** É melhor mostrar sempre a caixa de diálogo se os usuários realmente precisarem dela ou simplesmente eliminá-la se não forem.
    -   **Substituir \<item\> pelo item específico.** Por exemplo, não mostrar este lembrete novamente. Ao fazer referência a uma caixa de diálogo em geral, use não mostrar esta mensagem novamente.
    -   **Indique claramente quando a entrada do usuário será usada para valores padrão futuros** adicionando a seguinte frase sob a opção: suas seleções serão usadas por padrão no futuro.
    -   **Não selecione a opção por padrão. Se a caixa de diálogo realmente deve ser exibida apenas uma vez, faça isso sem perguntar.** Não use essa opção como uma desculpa para incomodar os usuários — certifique-se de que o comportamento padrão não seja irritante.
    -   **Se os usuários selecionarem a opção e clicarem em cancelar, essa opção entrará em vigor.** Essa configuração é uma meta-opção, portanto, não segue o comportamento padrão de cancelar de deixar nenhum efeito colateral. Observe que, se os usuários não desejarem ver a caixa de diálogo no futuro, provavelmente também desejarem cancelá-lo.
-   **Links**
    -   **Não atribua uma chave de** [acesso](glossary.md). Os links são acessados usando a tecla Tab.
    -   **Não adicione "clique" ou "clique aqui" ao texto do link.** Não é necessário porque um link implica clicar.
-   **Dicas de ferramentas**
    -   **Use dicas de ferramenta para fornecer rótulos para controles sem rótulo.** Você não precisa fornecer dicas de ferramentas de controles rotuladas simplesmente para fins de consistência.
    -   **Dicas de ferramenta também podem fornecer mais detalhes para botões de barra de ferramentas rotulados se isso for útil.** Não apenas repita ou dê uma renomeação de palavras do que já está no rótulo.
    -   **Evite abranger o objeto do qual o usuário está prestes a exibir ou interagir.** Sempre coloque a ponta no lado do objeto, mesmo se isso exigir a separação entre o ponteiro e a dica. Algumas separações não são um problema, contanto que a relação entre o objeto e sua gorjeta seja clara.
        -   **Exceção:** Dicas de ferramentas de nome completo usadas em listas e árvores.
    -   **Para coleções de itens, evite abranger o próximo objeto do qual o usuário provavelmente exibirá ou interagirá.** Para itens organizados horizontalmente, evite colocar dicas à direita; para itens organizados verticalmente, evite colocar as dicas abaixo.
-   **Divulgação progressiva**
    -   **Use mais/menos botões de divulgação progressiva para ocultar opções avançadas ou raramente usadas, comandos e detalhes que os usuários normalmente não precisam.** Não oculte os itens usados normalmente, pois os usuários talvez não os encontrem. Mas certifique-se de que tudo esteja oculto tenha valor.
    -   Se a superfície sempre exibir algumas opções, comandos ou detalhes, use os seguintes pares de rótulos:
        -   **Mais/menos opções.** Use para opções ou uma combinação de opções, comandos e detalhes.
        -   **Mais/menos comandos.** Use somente para comandos.
        -   **Mais/menos detalhes.** Use apenas para fins informativos.
        -   **Mais/menos \<object name\> .** Use para outros tipos de objeto, como pastas.
    -   Caso contrário:
        -   **Mostrar/Ocultar opções.** Use para opções ou uma combinação de opções, comandos e detalhes.
        -   **Mostrar/ocultar comandos.** Use somente para comandos.
        -   **Mostrar/ocultar detalhes.** Use apenas para fins informativos.
        -   **Mostrar/ocultar \<object name\> .** Use para outros tipos de objeto, como pastas.
-   **Barras de progresso**
    -   **Use as barras de progresso de desligamento para operações que exigem uma quantidade de tempo limitada,** mesmo que essa quantidade de tempo não possa ser prevista com precisão. As barras de progresso indeterminadas mostram que o progresso está sendo feito, mas não fornecem outras informações. Não escolha uma barra de progresso indeterminada com base apenas na possível falta de exatidão.
    -   **Forneça uma estimativa de tempo restante se você puder fazer isso com precisão.** As estimativas de tempo restantes que são precisas são úteis, mas as estimativas que estão longe de marcar ou saltar de forma significativa não são úteis. Talvez seja necessário executar algum processamento para que você possa fornecer estimativas precisas. Nesse caso, não exiba estimativas potencialmente imprecisas durante esse período inicial.
    -   **Não reinicie o progresso.** Uma barra de progresso perderá seu valor se ela for reiniciada (talvez porque uma etapa na operação seja concluída) porque os usuários não têm como saber quando a operação será concluída. Em vez disso, todas as etapas na operação compartilham uma parte do progresso e a barra de progresso passa para a conclusão uma vez.
    -   **Forneça detalhes úteis do progresso.** Forneça informações de progresso adicionais, mas somente se os usuários puderem fazer algo com ele. Verifique se o texto é exibido por tempo suficiente para que os usuários possam lê-lo.
    -   **Não combine uma barra de progresso com um ponteiro ocupado.** Use um ou outro, mas não ambos ao mesmo tempo.
-   **Solicitações**
    -   **Use um aviso quando o espaço da tela estiver em um nível tão alto que usar um rótulo ou instrução é indesejável,** como em uma barra de ferramentas.
    -   **O prompt destina-se principalmente a identificar a finalidade da caixa de texto ou da caixa de combinação de forma compacta.** Elas não devem ser informações cruciais que o usuário precisa ver ao usar o controle.
    -   **O texto do prompt não deve ser confundido com texto real.** Para fazer isso:
        -   Desenhe o texto do prompt em cinza itálico e o texto de entrada real em preto-branco.
        -   O texto do prompt não deve ser editável e deve desaparecer depois que os usuários clicarem na guia ou na caixa de texto.
            -   **Exceção:** Se a caixa de texto tiver o foco de entrada padrão, o prompt será exibido e desaparecerá depois que o usuário começar a digitar.
    -   Não use a pontuação final ou as reticpses.
-   **Notificações**
    -   **Use notificações para eventos que não estão relacionados à atividade do usuário atual, não exigem ação imediata do usuário e os usuários podem ignorar livremente.**
    -   **Não abuso de notificações:**
        -   **Use notificações somente se for necessário.** Ao exibir uma notificação, você pode interromper os usuários ou até mesmo desative-los. Certifique-se de que a interrupção seja justificada.
        -   **Use notificações para eventos não críticos ou situações que não exigem ação imediata do usuário.** Para eventos críticos ou situações que exigem ação imediata do usuário, use um elemento de interface do usuário alternativo (como uma caixa de diálogo modal).
        -   **Não use notificações para anúncios de recursos!**

## <a name="keyboard"></a>Keyboard

-   **Atribua o foco de entrada inicial ao controle com o** qual os usuários têm maior probabilidade de interagir primeiro, que geralmente é o primeiro controle interativo. Se o primeiro controle interativo não for uma boa opção, considere alterar o layout da janela.
-   **Atribua paradas de guias a todos os controles interativos, incluindo caixas de edição somente leitura. Exceções:**
    -   Agrupa conjuntos de controles relacionados que se comportam como um único controle, como botões de rádio. Esses grupos têm uma única parada de tabulação.
    -   Contêm grupos corretamente para que as teclas de direção andem para frente e para trás dentro do grupo e permaneçam dentro do grupo.
-   **A ordem de tabulação deve fluir da esquerda para a direita, de cima para baixo.** Em geral, a ordem de tabulação deve seguir a ordem de leitura. Considere fazer exceções para controles comumente usados colocando-os anteriormente na ordem de tabulação. A guia deve passar por todas as paradas da guia em ambas as direções sem parar. Dentro de um grupo, a ordem de tabulação deve estar em ordem sequencial, sem exceções.
-   **Em uma parada de tabulação, a ordem** de tecla de direção deve fluir da esquerda para a direita, de cima para baixo, sem exceções. As teclas de direção devem passar por todos os itens em ambas as direções sem parar.
-   **Apresente os botões de confirmação na seguinte ordem:**
    -   OK/ \[ Faça isso \] /Sim
    -   \[Não faça isso \] /Não
    -   Cancelar
    -   Aplicar (se presente)

em \[ que Fazer isso e Não fazer isso são respostas \] \[ \] específicas para a instrução principal.

-   **Não confunda chaves de acesso com teclas de atalho.** Embora as teclas de acesso e as teclas de atalho forneçam acesso de teclado à interface do usuário, elas têm diferentes finalidades e diretrizes.
-   **Sempre que possível, atribua chaves de acesso exclusivas a todos os controles interativos ou seus rótulos.** [Caixas de texto somente leitura são](ctrl-text-boxes.md) controles interativos (porque os usuários podem rolar e copiar texto), portanto, eles se beneficiam das chaves de acesso. **Não atribua chaves de acesso a:**
    -   Botões OK, Cancelar e Fechar. Enter e Esc são usados para suas chaves de acesso. No entanto, sempre atribua uma chave de acesso a um controle que significa OK ou Cancelar, mas tem um rótulo diferente.
-   **Atribua teclas de atalho aos comandos mais usados.** Programas e recursos usados raramente não precisam de teclas de atalho porque os usuários podem usar chaves de acesso.
-   **Não faça uma tecla de atalho a única maneira de executar uma tarefa.** Os usuários também devem ser capazes de usar o mouse ou o teclado com teclas tab, seta e acesso.
-   **Não atribua significados diferentes a teclas de atalho conhecidas.** Como eles são memorizados, significados inconsistentes para atalhos conhecidos são frustrantes e propensos a erros.
-   **Não tente atribuir teclas de atalho do programa em todo o sistema.** As teclas de atalho do programa terão efeito somente quando o programa tiver o foco de entrada.

## <a name="mouse"></a>Mouse

-   **Nunca exigir que os usuários cliquem em um objeto para determinar se ele é clicável.** Os usuários devem ser capazes de determinar a capacidade de clique somente pela inspeção visual.
    -   A interface do usuário primária (como botões de commit) deve ter uma capacidade de clique estático. Os usuários não devem ter que passar o mouse para descobrir a interface do usuário primária.
    -   A interface do usuário secundária (como comandos secundários ou controles de divulgação progressiva) pode exibir sua responsabilidade de clique ao passar o mouse.
    -   Os links de texto devem sugerir estaticamente o texto do link e exibir a capacidade de clique (sublinhado ou outra alteração de apresentação, com ponteiro de mão) ao passar o mouse.
    -   Os links gráficos exibem apenas um ponteiro de mão ao passar o mouse.
-   **Use o ponteiro de mão (ou "seleção de link") somente para links de texto e gráficos.** Caso contrário, os usuários teriam que clicar em objetos para determinar se são links.

## <a name="dialog-boxes"></a>Caixas de diálogo

-   **As caixas de diálogo modais exigem interação, portanto, use-as para coisas às qual os usuários devem responder antes de continuar com suas tarefas.** Certifique-se de que a interrupção seja justificada, como para tarefas críticas ou pouco frequentes que exigem conclusão. Caso contrário, considere alternativas sem modo.
-   **As caixas de diálogo sem modo não exigem interação, portanto, use-as quando os usuários precisam alternar entre uma caixa de diálogo e a janela do proprietário.** Eles são mais usados para tarefas frequentes, repetitivas ou contínuas. No entanto, faixas de opções, barras de ferramentas e janelas de paleta geralmente são alternativas melhores.

## <a name="property-sheets"></a>Folhas de propriedade

-   **Certifique-se de que as propriedades sejam necessárias.** Não atrapalha suas páginas de propriedades com propriedades desnecessárias apenas para evitar tomar decisões de design difíceis.
-   **Apresentar propriedades em termos de metas do usuário em vez de tecnologia.** Só porque uma propriedade configura uma tecnologia específica não significa que você deve apresentar a propriedade em termos dessa tecnologia.
    -   Se você precisa apresentar configurações em termos de tecnologia (talvez porque os usuários reconheçam o nome da tecnologia), inclua uma breve descrição do benefício do usuário.
-   **Use rótulos de tabulação específicos e significativos.** Evite rótulos de guia genéricos que podem ser aplicados a qualquer guia, como Geral, Avançado ou Configurações.
-   **Evite páginas gerais.** Você não precisa ter uma página Geral. Use uma página Geral somente se:
    -   As propriedades se aplicam a várias tarefas e são significativas para a maioria dos usuários. Não coloque propriedades especializadas ou avançadas em uma página Geral, mas você pode torná-las acessíveis por meio de um botão de comando na página Geral.
    -   As propriedades não se ajustam a uma categoria mais específica. Se fizerem isso, use esse nome para a página.
-   **Evite páginas avançadas.** Use uma página Avançado somente se:
    -   As propriedades se aplicam a tarefas incomuns e são significativas principalmente para usuários avançados.
    -   As propriedades não se ajustam a uma categoria mais específica. Se fizerem isso, use esse nome para a página.
-   **Não use guias se uma janela de propriedade tiver apenas uma única guia e não for extensível.** Use uma caixa de diálogo regular com OK, Cancelar e um botão Aplicar opcional. No entanto, as janelas de propriedades extensíveis (que podem ser estendidas por terceiros) devem usar guias.

## <a name="wizards"></a>Assistentes

-   **Considere alternativas leves primeiro, como caixas de diálogo, painéis de tarefas ou páginas individuais.** Os assistentes são uma interface do usuário pesada, mais usada para tarefas de várias etapas e executadas raramente. Você não precisa usar assistentes– você pode fornecer informações úteis e assistência em qualquer interface do usuário.
-   **Use Avançar somente ao avançar para a próxima página sem compromisso.** Avançar para a próxima página é considerado um compromisso quando seu efeito não pode ser desfeito clicando em Voltar ou Cancelar.
-   **Use Voltar somente para corrigir erros.** Além de corrigir erros, os usuários não devem ter que clicar em Voltar para fazer progresso em uma tarefa.
-   **Quando os usuários estão se comprometendo com uma tarefa, use um botão de confirmação que seja uma resposta específica à instrução principal (por exemplo, Imprimir, Conexão ou Iniciar).** Não use rótulos genéricos como Next (o que não implica compromisso) ou Concluir (que não é específico) para comprometer uma tarefa. Os rótulos nesses botões de confirmação devem fazer sentido por conta própria. Sempre inicie rótulos de botão de commit com um verbo. **Exceções:**
    -   Use Concluir quando as respostas específicas ainda são genéricas, como Salvar, Selecionar, Escolher ou Obter.
    -   Use Concluir para alterar uma configuração específica ou uma coleção de configurações.
-   **Use links de comando somente para opções, não compromissos.** Botões de commit específicos indicam o compromisso muito melhor do que os links de comando em um assistente.
-   **Ao usar links de comando, oculta o botão Próximo, mas deixe o botão Cancelar.**
-   **Use Fechar para Follow-Up e Páginas de conclusão.** Não use Cancelar porque fechar a janela não abandonará nenhuma alteração ou ação feita neste ponto. Não use Done porque ele não é um verbo imperativo.
-   **Não use "assistente" em nomes de assistente.** Por exemplo, use "Conexão para uma rede" em vez de "Rede Assistente de Instalação". No entanto, é aceitável referir-se a assistentes como assistentes. Por exemplo: "Se você estiver configurando uma rede pela primeira vez, poderá obter ajuda usando o Conexão para um assistente de rede".
-   **Preservar seleções de usuário por meio da navegação.** Por exemplo, se o usuário fizer alterações, clicar em Voltar e em Próximo, essas alterações deverão ser preservadas. Os usuários não esperam ter que inserir as alterações de forma re-inserir, a menos que tenham optado explicitamente por desemá-las.

## <a name="wizard-pages"></a>Páginas do Assistente

-   **Concentre-se na tomada de decisão eficiente.** Reduza o número de páginas para se concentrar nos fundamentos. Consolide páginas relacionadas e tire páginas opcionais do fluxo principal. Fazer com que os usuários cliquem completamente em Próximo por meio do assistente pode parecer uma boa experiência no início, mas se os usuários nunca precisam alterar os padrões, as páginas provavelmente serão desnecessárias.
-   **Não use páginas de boas-vindas — faça com que a primeira página seja funcional sempre que possível.** Use uma página Ponto de Partida opcional somente quando:
    -   O assistente tem pré-requisitos necessários para concluir o assistente com êxito.
    -   Os usuários podem não entender a finalidade do assistente com base em sua primeira página Escolha e não há espaço para mais explicações.
    -   A instrução principal para Ponto de Partida páginas é "Antes de começar:".
-   **Em páginas nas quais os usuários são solicitados a fazer escolhas, otimize para os casos mais prováveis.** Esses tipos de páginas devem apresentar opções reais, não apenas instruções.
    -   Se você não usar uma página Ponto de Partida, explique a finalidade do assistente na parte superior da primeira página de opções.
-   **Use Páginas de confirmação para deixar claro quando os usuários estão se comprometendo com a tarefa.** Normalmente, a página Confirmação é a última página de opções e o botão Próximo é rotulado de novo para indicar a tarefa que está sendo comprometida.
    -   Não use páginas de Resumo que simplesmente resumem as seleções anteriores do usuário, a menos que a tarefa seja arriscada (envolvendo segurança ou perda de tempo ou dinheiro) ou haja uma boa chance de os usuários não entenderem suas seleções e precisem revisá-las.
-   **Não use páginas parabéns que não fazem nada além de encerrar o assistente.** Se os resultados do assistente são claramente aparentes para os usuários, basta fechar o assistente no botão de confirmação final.
    -   Use Follow-Up páginas quando houver tarefas relacionadas que os usuários provavelmente realizarão como acompanhamento. Evite tarefas de acompanhamento familiares, como "Enviar uma mensagem de email".
    -   Use Páginas de conclusão somente quando os resultados não estão visíveis e não há uma maneira melhor de fornecer comentários para a conclusão da tarefa.
    -   Os assistentes que têm páginas Progresso devem usar uma página conclusão ou Follow-Up página para indicar a conclusão da tarefa. Para tarefas de execução longa, feche o assistente na página Confirmação e use notificações para fazer comentários.

## <a name="error-messages"></a>Mensagens de erro

-   **Não dê mensagens de erro quando os usuários não têm** probabilidade de executar uma ação ou alterar seu comportamento como resultado da mensagem. Se não houver nenhuma ação que os usuários possam tomar ou se o problema não for significativo, suprime a mensagem de erro.
-   **Sempre que possível, propor uma solução para que os usuários possam corrigir o problema.** No entanto, certifique-se de que a solução proposta provavelmente resolva o problema. Não perca tempo dos usuários sugerindo soluções possíveis, mas improváveis.
-   **Seja específico.** Evite palavras vaga, como erro de sintaxe e operação ilegal. Forneça nomes, locais e valores específicos dos objetos envolvidos.
-   **Não use frases que responsabilizam o usuário ou implicam em erro do usuário.** Evite usar você e seu na frase. Embora a voz ativa seja geralmente preferencial, use a voz passiva quando o usuário for o assunto e poderá se sentir responsável pelo erro se a voz ativa tiver sido usada.
-   **Não use OK para mensagens de erro.** Os usuários não visualizam erros como sendo OK. Se a mensagem de erro não tiver nenhuma ação direta, use Fechar.
-   **Não use as seguintes palavras:**
    -   Erro, falha (use o problema em vez disso)
    -   Falha ao (não é possível usar em vez disso)
    -   Ilegal, inválido, inválido (use incorreto ou inválido em vez disso)
    -   Anular, encerrar, encerrar (usar parar em vez disso)
    -   Catastrófico, fatal (use sério em vez disso)

Esses termos são desnecessários e contrários ao tom incentivador de Windows. Em vez disso, um ícone [de erro, quando usado corretamente,](vis-std-icons.md)comunica suficientemente que há um problema.

-   **Não acompanhe mensagens de erro com efeitos de som.** Fazer isso é jarring e desnecessário.

## <a name="warning-messages"></a>Mensagens de aviso

-   **Avisos descrevem uma condição que pode causar um problema no futuro.** Avisos não são erros ou perguntas, portanto, não expresse perguntas de rotina como avisos.
-   **Não dê mensagens de aviso quando os usuários não têm probabilidade de executar uma ação ou alterar seu comportamento como resultado da mensagem.** Se não houver nenhuma ação que os usuários possam tomar ou se a condição não for significativa, suprime a mensagem de aviso.

## <a name="confirmations"></a>Confirmações

-   **Não use confirmações desnecessárias.** Use confirmações somente quando:
    -   Há um motivo claro para não continuar e uma chance razoável de que, às vezes, os usuários não continuarão.
    -   A ação tem consequências significativas ou não pode ser facilmente desfeita.
    -   A ação tem consequências das quais os usuários podem não estar cientes.
    -   Continuar com a ação exige que os usuários façam uma escolha que não tenha um padrão adequado.
    -   Considerando o contexto atual, é provável que os usuários tenham executado uma ação com erro.
-   **Confirmações de frase como uma pergunta sim ou não e fornecem respostas sim ou nenhuma.** Ao contrário de outros tipos de caixas de diálogo, as confirmações são projetadas para impedir que os usuários tomam decisões rápidas. Se os usuários não pensarem na resposta, uma confirmação não terá valor.

## <a name="icons"></a>Ícones

-   **Todos os ícones devem seguir as diretrizes** [do ícone de estilo](vis-icons.md)aero. Substitua todos Windows ícones no estilo XP.
-   **Escolha ícones padrão com base no tipo de mensagem, não na gravidade do problema subjacente:**
    -   **Erro.** Um erro ou problema que ocorreu.
    -   **Aviso.** Uma condição que pode causar um problema no futuro.
    -   **Informações.** Informações úteis.

Se um problema combinar diferentes tipos de mensagem, concentre-se no aspecto mais importante no quais os usuários precisam agir.

-   **Os ícones devem sempre corresponder à instrução principal ou a outro texto correspondente.**
-   **Ícones de erro não são necessários para problemas de entrada de usuário não críticos.** No entanto, os ícones são necessários para erros in-loco, porque, caso contrário, esses comentários contextuais seriam muito fáceis de ignorar.
-   **Não use ícones de aviso para "suavizar" erros não críticos.** Erros não são avisos; em vez disso, aplique as diretrizes de ícone de erro.
-   **Para caixas de diálogo de pergunta, use ícones de aviso somente para perguntas com consequências significativas.** Não use ícones de aviso para perguntas rotineiras.

## <a name="help"></a>Ajuda

-   **Link para tópicos de ajuda específicos e relevantes.** Não vincule ao home page de ajuda, ao Sumário, a uma lista de resultados da pesquisa ou a uma página que apenas se vincula a outras páginas. Evite vincular a páginas estruturadas como uma grande lista de perguntas frequentes, pois ela força os usuários a procurar aquele que corresponda ao link em que eles clicaram. Não vincule a tópicos de ajuda específicos que não são relevantes e úteis para a tarefa em questão. Nunca vincular a páginas vazias.
-   **Não coloque links de ajuda em todas as janelas ou páginas para fins de consistência.** Fornecer um link de ajuda em um único lugar não significa que você precisa fornecê-los em todos os lugares.
-   **Sempre que possível, a ajuda de frase vincula o texto em termos da pergunta principal respondida pelo conteúdo da ajuda.** Não use a frase "Saiba mais sobre" ou "obter ajuda com este".
-   **Use o link de ajuda inteiro para o texto do link,** não apenas as palavras-chave.
-   **Use frases completas.**
-   **Não use pontuação final ou reticências, exceto pontos de interrogação.**
-   **Se o conteúdo da ajuda estiver online, torne-o claro no texto do link.** Isso ajuda a tornar o resultado dos links previsíveis.

