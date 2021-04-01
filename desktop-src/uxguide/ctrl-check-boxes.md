---
title: Caixas de seleção
description: Com uma caixa de seleção, os usuários tomarão uma decisão entre duas opções claramente opostas.
ms.assetid: 7c39987d-807b-41c1-9788-65c3d468b976
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 7a175893b2dfab2999ce37e3f00395d881f03973
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "103930062"
---
# <a name="check-boxes"></a>Caixas de seleção

> [!NOTE]
> Este guia de design foi criado para o Windows 7 e não foi atualizado para versões mais recentes do Windows. Grande parte da orientação ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais](/windows/uwp/design/).

Com uma caixa de seleção, os usuários tomarão uma decisão entre duas opções claramente opostas. O rótulo da caixa de seleção indica o estado selecionado, enquanto o significado do estado limpo deve ser o oposto não ambíguo do estado selecionado. Consequentemente, as **caixas de seleção devem ser usadas apenas para ativar ou desativar uma opção ou para selecionar ou desmarcar um item.**

![captura de tela de uma das quatro caixas de seleção selecionadas ](images/ctrl-check-boxes-image1.png)

Um grupo típico de caixas de seleção.

> [!Note]  
> As diretrizes relacionadas ao [layout](vis-layout.md) são apresentadas em um artigo separado.

 

## <a name="is-this-the-right-control"></a>Esse é o controle correto?

Para decidir, considere estas perguntas:

-   **A caixa de seleção é usada para ativar ou desativar uma opção ou para selecionar ou desmarcar um item?** Se não, use outro controle.
-   **Os Estados selecionado e limpo são opostos claros e não ambíguos?** Caso contrário, use [botões de opção](ctrl-radio-buttons.md) ou uma [lista suspensa](/windows/desktop/uxguide/ctrl-drop) para que você possa rotular os Estados de forma independente.
-   **Quando usado em um grupo, o grupo consiste em opções independentes, das quais os usuários podem escolher zero ou mais?** Caso contrário, considere os controles para as opções dependentes, como botões de opção e [exibições de árvore da caixa de seleção](ctrl-tree-views.md).
-   **Quando usado em um grupo, o grupo é composto por opções dependentes, das quais os usuários devem escolher um ou mais?** Nesse caso, use um grupo de caixas de seleção e manipule o erro quando nenhuma das opções estiver selecionada.
-   **O número de opções em um grupo é de 10 ou menos?** Como o espaço da tela usado é proporcional ao número de opções, mantenha o número de caixas de seleção para 10 ou menos. Para obter mais de 10 opções, use uma [lista de caixas de seleção](ctrl-list-boxes.md).
-   **Um botão de opção seria uma opção melhor?** Onde as caixas de seleção são adequadas apenas para ativar ou desativar uma opção, os botões de opção podem ser usados para opções completamente diferentes. Se ambas as soluções forem possíveis:
    -   Use botões de opção se o significado da caixa de seleção desmarcada não for completamente óbvio.

        **Incorreto:**

        ![captura de tela de uma caixa de seleção rotulada paisagem ](images/ctrl-check-boxes-image2.png)

        Neste exemplo, a escolha oposta da paisagem não é clara, portanto, a caixa de seleção não é uma boa opção.

        **Correto:**

        ![captura de tela de dois botões de opção ](images/ctrl-check-boxes-image3.png)

        Neste exemplo, as opções não são opostas, portanto, os botões de opção são a melhor opção.

    -   Use botões de opção em páginas de assistente para tornar as alternativas desclaradas, mesmo que uma caixa de seleção seja aceitável de outra forma.
    -   Use botões de opção se você tiver espaço de tela suficiente e as opções forem importantes o suficiente para ser um bom uso desse espaço de tela. Caso contrário, use uma caixa de seleção ou uma lista suspensa.

        **Incorreto:**

        ![captura de tela de botões Mostrar e não mostrar taxa ](images/ctrl-check-boxes-image4.png)

        Neste exemplo, as opções não são importantes o suficiente para usar botões de opção.

        **Correto:**

        ![captura de tela de caixa de seleção com não mostrar mensagem ](images/ctrl-check-boxes-image5.png)

        Neste exemplo, uma caixa de seleção é um uso eficiente do espaço da tela para essa opção de periférico.

