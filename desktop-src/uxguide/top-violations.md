---
title: Lista de verificação de UX para aplicativos de área de trabalho
description: Aqui está uma coleção de algumas das diretrizes importantes no guia do UX. Você pode usar isso como uma lista de verificação para verificar se a interface do usuário do programa obtém esses itens importantes.
ms.assetid: 4705a807-5949-4957-8ea6-70871beaf8e0
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: d1006b7ad9de30941b6ceb4cc7282ec578450840
ms.sourcegitcommit: 8755905962e156f29203705d09d6df8b7d0e2fca
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/25/2021
ms.locfileid: "105763322"
---
# <a name="ux-checklist-for-desktop-applications"></a>Lista de verificação de UX para aplicativos de área de trabalho

> [!NOTE]
> Este guia de design foi criado para o Windows 7 e não foi atualizado para versões mais recentes do Windows. Grande parte da orientação ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais](/windows/uwp/design/).

Aqui está uma coleção de algumas das diretrizes importantes no guia do UX. Você pode usar isso como uma lista de verificação para verificar se a interface do usuário do programa obtém esses itens importantes.

## <a name="windows"></a>Windows

-   **Suporte à resolução mínima efetiva do Windows de 800x600 pixels.** Para interfaces de usuário críticas (UIs) que devem funcionar no modo de segurança, dê suporte a uma [resolução efetiva](glossary.md) de 640x480 pixels. Certifique-se de considerar o espaço usado pela barra de tarefas reservando 48 [pixels relativos](glossary.md) verticais para o Windows exibido com a barra de tarefas.
-   **Otimize layouts de janela redimensionáveis para uma resolução efetiva de 1024x768 pixels.** Redimensione automaticamente essas janelas para resoluções de tela mais baixa de uma maneira que ainda está funcional.
-   **Certifique-se de testar suas janelas em 96 pontos por polegada (DPI) (em 800x600 pixels), 120 DPI (a 1024x768 pixels) e 144 DPI (em 1200x900 pixels).** Verifique se há problemas de layout, como recorte de controles, texto e janelas, e alargamento de ícones e bitmaps.
-   **Para programas com cenários de uso móvel e de toque, otimize para 120 dpi.** As telas de alto dpi atualmente são predominantes em PCs móveis e de toque.
-   **Se uma janela for uma janela de propriedade, você a exibirá inicialmente "centralizado" na janela do proprietário.** Nunca abaixo de. Para exibição subsequente, considere exibi-lo em seu último local (relativo à janela do proprietário) se isso for mais conveniente.
-   **Se uma janela for contextual, sempre a exibirá perto do objeto do qual foi iniciada.** No entanto, coloque-o fora do caminho (preferivelmente desloca para baixo e para a direita) para que o objeto não seja coberto pela janela.

## <a name="layout"></a>Layout

-   **Dimensionar controles e painéis dentro de uma janela para corresponder ao conteúdo típico.** Evite texto truncado e suas reticências associadas. Os usuários nunca devem ter que interagir com uma janela para exibir seu conteúdo típico, reservar redimensionamento e rolagem para conteúdo excepcionalmente grande. Verifique especificamente:
    -   **Tamanhos de controle.** Dimensionar controles para seu conteúdo típico, tornando os controles mais largos, mais altos ou de várias linhas, se necessário. Controles de tamanho para eliminar ou reduzir a rolagem no Windows com bastante espaço disponível. Além disso, nunca deve haver rótulos truncados ou texto truncado dentro do Windows com muito espaço disponível. No entanto, para facilitar a leitura do texto, considere limitar larguras de linha a 65 caracteres.
    -   **Larguras de coluna.** Verifique se as colunas de exibição de lista têm o dimensionamento padrão, mínimo e máximo adequado. Escolher lista exibe as larguras de coluna padrão que não resultam em texto truncado, especialmente se houver espaço disponível na exibição de lista.
    -   **Balanceamento de layout.** O layout de uma janela deve parecer aproximadamente equilibrado. Se o layout ficar pesado para a esquerda, considere tornar os controles mais largos e mover alguns controles para a direita.
    -   **Redimensionamento de layout.** Quando uma janela é redimensionável e os dados são truncados, certifique-se de que os tamanhos de janela maiores mostrem mais dados. Quando os dados são truncados, os usuários esperam redimensionar janelas para mostrar mais informações.
