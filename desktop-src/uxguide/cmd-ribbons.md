---
title: Faixas de opções
description: As faixas de palavras são a maneira moderna de ajudar os usuários a localizar, entender e usar comandos de forma eficiente e direta \ 8212; com um número mínimo de cliques, com menos necessidade de recorrer a avaliação e erro e sem precisar consultar a ajuda.
ms.assetid: 8a4699da-9840-4622-9e94-d6d5c4e7708c
ms.custom: contperf-fy21q1
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: cf74a58ae2fd9dda735c419f4ffa42b38d06c18c
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884442"
---
# <a name="ribbons"></a>Faixas de opções

> [!NOTE]
> este guia de design foi criado para o Windows 7 e não foi atualizado para versões mais recentes do Windows. Grande parte da orientação ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais](/windows/uwp/design/).

As faixas de palavras são a maneira moderna de ajudar os usuários a localizar, compreender e usar comandos de forma eficiente e direta com um número mínimo de cliques, com menos necessidade de recorrer a avaliação e erro e sem precisar consultar a ajuda.

Uma faixa de guia é uma barra de comandos que organiza os recursos de um programa em uma série de guias na parte superior de uma janela. O uso de uma faixa de faixas aumenta a capacidade de descoberta de recursos e funções, permite um aprendizado mais rápido do programa como um todo e faz com que os usuários se sintam mais no controle de sua experiência com o programa. Uma faixa de opções pode substituir a barra de menus e as barras de ferramentas tradicionais.

![captura de tela de uma faixa de uma ](images/cmd-ribbons-image1.png)

Uma faixa de uma típica.

As guias da faixa de guia são compostas por grupos, que são um conjunto rotulado de comandos fortemente relacionados. Além de guias e grupos, as faixas de faixa consistem em:

- Um botão de aplicativo, que apresenta um menu de comandos que envolvem fazer algo para ou com um documento ou espaço de trabalho, como comandos relacionados a arquivos.
- Uma barra de ferramentas de acesso rápido, que é uma barra de ferramentas pequena e personalizável que exibe comandos usados com frequência.
- As guias principais são as guias que são sempre exibidas.
- Guias contextuais, que são exibidas somente quando um determinado tipo de objeto é selecionado. As guias que são sempre exibidas são chamadas de guias de núcleo.
- Um conjunto de guias é uma coleção de guias contextuais para um único tipo de objeto. Como os objetos podem ter vários tipos (por exemplo, um cabeçalho em uma tabela que tem uma imagem é de três tipos), pode haver vários conjuntos de guias contextuais exibidos de cada vez.
- Guias modais, que são guias principais exibidas com um modo temporário específico, como visualização de impressão.
- Galerias, que são listas de comandos ou opções apresentadas graficamente. Uma galeria baseada em resultados ilustra o efeito dos comandos ou opções em vez dos próprios comandos. Uma galeria na faixa de faixas é exibida dentro de uma faixa de bits, em vez de uma janela pop-up.
- Dicas de ferramentas aprimoradas, que explicam de forma concisa seus comandos associados e fornecem as teclas de atalho. Eles também podem incluir elementos gráficos e referências para ajudar. As dicas de ferramentas aprimoradas reduzem a necessidade de ajuda relacionada a comandos.
- Inicializadores de caixa de diálogo, que são botões na parte inferior de alguns grupos que abrem caixas de diálogo contendo recursos relacionados ao grupo.

as faixas de faixa foram introduzidas originalmente com o Microsoft Office 2007. para saber por que Office precisa usar as faixas de faixa e os vários problemas que usam uma faixa de faixas, consulte [a história da faixa de](/archive/blogs/jensenh/the-story-of-the-ribbon)visão.

> [!Note]  
> As diretrizes relacionadas a [menus](cmd-menus.md), [barras de ferramentas](cmd-toolbars.md), botões de [comando](ctrl-command-buttons.md)e [ícones](vis-icons.md) são apresentadas em artigos separados.

## <a name="is-this-the-right-user-interface"></a>Esta é a interface do usuário correta?

Para decidir usar uma faixa de uma, considere estas perguntas:

### <a name="program-type"></a>Tipo de programa

- **Que tipo de programa você está projetando?** O tipo de programa é um bom indicador da adequação de uma faixa de opção. As faixas funcionam bem para criação de documentos e programas de criação, bem como visualizadores de documentos e navegadores. As faixas de faixa podem funcionar para outros tipos de programas, mas outras formas de apresentação de comando podem ser mais apropriadas. Em geral, os programas leves devem ter uma apresentação de comando leve.

### <a name="discoverability-and-learning-issues"></a>Problemas de descoberta e de aprendizagem

- **Os usuários têm problemas ao localizar comandos? Os usuários estão solicitando recursos que já estão no programa?** Nesse caso, usar uma faixa de faixas facilitará a localização dos comandos com rótulos autoexplicativos e o agrupamento de comandos relacionados. O uso de uma faixa de opção também escala melhor do que barras de menus e barras de ferramentas para crescimento futuro.
- **Os usuários têm problemas para entender os comandos do programa? Eles costumam recorrer a "avaliação e erro" para selecionar o comando correto ou determinar como os comandos funcionam?** Nesse caso, o uso de uma faixa de bits com comandos orientados a resultados baseados em galerias e visualizações dinâmicas facilita a compreensão dos comandos.

### <a name="command-characteristics"></a>Características do comando

- **Os comandos são apresentados em vários locais? Se o seu programa já existir, os comandos serão apresentados em barras de menus, barras de ferramentas, painéis de tarefas e dentro da própria área de trabalho?** Nesse caso, usar uma faixa de faixas unificará os comandos em um único local, facilitando sua localização.
- **Os comandos se aplicam a toda a janela ou somente a painéis específicos?** As faixas de opções funcionam melhor para comandos que se aplicam a toda a janela ou a objetos específicos. Os comandos in-loco funcionam melhor para os painéis de janela individuais.
- **A maioria dos comandos pode ser apresentada diretamente? Ou seja, os usuários podem interagir com eles usando um único clique? Se os comandos usados com frequência forem acessados em menus e caixas de diálogo, eles poderão ser refatoros para serem diretos?** Embora alguns comandos possam ser apresentados usando menus e caixas de diálogo, a apresentação da maioria dos comandos dessa forma envolve a eficiência de uma faixa de opções, possivelmente tornando uma barra de menus uma opção melhor.

### <a name="command-scale"></a>Escala de comando

- **Há um pequeno número de comandos? Os comandos usados com mais frequência podem ser apresentados facilmente em uma única barra de ferramentas simples?** Usar uma faixa de controle vale a pena se a adição de guias principal e contextual resultar em uma simples guia página inicial que pode ser usada sozinha para executar as tarefas mais comuns. Caso contrário, o benefício de usar uma faixa de faixas pode não justificar seu peso extra para um pequeno número de comandos.
- **Há um grande número de comandos? O uso de uma faixa de faixas requer mais de sete guias principais? Os usuários precisam constantemente alterar as guias para executar tarefas comuns?** Nesse caso, usar barras de ferramentas (que não exigem a alteração de guias) e [janelas de paleta](cmd-toolbars.md) (que podem exigir a alteração de guias, mas pode haver várias abertas por vez) pode ser uma opção mais eficiente.
- **Os usuários tendem a usar um pequeno número de comandos na maior parte do tempo?** Nesse caso, eles podem usar uma faixa de uma fita com eficiência, colocando esses comandos na guia página inicial. A alteração constante de guias tornaria uma faixa de uma forma muito ineficiente.
- **O programa se beneficia de tornar a área de conteúdo do programa o mais grande possível?** Nesse caso, usar uma barra de menus e uma única barra de ferramentas é mais eficiente em termos de espaço do que uma faixa de faixas. No entanto, se o seu programa exigir três ou mais linhas de barras de ferramentas ou usar painéis de tarefas, o uso de uma faixa de faixas será mais eficiente em termos de espaço.
- **Os usuários tendem a trabalhar em uma área específica dentro de uma janela grande no programa por longos períodos de tempo?** Nesse caso, eles se beneficiarão da proximidade das mini-barras de ferramentas, janelas de paletas e comandos diretos. Fazer a viagem de ida e volta da área de trabalho para a faixa de faixas seria muito ineficiente.
- **Para eficiência e flexibilidade, os usuários precisam fazer alterações significativas no conteúdo da apresentação do comando, no local ou no tamanho?** Nesse caso, barras de ferramentas personalizáveis e extensíveis e janelas de paleta são uma opção melhor. Observe que alguns tipos de barras de ferramentas podem ser desencaixados para se tornar janelas de paleta e janelas de paleta podem ser movidas, redimensionadas e personalizadas.

Por fim, considere essa pergunta final: **é o aprimoramento da capacidade de descoberta, da facilidade de aprendizado, da eficiência e da produtividade no custo do espaço extra e da necessidade de guias para organizar os comandos?** Nesse caso, usar uma faixa de opções é uma excelente opção. Se você não tiver certeza, considere o teste de usabilidade de um design baseado em faixa de opção e a comparação com a melhor alternativa.

As faixas de palavras são uma forma nova e atraente de apresentação de comandos e uma ótima maneira de modernizar um programa. Mas, como são convincentes, eles não são a escolha certa para todos os programas.

**Incorreto:**

![captura de tela de uma faixa de faixas com uma calculadora ](images/cmd-ribbons-image2.png)

Não faça isso!

## <a name="seven-most-important-things"></a>Sete coisas mais importantes