-   Use uma caixa de seleção se houver outras caixas de seleção na janela.
-   **A opção apresenta uma opção de programa, em vez de dados?** Os valores da opção não devem ser baseados em contexto ou outros dados. Para dados, use uma lista de caixas de seleção ou uma [lista de seleção múltipla](ctrl-list-boxes.md).

## <a name="usage-patterns"></a>Padrões de uso

As caixas de seleção têm vários padrões de uso:



|                                                                                                                                                                                                             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Uma opção individual** Uma única caixa de seleção é usada para selecionar uma opção individual. <br/>                                                                                                             | ![captura de tela de uma caixa de seleção com o rótulo lembrar-me ](images/ctrl-check-boxes-image6.png)<br/> Uma única caixa de seleção é usada para uma escolha individual.<br/>                                                                                                                                                                                                                                                                                                                        |
| **Opções independentes (zero ou mais)** Um grupo de caixas de seleção é usado para selecionar de um conjunto de zero ou mais opções.<br/>                                                                              | ao contrário dos controles de seleção única, como [botões de opção](ctrl-radio-buttons.md), os usuários podem selecionar qualquer combinação de opções em um grupo de caixas de seleção.<br/> ![captura de tela de duas das três caixas de seleção selecionadas ](images/ctrl-check-boxes-image7.png)<br/> Um grupo de caixas de seleção é usado para escolhas independentes.<br/>                                                                                                                                                  |
| **Opções dependentes (um ou mais)** Um grupo de caixas de seleção também pode ser usado para selecionar de um conjunto de uma ou mais opções.<br/>                                                                         | **talvez seja necessário representar uma seleção de uma ou mais opções dependentes**. como o Microsoft? Windows não tem um controle que dá suporte diretamente a esse tipo de entrada, a melhor solução é usar um grupo de caixas de seleção e manipular o erro quando nenhuma das opções estiver selecionada.<br/> ![captura de tela de uma das duas caixas de seleção selecionadas ](images/ctrl-check-boxes-image8.png)<br/> Um grupo de caixas de seleção é usado onde pelo menos um protocolo deve ser selecionado.<br/> |
| **Opção mista** Além dos Estados selecionados e limpos, as caixas de seleção também têm um estado misto para seleção múltipla para indicar que a opção está definida para alguns objetos, mas não todos.<br/> | ![captura de tela de uma caixa de seleção azul somente leitura sólida ](images/ctrl-check-boxes-image9.png)<br/> Uma caixa de seleção de estado misto.<br/>                                                                                                                                                                                                                                                                                                                                                      |



 

## <a name="guidelines"></a>Diretrizes

### <a name="general"></a>Geral

-   **Caixas de seleção relacionadas ao grupo**. Combine opções relacionadas e separe as opções não relacionadas em grupos de 10 ou menos, usando vários grupos, se necessário.

    ![captura de tela das caixas de seleção relacionadas e não relacionadas ](images/ctrl-check-boxes-image10.png)

    Um exemplo de grupos de opções relacionadas e independentes.

-   **Reconsidere o uso de caixas de grupo para organizar grupos de caixas de seleção** isso geralmente resulta em uma desordem de tela desnecessária.
-   **Listar caixas de seleção em uma ordem lógica**, como agrupar opções altamente relacionadas juntos ou colocar as opções mais comuns primeiro ou seguir alguma outra progressão natural. A ordenação alfabética não é recomendada porque é dependente de idioma e, portanto, não é localizável.
-   **Alinhar caixas de seleção verticalmente, não horizontalmente**. O alinhamento horizontal é mais difícil de ler.

    **Correto:**

    ![captura de tela das caixas de seleção alinhadas verticalmente ](images/ctrl-check-boxes-image11.png)

    Neste exemplo, as caixas de seleção estão alinhadas corretamente.

    **Incorreto:**

    ![captura de tela das caixas de seleção alinhadas horizontalmente ](images/ctrl-check-boxes-image12.png)

    Neste exemplo, o alinhamento horizontal é mais difícil de ler.