-   **Defina um tamanho mínimo de janela se houver um tamanho abaixo do qual o conteúdo não seja mais utilizável.** Para controles redimensionáveis, defina tamanhos mínimos de elemento redimensionáveis para seus menores tamanhos funcionais, como larguras de coluna funcionais mínimas em exibições de lista.

## <a name="text"></a>Texto

-   **Use termos comuns e de conversação quando puder.** Concentre-se nas metas do usuário, não na tecnologia. Isso é especialmente eficaz se você estiver explicando uma ação ou um conceito técnico complexo. Imagine-se examinando o ressalto do usuário e explicando como realizar a tarefa.
-   **Seja educado, de apoio e incentivador.** O usuário nunca deve se sentir à vontade, à culpa ou intimidação.
-   **Remova o texto redundante.** Procure texto redundante em títulos de janela, instruções principais, instruções complementares, áreas de conteúdo, links de comando e botões de confirmação. Em geral, deixe texto completo nas instruções principais e nos controles interativos e remova qualquer redundância dos outros locais.
-   **Use a capitalização de estilo de título para títulos e a capitalização de estilo de frase para todos os outros elementos da interface do usuário.** Fazer isso é mais apropriado para o tom do Windows.
    -   **Exceção:** Para aplicativos herdados, você pode usar a capitalização de estilo de título para botões de comando, menus e títulos de coluna, se necessário, para evitar a mistura de estilos de capitalização.
-   **Para nomes de recursos e tecnologias, seja conservador em maiúsculas.** Normalmente, somente os principais componentes devem ser capitalizados (usando a capitalização de estilo de título).
-   **Para nomes de recursos e tecnologias, seja consistente em maiúsculas.** Se o nome aparecer mais de uma vez em uma tela de interface do usuário, ele sempre deverá aparecer da mesma maneira. Da mesma forma, em todas as telas de interface do usuário no programa, o nome deve ser apresentado consistentemente.
-   **Não coloque maiúsculas nos nomes dos elementos genéricos da interface do usuário,** como barra de ferramentas, menu, barra de rolagem, botão e ícone.
    -   **Exceções:** Barra de endereços, barra de links, faixa de faixas.
-   **Não use todas as letras maiúsculas para as teclas do teclado.** Em vez disso, siga as letras maiúsculas usadas por teclados padrão ou em minúsculas se a chave não estiver rotulada como um painel.
-   **As reticências significam inintegridade.** Use reticências no texto da interface do usuário da seguinte maneira:
    -   **Comandos.** Indique que um comando precisa de informações adicionais. Não use reticências sempre que uma ação exibir outra janela — somente quando forem necessárias informações adicionais. Os comandos cujo verbo implícito é mostrar outra janela não têm uma elipse, como avançado, ajuda, opções, propriedades ou configurações.
    -   **Dado.** Indica que o texto está truncado.
    -   **Las.** Indique que uma tarefa está em andamento (por exemplo, "pesquisando...").

**Dica:** O texto truncado em uma janela ou página com espaço não utilizado indica um layout insatisfatório ou um tamanho de janela padrão muito pequeno. Busque layouts e tamanhos de janela padrão que eliminem ou reduzem a quantidade de texto truncado. Veja [Layout](vis-layout.md) para obter mais informações.

-   **Não use um texto azul que não seja um link, pois os usuários podem pressupor que ele é um link.** Use negrito ou um tom de cinza onde, caso contrário, você usaria texto colorido.
-   **Use em negrito para chamar atenção para texto que os usuários devem ler.**
-   **Use a instrução principal para explicar de forma concisa o que os usuários devem fazer em uma determinada janela ou página.** Boas instruções principais comunicam o objetivo do usuário em vez de se concentrar apenas na manipulação da interface do usuário.
-   **Expresse a instrução principal na forma de uma direção imperativa ou uma pergunta específica.**
-   **Não faça períodos no final dos rótulos de controle ou nas instruções principais.**
-   **Use um espaço entre as frases.** Não dois.

## <a name="controls"></a>Controles