1. Escolha uma solução de comando adequada para o tipo de programa. O uso de uma faixa de visão deve fazer com que um programa fique mais simples, mais eficiente e fácil de usar nunca o oposto. Se estiver usando uma faixa de faixas não for apropriada, considere usar comandos avançados em vez disso.  
2. Não subestime o desafio de criar uma faixa de faixas em vigor. Não espere que seja uma porta simples das barras de menus e barras de ferramentas existentes. E não é necessário que o uso de uma faixa de opção faça com que seu programa seja melhor. Estar disposto a confirmar o tempo e o esforço necessário para uma reestruturação de comando é um fator importante na decisão de usar uma faixa de uma.  
3. Tornar os comandos detectáveis. Escolha um design de guia que tenha um mapeamento claro, óbvio e exclusivo entre seus comandos e as guias rotuladas de forma descritiva em que residem. Os usuários devem ser capazes de determinar de forma rápida e confiável qual guia tem o comando que estão procurando e raramente escolher a guia errada.  
4. Torne os comandos auto-explicativos. Os usuários devem entender o efeito de um comando de seu rótulo, ícone, dica de ferramenta e visualização. Eles não devem ter que experimentar ou ler um tópico da ajuda para ver como funciona um comando.  
5. Faça usando os comandos de forma eficiente:
    - Os usuários devem passar a maior parte do tempo na guia página inicial.
    - Os usuários raramente precisam alterar as guias durante as tarefas comuns.
    - Quando a janela é maximizada e os usuários estão na guia correta, os comandos usados com mais frequência têm a ênfase mais visual e os usuários podem chamá-las com um único clique. Os usuários podem executar todos os outros comandos na guia com, no máximo, quatro cliques.
    - Os usuários não devem abrir caixas de diálogo para fornecer comandos e alterar atributos em tarefas comuns.
6. Ajude os usuários a escolher comandos e opções com confiança e minimizar a necessidade de tentativa e erro. Use comandos orientados a resultados sempre que apropriado, geralmente na forma de galerias e visualizações dinâmicas.  
7. Certifique-se de que a faixa de opções seja bem dimensiona dos maiores tamanhos de janela para o menor.  

## <a name="design-concepts"></a>Conceitos de design

### <a name="adapting-a-ribbon-in-an-existing-program"></a>Adaptando uma faixa de opções em um programa existente

Embora você possa simplesmente criar uma barra de menus tradicional e um design de barra de ferramentas de um programa existente para um formato de faixa de opções, fazer isso perde a maior parte do valor de usar uma faixa de opções. As faixas de opções têm o maior valor quando usadas para apresentar comandos imediatos orientados a resultados, geralmente na forma de galerias e visualizações ao vivo. Os comandos orientados a resultados facilitam a compreensão dos comandos e dos usuários muito mais eficientes e produtivos. Em vez de recriar seus comandos existentes, é melhor recriar completamente como os comandos são executados em seu programa.

Não suia o desafio de criar uma faixa de opções efetiva. E não leve em conta que usar uma faixa de opções torna seu programa melhor automaticamente. A criação de uma faixa de opções efetiva leva muito tempo e esforço. Estar disposto a comprometer o tempo e o esforço necessários para tal reprojeto de comando é um fator importante na decisão de usar uma faixa de opções.

### <a name="the-nature-of-ribbons"></a>A natureza das faixas de opções

Em comparação com barras de menu tradicionais e barras de ferramentas, as faixas de opções têm as seguintes características:

- **Uma interface do usuário única para todos os comandos.** As barras de menu são abrangentes e fáceis de aprender e as barras de ferramentas são eficientes e diretas, mas por que não usar um pouco mais de espaço na tela para criar uma interface do usuário de comandos que realiza todos eles? Com apenas uma interface do usuário, as faixas de opções não exigem que os usuários descubram qual interface do usuário tem o comando que eles estão procurando.
- **Visível e autoexplicativo.** Os comandos da barra de menus são autoexplicativos por meio de seus rótulos, mas ficam ocultos da exibição na maioria das vezes. Para economizar espaço na tela, os botões da barra de ferramentas são representados principalmente por ícones em vez de rótulos (embora alguns botões de barra de ferramentas usem ambos) e dependem de dicas de ferramenta quando o ícone não é autoexplicativo. No entanto, os usuários geralmente conhecem os ícones apenas para os comandos mais usados.
- Ao apresentar a maioria dos comandos com ícones rotulados, os comandos da faixa de opções são visíveis e autoexplicativos e usam dicas de ferramenta apenas para fornecer informações complementares. Há pouca necessidade de ir para outro lugar (como Ajuda) para entender um comando.
- **Agrupamento rotulado.** Embora as categorias de menu sejam rotuladas, os grupos em um menu suspenso não são e são indicados apenas com um separador sem rótulo. Grupos dentro de barras de ferramentas também são indicados com separadores sem rótulo.
- Ao organizar comandos em grupos rotulados, as faixas de opções facilitam a encontrar comandos e determinar sua finalidade.
- **Modal, mas não hierárquico.** As barras de menu são dimensionadas criando uma hierarquia de comandos. Menus com muitos itens podem usar um ou mais níveis de submenus para fornecer mais comandos.
- Os comandos da faixa de opções exigem mais espaço do que os comandos da barra de ferramentas, portanto, eles usam guias para dimensionar. Esse uso de guias torna as faixas de opções modais, exigindo que os usuários alterem os modos ocasionalmente para encontrar comandos. No entanto, em uma guia, a maioria dos comandos é direta ou usa um botão de divisão única ou um botão de menu, não uma hierarquia.
- **Direto e imediato.** Um comando será direto se invocado com um único clique (ou seja, sem navegar pelos menus) e imediato se entrar em vigor imediatamente (ou seja, sem caixas de diálogo para coletar entradas adicionais). Os comandos da barra de menus são sempre indiretos e geralmente não imediatos. Assim como as barras de ferramentas, a maioria dos comandos da faixa de opções é projetada para ser direta e imediata, com os comandos usados com mais frequência invocados com um único clique e sem a necessidade de uma caixa de diálogo para coletar entradas adicionais.
- **Espaçosos.** As barras de menu e as barras de ferramentas são projetadas principalmente para serem eficientes no espaço. Para fornecer seus benefícios, as faixas de opções podem consumir mais espaço vertical, sendo aproximadamente o equivalente a uma barra de menus mais três linhas de barras de ferramentas. Sendo que poucos programas têm três ou mais linhas de barras de ferramentas, as faixas de opções geralmente consomem mais espaço do que as UIs tradicionais para comandos.
- **Tem um botão Aplicativo e a Barra de Ferramentas de Acesso Rápido.** Uma faixa de opções sempre é apresentada com um botão Aplicativo e a Barra de Ferramentas de Acesso Rápido. Isso permite que os usuários acessem comandos relacionados a arquivos e usados com frequência sem alterar guias e promovem a consistência entre programas.
- **Personalização mínima.** Embora as barras de menu tenham uma apresentação fixa, muitas barras de ferramentas são bastante personalizáveis, permitindo aos usuários definir locais, tamanhos e conteúdo. Uma faixa de opções em si não é personalizável, mas a Barra de Ferramentas de Acesso Rápido fornece personalização limitada.
- **Acessibilidade aprimorada do teclado.** As barras de menu têm excelente acessibilidade de teclado porque pressionar a tecla Alt fornece diretamente o foco de entrada da barra de menus. No entanto, não há esse mecanismo para barras de ferramentas porque elas compartilham a navegação por teclado com o conteúdo da janela. Consequentemente, os usuários devem navegar até a barra de ferramentas usando a tecla Tab (que recebe a última parada da guia) e, em seguida, navegar até um comando específico usando as teclas de direção.

Por outro lado, as faixas de opções fornecem acessibilidade aprimorada do teclado por meio [de dicas de](glossary.md)tecla , geralmente com um processo de três etapas:

- Pressione Alt para entrar no modo de dica de tecla.
- Pressione um caractere para escolher uma guia, o botão Aplicativo ou um comando na Barra de Ferramentas de Acesso Rápido.
- Em uma guia, pressione uma ou duas letras para escolher um comando.

    Essa abordagem é altamente visual. Ele também é mais flexível, permitindo que ele seja dimensionado melhor e tenha mais atribuições de chave de acesso mnemônico.

    Não confunda chaves de acesso com teclas de atalho. Embora as teclas de acesso e as teclas de atalho forneçam acesso de teclado à interface do usuário, elas têm diferentes finalidades e diretrizes. Para obter mais informações, consulte [Teclado](inter-keyboard.md).

### <a name="the-nature-of-rich-commands"></a>A natureza dos comandos avançados

Comandos avançados referem-se à apresentação e à interação de comandos usados por faixas de opções, sem necessariamente usar um contêiner de faixa de opções. Comandos avançados têm estas características:

- **Rotulagem.** Todos os comandos receberão rótulos autoexplicativos, com exceções somente quando os ícones são extremamente conhecidos e o espaço está em um premium.

    **Correto:**

    ![captura de tela de uma faixa de opções de formatação de caracteres ](images/cmd-ribbons-image3.png)

    Esses comandos são extremamente conhecidos para que não precisem de rótulos.

    **Incorreto:**

    ![captura de tela de uma faixa de opções com ícones raramente usados ](images/cmd-ribbons-image4.png)

    Esses ícones ininteligíveis exigem rótulos para comandos avançados.