-   **Não use o estado misto para representar um terceiro estado.** O estado misto é usado para indicar que uma opção está definida para alguns objetos filho, mas não todos. Os usuários não devem ser capazes de definir um estado misto diretamente, em vez disso, o estado misto é uma reflexão dos objetos filho. O estado misto não é usado como um terceiro estado para um item individual. Para representar um terceiro estado, use botões de opção ou uma lista suspensa em vez disso.

    **Incorreto:**

    ![captura de tela da caixa de seleção de serviço de tema azul sólido ](images/ctrl-check-boxes-image13.png)

    Neste exemplo, o estado misto deve indicar que o serviço tema não está instalado.

    **Correto:**

    ![captura de tela da lista suspensa com três opções ](images/ctrl-check-boxes-image14.png)

    Neste exemplo, os usuários podem escolher entre uma lista de três opções claras.

-   **Clicar em uma caixa de seleção de estado misto deve percorrer todos os Estados mistos selecionados, todos limpos e originais.** Para Forgiveness, é importante poder restaurar o estado misto original, pois as configurações podem ser complexas ou desconhecidas para o usuário. Caso contrário, a única maneira de restaurar o estado misto com confiança seria cancelar a tarefa e começar novamente.
-   **Não use as caixas de seleção como um indicador de progresso**. Em vez disso, use um controle de [indicador de progresso](progress-bars.md) .

    **Incorreto:**

    ![captura de tela de quatro caixas de seleção mostrando progresso ](images/ctrl-check-boxes-image15.png)

    Neste exemplo, as caixas de seleção são usadas incorretamente como um indicador de progresso.

    **Correto:**

    ![captura de tela de uma barra de progresso parcialmente preenchida ](images/ctrl-check-boxes-image16.png)

    Exemplo de uma barra de progresso típica.

-   **Mostrar caixas de seleção desabilitadas usando o estado de seleção correto.** Mesmo que os usuários não possam alterá-los, as caixas de seleção desativadas transmitem informações para que sejam consistentes com os resultados.

    **Incorreto:**

    ![captura de tela de uma das duas caixas de seleção esmaecidas ](images/ctrl-check-boxes-image17.png)

    Neste exemplo, a opção "sempre ler esta seção em voz alta" deve ser desmarcada porque a seção não é lida quando a opção está desabilitada.

-   **Não use a seleção de uma caixa de seleção para**:
    -   Executar comandos.
    -   Exiba outras janelas, como uma caixa de diálogo para coletar mais entradas.
    -   Exibir dinamicamente outros controles relacionados ao controle selecionado (leitores de tela não podem detectar esses eventos).

### <a name="dont-show-this-item-again"></a>Não mostrar este <item> outra

-   **Considere usar uma opção não mostrar esta <item> novamente para permitir que os usuários suprimem uma caixa de diálogo recorrente somente se não houver uma alternativa melhor.** Tente determinar com antecedência se os usuários realmente precisam da caixa de diálogo; Se fizerem isso, sempre mostrarão a caixa de diálogo e, se não forem, eliminará a caixa de diálogo.

Para obter mais diretrizes e exemplos, consulte [caixas de diálogo](win-dialog-box.md).

### <a name="subordinate-controls"></a>Controles subordinados

-   Coloque controles subordinados à direita ou abaixo (recuado, libere com o rótulo da caixa de seleção) a caixa de seleção e seu rótulo. Termine o rótulo da caixa de seleção com dois-pontos.

    ![captura de tela da caixa de texto abaixo do rótulo da caixa de seleção ](images/ctrl-check-boxes-image18.png)

    Neste exemplo, a caixa de seleção e seu controle subordinado compartilham o rótulo da caixa de seleção e sua chave de acesso.

