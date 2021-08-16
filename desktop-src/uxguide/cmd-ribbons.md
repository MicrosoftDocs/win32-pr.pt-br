---
title: Faixas de opções
description: As faixas de opções são a maneira moderna de ajudar os usuários a encontrar, entender e usar comandos com eficiência e diretamente \ 8212; com um número mínimo de cliques, com menos necessidade de recorrer a avaliação e erro e sem precisar consultar a Ajuda.
ms.assetid: 8a4699da-9840-4622-9e94-d6d5c4e7708c
ms.custom: contperf-fy21q1
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: db5a64d50bd225b714c2ff0578145c47c66bedb557dd067e0cdf89f369178b1e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118042407"
---
# <a name="ribbons"></a>Faixas de opções

> [!NOTE]
> Este guia de design foi criado para Windows 7 e não foi atualizado para versões mais recentes do Windows. Grande parte das diretrizes ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais.](/windows/uwp/design/)

As faixas de opções são a maneira moderna de ajudar os usuários a encontrar, entender e usar comandos com eficiência e diretamente com um número mínimo de cliques, com menos necessidade de recorrer a avaliação e erro e sem precisar consultar a Ajuda.

Uma faixa de opções é uma barra de comandos que organiza os recursos de um programa em uma série de guias na parte superior de uma janela. O uso de uma faixa de opções aumenta a capacidade de descoberta de recursos e funções, permite um aprendizado mais rápido do programa como um todo e faz com que os usuários se sintam mais no controle de sua experiência com o programa. Uma faixa de opções pode substituir a barra de menus tradicional e as barras de ferramentas.

![captura de tela de uma faixa de opções ](images/cmd-ribbons-image1.png)

Uma faixa de opções típica.

As guias da faixa de opções são compostas por grupos, que são um conjunto rotulado de comandos intimamente relacionados. Além de guias e grupos, as faixas de opções consistem em:

- Um botão Aplicativo, que apresenta um menu de comandos que envolvem fazer algo com ou com um documento ou workspace, como comandos relacionados ao arquivo.
- Uma Barra de Ferramentas de Acesso Rápido, que é uma barra de ferramentas pequena e personalizável que exibe comandos usados com frequência.
- As guias principais são as guias que sempre são exibidas.
- Guias contextuais, que são exibidas somente quando um tipo de objeto específico é selecionado. As guias que sempre são exibidas são chamadas de guias principais.
- Um conjunto de guias é uma coleção de guias contextuais para um único tipo de objeto. Como os objetos podem ter vários tipos (por exemplo, um header em uma tabela que tem uma imagem é de três tipos), pode haver vários conjuntos de guias contextuais exibidos por vez.
- Guias modais, que são guias principais exibidas com um modo temporário específico, como visualização de impressão.
- Galerias, que são listas de comandos ou opções apresentadas graficamente. Uma galeria baseada em resultados ilustra o efeito dos comandos ou das opções em vez dos próprios comandos. Uma galeria na faixa de opções é exibida em uma faixa de opções, em vez de uma janela pop-up.
- Dicas de ferramentas aprimoradas, que explicam concisamente seus comandos associados e dão as teclas de atalho. Eles também podem incluir gráficos e referências à Ajuda. As dicas de ferramenta aprimoradas reduzem a necessidade de ajuda relacionada a comandos.
- Iniciadores de caixa de diálogo, que são botões na parte inferior de alguns grupos que abrem caixas de diálogo que contêm recursos relacionados ao grupo.

As faixas de opções foram introduzidas originalmente Microsoft Office 2007. Para saber por que Office precisa usar faixas de opções e os muitos problemas que usam uma faixa de opções são resolvidos, consulte [The Story of the Ribbon](/archive/blogs/jensenh/the-story-of-the-ribbon).

> [!Note]  
> Diretrizes [relacionadas a menus](cmd-menus.md), [barras de ferramentas,](cmd-toolbars.md) [botões de comando](ctrl-command-buttons.md)e ícones são [apresentadas](vis-icons.md) em artigos separados.

## <a name="is-this-the-right-user-interface"></a>Essa é a interface do usuário certa?

Para decidir usar uma faixa de opções, considere estas perguntas:

### <a name="program-type"></a>Tipo de programa

- **Que tipo de programa você está projetando?** O tipo de programa é um bom indicador da adequação de uma faixa de opções. As faixas de opções funcionam bem para programas de criação e criação de documentos, bem como visualizadores de documentos e navegadores. As faixas de opções podem funcionar para outros tipos de programas, mas outras formas de apresentação de comando podem ser mais apropriadas. Em geral, programas leves devem ter uma apresentação de comando leve.

### <a name="discoverability-and-learning-issues"></a>Problemas de descoberta e aprendizado

- **Os usuários têm problemas para localizar comandos? Os usuários estão solicitando recursos que já estão no programa?** Em caso afirmativo, o uso de uma faixa de opções facilitará a encontrar comandos com rótulos autoexplicativos e o agrupamento de comandos relacionados. Usar uma faixa de opções também é melhor do que barras de menu e barras de ferramentas para crescimento futuro.
- **Os usuários têm problemas para entender os comandos do programa? Geralmente, eles recorrem a "avaliação e erro" para selecionar o comando correto ou determinar como os comandos funcionam?** Nesse caso, usar uma faixa de opções com comandos orientados a resultados com base em galerias e visualizações ao vivo facilita a compreensão dos comandos.

### <a name="command-characteristics"></a>Características do comando

- **Os comandos são apresentados em vários locais? Se o programa já existir, os comandos serão apresentados em barras de menu, barras de ferramentas, painéis de tarefas e dentro da própria área de trabalho?** Nesse caso, o uso de uma faixa de opções unificará os comandos em um único local, tornando-os mais fáceis de localizar.
- **Os comandos se aplicam a toda a janela ou somente a painéis específicos?** As faixas de opções funcionam melhor para comandos que se aplicam a toda a janela ou a objetos específicos. Os comandos in-place funcionam melhor para painéis de janela individuais.
- **A maioria dos comandos pode ser apresentada diretamente? Ou seja, os usuários podem interagir com eles usando um único clique? Se os comandos comumente usados são acessados de menus e caixas de diálogo, eles podem ser refactorados para serem diretos?** Embora alguns comandos possam ser apresentados usando menus e caixas de diálogo, apresentar a maioria dos comandos dessa maneira prejudica a eficiência de uma faixa de opções, possivelmente tornando uma barra de menus uma opção melhor.