- **Dimensionamento.** Em vez de dimensionamento uniforme, os comandos são dimensionados em relação à frequência de uso e importância. Além de tornar os comandos usados com mais frequência mais fáceis de encontrar e clicar, ele também os torna mais [sensíveis.](https://msdn.microsoft.com/library/windows/desktop/cc872774.aspx)

    ![captura de tela de um botão grande e três botões pequenos ](images/cmd-ribbons-image5.png)

    Neste exemplo, o botão usado com mais frequência é maior do que os outros.

- **O ressamento dinâmico.** Controles de comando rich são reorganizado para aproveitar ao máximo o espaço disponível, em vez de usar um tamanho fixo e truncar ou usar estouro quando o tamanho for muito pequeno.

    ![captura de tela da faixa de opções larga com botões de tamanho igual ](images/cmd-ribbons-image6.png)![captura de tela da faixa de opções pequena com botões mistos ](images/cmd-ribbons-image7.png)

    Neste exemplo, os botões de comando são resizedos para funcionar bem no espaço disponível.

- **Botões de divisão.** Os botões divididos são uma boa maneira de consolidar um conjunto de variações de um comando quando necessário, mantendo a direcionamento para o comando usado com mais frequência.

    ![captura de tela de salvar como comando e suas opções ](images/cmd-ribbons-image8.png)

    Neste exemplo, o comando Salvar como usa um botão de divisão, em que o botão principal executa a variação mais comum e a parte do menu revela um menu com variações do comando.

- **Menus suspensos e galerias rich.** Menus suspensos, listas suspensos e galerias usam o espaço necessário para se comunicar e diferenciar o efeito das opções, geralmente usando gráficos e descrições de texto. As categorias são usadas para organizar grandes conjuntos de opções.

    ![captura de tela das opções de menu suspenso com ícones ](images/cmd-ribbons-image9.png)

    Nesses exemplos, clicar em um botão de menu exibe uma lista de opções que mostram seu efeito.

- **Visualizações ao vivo.** Sempre que o usuário passar o mouse sobre uma opção de formatação, o programa mostrará a aparência dos resultados com essa formatação usando o conteúdo real.

    ![captura de tela dos resultados das opções de formatação ](images/cmd-ribbons-image10.png)

    As visualizações ao vivo mostram os resultados da aplicação de uma opção de formatação ao passar o mouse.

- **Dicas de ferramenta aprimoradas.** Eles explicam concisamente seus comandos associados e dão as teclas de atalho. Eles também podem incluir gráficos e referências à Ajuda (embora eliminem em grande parte a necessidade de ajuda relacionada a comandos).

    ![captura de tela de dica de ferramenta grande com texto e gráfico ](images/cmd-ribbons-image11.png)

    Dicas de ferramentas aprimoradas explicam concisamente seus comandos associados.

Embora as faixas de opções possam não ser adequadas para todos os programas, todos os programas podem se beneficiar de comandos avançados.

### <a name="ribbons-always-have-an-application-button-and-quick-access-toolbar"></a>As faixas de opções sempre têm um botão Aplicativo e a Barra de Ferramentas de Acesso Rápido

O botão Aplicativo e a Barra de Ferramentas de Acesso Rápido fornecem comandos úteis em qualquer contexto, reduzindo a necessidade de alterar guias. Embora esses três componentes sejam logicamente independentes, uma faixa de opções sempre deve ter um botão Aplicativo e uma Barra de Ferramentas de Acesso Rápido. Considerando que os comandos podem ir na faixa de opções ou no botão Aplicativo, você pode estar se perguntando onde colocar comandos. A escolha não é arbitrária.

O botão Aplicativo é usado para apresentar um menu de comandos que envolvem fazer algo com ou com um arquivo, como comandos que tradicionalmente vão no menu Arquivo para criar, abrir e salvar arquivos, imprimir e enviar e publicar documentos.

Por outro lado, a faixa de opções em si é para comandos que afetam o conteúdo da janela. Os exemplos incluem comandos usados para ler, modificar ou usar o conteúdo ou alterar a exibição.

Se você usar uma faixa de opções, também deverá usar um botão Aplicativo mesmo que o programa não envolva documentos ou arquivos. Nesses casos, use o menu Aplicativo para apresentar comandos para impressão, opções de programa e saída do programa. Embora, indiscutivelmente, o botão Aplicativo não seja necessário para esses programas, usá-lo fornece consistência entre programas. Os usuários não precisam procurar comandos ou opções de programa salvar e desfazer porque estão sempre no mesmo lugar.

A Barra de Ferramentas de Acesso Rápido é necessária mesmo que a faixa de opções use apenas uma guia. Novamente, embora, indiscutivelmente, esses programas não precisem de uma Barra de Ferramentas de Acesso Rápido (porque todos os comandos já estão presentes na única guia), ter uma Barra de Ferramentas de Acesso Rápido personalizável fornece consistência entre programas. Por exemplo, se os usuários têm o hábito de clicar no comando Imprimir, eles devem ser capazes de fazer isso em qualquer programa que usa uma faixa de opções.

### <a name="organization-and-discoverability"></a>Organização e descoberta

Ao fornecer guias e grupos, as faixas de opções permitem organizar seus comandos para ajudar na descoberta. O desafio é que, se a organização for mal feita, ela poderá prejudicar muito a descoberta. Deve haver um mapeamento claro, óbvio e exclusivo entre seus comandos e as guias e grupos rotulados descritivo em que eles residem.

Os usuários formarão um modelo mental da faixa de opções depois de usá-lo por um tempo. Se esse modelo mental não fizer sentido para os usuários, for ineficiente ou estiver incorreto, isso levará a confusão e frustração. **Sua meta mais importante na criação de uma faixa de opções é facilitar a descoberta de comandos com rapidez e confiança. Se você não fizer isso, o design da faixa de opções falhará.** Atingir essa meta requer design cuidadoso, teste de usuário e iteração. Não suponha que será fácil.

Aqui estão algumas armadilhas comuns a evitar:

- **Evite nomes de guias e grupos genéricos.** Um bom nome de guia ou grupo deve descrever com precisão seu conteúdo específico, preferencialmente usando linguagem baseada em tarefa e meta. Evite nomes de guias e grupos genéricos, bem como nomes baseados em tecnologia. Por exemplo, quase qualquer comando em um documento criando e criando programa poderia pertencer a guias rotuladas Editar, Formatar, Ferramentas, Opções, Avançado e Muito mais. Dependa de rótulos descritivos específicos, não de memorização.
- **Evite nomes de guias e grupos muito específicos.** Embora queiramos que os nomes de guias e grupos sejam específicos, eles não devem ser tão específicos que os usuários ficam surpresas com seu conteúdo. Os usuários geralmente pesquisam coisas usando o processo de eliminação, portanto, evitem ignorar suas guias ou grupos porque o nome é enganoso.
- **Evite vários caminhos para o mesmo comando, especialmente se o caminho for inesperado ou se o comando exigir muitos cliques para invocar.** Pode parecer uma conveniência encontrar um comando por meio de vários caminhos. Mas tenha em mente que, quando os usuários encontram o que estão procurando, eles param de procurar. É muito fácil para os usuários presumirem que o primeiro caminho que eles encontram é o único caminho que é um problema sério se esse caminho for ineficiente ou inesperado. Além disso, ter comandos duplicados torna mais difícil para os usuários encontrar outros comandos que estão procurando.

![captura de tela do comando de caminho indireto para bordas ](images/cmd-ribbons-image12.png)

Neste exemplo, você pode alterar bordas de parágrafo por meio do comando Bordas da Página, mesmo que haja um caminho mais direto na guia Início. Se os usuários que procuram bordas de parágrafo fossem se deparar com esse caminho inesperado, eles poderiam facilmente supor que esse é o único caminho.

- **Evite o posicionamento arbitrário de comandos.** Suponha que você pense que tem uma boa guia e design de grupo, mas descubra que vários comandos simplesmente não se ajustam. É provável que seu design de guia e grupo não seja tão bom quanto você acha que é e você precisa continuar a refiná-lo. Não resolva esse problema colocando esses comandos onde eles não pertencem. Se você fizer isso, os usuários provavelmente terão que inspecionar cada guia para encontrá-las e, em seguida, esquecer imediatamente onde estão.
- **Evite o posicionamento baseado em marketing.** Suponha que você tenha uma nova versão do programa e sua equipe de marketing realmente queira promover seus novos recursos. Pode ser uma tentação colocá-los na guia Página Base, mas fazer isso é um erro caro se prejudicar a descoberta geral. Considere as versões futuras do seu produto e a frustração que uma organização em constante mudança causará.

### <a name="tabs"></a>Guias

A melhor primeira etapa é revisar as [guias de faixa de opções padrão](#standard-ribbon-tabs). Se os comandos do programa mapearem naturalmente para as guias padrão, basee sua organização de guias nesses padrões. Por outro lado, se os comandos do programa não mapearem naturalmente, não tente forçá-lo. Determine uma estrutura mais natural e certifique-se de executar muitos testes de usuário para garantir que você a tenha correto.

Para guias não padrão, considere estes problemas:

- **Cada nome de guia deve descrever seu conteúdo.** Escolha nomes significativos específicos, mas não muito específicos. Os usuários nunca devem se surpresar com seu conteúdo.
- **Cada nome de guia deve refletir sua finalidade.** Considere a meta ou a tarefa associada aos comandos.
- **Cada nome de guia deve ser claramente diferente de todos os outros nomes de tabulação.**

A guia Página Home é uma exceção a essas considerações. Embora você não tenha que ter uma guia Página Principal, a maioria dos programas deve. A guia Início é a primeira guia e contém os comandos usados com mais frequência. Se você tiver usado comandos que não se ajustam às outras guias com frequência, a guia Página Página 1 é o lugar certo para elas.

Se você não puder determinar um nome de guia significativo e descritivo, provavelmente será porque a guia não foi bem projetada. Se sua organização da faixa de opções simplesmente não estiver funcionando, reverte o design da guia.

### <a name="groups"></a>Grupos

Dividir comandos em grupos estrutura os comandos em conjuntos relacionados. O rótulo do grupo explica a finalidade comum de seus comandos.

Há uma variedade de fatores a considerar ao determinar grupos e sua apresentação:

- **Agrupamento padrão.** Embora haja diferenças significativas em comandos entre programas, há grupos [padrão](#standard-ribbon-groups) que são comuns em muitos programas. Fazer com que esses comandos apareçam com os mesmos nomes e locais semelhantes melhora muito a capacidade de descoberta.

| Correto                                                                                      | Incorreto                                                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| ![captura de tela do zoom separado do grupo de edição ](images/cmd-ribbons-image13.png)<br/>O grupo de comandos de edição inclui todos os comandos de edição, mas não inclui o comando Zoom.         | ![captura de tela do zoom incluído no grupo de edição ](images/cmd-ribbons-image14.png)<br/>O comando Zoom não é um comando de edição, mas está no grupo de edição. |

- **Granularidade.** Alguma estrutura é boa, mas a estrutura demais dificulta a encontrar comandos. Se os nomes de grupo são genéricos, talvez você não tenha granularidade suficiente. Se houver grupos com apenas um ou dois comandos, você provavelmente terá muito (embora ter uma galeria na faixa de opções sem outros comandos em um grupo seja aceitável).

| Correto                                                                                                 | Incorreto                                                                                                  |
|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| ![captura de tela do zoom separado do grupo de edição ](images/cmd-ribbons-image13.png)<br/> O grupo de comandos de edição inclui todos os comandos de edição| ![captura de tela da divisão do grupo de edição em dois grupos ](images/cmd-ribbons-image15.png)<br/>O grupo de comandos de edição foi dividido em seções muito granulares. Evite grupos com apenas um ou dois comandos.|

- **Nomes.** Bons nomes de grupo explicam a finalidade de seus comandos. Se os nomes de grupo não o deem, remente o nome ou o grupo. Se você não puder determinar um nome significativo e descritivo, provavelmente será porque o grupo não foi bem projetado.

| Correto                                                                                                 | Incorreto                                                                                                  |
|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| ![captura de tela de comandos divididos em quatro grupos ](images/cmd-ribbons-image17.png) <br/> Use nomes de grupo específicos o suficiente para descrever os comandos contidos no grupo. | ![captura de tela do grupo de formatos com vários comandos ](images/cmd-ribbons-image16.png) <br/> Esse nome de grupo é muito indefinitivo para ser útil. Uma abordagem melhor seria reorganizar esses comandos em grupos mais específicos. |

- **Ordem.** As pessoas leem em uma ordem da esquerda para a direita (em culturas ocidental), portanto, você pode pensar que os grupos à extrema esquerda são os mais perceptíveis. No entanto, o nome da guia realçada e o conteúdo da janela tendem a atuar como pontos focal, portanto, os grupos no centro da guia geralmente recebem mais atenção do que o grupo mais à esquerda. [](vis-layout.md) Coloque os grupos mais usados nos locais mais proeminentes e certifique-se de que haja um fluxo lógico para os grupos na guia.

![captura de tela do grupo de área de transferência na extrema esquerda ](images/cmd-ribbons-image18.png)

Neste exemplo, os grupos Fonte e Parágrafo são mais perceptíveis do que o grupo Área de Transferência, pois eles são o que o olho vê primeiro ao mover para cima do documento.

![captura de tela do grupo de acompanhamento na guia revisão ](images/cmd-ribbons-image19.png)

Neste exemplo, o grupo Acompanhamento recebe mais atenção, em parte porque a guia Revisão realçada atua como um ponto focal.

- **Uniformidade.** Pode ser difícil reconhecer comandos quando a apresentação do comando tem a mesma aparência. O uso de ícones com diferentes formas e cores, grupos com formatos variados e comandos com tamanhos diferentes facilita o reconhecimento de grupos de comandos pelos usuários. Os comandos devem ter um dimensionamento uniforme somente quando a faixa de opções é dimensionada para seus tamanhos menores.

| Correto | Incorreto |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| ![captura de tela do grupo com ícones de tamanhos diferentes ](images/cmd-ribbons-image20.png)<br/>Usar uma variedade de tamanhos de ícone para melhorar a reconhecimento| ![captura de tela do grupo com ícones do mesmo tamanho ](images/cmd-ribbons-image21.png)<br/>Esses comandos são muito semelhantes uns aos outros porque têm o mesmo tamanho. |

### <a name="previews"></a>Visualizações

Você pode usar vários tipos de visualizações para mostrar o que resultará de um comando. Usando visualizações úteis, você pode melhorar a eficiência do programa e reduzir a necessidade da abordagem de aprendizado de avaliação e erro. As visualizações ao vivo também convidam experimentação e incentivam a criatividade.

Aqui estão alguns dos diferentes tipos de visualizações que você pode usar:

- **Ícones estáticos e gráficos realistas.** Imagens estáticas que dão uma indicação realista do efeito de um comando. Eles podem ser usados em galerias, menus suspensos e dicas de ferramentas aprimoradas.

![captura de tela da lista de listas lista de fontes ](images/cmd-ribbons-image22.png)

Neste exemplo, a listada Fonte mostra cada nome de fonte usando a própria fonte.

![captura de tela da galeria de miniaturas de marca d'água ](images/cmd-ribbons-image23.png)

Neste exemplo, miniaturas realistas são usadas para mostrar as diferentes marcas-d'água.

- **Ícones dinâmicos e gráficos.** Ícones e elementos gráficos que são modificados para refletir o estado atual. Esses ícones são especialmente úteis para galerias, bem como botões de divisão que alteram seu efeito padrão para serem iguais aos da última ação.

![captura de tela da galeria de estilos de parágrafo ](images/cmd-ribbons-image24.png)

Neste exemplo, Microsoft Word a galeria estilos para refletir os estilos atuais.

![captura de tela dos botões de comando de formatação de texto ](images/cmd-ribbons-image25.png)

Neste exemplo, o Word altera os comandos Cor de realçada de texto e Cor da fonte para indicar seu efeito atual.

- **Visualizações ao vivo.** Quando os usuários passarem o mouse sobre uma opção de formatação, a visualização ao vivo mostrará a aparência dos resultados com essa formatação. As visualizações ao vivo ajudam os usuários a fazer seleções com mais eficiência e confiança com base no contexto real do usuário.

![captura de tela do seletor de cor do comando de cor da página ](images/cmd-ribbons-image26.png)

Neste exemplo, o comando Cor da Página executa uma visualização ao vivo mostrando o efeito das opções de cor ao passar o mouse.

As visualizações ao vivo são um recurso poderoso que pode realmente melhorar a produtividade dos usuários, mas até mesmo visualizações estáticas simples podem ser uma grande ajuda.

### <a name="scaling-the-ribbon"></a>Dimensionamento da faixa de opções

Dimensionar uma barra de ferramentas é simples: se uma janela for muito estreita para exibir uma barra de ferramentas, a barra de ferramentas exibirá o que se ajusta e torna todo o resto acessível por meio de um botão de estouro. Uma meta dos comandos avançados é aproveitar ao máximo o espaço disponível, portanto, dimensionar uma faixa de opções requer mais trabalho de design. Não há nenhum tamanho de faixa de opções padrão, portanto, você não deve criar uma faixa de opções com uma largura específica em mente. Você precisa projetar layouts com uma ampla variedade de larguras e perceber que qualquer um deles pode ser o que a maioria dos usuários verá. O dimensionamento é uma parte fundamental do design da faixa de opções, não a última etapa. Ao criar uma guia, especifique os layouts diferentes para cada grupo (até três), bem como as combinações que podem ser usadas em conjunto. A faixa de opções mostrará a maior combinação válida que se ajusta ao tamanho da janela atual.

![captura de tela dos comandos de formato no menu de estouro ](images/cmd-ribbons-image27.png) Barras de ferramentas dimensionam usando um botão de estouro.

![captura de tela de faixas de opções com várias larguras ](images/cmd-ribbons-image28.png) Não há nenhum tamanho de faixa de opções padrão. O menor tamanho é um ícone de grupo pop-up único.

## <a name="guidelines"></a>Diretrizes

### <a name="general"></a>Geral

- **Não combine faixas de opções com barras de menu e barras de ferramentas em uma janela.** As faixas de opções devem ser usadas no lugar de barras de menu e barras de ferramentas. No entanto, uma faixa de opções pode ser combinada com janelas de paleta e elementos de navegação, como botões Voltar e Avançar e uma barra de endereços.
- **Sempre combine uma faixa de opções com um botão Aplicativo e a Barra de Ferramentas de Acesso Rápido.**
- **Selecione a guia mais à esquerda (geralmente Página Início) quando um programa for iniciado.** Não faça com que a última guia selecionada persista entre as instâncias do programa.
- **Mostrar a faixa de opções em seu estado normal (não minimizado) quando um programa for iniciado pela primeira vez.** Os usuários geralmente deixam as configurações padrão inalteradas, portanto, minimizar a faixa de opções no início do programa provavelmente fará com que todos os comandos sejam menos eficientes. Além disso, mostrar a faixa de opções inicialmente minimizada pode ser um grande risco.
- **Faça com que o estado da faixa de opções persista entre as instâncias do programa.** Por exemplo, se um usuário minimizar a faixa de opções, ela deverá ser mostrada minimizada na próxima vez que o programa for executado. Mas, novamente, não faça com que a última guia selecionada persista dessa maneira.

### <a name="using-tabs"></a>Usando guias

Em geral, ter menos guias é melhor, portanto, remova guias que não ajudam a atingir essas metas.

- **Sempre que for prático, use guias padrão.** O uso de guias padrão melhora muito a capacidade de descoberta, especialmente entre programas. Consulte as [guias da faixa de opções padrão](#standard-ribbon-tabs) mais adiante neste artigo.
- **Rotule a primeira guia Página Início, se apropriado.** A guia Página Principal deve conter os comandos usados com mais frequência. Se você tiver usado comandos que não se ajustam às outras guias com frequência, a guia Página Página 1 é o lugar certo para elas.
- Adicione uma nova guia se:
  - **Seus comandos estão fortemente relacionados a tarefas específicas e podem ser descritos com precisão pelo rótulo da guia.** Adicionar a guia deve ajudar a tornar seus comandos fáceis de encontrar, não mais difíceis.
  - **Seus comandos não estão relacionados principalmente a tarefas em outras guias.** Adicionar a guia não deve exigir mais alternação de tabulação durante tarefas normalmente executadas.
  - **A guia tem comandos suficientes para justificar ter um local extra para procurar.** Não tem guias com apenas alguns comandos. **Exceção:** Considere adicionar uma guia com alguns comandos se eles estão fortemente relacionados a uma tarefa específica e adicionar a guia simplifica muito uma guia Página Página Principal muito complexa.
- **Para as guias restantes, primeiro coloque as guias usadas com mais frequência, mantendo uma ordem lógica entre as guias.**
- **Otimize o design da guia para que os usuários encontrem comandos com rapidez e confiança.** Todas as outras considerações são secundárias.
- **Não forneça uma guia Ajuda.** Em vez disso, forneça assistência usando a Ajuda em todo o programa e dicas de ferramentas aprimoradas.
- **Use no máximo sete guias principais.** Se houver mais de sete, será difícil determinar qual guia tem um comando. Embora sete guias principais seja aceitável para aplicativos com muitos comandos, a maioria dos programas deve visar quatro ou menos guias.

### <a name="contextual-tabs"></a>Guias contextuais

- **Use uma guia contextual para exibir uma coleção de comandos que são relevantes somente quando os usuários selecionam um tipo de objeto específico.** Se houver apenas alguns comandos usados com frequência, pode ser mais conveniente e estável usar uma guia regular e simplesmente desabilitar comandos quando eles não se aplicam.
- ![captura de tela dos comandos recortar e copiar esmaecida ](images/cmd-ribbons-image29.png)<br>É melhor desabilitar comandos comuns como Recortar e Copiar do que usar uma guia contextual.
- **Inclua apenas os comandos que são específicos para um tipo de objeto específico.** Não coloque comandos somente em uma guia contextual se os usuários talvez precisem deles sem primeiro selecionar um objeto.
- **Inclua os comandos usados com frequência ao trabalhar com um tipo de objeto específico.** Coloque comandos contextuais gerais usados com frequência em menus de contexto e minibaras de ferramentas para evitar a alternência de tabulação durante tarefas normalmente executadas. Como alternativa, considere colocar comandos gerais com redundância em uma guia contextual se isso evitar a alternância de tabulação frequente. Mas não exagerar isso – não tente incluir todos os comandos que um usuário possa precisar ao trabalhar com o objeto.
- ![captura de tela de comando de bordas na guia Design ](images/cmd-ribbons-image30.png)<br/>Neste exemplo, o comando bordas está incluído na guia Design para evitar a alternância de tabulação frequente durante as tarefas normalmente executadas. \
- **Escolha uma cor de guia contextual que seja diferente das guias contextuais exibidas no momento.** O mesmo conjunto de guias pode aparecer mais tarde usando uma cor diferente para conseguir isso, mas tente usar atribuições de cores consistentes em invocações sempre que possível.
- A **seleção de uma guia contextual ajuda automaticamente** a descoberta, melhora a percepção da estabilidade e reduz a necessidade de alternar entre as guias. Selecione uma guia contextual automaticamente quando:
  - **O usuário insere um objeto.** Nesse caso, selecione a primeira guia contextual no conjunto.
  - **O usuário clica duas vezes em um objeto.** Nesse caso, selecione a primeira guia contextual no conjunto.
  - **O usuário selecionou uma guia contextual, clicou fora do objeto e clicou imediatamente em um objeto do mesmo tipo.** Nesse caso, retorne à guia contextual selecionada anteriormente.
- **Ao remover uma guia contextual que é a guia ativa, faça com que a guia página inicial ou a primeira guia ativa.** Fazer isso parece o mais estável.

### <a name="modal-tabs"></a>Guias modais

- **Use uma guia modal para exibir uma coleção de comandos que se aplicam a um modo temporário específico e nenhuma das guias principais se aplica.** Se algumas das guias principais se aplicarem, use uma guia contextual, em vez disso, e desabilite os comandos que não se aplicam. Como as guias modais estão muito limitando, elas devem ser usadas somente quando não há uma alternativa melhor.
- ![captura de tela da guia Visualizar impressão ](images/cmd-ribbons-image31.png)<br/>A visualização de impressão é uma guia modal comumente usada.
- **Para fechar uma guia modal, coloque o &lt; comando Close mode &gt; como o último comando na guia.** Use o ícone fechar para facilitar a localização do comando. Dê ao modo no comando para evitar confusão sobre o que está sendo fechado.
- ![captura de tela do botão fechar visualização de impressão ](images/cmd-ribbons-image32.png)<br/>Neste exemplo, rotular explicitamente o comando fechar com o modo remove qualquer dúvida sobre o que está sendo fechado.
- **Para fechar uma guia modal, também redefina o botão fechar na barra de título da janela para fechar o modo em vez do programa.** O teste do usuário mostrou que muitos usuários esperam esse comportamento.

### <a name="standard-ribbon-tabs"></a>Guias da faixa de faixas padrão

Sempre que for prático, mapeie os comandos do programa para essas guias padrão, dadas em sua ordem padrão de aparência.

#### <a name="regular-tabs"></a>Guias regulares

- **Casa.** Contém os comandos usados com mais frequência. Se usado, é sempre a primeira guia.
- **Inserido.** Contém comandos para inserir conteúdo e objetos em um documento. Se usado, é sempre a segunda guia.
- **Layout da página.** Contém comandos que afetam o layout da página, incluindo temas, configuração de página, planos de fundo de página, recuo, espaçamento e posicionamento. (Observe que os grupos de recuo e espaçamento podem estar na guia início, em vez disso, se houver espaço suficiente.) Se usado, é sempre a terceira guia.
- **Revê.** Contém comandos para adicionar comentários, controlar alterações e comparar versões.
- **Exibição.** contém comandos que afetam o modo de exibição de documento, incluindo modo de exibição, opções de mostrar/ocultar, zoom, gerenciamento de janelas e macros tradicionalmente encontrados na categoria de menu Windows. Se usado, é a última guia regular, a menos que a guia desenvolvedor esteja sendo exibida.
- **Desenvolvedor.** Contém comandos usados somente por desenvolvedores. Se usado, ele fica oculto por padrão e a última guia regular quando exibido.

A maioria dos programas não precisa das guias revisão e desenvolvedor.

#### <a name="standard-contextual-tabs"></a>Guias contextuais padrão

- **Ao.** Contém comandos relacionados à alteração do formato do tipo de objeto selecionado. Geralmente se aplica a parte de um objeto.
- **Desenvolver.** Contém comandos, geralmente em galerias, para aplicar estilos ao tipo de objeto selecionado. Geralmente se aplica ao objeto inteiro.
- **Layout.** Contém comandos para alterar a estrutura de um objeto complicado, como uma tabela ou um gráfico.

Se você tiver comandos contextuais relacionados ao formato, design e layout, mas não o suficiente para várias guias, basta fornecer uma guia formato.

### <a name="standard-groups"></a>Grupos padrão

- **Sempre que for prático, use grupos padrão.** Ter comandos comuns aparecem com os mesmos nomes e locais semelhantes melhora muito a descoberta. Consulte os [grupos de faixa de faixas padrão](#standard-ribbon-groups) mais adiante neste artigo.
- **Adicione um novo grupo** se:
  - **Seus comandos estão fortemente relacionados e podem ser descritos com precisão pelo rótulo do grupo.** Adicionar o grupo deve ajudar a facilitar a localização de seus comandos, e não mais difícil.
  - **Seus comandos têm uma relação mais fraca aos comandos em outros grupos.** Embora todos os comandos em uma guia devam estar fortemente relacionados, algumas relações de comando são mais fortes do que outras.
  - **O grupo tem comandos suficientes para justificar ter um local extra a ser examinado.** Objetivo dos comandos 3-5 para a maioria dos grupos. Evite ter grupos com apenas 1-2 comandos, embora ter uma galeria na faixa de tipos sem outros comandos dentro de um grupo seja aceitável. Ter muitos grupos com um único comando sugere muita estrutura ou falta de coesão de comandos.
- **Não reorganize** adicionando grupos onde eles não são necessários.
- **Considere dividir um grupo** se:
  - ![captura de tela do grupo de comandos desorganizados ](images/cmd-ribbons-image35.png)<br/>O grupo tem muitos comandos de tamanhos e necessidades de organização diferentes.
  - ![captura de tela de dois nomes de grupo de parágrafos longos ](images/cmd-ribbons-image33.png)<br>O grupo tem comandos que se beneficiam muito da existência de rótulos adicionais.
- **Coloque os grupos usados com mais frequência nos locais mais proeminentes e verifique se há uma ordem lógica para os grupos na guia.**
- **Otimize o design do grupo para que os usuários encontrem comandos com rapidez e confiança.** Todas as outras considerações são secundárias.
- **Não dimensione grupos contendo um único botão para um ícone de grupo pop-up.** Ao reduzir verticalmente, deixe-os como um único botão.
- **Use um máximo de sete grupos.** Se houver mais de sete grupos, será mais difícil determinar qual grupo tem um comando.

### <a name="standard-ribbon-groups"></a>Grupos de faixas de faixa padrão

Sempre que for prático, mapeie os comandos do programa para esses grupos padrão, que são fornecidos em suas guias associadas na ordem padrão de aparência.

#### <a name="main-tab"></a>Guia principal

- Área de Transferência
- Fonte
- Paragraph
- Edição

#### <a name="insert-tab"></a>Guia Inserir

- Tabelas
- Ilustrações

#### <a name="page-layout-tab"></a>Guia layout da página

- Temas
- Configuração de página
- Organizar

#### <a name="review-tab"></a>Guia revisar

- Revisão de texto
- Comentários

#### <a name="view-tab"></a>Guia Exibir

- Exibições de documento
- Mostrar/ocultar
- Zoom
- Janela

### <a name="commands"></a>Comandos

- ![captura de tela do comando de números de linha na faixa de opções ](images/cmd-ribbons-image36.png)<br/>**Aproveite a descoberta e a escalabilidade das faixas de opções expondo todos os comandos comumente usados.** Quando apropriado, mova os comandos usados com frequência das caixas de diálogo para a faixa de opções, especialmente aqueles que são conhecidos como difíceis de encontrar. O ideal é que os usuários sejam capazes de executar tarefas comuns sem usar nenhuma caixa de diálogo.

- **Não use a escalabilidade das faixas de opções para justificar a adição de complexidade desnecessária.** Continue a praticar exercícios e não adicione comandos a uma faixa de opções apenas porque você pode. Mantenha a experiência geral de comando simples. Veja a seguir maneiras de simplificar a apresentação:
  - ![captura de tela da minibara de ferramentas e do menu de contexto ](images/cmd-ribbons-image37.png)</br>**Use menus de contexto e minibaras de ferramentas para comandos contextuais in-locar.**
  - **Mover (ou manter) comandos raramente usados nas caixas de diálogo.** Use os iniciadores da caixa de diálogo para acessar esses comandos. Você ainda pode usar caixas de diálogo com faixas de opções! Tente reduzir a necessidade de usá-los durante tarefas comuns.
  - **Elimine recursos redundantes e raramente usados.**

#### <a name="presentation"></a>Apresentação

- **Apresente cada comando em apenas uma guia. Evite vários caminhos para o mesmo comando, especialmente se o comando exigir muitos cliques para invocar.** Pode parecer uma conveniência encontrar um comando por meio de vários caminhos. Mas tenha em mente que, quando os usuários encontram o que estão procurando, eles param de procurar. É muito fácil para os usuários presumirem que o primeiro caminho que eles encontram é o único caminho que será um problema sério se esse caminho for ineficiente. **Exceção:** As guias contextuais podem duplicar alguns comandos das guias Home e Insert se isso impedir a alteração de guias para tarefas contextuais comuns.
- **Em um grupo, coloque os comandos em sua ordem lógica, dando preferência aos comandos usados com mais frequência.** Em geral, os comandos devem ter um fluxo lógico para torná-los fáceis de encontrar, enquanto ainda têm os comandos usados com mais frequência aparecem primeiro. Em geral, comandos com ícones de 32 x 32 pixels aparecem antes de comandos com ícones de 16 x 16 pixels para auxiliar na verificação entre grupos.
- **Evite colocar comandos destrutivas ao lado dos comandos usados com frequência.** Um comando será considerado destrutiva se seu efeito for generalizado e não puder ser desfeita facilmente ou se o efeito não for imediatamente perceptível.
- **Use separadores para indicar comandos fortemente relacionados, como um conjunto de opções mutuamente exclusivas.**
- ![captura de tela dos grupos de fontes e parágrafos ](images/cmd-ribbons-image3.png)<br/> **Considere o uso de grupos de estilo de barra de ferramentas para conjuntos de comandos fortemente relacionados e conhecidos que não precisam de rótulos.** Isso permite que você apresente muitos comandos em um espaço compacto sem afetar a capacidade de descoberta e a facilidade de aprendizado. Para ser tão conhecido, esses comandos são usados com frequência, reconhecidos instantaneamente e, portanto, tendem a estar na guia Página Base.

- **Use ícones de 32 x 32 pixels para os comandos rotulados mais usados e importantes.** Ao dimensionar um grupo para baixo, transforme esses comandos no último a converter em ícones de 16 x 16 pixels.
- **Evite o posicionamento arbitrário de comandos.** Pense cuidadosamente no design da guia e do grupo para garantir que os usuários não percam tempo inspecionando cada guia para encontrar o comando que eles querem.
- **Evite o posicionamento baseado em marketing.** Os objetivos de marketing em torno da promoção de novos recursos tendem a mudar ao longo do tempo. Considere as versões futuras do seu produto e a frustração que uma organização em constante mudança causará.

#### <a name="interaction"></a>Interação

- **Desabilitar comandos que não se aplicam ao contexto atual ou que resultariam diretamente em um erro.** Se útil, use a [dica de ferramenta aprimorada](glossary.md) para explicar por que o comando está desabilitado. Não o oculta, pois isso pode fazer com que o layout da faixa de opções seja alterado, tornando a apresentação da faixa de opções instável.
- **Não atualize os rótulos de comando dinamicamente.** Novamente, fazer isso pode fazer com que o layout da guia mude, resultando em uma aparência instável. Em vez disso, projete comandos para que eles funcionem com rótulos constantes.

    | Correto                                                                                       | Incorreto                                                                 |
    |-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
    | ![captura de tela da observação de inserção e observação de exclusão ](images/cmd-ribbons-image38.png)<br/> Desabilitar comandos quando eles não estão disponíveis | ![captura de tela da observação de inserção, nenhuma observação de exclusão ](images/cmd-ribbons-image39.png)<br/>Não ocultar comandos, mesmo quando eles não estão disponíveis |

- **Prefira controles diretos.** Um comando será direto se invocado com um único clique (ou seja, sem navegar pelos menus). No entanto, com exceção das galerias na faixa de opções, os controles diretos não suportam a visualização ao vivo, portanto, a necessidade de visualização ao vivo também é um fator.
- **Use a** visualização ao vivo para indicar o efeito das opções quando um comando estiver entre um conjunto relacionado de opções de formatação e a visualização ao vivo for importante e prática, especialmente se os usuários provavelmente escolherem a opção errada caso contrário.
  - Se o comando for usado com frequência, use uma galeria na faixa de opções para direcionamento.
  - Se o comando for usado raramente, use uma galeria listada.
- **Expor comandos diretos** usando os seguintes controles na ordem de preferência a seguir
  - **Botões de comando, caixas de seleção, botões de rádio e galerias in-locar.** Eles são sempre diretos.
  - **Botões de divisão.** Direto para o comando mais comum, mas indireto para as variações de comando.
  - **Botões de menu.** Eles são indiretos, mas apresentam muitos comandos fáceis de encontrar.
  - **Caixas de texto (com controles de rotação).** A entrada de texto geralmente requer mais esforço do que os outros tipos de controle.
- ![captura de tela da faixa de opções com apenas botões de menu ](images/cmd-ribbons-image42.png)</br>Se a faixa de opções consistir principalmente em botões de menu quando exibidos em tamanho total, você também pode usar uma barra de menus.
- **Prefira comandos imediatos.** ![captura de tela do botão de impressão dividida e seu submenu ](images/cmd-ribbons-image43.png)<br/>Um comando será imediato se entrar em vigor imediatamente (ou seja, sem caixas de diálogo para coletar entradas adicionais). Se um comando pode exigir entrada, considere usar um botão de divisão, com o comando imediato na parte do botão e os comandos que exigem entrada no submenu.

### <a name="galleries"></a>Galerias

**Use uma [galeria](glossary.md)** se:

- **Há um conjunto de opções bem definido e relacionado entre os quais os usuários normalmente escolhem.** Pode haver um número irrível de variações, mas as seleções prováveis devem estar bem contidas. Se as opções não estão fortemente relacionadas, considere o uso de galerias separadas.
- **As opções são melhor expressas visualmente, como recursos de formatação.** O uso de miniaturas torna mais fácil procurar, entender e fazer escolhas. Embora as opções possam ser rotuladas, a seleção é feita visualmente e os rótulos de texto não devem ser necessários para entender as opções.
- **As opções mostram o resultado obtido imediatamente com um único clique.** Não deve haver nenhuma caixa de diálogo de acompanhamento para esclarecer ainda mais a intenção do usuário ou um conjunto de etapas para obter o resultado indicado. Se os usuários quiserem ajustar a escolha, deixe-os fazer isso posteriormente.

**Use uma galeria na faixa de opções** se:

- **As opções são usadas com frequência.** As opções precisam do espaço e vale a pena o espaço potencialmente sendo retirado de outros comandos.
- **Para uso típico, não é necessário agrupar ou filtrar as opções apresentadas.**
- **As opções podem ser exibidas efetivamente dentro da altura de uma faixa de opções (que é de 48 pixels).**

#### <a name="thumbnails-in-galleries"></a>Miniaturas em galerias

**Escolha o menor tamanho de miniatura** padrão da galeria que faz o trabalho bem.

- Para galerias na faixa de opções, use miniaturas de 16 x 16, 48 x 48 ou 64 x 48 pixels.
- Para galerias listadas, use miniaturas de 16x16, 32x32, 48x48, 64x48, 72x96, 96x72, 96x96 ou 128x128 pixels.
- Todos os itens da galeria devem ter o mesmo tamanho de miniatura.

Para galerias na faixa de bits:

- **Exibir um mínimo de três opções; mais se houver espaço.** Se não houver espaço suficiente para exibir pelo menos três opções no tamanho típico da janela, use uma galeria suspensa em vez disso.
- **Expanda as galerias de faixa de bits para aproveitar o espaço disponível.** Use o espaço adicional para mostrar mais itens e torná-los mais fáceis de escolher com um único clique.

Para galerias suspensas:

- **Exiba a Galeria de uma caixa de combinação, lista suspensa, botão de divisão ou botão de menu.**
- **Se o usuário clicar na janela principal para ignorar a Galeria suspensa, apenas ignore a Galeria sem selecionar ou modificar o conteúdo da janela principal.**
- **Se uma galeria tiver muitas opções e algumas opções forem usadas raramente, Simplifique a Galeria padrão concentrando-se nas opções usadas com frequência.** Para os comandos restantes, forneça um comando apropriado na parte inferior da lista suspensa galeria.
  - Se o comando mostrar uma lista de mais variações, nomeie-a como "mais `singular feature name` opções..."
  - Se o comando apresentar uma caixa de diálogo que permite aos usuários criar suas próprias opções personalizadas, nomeie-o como "Custom `feature name` ..."
- **Organize as opções em grupos, se isso tornar a navegação mais eficiente.**
- ![captura de tela de galeria de símbolos e filtros ](images/cmd-ribbons-image44.png)<br/>**Se uma galeria tiver muitos itens, considere adicionar um filtro para ajudar os usuários a localizar escolhas com mais eficiência.** Para evitar confusão, inicialmente, exiba a Galeria sem filtro. No entanto, a maioria das galerias não deve exigir um filtro porque eles não devem ter tantas opções, e o uso de grupos deve ser suficiente.

### <a name="command-previews"></a>Visualizações de comando

- **Use visualizações para mostrar o efeito de um comando sem que os usuários precisem executá-lo primeiro.** Usando as visualizações úteis, você pode melhorar a eficiência e a facilidade de aprendizado de seu programa e reduzir a necessidade de avaliação e erro. Para os diferentes tipos de visualizações de comando, consulte [visualizações](#previews) na seção conceitos de design deste artigo.
- **Para visualizações dinâmicas, verifique se a visualização pode ser aplicada e o estado atual restaurado em 500 milissegundos.** Isso requer a capacidade de aplicar alterações de formatação rapidamente e de forma a ser passível de interrupção. Os usuários devem ser capazes de avaliar diferentes opções rapidamente para que as visualizações dinâmicas tenham seu benefício total.
- **Evite usar texto em visualizações.** Caso contrário, as imagens de visualização precisarão ser localizadas.

### <a name="icons"></a>Ícones

- ![captura de tela de lista suspensa e caixas de seleção ](images/cmd-ribbons-image45.png)<br/>**Forneça ícones para todos os controles da faixa de opção, exceto listas suspensas, caixas de seleção e botões de rádio.** A maioria dos comandos exigirá ícones de 32x32 e 16x16 pixels (somente ícones de 16x16 pixels são usados pela barra de ferramentas de acesso rápido). As galerias normalmente usam ícones de 48x48 de 16x16, de 64x48 ou de pixels.
- **Forneça ícones exclusivos.** Não use o mesmo ícone para comandos diferentes.
- **Certifique-se de que os ícones da faixa de faixas estejam claramente visíveis em relação à cor da faixa de** Sempre avalie os ícones da faixa de posição no contexto e no modo de alto contraste.
- **Escolha os designs de ícone que comunicam claramente seu efeito,** especialmente para os comandos usados com mais frequência. As faixas de faixa bem projetadas têm ícones autoexplicativos para ajudar os usuários a localizar e entender os comandos com eficiência.
- **Escolha ícones que sejam reconhecíveis e distinguíveis,** especialmente para os comandos usados com mais frequência. Verifique se os ícones têm formas e cores distintivos. Isso ajuda os usuários a localizar os comandos rapidamente, mesmo que não se lembrem do símbolo de ícone.

    | Correto                                                                                                 | Incorreto                                                                               |
    |--------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
    | ![captura de tela do conta-gotas de olho azul e lápis amarelo ](images/cmd-ribbons-image46.png)<br/>Use forma e cor para criar ícones que são fáceis de distinguir. | ![captura de tela do conta-gotas de olho azul e lápis azul ](images/cmd-ribbons-image47.png)<br/> Os ícones que têm a mesma cor são difíceis de distinguir|

- ![captura de tela do comando de comentários no contêiner Popup ](images/cmd-ribbons-image48.png)<br/>**Considere a criação de ícones de grupos de pop-up colocando o ícone de 16x16 pixels do comando mais proeminente no grupo dentro de um contêiner visual de 32 pixels.** Você não precisa criar ícones diferentes para grupos pop-up.
- ![captura de tela dos botões de comando de formatação de texto ](images/cmd-ribbons-image25.png)<br/>**Se for útil, altere o ícone para refletir o estado atual.** Fazer isso é especialmente útil para botões de divisão cujo efeito padrão pode ser alterado.
- **Verifique se os ícones da faixa de medida estão em conformidade com as diretrizes de ícone do estilo Aero.** No entanto, os ícones da faixa de faixas são exibidos diretamente em, em vez de serem mostrados em perspectiva.

| Correto                                                                                                 | Incorreto                                                                               |
    |--------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
    | ![captura de tela de ícones de comando bidimensionais ](images/cmd-ribbons-image49.png)<br/> Use ícones bidimensionais.|![captura de tela de ícones de comando tridimensionais ](images/cmd-ribbons-image50.png)<br/> Não use ícones tridimensionais. |
 
### <a name="enhanced-tooltips"></a>Dicas de ferramentas aprimoradas

- **Todos os comandos da faixa de ferramentas devem ter dicas de ferramenta aprimoradas** para fornecer o nome do comando, a tecla de atalho, a descrição e as informações complementares opcionais. Evite dicas de ferramenta que simplesmente redeclarem o rótulo.

    **Incorreto:**

    ![captura de tela da dica de ferramenta que repete o nome do comando ](images/cmd-ribbons-image51.png)

    Neste exemplo, a dica de ferramenta simplesmente renomeia o rótulo de comando.

- **Quando for prático, descreva completamente o comando usando uma descrição concisa.** Vincule-se à ajuda somente se uma explicação adicional for realmente necessária.

    **Incorreto:**

    ![captura de tela da dica de ferramenta para o comando tachado ](images/cmd-ribbons-image52.png)

    Neste exemplo, o comando não precisa de ajuda.

- **Quando for útil, ilustre o efeito do comando usando uma visualização.**

    ![captura de tela de dica de ferramenta e grafo para inserir gráfico ](images/cmd-ribbons-image53.png)

    Neste exemplo, a imagem de dica de ferramenta ilustra o efeito do comando.

Para obter diretrizes de rotulamento, consulte [Rótulos de dica de ferramenta aprimorados](#enhanced-tooltips).

### <a name="access-keys-and-keytips"></a>Teclas de acesso e dicas de tecla

Keytips são o mecanismo usado para exibir chaves de acesso para comandos exibidos diretamente em uma faixa de faixas.

As chaves de acesso para comandos de menu suspenso são indicadas com um caractere sublinhado. Elas diferem das chaves de acesso de menu das seguintes maneiras:

- Podem ser usadas duas chaves de acesso de caractere. Por exemplo, FP pode ser usado para acessar o comando de pincel de formatação.
- As atribuições de chave de acesso são mostradas usando dicas em vez de sublinhados, portanto, a largura de caractere e os descendentes não são um fator para fazer atribuições.

- **Atribua chaves de acesso a todos os comandos e guias da faixa de e.** A única exceção possível é para comandos provenientes de suplementos herdados.
- **Para o botão aplicativo e a barra de ferramentas de acesso rápido:**
  - Atribua F ao botão do aplicativo. Essa atribuição é usada devido à similaridade do botão do aplicativo para o menu de arquivo tradicional.
  - ![captura de tela de dicas de atalho de comando em uma faixa de faixas ](images/cmd-ribbons-image54.png)<br/>Para a barra de ferramentas de acesso rápido e as listas de arquivos usados recentemente, atribua chaves de acesso numericamente.
- ![captura de tela mostrando KeyTips para guias ](images/cmd-ribbons-image55.png)<br/>**Para guias:**
  - Atribua H a página inicial.
  - Começando com as guias usadas com mais frequência, atribua a primeira letra do rótulo.
  - Para qualquer guia que não possa ser atribuída à primeira letra, escolha uma consoante distinta ou uma vogal no rótulo.
  - Para programas que usaram suporte para barras de menu, busque manter a compatibilidade de chave de acesso com a melhor extensão prática. Evite atribuir diferentes significados para acessar chaves de categorias de menu herdadas. Por exemplo, se a versão da barra de menus herdada de um programa tivesse um menu Editar, busque usar uma tecla de acesso E para a guia equivalente. Se não houver nenhuma guia equivalente, não atribua uma tecla de acesso E a qualquer guia para evitar confusão.
- ![captura de tela mostrando KeyTips para uma faixa de uma ](images/cmd-ribbons-image56.png)<br/>**Para comandos, menus e submenus da faixa de medida:**
  - Atribua combinações de teclas de acesso exclusivas dentro de uma guia. Você pode reutilizar combinações de teclas de acesso dentro de guias diferentes.
  - Sempre que possível, atribua as chaves de acesso padrão para comandos comumente usados. Consulte a [tabela de chave de acesso padrão](inter-keyboard.md).
  - Para outros comandos:
    - Para os comandos usados com mais frequência, escolha letras no início da primeira ou segunda palavra do rótulo, preferivelmente a primeira letra.
    - Para comandos usados com menos frequência, escolha letras que sejam uma consoante distinta ou uma vogal no rótulo, como "x" em "Exit".
    - Para os comandos usados com menos frequência e iniciadores de caixa de diálogo, use duas letras conforme necessário.
    - Para menus e submenus, use uma única letra para reduzir o número de pressionamentos de tecla necessários para o comando completo.
    - Não use chaves de acesso começando com J, Y ou Z porque elas são usadas para guias contextuais, dicas de tecla não atribuídas e grupos de pop-ups.
- ![captura de tela de KeyTips para grupos de pop-up ](images/cmd-ribbons-image58.png)<br/>**Para grupos de pop-up:**
  - Use uma chave de acesso de duas letras que comece com Z.
  - Começando com os grupos usados com mais frequência, atribua a segunda letra de tecla de acesso à primeira letra do rótulo.
  - Para todos os grupos restantes, escolha uma consoante distinta ou uma vogal no rótulo.

Para obter diretrizes de teclas de atalho, consulte [teclado](inter-keyboard.md).

### <a name="application-buttons"></a>Botões de aplicativo

- **Use um botão de aplicativo para apresentar um menu de comandos que envolvem algo para ou com um arquivo.** Os exemplos incluem comandos que tradicionalmente entram no menu arquivo para criar, abrir e salvar arquivos, imprimir e enviar e publicar documentos.
- **Sempre forneça um botão de aplicativo ao usar uma faixa de faixas.** Se o programa não usar arquivos, use o botão aplicativo para acessar as opções do programa e o comando sair. Os botões de aplicativo sempre exibem um menu de comando que nunca são apenas decorativos.
- **Use os comandos de menu do aplicativo padrão a seguir quando apropriado:**
  - Novo  
  - Aberto  
  - Salvar  
  - Salvar como...
  - Imprimir...
  - Impressão rápida  
  - Visualizar impressão  
  - Fechar  
  - Opções  
  - Fechar  
  
- **Reserve comandos que pertençam ao menu do aplicativo apenas para esse menu.** Não os coloque de forma redundante em qualquer uma das guias.
- Para cada item de menu, forneça:
  - **Um rótulo com o nome do comando.**
  - **Um ícone de 32 pixels.**
  - **Uma breve descrição.** Verifique se a descrição pode ser exibida usando no máximo duas linhas de texto.
- ![captura de tela da dica de ferramenta documentando a tecla de atalho ](images/cmd-ribbons-image59.png)<br/>**Use dicas de ferramenta para documentar as teclas de atalho.** Ao contrário dos menus normais, os menus de aplicativo não documentam as teclas de atalho usando rótulos.

### <a name="quick-access-toolbars"></a>Barras de ferramentas de acesso rápido

- **Use a barra de ferramentas de acesso rápido para fornecer acesso a comandos usados com frequência.** Os comandos podem ser do botão aplicativo ou da faixa de faixas.
- **Sempre forneça uma barra de ferramentas de acesso rápido ao usar uma faixa de faixas.** Faça isso mesmo se a faixa de faixas tiver uma única guia; Isso fornece consistência entre programas.
- **Preencha a barra de ferramentas de acesso rápido com os comandos usados com frequência no menu do aplicativo.** Forneça salvar e desfazer se o seu programa oferecer suporte a eles e abrir e imprimir, se houver suporte e frequentemente usados.
- **Para o menu Personalizar barra de ferramentas de acesso rápido, forneça até 12 dos comandos imediatos usados com mais frequência.** Os comandos imediatos não exigem entrada adicional antes de entrarem em vigor e, portanto, são bem adequados para a barra de ferramentas de acesso rápido. Embora esses possam ser comandos imediatos, prefira os comandos que não estão na guia início, porque os usuários têm mais probabilidade de escolher esses.
- **Para o menu Personalizar barra de ferramentas de acesso rápido, se houver um par de comandos relacionados, forneça ambos, independentemente da frequência.** Pares comuns são abrir/fechar, voltar/avançar e desfazer/refazer.
- **Para a caixa de diálogo Personalizar acesso rápido da barra de ferramentas, forneça uma maneira de adicionar qualquer comando.** Forneça um filtro de comandos populares que exibe os comandos usados com mais frequência e selecione esse filtro por padrão.

### <a name="dialog-box-launchers"></a>Inicializadores de caixa de diálogo

- ![captura de tela de caixa de diálogo fonte e grupo de fontes ](images/cmd-ribbons-image60.png)<br/>**Forneça um grupo com um iniciador de caixa de diálogo se houver uma caixa de diálogo relacionada com comandos e configurações usados com pouca frequência.** A caixa de diálogo deve conter todos os comandos do grupo, além de outros não um conjunto de comandos completamente diferente ou os mesmos comandos que o grupo.
- **Não use um iniciador de caixa de diálogo para executar comandos diretamente.** Um iniciador de caixa de diálogo deve exibir uma caixa de diálogo.
- **Não use um iniciador de caixa de diálogo para acessar configurações e comandos usados com frequência.** Em comparação com os comandos diretamente na faixa de opções, os comandos e as configurações da caixa de diálogo são relativamente não detectáveis.
- **Corresponda ao nome da caixa de diálogo com o nome do grupo.** Não precisa ser uma correspondência exata, mas os nomes devem ser semelhantes o suficiente para que os usuários não fiquem surpresos com os resultados.

    **Incorreto:**

    ![captura de tela da caixa de diálogo som do lembrete ](images/cmd-ribbons-image61.png)

    Embora um alarme de lembrete seja uma opção de lembrete, o uso do iniciador da caixa de diálogo para definir o som do lembrete é inesperado.

- **Exibe somente os comandos e configurações relacionados ao grupo.** Se a caixa de diálogo Exibir outras coisas, os usuários poderão concluir que esse caminho para esses outros comandos e configurações é o único caminho.

    **Incorreto:**

    ![captura de tela da caixa de diálogo fonte ](images/cmd-ribbons-image62.png)

    Neste exemplo, a caixa de diálogo fonte exibe as configurações de espaçamento de caracteres, que não estão relacionadas à guia associada.

## <a name="labels&quot;></a>Rótulos

### <a name=&quot;tab-labels&quot;></a>Rótulos de guia

- **Rotular todas as guias.**
- Sempre que for prático, **use as guias da faixa de medida padrão**.
- **Prefira rótulos concisos e de palavras simples.** Embora os rótulos de várias palavras sejam aceitáveis, eles ocupam mais espaço e são mais difíceis de localizar.
- **Escolha nomes de guias significativos que descrevam claramente e precisamente seu conteúdo.** Os nomes devem ser específicos, mas não muito específicos. Os nomes de guias devem ser previsíveis o suficiente para que os usuários não fiquem surpresos com seu conteúdo. Observe que a guia página inicial é genericamente nomeada porque é usada para os comandos usados com mais frequência.
- **Não use nomes** de grupo, como &quot;básico&quot; e &quot;avançado&quot;. Eles exigem que os usuários determinem se o comando que ele está procurando é básico ou avançado.
- **Escolha nomes de guias que reflitam sua finalidade.** Considere as metas ou tarefas associadas à guia.
- **Escolha nomes de guias que sejam claramente distintos de todos os outros nomes de guias.**
- **Use substantivos ou verbos para guias.** Nomes de guias não exigem frases paralelas, portanto, escolha o melhor rótulo, independentemente de ser um substantivo ou verbo.
- **Não use gerúndios** (nomes que terminam em &quot;-ing"). Use o verbo do qual o gerund é derivado em seu lugar. (por exemplo, use "Draw" em vez de "Drawing".)
- **Evite nomes de guias com as mesmas letras iniciais, especialmente guias adjacentes.** Quando a faixa de faixas for reduzida, esses nomes de guias terão o mesmo texto truncado.
- **Prefira nomes singulares.** No entanto, você pode usar um nome de pural se o nome do singular for estranho.
- **Use a capitalização de estilo de título.**
- **Não use pontuação final.**

### <a name="contextual-tab-and-tab-set-labels"></a>Rótulos de guia contextual e conjunto de guias

- **Encerrar rótulos de conjunto de guias contextuais com "Ferramentas".** Isso ajuda a identificar a finalidade das guias contextuais.
- Use a capitalização de estilo de título.
- Não use pontuação final.

### <a name="group-labels"></a>Rótulos de grupo

- **Rotule todos os** grupos, a menos que o grupo tenha um único comando e os rótulos de grupo e comando sejam os mesmos.

- **Use os grupos de faixa de opções padrãoTodos os práticos.**
- **Prefira rótulos concisos e de palavra única.** Embora rótulos de várias palavras sejam aceitáveis, eles levam mais espaço e são mais difíceis de ser localizados.
- **Escolha nomes de grupo significativos que descrevam seu conteúdo com clareza e precisão.** Os nomes devem ser específicos, não genéricos.
- **Escolha nomes de grupo que reflitam sua finalidade.** Considere as metas ou tarefas associadas aos comandos no grupo.
- **Evite usar gerunds** (nomes que terminam em "-ing"). No entanto, você pode usar gerunds se usar o verbo do qual o gerund é derivado seria confuso. Por exemplo, use "Edição" e "Prova" em vez de "Editar" e "Prova".
- **Não use nomes de grupo que sejam iguais aos nomes de tabulação.** Usar o nome da guia em que o grupo está não fornece informações e usar o nome de uma guia diferente é confuso.
- **Prefira nomes singulares.** No entanto, você poderá usar um nome pural se o nome singular for estranho. 
- **Use a capitalização com estilo de frase.**
- **Não use pontuação final.**

### <a name="command-labels"></a>Rótulos de comando

- **Rotule todos os comandos.** Ter rótulos de texto explícito ajuda os usuários a encontrar e entender comandos. **Exceção:** Um comando poderá ser sem rótulo se seu ícone for extremamente conhecido e o espaço estiver em um premium. Provavelmente, os comandos sem rótulo estarão na guia Página Base. Nesse caso, atribua sua propriedade Name a um rótulo de texto apropriado. Isso permite que produtos de tecnologia adaptativa, como leitores de tela, forneçam aos usuários informações alternativas sobre o gráfico.
- **Para botões de comando, use um rótulo conciso e autoexplicativo.** Use uma única palavra, se possível; máximo de quatro palavras.
- **Para listas listadas, se a lista sempre tiver um valor, use o valor atual como o rótulo.**
- ![captura de tela do prompt de livros de endereços de pesquisa ](images/cmd-ribbons-image67.png)<br/>Se uma [lista de listas listadas editáveis](/windows/desktop/uxguide/ctrl-drop) não tiver um valor, use um [prompt](glossary.md).
- **Listas listadas que não são autoexplicativas ou que são usadas com pouca pouca experiência precisam de um rótulo explícito.** Coloque dois-pontos no final do rótulo.
- ![captura de tela de automaticamente após: \[ segundos \] ](images/cmd-ribbons-image69.png)<br.>Para caixas **de texto, use um rótulo explícito.** Coloque dois-pontos no final do rótulo.
- **Use a capitalização com estilo de frase.** Fazer isso é mais apropriado para o Windows [tom](text-style-tone.md).
- **Inicie o rótulo com um verbo imperativo.** a menos que seja o mesmo que o nome da guia ou do grupo ou um verbo comum como Mostrar, Criar, Inserir ou Formatar.
- **Não use pontuação final.**
- **Para economizar espaço, não coloque reellips nos rótulos de comando da faixa de opções.** No entanto, as reellipses são usadas por comandos no botão Aplicativo e nos menus suspensos.

### <a name="enhanced-tooltip-labels"></a>Rótulos de dica de ferramenta aprimorados

- **Use o título para dar o nome do comando e sua tecla de atalho, se aplicável.**
- **Para o título, não use pontuação final.**
- **Inicie a descrição com um verbo.** Use a descrição para ajudar os usuários a determinar se um recurso específico é aquele que eles estão procurando. A descrição deve ser formulada para concluir a frase "Este é o recurso certo a ser usado se você quiser...".
- **Mantenha a descrição curta.** Vá direto para o ponto. Texto longo não desanimo a leitura.
-   ![captura de tela do botão de divisão de colar e duas dicas de ferramenta ](images/cmd-ribbons-image70.png)<br/>**Para botões de divisão, use uma dica de ferramenta diferente para explicar o menu de botão de divisão.**
- **Use uma descrição complementar opcional para explicar como usar o controle .** Esse texto poderá incluir informações sobre o estado do controle (incluindo por que ele está desabilitado) se o próprio controle não indicar estado. Mantenha este texto curto e use um tópico de Ajuda para obter explicações mais detalhadas.
- ![captura de tela da dica de ferramenta com gráfico e texto Para a descrição e a descrição ](images/cmd-ribbons-image71.png)**complementares, use frases completas com pontuação final.**
- Use a capitalização com estilo de frase.

### <a name="application-button-labels"></a>Rótulos de botão do aplicativo

- [captura de tela da opção de impressão rápida selecionada ](images/cmd-ribbons-image72.png)<br/>**Use "Rápido" para indicar uma versão imediata de um comando.**

- **Use uma reellipse para indicar que um comando requer mais informações.**
- **Use a capitalização com estilo de frase.**

## <a name="documentation"></a>Documentação

Ao se referir a faixas de opções:

- Consulte a faixa de opções e seus componentes como faixa de opções, guias, grupos e controles. Esses termos não estão em maiúsculas.
- Consulte o botão arredondar como o botão Aplicativo e o menu que ele contém como o menu Aplicativo.
- Consulte a barra de ferramentas como a Barra de Ferramentas de Acesso Rápido.
- Consulte as guias por seus rótulos e a guia de palavras. Use o texto exato do rótulo, incluindo sua capitalização.
- Consulte os comandos por seus rótulos. Consulte comandos sem rótulo por seus nomes de dica de ferramenta. Use o texto exato do rótulo, incluindo sua capitalização, mas não inclua as reellipses. Não inclua a palavra botão ou comando.
- Para descrever a interação do usuário, use clique para guias e controles. Use Enter para listas de listas listadas editáveis. Não use escolher, selecionar ou escolher.
- Consulte itens indisponíveis como indisponíveis, não como esmaecidas, desabilitadas ou esmaecidas. Na documentação de programação, use desabilitado.
- Quando possível, forja os rótulos usando texto em negrito. Caso contrário, coloque os rótulos entre aspas somente se necessário para evitar confusão.

Exemplos:

- Na guia **Página** Base, clique **em Colar especial.**
- Na guia **Página** Base, na caixa **Fonte,** insira "Segoe UI".
- Na guia **Revisão,** clique em **Mostrar marcação** e, em seguida, clique **em Revistores**.
- Na guia **Formato** , em **Ferramentas de imagem**, clique em **Compactar imagens**.