-   **Deixe caixas de texto editáveis e listas suspensas dependentes habilitadas se compartilharem o rótulo da caixa de seleção.** Quando os usuários digitam ou colam qualquer coisa na caixa, selecione a opção correspondente automaticamente. Fazer isso simplifica a interação.

    ![captura de tela de caixas de texto de cabeçalho e rodapé ](images/ctrl-check-boxes-image19.png)

    Neste exemplo, a inserção de um cabeçalho ou rodapé automaticamente seleciona a opção.

-   Se você aninhar caixas de seleção com botões de opção ou outras caixas de seleção, **Desabilite esses controles subordinados até que a opção de alto nível seja selecionada**. Isso evita a confusão sobre o significado dos controles subordinados.
-   Torne os controles subordinados a uma caixa de seleção contíguas com a caixa de seleção na ordem de tabulação.
-   **Se a seleção de uma opção implica selecionar caixas de seleção subordinadas, marque explicitamente as caixas de seleção para tornar a relação clara.**

    **Incorreto:**

    ![captura de tela: botão selecionado, caixas de seleção desmarcadas ](images/ctrl-check-boxes-image20.png)

    Neste exemplo, as caixas de seleção subordinadas não estão selecionadas.

    **Correto:**

    ![captura de tela: botão selecionado, caixas de seleção selecionadas ](images/ctrl-check-boxes-image21.png)

    Neste exemplo, as caixas de seleção subordinadas são selecionadas, tornando sua relação com a opção selecionada desmarcada.

-   **Use as caixas de seleção dependentes se as alternativas adicionarem complexidade desnecessária**. Enquanto as caixas de seleção devem ser opções independentes, algumas vezes alternativas como botões de opção adicionam complexidade desnecessária.

    **Correto:**

    ![captura de tela de botões confusos e caixas de seleção ](images/ctrl-check-boxes-image22.png)

    Neste exemplo, o uso de botões de opção é preciso, mas cria uma complexidade desnecessária.

    **Melhor:**

    ![captura de tela apenas de caixas de seleção ](images/ctrl-check-boxes-image23.png)

    Neste exemplo, o uso de caixas de seleção é mais simples e permite que os usuários se concentrem na seleção das opções desejadas em vez de em sua relação complexa.

    **Importante: aplique essa diretriz somente em circunstâncias extremamente raras**, quando a exibição das dependências adicionar uma complexidade significativa sem aumentar a clareza. No exemplo anterior, é improvável que os usuários tentem escolher sobrescrito e subscrito e, se tiverem feito isso, seria fácil entender que eram opções exclusivas.

### <a name="default-values"></a>Valores padrão

-   Se uma caixa de seleção for para uma opção de usuário, **defina o mais seguro (para evitar a perda de dados ou acesso ao sistema), o estado mais seguro e privado por padrão.** Se não houver fatores de segurança e segurança, selecione o valor mais provável ou conveniente.

## <a name="recommended-sizing-and-spacing"></a>Dimensionamento e espaçamento recomendados

![figura do espaçamento e dimensionamento da caixa de seleção sugerido ](images/ctrl-check-boxes-image24.png)

Dimensionamento e espaçamento recomendados para caixas de seleção.

## <a name="labels"></a>Rótulos

**Rótulos da caixa de seleção**

-   Rotular todas as caixas de seleção.
-   Atribua uma [chave de acesso](glossary.md) exclusiva para cada rótulo. Para obter diretrizes, consulte [teclado](inter-keyboard.md).
-   Use [a capitalização no estilo de frase](glossary.md).
-   Escreva o rótulo como uma frase ou uma frase imperativa e não use pontuação final.
    -   **Exceção:** Se um rótulo da caixa de seleção também rotular um controle subordinado que o segue, termine o rótulo com dois-pontos.