### <a name="command-scale"></a>Escala de comando

- **Há um pequeno número de comandos? Os comandos usados com mais frequência podem ser apresentados facilmente em uma única barra de ferramentas simples?** O uso de uma faixa de opções vale a pena se a adição de guias principais e contextuais resulta em uma guia Página Base simples que pode ser usada sozinho para executar as tarefas mais comuns. Caso não seja, o benefício de usar uma faixa de opções pode não justificar seu peso extra para um pequeno número de comandos.
- **Há um grande número de comandos? Usar uma faixa de opções exigiria mais de sete guias principais? Os usuários constantemente teriam que alterar guias para executar tarefas comuns?** Nesse caso, usar barras de ferramentas (que não exigem alteração de guias) e janelas de paleta [(o](cmd-toolbars.md) que pode exigir a alteração de guias, mas pode haver várias abertas por vez) pode ser uma opção mais eficiente.
- **Os usuários tendem a usar um pequeno número de comandos na maioria das vezes?** Nesse caso, eles podem usar uma faixa de opções com eficiência colocando esses comandos na guia Página Base. A alteração constante de guias torna uma faixa de opções muito ineficiente.
- **O programa se beneficia de tornar a área de conteúdo do programa o mais grande possível?** Se sim, usar uma barra de menus e uma única barra de ferramentas é mais eficiente do que uma faixa de opções. No entanto, se o programa exigir três ou mais linhas de barras de ferramentas ou usar painéis de tarefas, o uso de uma faixa de opções será mais eficiente em termos de espaço.
- **Os usuários tendem a trabalhar em uma área específica dentro de uma janela grande no programa por longos períodos de tempo?** Em caso afirmado, eles se beneficiariam da proximidade de minibaras de ferramentas, janelas de paleta e comandos diretos. Fazer a viagem de ida e volta da área de trabalho para a faixa de opções seria muito ineficiente.
- **Para eficiência e flexibilidade, os usuários precisam fazer alterações significativas no conteúdo, no local ou no tamanho da apresentação do comando?** Se sim, barras de ferramentas personalizáveis e extensíveis e janelas de paleta são uma opção melhor. Observe que alguns tipos de barras de ferramentas podem ser desencaixados para se tornarem janelas de paleta, e as janelas de paleta podem ser movidas, relizadas e personalizadas.

Por fim, considere essa pergunta final: A melhoria na capacidade de descoberta, na facilidade de aprendizado, na eficiência e na produtividade vale o custo do espaço extra e a necessidade de guias organizar **comandos?** Se sim, usar uma faixa de opções é uma excelente opção. Se você não tiver certeza, considere a usabilidade de testar um design baseado em faixa de opções e compará-lo com a melhor alternativa.

As faixas de opções são uma forma nova e envolvente de apresentação de comando e uma ótima maneira de modernizar um programa. Mas, por mais atraentes que sejam, eles não são a escolha certa para cada programa.

**Incorreto:**

![captura de tela de uma faixa de opções com uma calculadora ](images/cmd-ribbons-image2.png)

Não faça isso!

## <a name="seven-most-important-things"></a>Sete coisas mais importantes

1. Escolha uma solução de comando adequada para o tipo de programa. Usar uma faixa de opções deve tornar um programa mais simples, mais eficiente e mais fácil de usar nunca o oposto. Se usar uma faixa de opções não for apropriado, considere usar comandos avançados.  
2. Não suia o desafio de criar uma faixa de opções efetiva. Não espere que seja uma porta simples das barras de menu e das barras de ferramentas existentes. E não leve em conta que usar uma faixa de opções torna seu programa melhor automaticamente. Estar disposto a comprometer o tempo e o esforço necessários para um reprojeto de comando é um fator importante na decisão de usar uma faixa de opções.  
3. Tornar os comandos descobertos. Escolha um design de guia que tenha um mapeamento claro, óbvio e exclusivo entre seus comandos e as guias rotuladas descritivo onde eles residem. Os usuários devem ser capazes de determinar com rapidez e confiança qual guia tem o comando que eles estão procurando e raramente escolher a guia errada.  
4. Tornar os comandos autoexplicativos. Os usuários devem entender o efeito de um comando de seu rótulo, ícone, dica de ferramenta e versão prévia. Eles não devem ter que experimentar ou ler um tópico de Ajuda para ver como um comando funciona.  
5. Tornar o uso dos comandos eficiente:
    - Os usuários devem gastar a maior parte do tempo na guia Página Base.
    - Os usuários raramente devem ter que alterar guias durante tarefas comuns.
    - Quando a janela é maximizada e os usuários estão na guia correta, os comandos usados com mais frequência têm mais ênfase visual e os usuários podem invocá-los com um único clique. Os usuários podem executar todos os outros comandos na guia com no máximo quatro cliques.
    - Os usuários não devem ter que abrir caixas de diálogo para dar comandos e alterar atributos em tarefas comuns.
6. Ajude os usuários a escolher comandos e opções com segurança e minimizar a necessidade de avaliação e erro. Use comandos orientados a resultados sempre que apropriado, geralmente na forma de galerias e visualizações ao vivo.  
7. Verifique se a faixa de faixas é dimensionada bem com os maiores tamanhos de janela para o menor.  

## <a name="design-concepts"></a>Conceitos de design

### <a name="adapting-a-ribbon-in-an-existing-program"></a>Adaptando uma faixa de faixas em um programa existente

Embora você possa simplesmente refatorar uma barra de menus tradicional e um design de barra de ferramentas de um programa existente para um formato de faixa de faixas, fazer com que a maior parte do valor de usar uma faixa de uma. As faixas de faixa têm mais valor quando usadas para apresentar comandos imediatos, orientados a resultados, geralmente na forma de galerias e visualizações dinâmicas. Comandos orientados a resultados facilitam a compreensão dos comandos e os usuários muito mais eficientes e produtivos. Em vez de refatorar seus comandos existentes, é melhor reformular completamente como os comandos são executados em seu programa.

Não subestime o desafio de criar uma faixa de faixas em vigor. E não é necessário que o uso de uma faixa de opção faça com que seu programa seja melhor. A criação de uma faixa de uma vez em vigor leva muito tempo e esforço. Estar disposto a confirmar o tempo e o esforço necessários para tal reestruturação de comandos é um fator importante na decisão de usar uma faixa de uma.