-   **Geral**
    -   **Rotular cada controle ou grupo de controles. Exceção**
        -   Caixas de texto e listas suspensas podem ser rotuladas usando prompts.
        -   Controles subordinados usam o rótulo de seu controle associado. Controles de rotação são sempre controles subordinados.
    -   **Para todos os controles, selecione o mais seguro (para evitar a perda de dados ou acesso ao sistema), o valor mais seguro por padrão.** Se não houver fatores de segurança e segurança, selecione o valor mais provável ou conveniente.
    -   **Prefira controles restritos.** Use controles restritos como listas e controles deslizantes sempre que possível, em vez de controlar unrestrição como caixas de texto, para reduzir a necessidade de entrada de texto.
    -   **Reconsidere os controles desabilitados.** Controles desabilitados podem ser difíceis de usar porque os usuários literalmente precisam deduzir por que estão desabilitados. Desabilite um controle quando os usuários esperam que eles se apliquem e podem facilmente deduzir por que o controle está desabilitado. Remova o controle quando não há nenhuma maneira para os usuários habilitá-lo ou se eles não esperam que ele seja aplicado, ou deixe-o habilitado, mas forneça uma mensagem de erro quando ele for usado incorretamente.
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
        -   Desenhe o texto do prompt em cinza itálico e o texto de entrada real em preto romano.
        -   O texto do prompt não deve ser editável e deve desaparecer quando os usuários clicarem na guia ou na caixa de texto.
            -   **Exceção:** Se a caixa de texto tiver o foco de entrada padrão, o prompt será exibido e desaparece quando o usuário começa a digitar.
    -   Não use pontuação final ou reticências.
-   **Notificações**
    -   **Use notificações para eventos que não estão relacionados à atividade do usuário atual, não exigem ação imediata do usuário e os usuários podem ignorar livremente.**
    -   **Não incorra em notificações:**
        -   **Use notificações somente se precisar.** Quando você exibe uma notificação, você está potencialmente interrompendo os usuários ou até mesmo irritantes. Certifique-se de que a interrupção seja justificada.
        -   **Use notificações para eventos não críticos ou situações que não exigem ação imediata do usuário.** Para eventos críticos ou situações que exigem ação imediata do usuário, use um elemento de interface do usuário alternativo (como uma caixa de diálogo modal).
        -   **Não use notificações para anúncios de recursos!**

## <a name="keyboard"></a>Keyboard

-   **Atribua o foco de entrada inicial ao controle que os usuários têm mais probabilidade de interagir com o primeiro,** que é geralmente o primeiro controle interativo. Se o primeiro controle interativo não for uma boa opção, considere alterar o layout da janela.
-   **Atribuir tabulações para todos os controles interativos, incluindo caixas de edição somente leitura. Exceção**
    -   Agrupar conjuntos de controles relacionados que se comportam como um único controle, como botões de opção. Esses grupos têm uma única parada de tabulação.
    -   Contém adequadamente os grupos para que as teclas de direção passem para frente e para trás dentro do grupo e permaneçam dentro do grupo.
-   **A ordem de tabulação deve fluir da esquerda para a direita, de cima para baixo.** Em geral, a ordem de tabulação deve seguir a ordem de leitura. Considere fazer exceções para controles comumente usados colocando-os anteriormente na ordem de tabulação. Tab deve percorrer todas as paradas de tabulação em ambas as direções sem parar. Dentro de um grupo, a ordem de tabulação deve estar em ordem sequencial, sem exceções.
-   **Dentro de uma parada de tabulação, a ordem da tecla de direção deve fluir da esquerda para a direita, de cima para baixo,** sem exceções. As teclas de direção devem percorrer todos os itens em ambas as direções sem parar.
-   **Apresente os botões de confirmação na seguinte ordem:**
    -   OK/ \[ fazer o \] /Yes
    -   \[Não faça isso \] /não
    -   Cancelar
    -   Aplicar (se houver)

onde \[ fazer isso \] e \[ não fazer isso \] são respostas específicas para a instrução principal.

-   **Não confunda chaves de acesso com teclas de atalho.** Embora as teclas de acesso e as chaves de atalho forneçam acesso de teclado à interface do usuário, elas têm finalidades e diretrizes diferentes.
-   **Sempre que possível, atribua chaves de acesso exclusivas a todos os controles interativos ou seus rótulos.** [Caixas de texto somente leitura](ctrl-text-boxes.md) são controles interativos (porque os usuários podem rolar e copiar texto), para que se beneficiem das chaves de acesso. **Não atribua chaves de acesso para:**
    -   Botões OK, cancelar e fechar. Enter e ESC são usados para suas chaves de acesso. No entanto, sempre atribua uma chave de acesso a um controle que significa OK ou cancelar, mas tem um rótulo diferente.