-   Escreva o rótulo para que ele descreva o estado selecionado da caixa de seleção.
-   Para um grupo de caixas de seleção, use frases paralelas e tente manter o comprimento sobre o mesmo para todos os rótulos.
-   Para um grupo de caixas de seleção, concentre o texto do rótulo nas diferenças entre as opções. Se todas as opções tiverem o mesmo texto introdutório, mova esse texto para o rótulo do grupo.
-   Use frases positivas. Não formule um rótulo para que a seleção de uma caixa de seleção signifique não executar uma ação.

    -   **Exceção: não mostrar esta <item>** caixa de seleção novamente.

    **Incorreto:**

    ![captura de tela do rótulo negativo ' desligar '](images/ctrl-check-boxes-image25.png)

    Neste exemplo, a opção não usa frases positivas.

-   Descreva apenas a opção com o rótulo. Mantenha os rótulos breves para que seja fácil consultá-los em mensagens e documentação. Se a opção exigir mais explicações, forneça a explicação em um controle de [texto estático](./glossary.md) usando frases completas e pontuação final.

    > [!Note]
    >
    > Adicionar uma explicação a uma caixa de seleção em um grupo não significa que você precisa fornecer explicações para todas as caixas de seleção no grupo. Forneça as informações relevantes no rótulo, se possível, e use explicações somente quando necessário. Não apenas redeclare o rótulo para fins de consistência.

     

    ![captura de tela de caixa de seleção, rótulo e descrição ](images/ctrl-check-boxes-image26.png)

    Neste exemplo, um rótulo de caixa de seleção tem um texto explicativo adicional abaixo dele.

-   Se uma opção for altamente recomendável, considere adicionar "(recomendado)" ao rótulo. Certifique-se de adicionar ao rótulo de controle, não às anotações complementares.
-   Se você precisar usar rótulos de várias linhas, alinhe a parte superior do rótulo com a caixa de seleção.
-   Não use um controle subordinado, os valores que ele contém ou seu rótulo de unidades para criar uma frase ou frase. Esse tipo de design não é localizável porque a estrutura da frase varia de acordo com a linguagem.

    **Incorreto:**

    ![captura de tela de rótulo de caixa de seleção com caixa de texto ](images/ctrl-check-boxes-image27.png)

    Neste exemplo, a caixa de texto é colocada incorretamente dentro do rótulo da caixa de seleção.

**Rótulos de grupo da caixa de seleção**

-   Use o rótulo de grupo para explicar a finalidade do grupo, não como fazer a seleção. Suponha que os usuários saibam como usar as caixas de seleção. Por exemplo, não diga "Selecione qualquer uma das opções a seguir".
-   Termine cada rótulo com dois-pontos.
-   Não atribua uma chave de acesso ao rótulo. Fazer isso não é necessário e torna mais difícil atribuir as outras chaves de acesso.
-   Para uma seleção de uma ou mais opções dependentes, explique o requisito no rótulo.

    **Correto:**

    ![captura de tela do rótulo para dois controles: protocolos ](images/ctrl-check-boxes-image28.png)

    Neste exemplo, os usuários podem imaginar que eles só podem fazer uma seleção.

    **Melhor:**

    ![captura de tela de rótulo: protocolos selecione um ou mais ](images/ctrl-check-boxes-image29.png)

    Neste exemplo, é claro que os usuários podem fazer mais de uma seleção.

## <a name="documentation"></a>Documentação

Ao se referir a caixas de seleção:

-   Use o texto exato do rótulo, incluindo sua capitalização, mas não inclua a tecla de acesso sublinhado ou dois-pontos. Inclua a caixa de seleção Word.
-   Consulte uma caixa de seleção como caixa de seleção, não opção, caixa de seleção ou caixa apenas, porque a caixa sozinha é ambígua para os localizadores.
-   Para descrever a interação do usuário, use selecionar e limpar.
-   Quando possível, formate o rótulo usando texto em negrito. Caso contrário, coloque o rótulo entre aspas somente se necessário para evitar confusão.

    Exemplo: marque a caixa de seleção **sublinhado** .