### <a name="the-nature-of-ribbons"></a>A natureza das faixas de faixa

Em comparação com barras de menus e barras de ferramentas tradicionais, as faixas de opções têm as seguintes características:

- **Uma interface do usuário única (IU) para todos os comandos.** As barras de menu são abrangentes e fáceis de aprender, e as barras de ferramentas são eficientes e diretas, mas por que não usar um pouco mais espaço na tela para criar uma interface do usuário de comandos únicos que realiza todos eles? Com apenas uma interface do usuário, as faixas de faixa não exigem que os usuários descubram qual interface do usuário tem o comando que estão procurando.
- **Visível e auto-explicativa.** Os comandos da barra de menus são autoexplicativos por meio de seus rótulos, mas ficam ocultos na exibição na maior parte do tempo. Para economizar espaço na tela, os botões da barra de ferramentas são basicamente representados por ícones em vez de rótulos (embora alguns botões da barra de ferramentas usem ambos) e dependam de dicas de ferramenta quando o ícone não é auto-explicativo. No entanto, os usuários geralmente conhecem os ícones apenas para os comandos usados com mais frequência.
- Ao apresentar a maioria dos comandos com ícones rotulados, os comandos da faixa de opções são visíveis e autoexplicativos e usam dicas de ferramenta somente para fornecer informações complementares. Há pouca necessidade de ir em outro lugar (como ajuda) para entender um comando.
- **Rotulado como agrupamento.** Enquanto as categorias de menu são rotuladas, os grupos dentro de um menu suspenso não são e são indicados somente com um separador sem rótulo. Os grupos dentro das barras de ferramentas também são indicados com separadores sem rótulo.
- Ao organizar comandos em grupos rotulados, as faixas de faixa facilitam a localização de comandos e a determinação da finalidade.
- **Modal, mas não hierárquico.** Escala de barras de menu criando uma hierarquia de comandos. Os menus com muitos itens podem usar um ou mais níveis de submenus para fornecer mais comandos.
- Os comandos da faixa de medida exigem mais espaço que os comandos da barra de ferramentas, portanto, eles usam guias para dimensionar. Esse uso de guias torna as faixas de formas modais, exigindo que os usuários alterem os modos ocasionalmente para localizar comandos. No entanto, dentro de uma guia, a maioria dos comandos é direta ou usa um único botão de divisão ou botão de menu, não uma hierarquia.
- **Direto e imediato.** Um comando é direto se for invocado com um único clique (ou seja, sem navegar pelos menus) e imediato se entrar em vigor imediatamente (ou seja, sem caixas de diálogo para coletar entrada adicional). Os comandos da barra de menus são sempre indiretos e geralmente não imediatos. Assim como as barras de ferramentas, a maioria dos comandos da faixa de medida é projetada para ser direta e imediata, com os comandos usados com mais frequência invocados com um único clique e sem a necessidade de uma caixa de diálogo para coletar entrada adicional.
- **Espaçoso.** Barras de menus e barras de ferramentas são projetadas principalmente para serem eficientes em termos de espaço. Para fornecer seus benefícios, as faixas de ferramentas podem consumir mais espaço vertical, sendo aproximadamente o equivalente de uma barra de menus, além de três linhas de barras. Sendo que poucos programas têm três ou mais linhas de barras de ferramentas, a faixa de faixas geralmente consome mais espaço do que as UIs tradicionais para comandos.
- **Tem um botão de aplicativo e uma barra de ferramentas de acesso rápido.** Uma faixa de Ribbon sempre é apresentada com um botão de aplicativo e uma barra de ferramentas de acesso rápido. Isso permite que os usuários acessem comandos relacionados a arquivos e frequentemente usados sem alterar as guias e promove a consistência entre programas.
- **Personalização mínima.** Embora as barras de menu tenham uma apresentação fixa, muitas barras de ferramentas são bastante personalizáveis, permitindo que os usuários definam locais, tamanhos e conteúdos. Uma faixa de medida em si não é personalizável, mas a barra de ferramentas de acesso rápido fornece personalização limitada.
- **Acessibilidade de teclado aprimorada.** As barras de menu têm excelente acessibilidade de teclado porque pressionar a tecla Alt diretamente fornece o foco de entrada da barra de menus. No entanto, não há tal mecanismo para barras de ferramentas porque elas compartilham a navegação de teclado com o conteúdo da janela. Consequentemente, os usuários devem navegar até a barra de ferramentas usando a tecla Tab (que recebe a última parada de tabulação) e, em seguida, navegar até um comando específico usando as teclas de direção.

Por outro lado, as faixas de faixa fornecem acessibilidade de teclado aprimorada por meio de [dicas](glossary.md)de tecla, geralmente com um processo de três etapas:

- Pressione Alt para entrar no modo KeyTip.
- Pressione um caractere para escolher uma guia, o botão aplicativo ou um comando na barra de ferramentas de acesso rápido.
- Em uma guia, pressione uma ou duas letras para escolher um comando.

    Essa abordagem é altamente Visual. Ele também é mais flexível, permitindo que ele Escale melhor e tenha mais atribuições de chave de acesso mnemônico.

    Não confunda chaves de acesso com teclas de atalho. Embora as teclas de acesso e as chaves de atalho forneçam acesso de teclado à interface do usuário, elas têm finalidades e diretrizes diferentes. Para obter mais informações, consulte [teclado](inter-keyboard.md).

### <a name="the-nature-of-rich-commands"></a>A natureza dos comandos avançados

Comandos avançados referem-se à apresentação e à interação dos comandos usados pelas faixas de faixa, sem necessariamente usar um contêiner da faixa de uma. Os comandos avançados têm estas características:

- **Rotulagem.** Todos os comandos recebem rótulos autoexplicativos, com exceções somente quando os ícones são extremamente conhecidos e o espaço está em um nível Premium.

    **Correto:**

    ![captura de tela de uma faixa de formatos de formatação de caracteres ](images/cmd-ribbons-image3.png)

    Esses comandos são extremamente conhecidos e, portanto, não precisam de rótulos.

    **Incorreto:**

    ![captura de tela de uma faixa de bits com ícones usados raramente ](images/cmd-ribbons-image4.png)

    Esses ícones ininteligívels exigem rótulos para comandos avançados.