-   **Atribua teclas de atalho para os comandos usados com mais frequência.** Os programas e recursos usados raramente não precisam de teclas de atalho porque os usuários podem usar chaves de acesso em vez disso.
-   **Não crie uma tecla de atalho a única maneira de executar uma tarefa.** Os usuários também devem ser capazes de usar o mouse ou o teclado com teclas de tabulação, seta e acesso.
-   **Não atribua diferentes significados a teclas de atalho bem conhecidas.** Como eles são memorizados, os significados inconsistentes para atalhos bem conhecidos são frustrantes e sujeitos a erros.
-   **Não tente atribuir teclas de atalho do programa em todo o sistema.** As teclas de atalho do programa terão efeito somente quando o seu programa tiver o foco de entrada.

## <a name="mouse"></a>Mouse

-   **Nunca exija que os usuários cliquem em um objeto para determinar se ele é clicável.** Os usuários devem ser capazes de determinar a possibilidade de clicar por inspeção visual apenas.
    -   A interface do usuário primária (como botões de confirmação) deve ter uma premissa de clique estático. Os usuários não devem ter que focalizar para descobrir a interface do usuário principal.
    -   A interface do usuário secundária (como comandos secundários ou controles de divulgação progressiva) pode exibir a sua preposição de clique ao focalizar.
    -   Os links de texto devem sugerir estaticamente o texto do link e, em seguida, exibir a sua preposição de clique (sublinhado ou outra alteração de apresentação, com ponteiro à mão) ao focalizar.
    -   Os links gráficos exibem apenas um ponteiro de mão ao focalizar.
-   **Use o ponteiro de mão (ou "vincular seleção") somente para links de texto e gráficos.** Caso contrário, os usuários teriam que clicar em objetos para determinar se eles são links.

## <a name="dialog-boxes"></a>Caixas de diálogo

-   **As caixas de diálogo modais exigem interação, portanto, use-as para as coisas que os usuários devem responder antes de continuar com sua tarefa.** Certifique-se de que a interrupção seja justificada, como para tarefas críticas ou pouco frequentes que exigem a conclusão. Caso contrário, considere alternativas sem janela restrita.
-   **As caixas de diálogo sem janela restrita não exigem interação, portanto, use-as quando os usuários precisarem alternar entre uma caixa de diálogo e a janela do proprietário.** Elas são mais bem usadas para tarefas frequentes, repetitivas ou contínuas. No entanto, as faixas de opções, as barras de ferramentas e as janelas de paleta geralmente são melhores alternativas.

## <a name="property-sheets"></a>Folhas de propriedade

-   **Verifique se as propriedades são necessárias.** Não contorne suas páginas de propriedades com propriedades desnecessárias apenas para evitar tomar decisões de design rígido.
-   **Apresente as propriedades em termos de metas de usuário em vez de tecnologia.** Só porque uma propriedade configura uma tecnologia específica não significa que você deve apresentar a propriedade em termos dessa tecnologia.
    -   Se você precisar apresentar as configurações em termos de tecnologia (talvez porque seus usuários reconheçam o nome da tecnologia), inclua uma breve descrição do benefício do usuário.
-   **Use rótulos de guias específicos e significativos.** Evite rótulos de guia genéricos que possam se aplicar a qualquer guia, como geral, avançado ou configurações.
-   **Evite páginas gerais.** Não é necessário ter uma página geral. Use uma página Geral somente se:
    -   As propriedades se aplicam a várias tarefas e são significativas para a maioria dos usuários. Não coloque propriedades especializadas ou avançadas em uma página geral, mas você pode torná-las acessíveis por meio de um botão de comando na página geral.
    -   As propriedades não se ajustam a uma categoria mais específica. Em vez disso, use esse nome para a página.
-   **Evite páginas avançadas.** Use uma página avançada somente se:
    -   As propriedades se aplicam a tarefas não comuns e são significativas principalmente para usuários avançados.
    -   As propriedades não se ajustam a uma categoria mais específica. Em vez disso, use esse nome para a página.
-   **Não use guias se uma janela de propriedades tiver apenas uma única guia e não for extensível.** Use uma caixa de diálogo normal com OK, cancelar e um botão de aplicação opcional em vez disso. No entanto, as janelas de propriedades extensíveis (que podem ser estendidas por terceiros) devem usar guias.

## <a name="wizards"></a>Assistentes

-   **Considere as alternativas leves primeiro, como caixas de diálogo, painéis de tarefas ou páginas únicas.** Os assistentes são uma interface do usuário pesada, melhor usada para tarefas de várias etapas executadas com pouca frequência. Você não precisa usar assistentes — você pode fornecer informações úteis e assistência em qualquer interface do usuário.
-   **Use o próximo somente ao avançar para a próxima página sem compromisso.** Avançar para a próxima página é considerado um compromisso quando seu efeito não pode ser desfeito ao clicar em voltar ou cancelar.
-   **Use novamente para corrigir erros.** Além de corrigir erros, os usuários não precisam clicar em voltar para fazer o progresso em uma tarefa.
-   **Quando os usuários estão confirmando uma tarefa, use um botão confirmar que seja uma resposta específica para a instrução principal (por exemplo, imprimir, conectar ou iniciar).** Não use rótulos genéricos como Next (que não implicam em compromisso) ou Finish (que não é específico) para confirmar uma tarefa. Os rótulos desses botões de confirmação devem fazer sentido por conta própria. Sempre iniciar os rótulos do botão de confirmação com um verbo. **Exceção**
    -   Use concluir quando as respostas específicas ainda forem genéricas, como salvar, selecionar, escolher ou obter.
    -   Use concluir para alterar uma configuração específica ou uma coleção de configurações.
-   **Use links de comando somente para escolhas, não para compromissos.** Botões de confirmação específicos indicam o compromisso muito melhor do que os links de comando em um assistente.
-   **Ao usar links de comando, oculte o botão Avançar, mas deixe o botão Cancelar.**
-   **Use fechar para obter Follow-Up e páginas de conclusão.** Não use cancelar porque fechar a janela não abandonará nenhuma alteração ou ação feita neste momento. Não use o Done porque não é um verbo imperativo.
-   **Não use "assistente" em nomes de assistente.** Por exemplo, use "conectar-se a uma rede" em vez de "Assistente de configuração de rede". No entanto, é aceitável referir-se a assistentes como assistentes. Por exemplo: "se você estiver configurando uma rede pela primeira vez, poderá obter ajuda usando o assistente conectar-se a uma rede".
-   **Preserve as seleções de usuário por meio de navegação.** Por exemplo, se o usuário fizer alterações, clicar em voltar e, em seguida, essas alterações deverão ser preservadas. Os usuários não esperam ter de reinserir as alterações, a menos que decidam explicitamente desmarcá-las.

## <a name="wizard-pages"></a>Páginas do Assistente

-   **Concentre-se na tomada de decisão eficiente.** Reduza o número de páginas para se concentrar no Essentials. Consolide páginas relacionadas e faça páginas opcionais fora do fluxo principal. Fazer com que os usuários cliquem em Avançar completamente por meio do assistente pode parecer uma boa experiência inicialmente, mas se os usuários nunca precisarem alterar os padrões, as páginas provavelmente serão desnecessárias.
-   **Não use páginas de boas-vindas — torne a primeira página funcional sempre que possível.** Use uma página de Introdução opcional somente quando:
    -   O assistente tem pré-requisitos que são necessários para concluir o assistente com êxito.
    -   Os usuários podem não entender a finalidade do assistente com base em sua primeira página de escolha e não há espaço para mais explicações.
    -   A instrução principal para as páginas Introdução é "antes de começar:".
-   **Em páginas nas quais os usuários são solicitados a fazer escolhas, otimize para os casos mais prováveis.** Esses tipos de páginas devem apresentar opções reais, não apenas instruções.
    -   Se você não usar uma página Introdução, explique a finalidade do assistente na parte superior da primeira página de opções.
-   **Use as páginas de confirmação para torná-las claras quando os usuários estiverem confirmando a tarefa.** Geralmente, a página de confirmação é a última página de opções e o botão Avançar é rotulado novamente para indicar a tarefa que está sendo confirmada.
    -   Não use páginas de resumo que meramente resumam as seleções anteriores do usuário, a menos que a tarefa seja arriscada (envolvendo segurança ou perda de tempo ou dinheiro) ou haja uma boa chance de que os usuários não compreendam suas seleções e precisem examiná-las.
-   **Não use páginas de parabenização que não façam nada, mas terminem o assistente.** Se os resultados do assistente forem claramente aparentes para os usuários, basta fechar o assistente no botão de confirmação final.
    -   Use Follow-Up páginas quando houver tarefas relacionadas que os usuários provavelmente farão como acompanhamento. Evite tarefas de acompanhamento familiares, como "Enviar uma mensagem de email".
    -   Use as páginas de conclusão somente quando os resultados não estiverem visíveis e não houver uma maneira melhor de fornecer comentários para a conclusão da tarefa.
    -   Os assistentes que têm páginas de progresso devem usar uma página de conclusão ou Follow-Up para indicar a conclusão da tarefa. Para tarefas de execução longa, feche o assistente na página de confirmação e use as notificações para fornecer comentários.