- **Automático.** Em vez de dimensionamento uniforme, os comandos são dimensionados em relação à sua frequência de uso e importância. Além de tornar mais fácil localizar e clicar nos comandos mais usados, ele também os torna mais [tocáveis](https://msdn.microsoft.com/library/windows/desktop/cc872774.aspx).

    ![captura de tela de um grande e três botões pequenos ](images/cmd-ribbons-image5.png)

    Neste exemplo, o botão usado com mais frequência é maior do que os outros.

- **Dimensionamento dinâmico.** Os controles de comando avançados se redimensionam para aproveitar ao máximo o espaço disponível, em vez de usar um tamanho fixo e truncar ou usar overflow quando o tamanho for muito pequeno.

    ![captura de tela de ampla faixa de forma com botões de tamanho igual ](images/cmd-ribbons-image6.png)![captura de tela de faixa de faixas pequena com botões mistos ](images/cmd-ribbons-image7.png)

    Neste exemplo, os botões de comando redimensionam para funcionar bem no espaço disponível.

- **Botões de divisão.** Os botões de divisão são uma boa maneira de consolidar um conjunto de variações de um comando quando necessário, mantendo a direção do comando usado com mais frequência.

    ![captura de tela do comando Salvar como e suas opções ](images/cmd-ribbons-image8.png)

    Neste exemplo, o comando Salvar como usa um botão de divisão, em que o botão principal executa a variação mais comum e a parte do menu revela um menu com variações do comando.

- **Menus suspensos avançados e galerias.** Os menus suspensos, listas suspensas e galerias usam o espaço necessário para se comunicar e diferenciar o efeito das opções, geralmente usando descrições de texto e gráficos. As categorias são usadas para organizar grandes conjuntos de opções.

    ![captura de tela das opções de menu suspenso com ícones ](images/cmd-ribbons-image9.png)

    Nestes exemplos, clicar em um botão de menu exibe uma lista de opções que mostram seu efeito.

- **Visualizações dinâmicas.** Sempre que o usuário passa o mouse sobre uma opção de formatação, o programa mostra a aparência dos resultados com essa formatação usando o conteúdo real.

    ![captura de tela de resultados de opções de formatação ](images/cmd-ribbons-image10.png)

    As visualizações dinâmicas mostram os resultados da aplicação de uma opção de formatação ao focalizar.

- **Dicas de ferramentas aprimoradas.** Eles explicam de forma concisa seus comandos associados e fornecem as teclas de atalho. Eles também podem incluir elementos gráficos e referências para ajudar (embora eles eliminem amplamente a necessidade de ajuda relacionada a comandos).

    ![captura de tela de grande dica de ferramenta com texto e gráfico ](images/cmd-ribbons-image11.png)

    As dicas de ferramentas avançadas explicam seus comandos associados de forma concisa.

Embora as faixas de faixa possam não ser adequadas para todos os programas, todos os programas podem se beneficiar potencialmente de comandos avançados.

### <a name="ribbons-always-have-an-application-button-and-quick-access-toolbar"></a>As faixas de faixa sempre têm um botão do aplicativo e uma barra de ferramentas de acesso rápido

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

- **Ordene.** As pessoas lidam em uma ordem da esquerda para a direita (em culturas ocidentais), portanto, você pode imaginar que os grupos na extrema esquerda são os mais perceptíveis. No entanto, o nome da guia realçado e o conteúdo da janela tendem a atuar como [pontos focal](vis-layout.md), de modo que os grupos no centro da guia geralmente recebam mais atenção do que o grupo mais à esquerda. Coloque os grupos usados com mais frequência nos locais mais proeminentes e verifique se há um fluxo lógico para os grupos na guia.

![captura de tela do grupo da área de transferência à extrema esquerda ](images/cmd-ribbons-image18.png)

Neste exemplo, os grupos de fontes e parágrafos são mais perceptíveis do que o grupo da área de transferência, pois eles são o que os olhos veem primeiro ao se mover para cima do documento.

![captura de tela do grupo de controle na guia revisão ](images/cmd-ribbons-image19.png)

Neste exemplo, o grupo de rastreamento recebe a maior atenção, em parte porque a guia realçada de revisão atua como um ponto focal.

- **Uniformidade.** Pode ser difícil reconhecer comandos quando a apresentação do comando parece ser a mesma. Usar ícones com diferentes formas e cores, grupos com formatos variados e comandos com tamanhos diferentes torna mais fácil para os usuários reconhecer grupos de comandos. Os comandos devem ter dimensionamento uniforme somente quando a faixa de faixas é reduzida para seus tamanhos menores.

| Correto | Incorreto |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| ![captura de tela de grupo com ícones de tamanho diferente ](images/cmd-ribbons-image20.png)<br/>Use uma variedade de tamanhos de ícone para melhorar a capacidade de reconhecimento| ![captura de tela do grupo com ícones de mesmo tamanho ](images/cmd-ribbons-image21.png)<br/>Esses comandos parecem muito semelhantes entre si porque são do mesmo tamanho. |

### <a name="previews"></a>Visualizações

Você pode usar vários tipos de visualizações para mostrar o que resultará de um comando. Usando as visualizações úteis, você pode melhorar a eficiência do seu programa e reduzir a necessidade da abordagem de aprendizagem de avaliação e erro. As visualizações dinâmicas também convidam experimentação e estimulam a criatividade.

Aqui estão alguns dos diferentes tipos de visualizações que você pode usar:

- **Ícones e gráficos realistas.** Imagens estáticas que fornecem uma indicação realista do efeito de um comando. Eles podem ser usados em galerias, menus suspensos e dicas de ferramentas aprimoradas.

![captura de tela da lista suspensa fonte ](images/cmd-ribbons-image22.png)

Neste exemplo, a lista suspensa fonte mostra cada nome de fonte usando a própria fonte.

![captura de tela da Galeria de miniaturas de marca d' água ](images/cmd-ribbons-image23.png)

Neste exemplo, miniaturas realísticas são usadas para mostrar as diferentes marcas d' água.

- **Ícones e elementos gráficos dinâmicos.** Ícones e gráficos que são modificados para refletir o estado atual. Esses ícones são especialmente úteis para galerias, bem como botões de divisão que alteram seu efeito padrão para que sejam iguais à última ação.

![captura de tela da Galeria de estilos de parágrafo ](images/cmd-ribbons-image24.png)

neste exemplo, Microsoft Word altera a galeria de estilos para refletir os estilos atuais.

![captura de tela dos botões de comando de formatação de texto ](images/cmd-ribbons-image25.png)

Neste exemplo, o Word altera os comandos de cor de realce de texto e cor da fonte para indicar seu efeito atual.

- **Visualizações dinâmicas.** Quando os usuários focalizam uma opção de formatação, a visualização dinâmica mostra a aparência dos resultados com essa formatação. As visualizações dinâmicas ajudam os usuários a fazer seleções com mais eficiência e confiança com base no contexto real do usuário.

![captura de tela do seletor de cor do comando de cor da página ](images/cmd-ribbons-image26.png)

Neste exemplo, o comando de cor da página executa uma visualização dinâmica mostrando o efeito das opções de cor ao focalizar.

As visualizações dinâmicas são um recurso poderoso que pode realmente melhorar a produtividade dos seus usuários, mas até mesmo as visualizações estáticas simples podem ser uma grande ajuda.

### <a name="scaling-the-ribbon"></a>Dimensionando a faixa de faixas

Dimensionar uma barra de ferramentas é simples: se uma janela for muito estreita para exibir uma barra de ferramentas, a barra de ferramentas exibirá o que se ajusta e tornará tudo mais acessível por meio de um botão de estouro. Uma meta dos comandos avançados é tirar o máximo proveito do espaço disponível, portanto, dimensionar uma faixa de faixas requer mais trabalho de design. Não há nenhum tamanho de faixa de fita padrão, portanto, você não deve criar uma faixa de bits com uma largura específica em mente. Você precisa criar layouts com uma ampla gama de larguras e perceber que qualquer uma delas pode ser a mais que seus usuários verão. O dimensionamento é uma parte fundamental do design da faixa de faixas, não a última etapa. Ao criar uma guia, especifique os layouts diferentes para cada grupo (até três), bem como as combinações que podem ser usadas juntas. A faixa de faixas mostrará a maior combinação válida que se ajusta ao tamanho da janela atual.

![captura de tela dos comandos de formatação nas barras de ferramentas do menu de estouro ](images/cmd-ribbons-image27.png) dimensionar usando um botão de estouro.

![captura de tela de faixas de faixa com várias larguras não há ](images/cmd-ribbons-image28.png) nenhum tamanho de faixa de bits padrão. O menor tamanho é um único ícone de grupo de pop-up.

## <a name="guidelines"></a>Diretrizes

### <a name="general"></a>Geral

- **Não combine faixas de ferramentas com barras de menus e barras de ferramentas em uma janela.** As faixas de faixa devem ser usadas no lugar de barras de menus e barras de ferramentas. No entanto, uma faixa de faixas pode ser combinada com elementos de navegação e janelas de paleta, como botões voltar e avançar e uma barra de endereços.
- **Sempre Combine uma faixa de guia com um botão do aplicativo e uma barra de ferramentas de acesso rápido.**
- **Selecione a guia mais à esquerda (geralmente página inicial) quando um programa é iniciado.** Não faça a última guia selecionada persistir nas instâncias do programa.
- **Mostrar a faixa de faixas em seu estado normal (não minimizada) quando um programa for iniciado pela primeira vez.** Os usuários geralmente deixam as configurações padrão inalteradas, portanto, minimizar a faixa de opções no início do programa provavelmente fará com que todos os comandos sejam menos eficientes. Além disso, mostrar a faixa de faixas inicialmente minimizada pode ser desorientada.
- **Fazer o estado da faixa de medida persistir nas instâncias do programa.** Por exemplo, se um usuário minimizar a faixa de faixas, ela deverá ser mostrada minimizada na próxima vez em que o programa for executado. Mas, novamente, não faça a última guia selecionada persistir dessa maneira.

### <a name="using-tabs"></a>Usando guias

Em geral, ter menos guias é melhor, portanto, remova as guias que não ajudam a atingir essas metas.

- **Sempre que for prático, use as guias padrão.** O uso de guias padrão melhora muito a descoberta, especialmente entre programas. Consulte as [guias da faixa](#standard-ribbon-tabs) de medida padrão mais adiante neste artigo.
- **Rotule a primeira guia página inicial, se apropriado.** A guia página inicial deve conter os comandos usados com mais frequência. Se você tiver usado comandos com frequência que não se ajustam às outras guias, a guia página inicial será o lugar certo para eles.
- Adicione uma nova guia se:
  - **Seus comandos estão fortemente relacionados a tarefas específicas e podem ser descritos com precisão pelo rótulo da guia.** Adicionar a guia deve ajudar a facilitar a localização de seus comandos, e não mais difícil.
  - **Seus comandos estão praticamente não relacionados a tarefas em outras guias.** A adição da guia não deve exigir mais alternância de tabulação durante tarefas normalmente executadas.
  - **A guia tem comandos suficientes para justificar a aparência de um local extra.** Não tenha guias com apenas alguns comandos. **Exceção:** Considere adicionar uma guia com alguns comandos se eles estiverem fortemente relacionados a uma tarefa específica e a adição da guia simplificar muito uma guia inicial excessivamente complexa.
- **Para as guias restantes, coloque as guias usadas com mais frequência primeiro, mantendo uma ordem lógica entre as guias.**
- **Otimize o design da guia para que os usuários encontrem comandos com rapidez e confiança.** Todas as outras considerações são secundárias.
- **Não forneça uma guia de ajuda.** Em vez disso, forneça assistência usando a ajuda de todo o programa e dicas de ferramenta aprimoradas.
- **Use um máximo de sete guias principais.** Se houver mais de sete, será difícil determinar qual guia tem um comando. Embora sete guias principais sejam aceitáveis para aplicativos com muitos comandos, a maioria dos programas deve visar quatro ou menos guias.

### <a name="contextual-tabs"></a>Guias contextuais

- **Use uma guia contextual para exibir uma coleção de comandos que são relevantes somente quando os usuários selecionam um determinado tipo de objeto.** Se houver apenas alguns comandos usados com frequência, poderá ser mais conveniente e mais estável usar uma guia regular e simplesmente desabilitar comandos quando eles não se aplicarem.
- ![captura de tela dos comandos Recortar e copiar esmaecidos ](images/cmd-ribbons-image29.png)<br>É melhor desabilitar comandos comuns, como recortar e copiar do que usar uma guia contextual.
- **Inclua somente os comandos que são específicos de um determinado tipo de objeto.** Não coloque os comandos somente em uma guia contextual se os usuários puderem precisar deles sem primeiro selecionar um objeto.
- **Inclua os comandos frequentemente usados ao trabalhar com um tipo de objeto específico.** Coloque os comandos contextuais gerais usados com frequência em menus de contexto e mini barras de ferramentas para evitar a alternância de tabulação durante as tarefas normalmente executadas. Como alternativa, considere colocar comandos gerais com redundância em uma guia contextual se isso evitar a alternância de tabulação frequente. Mas não exagerar isso – não tente incluir todos os comandos que um usuário possa precisar ao trabalhar com o objeto.
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
- **Para fechar uma guia modal, coloque o <mode> comando Close como o último comando na guia.** Use o ícone fechar para facilitar a localização do comando. Dê ao modo no comando para evitar confusão sobre o que está sendo fechado.
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

- ![captura de tela do comando de números de linha na faixa de faixas ](images/cmd-ribbons-image36.png)<br/>**Aproveite a capacidade de descoberta e a escalabilidade das faixas expondo todos os comandos usados com frequência.** Quando apropriado, mova os comandos usados com frequência das caixas de diálogo para a faixa de quadros, especialmente as que são difíceis de encontrar. O ideal é que os usuários possam executar tarefas comuns sem usar nenhuma caixa de diálogo.

- **Não use a escalabilidade das faixas de as para justificar a adição de complexidade desnecessária.** Continue para o retentor de exercício não adicione comandos a uma faixa de uma só porque você pode. Mantenha a experiência de comando geral simples. Veja a seguir as maneiras de simplificar a apresentação:
  - ![captura de tela da minibarra de ferramentas e menu de contexto ](images/cmd-ribbons-image37.png)</br>**Use menus de contexto e mini barras de ferramentas para comandos contextuais in-loco.**
  - **Mover (ou manter) comandos raramente usados em caixas de diálogo.** Use iniciadores de caixa de diálogo para acessar esses comandos. Você ainda pode usar caixas de diálogo com faixas de as! Apenas tente reduzir a necessidade de usá-los durante tarefas comuns.
  - **Elimine os recursos redundantes e raramente usados.**

#### <a name="presentation"></a>Apresentação

- **Apresente cada comando em apenas uma guia. Evite vários caminhos para o mesmo comando, especialmente se o comando exigir muitos cliques para invocar.** Pode parecer uma conveniência para encontrar um comando por meio de vários caminhos. Mas tenha em mente que, quando os usuários encontrarem o que estão procurando, eles param de olhar. É muito fácil para os usuários pressuporem que o primeiro caminho encontrado é o único caminho que é um problema sério se esse caminho não for eficiente. **Exceção:** As guias contextuais podem duplicar alguns comandos das guias Home e INSERT, caso isso impeça a alteração de guias para tarefas contextuais comuns.
- **Dentro de um grupo, coloque os comandos em sua ordem lógica e, ao mesmo tempo, dê preferência aos comandos usados com mais frequência.** Em geral, os comandos devem ter um fluxo lógico para facilitar a localização, ao mesmo tempo em que os comandos usados com mais frequência aparecem primeiro. Geralmente, os comandos com ícones de 32 pixels aparecem antes dos comandos com ícones de 16 pixels para auxiliar na verificação entre grupos.
- **Evite colocar comandos destrutivos ao lado dos comandos usados com frequência.** Um comando é considerado destrutivo se seu efeito é generalizado e não pode ser facilmente desfeito ou o efeito não é imediatamente perceptível.
- **Use separadores para indicar comandos fortemente relacionados, como um conjunto de opções mutuamente exclusivas.**
- ![captura de tela de grupos de fontes e parágrafos ](images/cmd-ribbons-image3.png)<br/> **Considere o uso de grupos de estilo de barra de ferramentas para conjuntos de comandos fortemente relacionados e bem conhecidos que não precisam de rótulos.** Isso permite que você apresente muitos comandos em um espaço compacto sem afetar a descoberta e a facilidade de aprendizado. Para ser bem conhecido, esses comandos são frequentemente usados, reconhecidos instantaneamente e, portanto, tendem a estar na guia início.

- **Use ícones de 32 pixels para os comandos rotulados mais importantes e usados com mais frequência.** Ao dimensionar um grupo para baixo, faça com que esses comandos sejam convertidos em ícones de 16x16 pixels.
- **Evite o posicionamento de comandos arbitrários.** Pense cuidadosamente em sua guia e design de grupo para garantir que os usuários não estejam desperdiçando tempo inspecionando cada guia para localizar o comando desejado.
- **Evite o posicionamento baseado em marketing.** Os objetivos de marketing em toda a promoção de novos recursos tendem a mudar ao longo do tempo. Considere as versões futuras do seu produto e a quantidade de frustração que uma organização em constante mudança causará.

#### <a name="interaction"></a>Interação

- **Desabilitar comandos que não se aplicam ao contexto atual ou que resultaria em um erro diretamente.** Se for útil, use a [dica de ferramenta aprimorada](glossary.md) para explicar por que o comando está desabilitado. Não oculte esses comandos, pois fazer isso pode fazer com que o layout da faixa de opção seja alterado, tornando a apresentação da faixa de modo instável.
- **Não atualize rótulos de comando dinamicamente.** Novamente, fazer isso pode fazer com que o layout da guia seja alterado, resultando em uma aparência instável. Em vez disso, crie comandos de design para que eles funcionem com rótulos constantes.

    | Correto                                                                                       | Incorreto                                                                 |
    |-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
    | ![captura de tela de inserir anotação e excluir nota ](images/cmd-ribbons-image38.png)<br/> Desabilitar comandos quando eles não estiverem disponíveis | ![captura de tela de inserir anotação, sem observação de exclusão ](images/cmd-ribbons-image39.png)<br/>Não ocultar comandos, mesmo quando eles não estiverem disponíveis |

- **Prefira controles diretos.** Um comando é direto se invocado com um único clique (ou seja, sem navegar pelos menus). No entanto, com exceção das galerias na faixa de das, os controles diretos não dão suporte à visualização dinâmica, portanto, a necessidade de visualização dinâmica também é um fator.
- **Use a visualização dinâmica** para indicar o efeito das opções quando um comando estiver entre um conjunto relacionado de opções de formatação e a visualização dinâmica for importante e prática, especialmente se os usuários provavelmente escolherem a opção errada.
  - Se o comando for usado com frequência, use uma galeria de faixa de bits para direcionamento.
  - Se o comando for usado com pouca frequência, use uma galeria suspensa.
- **Expor comandos diretos** usando os seguintes controles na seguinte ordem de preferência
  - **Botões de comando, caixas de seleção, botões de opção e galerias in-loco.** Eles são sempre diretos.
  - **Botões de divisão.** Direto para o comando mais comum, mas indireto para as variações de comando.
  - **Botões de menu.** Eles são indiretos, mas apresentam muitos comandos que são fáceis de encontrar.
  - **Caixas de texto (com controles de rotação).** A entrada de texto geralmente requer mais esforço do que os outros tipos de controle.
- ![captura de tela da faixa de faixas com apenas botões de menu ](images/cmd-ribbons-image42.png)</br>Se a faixa de faixas consistir principalmente de botões de menu quando forem exibidas em tamanho normal, você também poderá usar uma barra de menus.
- **Prefira comandos imediatos.** ![captura de tela do botão de impressão de divisão e seu submenu ](images/cmd-ribbons-image43.png)<br/>Um comando é imediato se entrar em vigor imediatamente (ou seja, sem caixas de diálogo para coletar entrada adicional). Se um comando puder exigir entrada, considere usar um botão de divisão, com o comando imediato na parte do botão e os comandos que exigem entrada no submenu.

### <a name="galleries"></a>Galerias

**Use uma [Galeria](glossary.md)** se:

- **Há um conjunto bem definido de opções relacionadas que os usuários normalmente escolhem.** Pode haver um número não associado de variações, mas as seleções prováveis devem estar bem contidas. Se as opções não estiverem fortemente relacionadas, considere o uso de galerias separadas.
- **As opções são mais bem expressas visualmente, como recursos de formatação.** O uso de miniaturas torna mais fácil navegar, entender e fazer escolhas. Embora as escolhas possam ser rotuladas, a seleção é feita visualmente e os rótulos de texto não devem ser necessários para entender as opções.
- **As opções mostram o resultado que é obtido imediatamente com um único clique.** Não deve haver nenhuma caixa de diálogo de acompanhamento para esclarecer ainda mais a intenção do usuário ou um conjunto de etapas para atingir o resultado indicado. Se os usuários quiserem ajustar a escolha, deixe que eles façam isso posteriormente.

**Use uma galeria na faixa de faixas** se:

- **As opções são usadas com frequência.** As opções precisam do espaço e valem o espaço potencialmente em uso de outros comandos.
- **Para uso típico, não é necessário agrupar ou filtrar as opções apresentadas.**
- **As escolhas podem ser exibidas com eficiência na altura de uma faixa de opções (que é de 48 pixels).**

#### <a name="thumbnails-in-galleries"></a>Miniaturas nas galerias

**Escolha o menor tamanho de miniatura da Galeria padrão** que faz o trabalho bem.

- Para galerias na faixa de bits, use miniaturas de 16x16, 48x48 ou 64x48 pixels.
- Para galerias suspensas, use miniaturas de 16x16, 32x32, 48x48, 64x48, 72x96, 96x72, 96x96 ou 128x128 pixels.
- Todos os itens da Galeria devem ter o mesmo tamanho de miniatura.

Para galerias na faixa de opções:

- **Exibir um mínimo de três opções; mais se houver espaço.** Se não houver espaço suficiente para exibir pelo menos três opções no tamanho típico da janela, use uma galeria de lista de opções.
- **Expanda galerias na faixa de opções para aproveitar o espaço disponível.** Use o espaço adicional para mostrar mais itens e torná-los mais fáceis de escolher com um único clique.

Para galerias de lista de usuários:

- **Exibir a galeria de uma caixa de combinação, lista de menus suspensos, botão de divisão ou botão de menu.**
- **Se o usuário clicar na janela principal para descartar a galeria listada, basta descartar a galeria sem selecionar ou modificar o conteúdo da janela principal.**
- **Se uma galeria tiver muitas opções e algumas opções raramente são usadas, simplifique a galeria padrão concentrando-se nas opções comumente usadas.** Para os comandos restantes, forneça um comando apropriado na parte inferior da lista de menus da galeria.
  - Se o comando mostrar uma lista de mais variações, nomee-o como "Mais `singular feature name` opções..."
  - Se o comando apresentar uma caixa de diálogo que permite que os usuários criem suas próprias opções personalizadas, nomeia-a como `feature name` "Personalizado..."
- **Organize as opções em grupos, se isso fizer isso, torna a navegação mais eficiente.**
- ![captura de tela da galeria de símbolos e filtros ](images/cmd-ribbons-image44.png)<br/>**Se uma galeria tiver muitos itens, considere adicionar um filtro para ajudar os usuários a encontrar opções com mais eficiência.** Para evitar confusão, inicialmente, exibe a galeria não filtrada. No entanto, a maioria das galerias não deve exigir um filtro porque elas não devem ter muitas opções e usar grupos deve ser suficiente.

### <a name="command-previews"></a>Visualizações de comando

- **Use previews para mostrar o efeito de um comando sem que os usuários o executem primeiro.** Usando visualizações úteis, você pode melhorar a eficiência e a facilidade de aprendizado do programa e reduzir a necessidade de avaliação e erro. Para os diferentes tipos de visualizações de comando, consulte [Visualizações](#previews) na seção Conceitos de Design deste artigo.
- **Para visualizações ao vivo, certifique-se de que a versão prévia possa ser aplicada e o estado atual restaurado em 500 milissegundos.** Isso requer a capacidade de aplicar alterações de formatação rapidamente e de uma maneira que seja interruptível. Os usuários devem ser capazes de avaliar opções diferentes rapidamente para que as visualizações ao vivo tenham seu benefício completo.
- **Evite usar texto em visualizações.** Caso contrário, as imagens de visualização deverão ser localizadas.

### <a name="icons"></a>Ícones

- ![captura de tela da lista lista e caixas de seleção ](images/cmd-ribbons-image45.png)<br/>**Forneça ícones para todos os controles de faixa de opções, exceto listas listadas, caixas de seleção e botões de rádio.** A maioria dos comandos exigirá ícones de 32 x 32 e 16 x 16 pixels (somente ícones de 16 x 16 pixels são usados pela Barra de Ferramentas de Acesso Rápido). As galerias normalmente usam ícones de 16 x 16, 48 x 48 ou 64 x 48 pixels.
- **Forneça ícones exclusivos.** Não use o mesmo ícone para comandos diferentes.
- **Certifique-se de que os ícones da faixa de opções estão claramente visíveis em relação à cor da tela de fundo da faixa de opções.** Sempre avalie ícones de faixa de opções no contexto e no modo de alto contraste.
- **Escolha designs de ícone que comuniquem claramente seu efeito,** especialmente para os comandos usados com mais frequência. Faixas de opções bem projetadas têm ícones autoexplicativos para ajudar os usuários a encontrar e entender comandos com eficiência.
- **Escolha ícones reconhecíveis e diferenciáveis,** especialmente para os comandos usados com mais frequência. Certifique-se de que os ícones tenham cores e formas distintas. Isso ajuda os usuários a encontrar os comandos rapidamente, mesmo que eles não se lembre do símbolo de ícone.

    | Correto                                                                                                 | Incorreto                                                                               |
    |--------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
    | ![captura de tela do dropper de olho azul e lápis amarelo ](images/cmd-ribbons-image46.png)<br/>Use forma e cor para tornar ícones fáceis de distinguir. | ![captura de tela do dropper de olho azul e lápis azul ](images/cmd-ribbons-image47.png)<br/> Ícones que têm a mesma cor são difíceis de distinguir|

- ![captura de tela do comando comments no contêiner pop-up ](images/cmd-ribbons-image48.png)<br/>**Considere criar ícones de grupo pop-up colocando o ícone de 16 x 16 pixels do comando mais proeminente no grupo dentro de um contêiner visual de 32 x 32 pixels.** Você não precisa criar ícones diferentes para grupos pop-up.
- ![captura de tela dos botões de comando de formatação de texto ](images/cmd-ribbons-image25.png)<br/>**Se for útil, altere o ícone para refletir o estado atual.** Fazer isso é especialmente útil para botões divididos cujo efeito padrão pode ser alterado.
- **Certifique-se de que os ícones de faixa de opções estão em conformidade com as diretrizes do ícone de estilo aero.** No entanto, os ícones de faixa de opções são mostrados diretamente em vez de serem mostrados em perspectiva.

| Correto                                                                                                 | Incorreto                                                                               |
    |--------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
    | ![captura de tela de ícones de comando bidimensionais ](images/cmd-ribbons-image49.png)<br/> Use ícones bidimensionais.|![captura de tela de ícones de comando tridimensionais ](images/cmd-ribbons-image50.png)<br/> Não use ícones tridimensionais. |
 
### <a name="enhanced-tooltips"></a>Dicas de ferramentas aprimoradas

- **Todos os comandos da faixa de opções devem** ter dicas de ferramenta aprimoradas para dar o nome do comando, a tecla de atalho, a descrição e as informações complementares opcionais. Evite dicas de ferramenta que simplesmente restate o rótulo.

    **Incorreto:**

    ![captura de tela da dica de ferramenta que repete o nome do comando ](images/cmd-ribbons-image51.png)

    Neste exemplo, a dica de ferramenta simplesmente restauria o rótulo do comando.

- **Quando prático, descreva completamente o comando usando uma descrição concisa.** Link para Ajuda somente se mais explicações são realmente necessárias.

    **Incorreto:**

    ![captura de tela da dica de ferramenta para o comando tachado ](images/cmd-ribbons-image52.png)

    Neste exemplo, o comando não precisa de Ajuda.

- **Quando útil, ilustra o efeito do comando usando uma versão prévia.**

    ![captura de tela da dica de ferramenta e do gráfico para inserir gráfico ](images/cmd-ribbons-image53.png)

    Neste exemplo, a imagem da dica de ferramenta ilustra o efeito do comando.

Para diretrizes de rotulagem, consulte [Rótulos de dica de ferramenta aprimorados.](#enhanced-tooltips)

### <a name="access-keys-and-keytips"></a>Chaves de acesso e dicas de chave

Dicas de tecla são o mecanismo usado para exibir chaves de acesso para comandos exibidos diretamente em uma faixa de opções.

As chaves de acesso para comandos de menu suspenso são indicadas com um caractere sublinhado. Elas diferem das chaves de acesso do menu das seguintes maneiras:

- Duas chaves de acesso de caractere podem ser usadas. Por exemplo, o FP pode ser usado para acessar o comando Format desatar.
- As atribuições de chave de acesso são mostradas usando dicas em vez de sublinhados, portanto, a largura e os descendentes de caracteres não são um fator para fazer atribuições.

- **Atribua chaves de acesso a todas as guias e comandos da faixa de opções.** A única exceção possível é para comandos provenientes de complementos herdado.
- **Para o botão Aplicativo e a Barra de Ferramentas de Acesso Rápido:**
  - Atribua F ao botão Aplicativo. Essa atribuição é usada devido à similaridade do botão Aplicativo com o menu Arquivo tradicional.
  - ![captura de tela de dicas de tecla de comando em uma faixa de opções ](images/cmd-ribbons-image54.png)<br/>Para a Barra de Ferramentas de Acesso Rápido e listas de arquivos usadas recentemente, atribua chaves de acesso numericamente.
- ![captura de tela mostrando dicas de tecla para guias ](images/cmd-ribbons-image55.png)<br/>**Para guias:**
  - Atribua H à Página Home.
  - Começando com as guias usadas com mais frequência, atribua a primeira letra do rótulo.
  - Para todas as guias que não podem ser atribuídas à primeira letra, escolha uma consoante distinta ou uma voga no rótulo.
  - Para programas que costumavam dar suporte a barras de menu, procure manter a compatibilidade da chave de acesso com a melhor extensão prática. Evite atribuir significados diferentes para acessar chaves de categorias de menu herdadas. Por exemplo, se a versão da barra de menus herdada de um programa tiver um menu Editar, procure usar uma chave de acesso E para a guia equivalente. Se não houver nenhuma guia equivalente, não atribua uma chave de acesso E a nenhuma guia para evitar confusão.
- ![captura de tela mostrando dicas de tecla para uma faixa de opções ](images/cmd-ribbons-image56.png)<br/>**Para comandos, menus e submenus da faixa de opções:**
  - Atribua combinações de chave de acesso exclusivas em uma guia. Você pode reutilizar combinações de teclas de acesso em guias diferentes.
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