## <a name="error-messages"></a>Mensagens de erro

-   **Não forneça mensagens de erro quando não for provável que os usuários executem uma ação ou alterem seu comportamento** como resultado da mensagem. Se não houver ação que os usuários podem executar ou se o problema não for significativo, suprima a mensagem de erro.
-   **Sempre que possível, proponha uma solução para que os usuários possam corrigir o problema.** No entanto, certifique-se de que a solução proposta provavelmente resolverá o problema. Não gaste o tempo dos usuários sugerindo soluções possíveis, mas que podem ser investigadas.
-   **Seja específico.** Evite palavras vagas, como erro de sintaxe e operação ilegal. Forneça nomes, locais e valores específicos dos objetos envolvidos.
-   **Não use frases que culpam o usuário ou implicam erro do usuário.** Evite usar você e seu na formulação. Embora a voz ativa seja geralmente preferida, use a voz passiva quando o usuário for o assunto e poderá sentir a culpa do erro se a voz ativa fosse usada.
-   **Não use OK para mensagens de erro.** Os usuários não exibem erros como OK. Se a mensagem de erro não tiver nenhuma ação direta, use fechar em vez disso.
-   **Não use as seguintes palavras:**
    -   Erro, falha (em vez disso, use o problema)
    -   Falha ao (em vez disso, use não é possível)
    -   Inválido, inválido, incorreto (use incorreto ou não válido em vez disso)
    -   Abort, Kill e Terminate (use parar em vez disso)
    -   Catastrófico, fatal (em vez disso, use grave)

Esses termos são desnecessários e ao contrário do Tom incentivado do Windows. Em vez disso, um ícone de erro, [quando usado corretamente](vis-std-icons.md), comunica suficientemente que há um problema.

-   **Não acompanha mensagens de erro com efeitos de som.** Fazer isso é dissonante e desnecessário.

## <a name="warning-messages"></a>Mensagens de aviso

-   **Os avisos descrevem uma condição que pode causar um problema no futuro.** Avisos não são erros ou perguntas, portanto, não frases perguntas rotineiras como avisos.
-   **Não forneça mensagens de aviso quando não for provável que os usuários executem uma ação ou alterem seu comportamento como resultado da mensagem.** Se não houver ação que os usuários podem executar ou se a condição não for significativa, omita a mensagem de aviso.

## <a name="confirmations"></a>Confirmações

-   **Não use confirmações desnecessárias.** Use confirmações somente quando:
    -   Há um motivo claro para não continuar e uma chance razoável que às vezes os usuários não.
    -   A ação tem consequências significativas ou não pode ser facilmente desfeita.
    -   A ação tem consequências de que os usuários podem não estar cientes.
    -   Prosseguir com a ação requer que os usuários façam uma escolha que não tenha um padrão adequado.
    -   Considerando o contexto atual, é provável que os usuários tenham executado uma ação em caso de erro.
-   **Confirmações de frase como uma pergunta Sim ou não e forneça respostas sim ou não.** Ao contrário de outros tipos de caixas de diálogo, as confirmações são projetadas para impedir que os usuários tomem decisões rápidas. Se os usuários não tiverem pensado em sua resposta, uma confirmação não terá valor.

## <a name="icons"></a>Ícones

-   **Todos os ícones devem aderir às diretrizes de ícone do** [estilo Aero](vis-icons.md). Substitua todos os ícones de estilo do Windows XP.
-   **Escolha ícones padrão com base em seu tipo de mensagem, não a severidade do problema subjacente:**
    -   **Ao.** Erro ou problema ocorrido.
    -   **Alerta.** Uma condição que pode causar um problema no futuro.
    -   **Divulgação.** Informações úteis.

Se um problema combinar tipos de mensagens diferentes, concentre-se no aspecto mais importante em que os usuários precisam agir.

-   **Os ícones devem sempre corresponder à instrução principal ou a outro texto correspondente.**
-   **Ícones de erro não são necessários para problemas de entrada não críticos do usuário.** No entanto, os ícones são necessários para erros in-loco, pois, caso contrário, esses comentários contextuais seriam muito fáceis de se ignorar.
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

