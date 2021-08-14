---
title: Caixas de seleção
description: Com uma caixa de seleção, os usuários tomarão uma decisão entre duas opções claramente opostas.
ms.assetid: 7c39987d-807b-41c1-9788-65c3d468b976
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 29666991d0a0659f7ff3a95f12953504b70c6dc782049ac8d93d70df73afa5d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118040549"
---
# <a name="check-boxes"></a>Caixas de seleção

> [!NOTE]
> Este guia de design foi criado para Windows 7 e não foi atualizado para versões mais recentes do Windows. Grande parte das diretrizes ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais.](/windows/uwp/design/)

Com uma caixa de seleção, os usuários tomarão uma decisão entre duas opções claramente opostas. O rótulo da caixa de seleção indica o estado selecionado, enquanto o significado do estado limpo deve ser o oposto não ambíguo do estado selecionado. Consequentemente, as caixas de seleção devem ser usadas apenas para alternar ou desligar uma opção ou selecionar ou **desmarcar um item.**

![captura de tela de uma das quatro caixas de seleção selecionadas ](images/ctrl-check-boxes-image1.png)

Um grupo típico de caixas de seleção.

> [!Note]  
> As diretrizes relacionadas [ao layout](vis-layout.md) são apresentadas em um artigo separado.

 

## <a name="is-this-the-right-control"></a>Esse é o controle correto?

Para decidir, considere estas perguntas:

-   **A caixa de seleção é usada para alternar ou desligar uma opção ou selecionar ou desmarcar um item?** Se não, use outro controle.
-   **Os estados selecionados e limpos são opostos claros e não ambíguos?** Caso não, use [botões de rádio](ctrl-radio-buttons.md) ou uma lista [de](/windows/desktop/uxguide/ctrl-drop) listas listadas para que você possa rotular os estados de forma independente.
-   **Quando usado em um grupo, o grupo compreende opções independentes, das quais os usuários podem escolher zero ou mais?** Caso não, considere os controles para opções dependentes, como botões de opção e exibições [de árvore de caixa de seleção](ctrl-tree-views.md).
-   **Quando usado em um grupo, o grupo compreende opções dependentes, das quais os usuários devem escolher uma ou mais?** Se sim, use um grupo de caixas de seleção e tratar o erro quando nenhuma das opções estiver selecionada.
-   **O número de opções em um grupo é 10 ou menos?** Como o espaço de tela usado é proporcional ao número de opções, mantenha o número de caixas de seleção como 10 ou menos. Para mais de 10 opções, use uma lista [de caixas de seleção](ctrl-list-boxes.md).
-   **Um botão de opção seria uma opção melhor?** Quando as caixas de seleção são adequadas apenas para ligar ou desligar uma opção, os botões de opção podem ser usados para opções completamente diferentes. Se ambas as soluções são possíveis:
    -   Use botões de rádio se o significado da caixa de seleção des limpa não for completamente óbvio.

        **Incorreto:**

        ![captura de tela de uma caixa de seleção rotulada paisagem ](images/ctrl-check-boxes-image2.png)

        Neste exemplo, a opção oposta de Paisagem não está clara, portanto, a caixa de seleção não é uma boa opção.

        **Correto:**

        ![captura de tela de dois botões de rádio ](images/ctrl-check-boxes-image3.png)

        Neste exemplo, as opções não são opostas, portanto, os botões de opção são a melhor opção.

    -   Use botões de opção em páginas do assistente para limpar as alternativas, mesmo que uma caixa de seleção seja aceitável.
    -   Use botões de opção se você tiver espaço suficiente na tela e as opções são importantes o suficiente para ser um bom uso desse espaço na tela. Caso contrário, use uma caixa de seleção ou uma lista de listas.

        **Incorreto:**

        ![captura de tela de mostrar e não mostrar botões de proporção ](images/ctrl-check-boxes-image4.png)

        Neste exemplo, as opções não são importantes o suficiente para usar botões de opção.

        **Correto:**

        ![captura de tela da caixa de seleção com não mostrar mensagem ](images/ctrl-check-boxes-image5.png)

        Neste exemplo, uma caixa de seleção é um uso eficiente do espaço de tela para essa opção de periférico.

-   Use uma caixa de seleção se houver outras caixas de seleção na janela.
-   **A opção apresenta uma opção de programa, em vez de dados?** Os valores da opção não devem ser baseados no contexto ou em outros dados. Para dados, use uma lista de caixas de seleção ou [lista de seleção múltipla](ctrl-list-boxes.md).

## <a name="usage-patterns"></a>Padrões de uso

As caixas de seleção têm vários padrões de uso:



|    Uso                                                                          |         Exemplo                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Uma escolha individual** Uma única caixa de seleção é usada para selecionar uma opção individual. <br/>                                                                                                             | ![captura de tela de uma caixa de seleção com lembretes rótulo ](images/ctrl-check-boxes-image6.png)<br/> Uma única caixa de seleção é usada para uma escolha individual.<br/>                                                                                                                                                                                                                                                                                                                        |
| **Opções independentes (zero ou mais)** Um grupo de caixas de seleção é usado para selecionar de um conjunto de zero ou mais opções.<br/>                                                                              | ao contrário de controles de seleção única, como [botões de](ctrl-radio-buttons.md)opção , os usuários podem selecionar qualquer combinação de opções em um grupo de caixas de seleção.<br/> ![captura de tela de duas das três caixas de seleção selecionadas ](images/ctrl-check-boxes-image7.png)<br/> Um grupo de caixas de seleção é usado para opções independentes.<br/>                                                                                                                                                  |
| **Opções dependentes (uma ou mais)** Um grupo de caixas de seleção também pode ser usado para selecionar um conjunto de uma ou mais opções.<br/>                                                                         | **talvez seja necessário representar uma seleção de uma ou mais opções dependentes.** como microsoft?windows não tem um controle que dá suporte diretamente a esse tipo de entrada, a melhor solução é usar um grupo de caixas de seleção e tratar o erro quando nenhuma das opções for selecionada.<br/> ![captura de tela de uma das duas caixas de seleção selecionadas ](images/ctrl-check-boxes-image8.png)<br/> Um grupo de caixas de seleção é usado em que pelo menos um protocolo deve ser selecionado.<br/> |
| **Opção mista** Além dos estados selecionados e limpos, as caixas de seleção também têm um estado misto para várias seleções para indicar que a opção está definida para alguns objetos, mas não para todos.<br/> | ![captura de tela de uma caixa de seleção somente leitura azul sólida ](images/ctrl-check-boxes-image9.png)<br/> Uma caixa de seleção de estado misto.<br/>                                                                                                                                                                                                                                                                                                                                                      |



 

## <a name="guidelines"></a>Diretrizes

### <a name="general"></a>Geral

-   **Caixas de seleção relacionadas ao grupo**. Combine opções relacionadas e separe opções não relacionadas em grupos de 10 ou menos, usando vários grupos, se necessário.

    ![captura de tela de caixas de seleção relacionadas e não relacionadas ](images/ctrl-check-boxes-image10.png)

    Um exemplo de grupos de opções independentes relacionadas.

-   **A reação ao uso de caixas de grupo para organizar grupos de caixas de** seleção geralmente resulta em uma desorganização desnecessária da tela.
-   **Marque as caixas de seleção** em uma ordem lógica, como agrupar opções altamente relacionadas ou colocar as opções mais comuns primeiro ou seguir alguma outra progressão natural. A ordenação alfabética não é recomendada porque é dependente de idioma e, portanto, não é localizável.
-   **Alinhe as caixas de seleção verticalmente, não horizontalmente.** O alinhamento horizontal é mais difícil de ler.

    **Correto:**

    ![captura de tela de caixas de seleção alinhadas verticalmente ](images/ctrl-check-boxes-image11.png)

    Neste exemplo, as caixas de seleção estão alinhadas corretamente.

    **Incorreto:**

    ![captura de tela de caixas de seleção alinhadas horizontalmente ](images/ctrl-check-boxes-image12.png)

    Neste exemplo, o alinhamento horizontal é mais difícil de ler.

-   **Não use o estado misto para representar um terceiro estado.** O estado misto é usado para indicar que uma opção é definida para alguns objetos filho, mas não todos. Os usuários não devem ser capazes de definir um estado misto diretamente, em vez disso, o estado misto é um reflexão dos objetos filho. O estado misto não é usado como um terceiro estado para um item individual. Para representar um terceiro estado, use botões de rádio ou uma lista de listas listadas.

    **Incorreto:**

    ![captura de tela da caixa de seleção do serviço de tema azul sólido ](images/ctrl-check-boxes-image13.png)

    Neste exemplo, o estado misto deve indicar que o serviço Tema não está instalado.

    **Correto:**

    ![captura de tela da listada com três opções ](images/ctrl-check-boxes-image14.png)

    Neste exemplo, os usuários podem escolher em uma lista de três opções claras.

-   **Clicar em uma caixa de seleção de estado misto deve passar por todos os estados selecionados, todos limpos e mistos originais.** Por questões de saúde, é importante poder restaurar o estado misto original porque as configurações podem ser complexas ou desconhecidas para o usuário. Caso contrário, a única maneira de restaurar o estado misto com confiança seria cancelar a tarefa e começar de novo.
-   **Não use caixas de seleção como um indicador de progresso.** Em vez disso, [use um controle de indicador](progress-bars.md) de progresso.

    **Incorreto:**

    ![captura de tela de quatro caixas de seleção mostrando o progresso ](images/ctrl-check-boxes-image15.png)

    Neste exemplo, as caixas de seleção são usadas incorretamente como um indicador de progresso.

    **Correto:**

    ![captura de tela de uma barra de progresso parcialmente preenchida ](images/ctrl-check-boxes-image16.png)

    Exemplo de uma barra de progresso típica.

-   **Mostrar caixas de seleção desabilitadas usando o estado de seleção correto.** Embora os usuários não possam alterá-los, as caixas de seleção desabilitadas transmitem informações para que eles sejam consistentes com os resultados.

    **Incorreto:**

    ![captura de tela de uma das duas caixas de seleção esmaecida ](images/ctrl-check-boxes-image17.png)

    Neste exemplo, a opção "Sempre ler esta seção em voz alta" deve ser limpa porque a seção não é lida quando a opção está desabilitada.

-   **Não use a seleção de uma caixa de seleção para**:
    -   Executar comandos.
    -   Exibir outras janelas, como uma caixa de diálogo para coletar mais entradas.
    -   Exibir dinamicamente outros controles relacionados ao controle selecionado (leitores de tela não podem detectar esses eventos).

### <a name="dont-show-this-item-again"></a>Não mostre isso <item> Novamente

-   **Considere usar uma opção Não mostrar novamente para permitir que os usuários suprimem uma caixa de diálogo recorrente somente se não <item> houver uma alternativa melhor.** Tente determinar com antecedência se os usuários realmente precisam da caixa de diálogo; se fizerem isso, sempre mostre a caixa de diálogo e, se não o fizerem, elimine a caixa de diálogo.

Para obter mais diretrizes e exemplos, consulte Caixas [de diálogo](win-dialog-box.md).

### <a name="subordinate-controls"></a>Controles subordinados

-   Coloque os controles subordinados à direita ou abaixo (recuado, liberando com o rótulo da caixa de seleção) a caixa de seleção e seu rótulo. Termine o rótulo da caixa de seleção com dois-pontos.

    ![captura de tela da caixa de texto abaixo do rótulo da caixa de seleção ](images/ctrl-check-boxes-image18.png)

    Neste exemplo, a caixa de seleção e seu controle subordinado compartilham o rótulo da caixa de seleção e sua chave de acesso.

-   **Deixe caixas de texto editáveis dependentes e listas listadas habilitadas se elas compartilharem o rótulo da caixa de seleção.** Quando os usuários digitarem ou colarem qualquer coisa na caixa, selecione a opção correspondente automaticamente. Isso simplifica a interação.

    ![captura de tela das caixas de texto de rodapé e de rodapé ](images/ctrl-check-boxes-image19.png)

    Neste exemplo, inserir um rodapé ou um rodapé seleciona automaticamente a opção .

-   Se você aninhar caixas de seleção com botões de opção ou outras caixas de seleção, desabilite esses controles subordinados até que a opção de **alto nível seja selecionada.** Isso evita confusão sobre o significado dos controles subordinados.
-   Tornar os controles subordinados em uma caixa de seleção contíguas com a caixa de seleção na ordem de tabulação.
-   **Se selecionar uma opção implica marcar caixas de seleção subordinadas, marque explicitamente essas caixas de seleção para limpar a relação.**

    **Incorreto:**

    ![captura de tela: botão selecionado, caixas de seleção des limpas ](images/ctrl-check-boxes-image20.png)

    Neste exemplo, as caixas de seleção subordinadas não estão selecionadas.

    **Correto:**

    ![captura de tela: botão selecionado, caixas de seleção selecionadas ](images/ctrl-check-boxes-image21.png)

    Neste exemplo, as caixas de seleção subordinadas são selecionadas, tornando sua relação com a opção selecionada clara.

-   **Use caixas de seleção dependentes se as alternativas adicionarem complexidade desnecessária.** Embora as caixas de seleção devem ser opções independentes, às vezes, alternativas como botões de opção adicionam complexidade desnecessária.

    **Correto:**

    ![captura de tela de botões confusos e caixas de seleção ](images/ctrl-check-boxes-image22.png)

    Neste exemplo, o uso de botões de rádio é preciso, mas cria complexidade desnecessária.

    **Melhor:**

    ![captura de tela somente de caixas de seleção ](images/ctrl-check-boxes-image23.png)

    Neste exemplo, o uso de caixas de seleção é mais simples e permite que os usuários se concentrem na seleção das opções desejadas em vez de em sua relação complexa.

    **Importante: aplique essa diretriz somente em circunstâncias extremamente raras,** ao mostrar que as dependências adicionam complexidade significativa sem adicionar clareza. No exemplo anterior, é improvável que os usuários tentarem escolher o superscrito e o subscrito e, se o fizeram, seria fácil entender que eles eram opções exclusivas.

### <a name="default-values"></a>Valores padrão

-   Se uma caixa de seleção for para uma opção de usuário, de definir o mais seguro (para evitar a perda de dados ou acesso ao sistema), o estado mais seguro **e privado por padrão.** Se segurança e segurança não são fatores, selecione o valor mais provável ou conveniente.

## <a name="recommended-sizing-and-spacing"></a>Espaçamento e o espaçamento recomendados

![figura do espaçamento e o espaçamento sugeridos da caixa de seleção ](images/ctrl-check-boxes-image24.png)

O espaçamento e o espaçamento recomendados para caixas de seleção.

## <a name="labels"></a>Rótulos

**Rótulos da caixa de seleção**

-   Marque cada caixa de seleção.
-   Atribua uma chave [de acesso exclusiva](glossary.md) a cada rótulo. Para diretrizes, consulte [Teclado](inter-keyboard.md).
-   Use [a capitalização de estilo de frase](glossary.md).
-   Escreva o rótulo como uma frase ou uma frase imperativa e não use nenhuma pontuação final.
    -   **Exceção:** Se um rótulo de caixa de seleção também rotular um controle subordinado que o segue, termine o rótulo com dois-pontos.
-   Escreva o rótulo para que ele descreva o estado selecionado da caixa de seleção.
-   Para um grupo de caixas de seleção, use frase paralela e tente manter o comprimento aproximadamente o mesmo para todos os rótulos.
-   Para um grupo de caixas de seleção, concentre o texto do rótulo nas diferenças entre as opções. Se todas as opções têm o mesmo texto introdutório, mova esse texto para o rótulo do grupo.
-   Use frases positivas. Não expresse um rótulo para que a seleção de uma caixa de seleção significa não executar uma ação.

    -   **Exceção: não mostre isso novamente <item> nas caixas** de seleção.

    **Incorreto:**

    ![captura de tela do rótulo negativo 'desligar'](images/ctrl-check-boxes-image25.png)

    Neste exemplo, a opção não usa frase positiva.

-   Descreva apenas a opção com o rótulo. Mantenha os rótulos breves para que seja fácil fazer referência a eles em mensagens e documentação. Se a opção exigir mais explicação, forneça a explicação em um controle de [texto](./glossary.md) estático usando frases completas e pontuação final.

    > [!Note]
    >
    > Adicionar uma explicação a uma caixa de seleção em um grupo não significa que você precisa fornecer explicações para todas as caixas de seleção no grupo. Forneça as informações relevantes no rótulo, se possível, e use explicações somente quando necessário. Não apenas restate o rótulo para consistência.

     

    ![captura de tela da caixa de seleção, rótulo e descrição ](images/ctrl-check-boxes-image26.png)

    Neste exemplo, um rótulo de caixa de seleção tem texto explicativo adicional abaixo dele.

-   Se uma opção for altamente recomendada, considere adicionar "(recomendado)" ao rótulo. Certifique-se de adicionar ao rótulo de controle, não às notas complementares.
-   Se você precisa usar rótulos de várias linhas, alinhe a parte superior do rótulo com a caixa de seleção.
-   Não use um controle subordinado, os valores que ele contém ou seu rótulo de unidades para criar uma frase ou frase. Esse design não é localizável porque a estrutura de frase varia de acordo com o idioma.

    **Incorreto:**

    ![captura de tela do rótulo da caixa de seleção com a caixa de texto nele ](images/ctrl-check-boxes-image27.png)

    Neste exemplo, a caixa de texto é colocada incorretamente dentro do rótulo da caixa de seleção.

**Rótulos de grupo da caixa de seleção**

-   Use o rótulo do grupo para explicar a finalidade do grupo, não como fazer a seleção. Suponha que os usuários saibam como usar caixas de seleção. Por exemplo, não diga "Selecione qualquer uma das opções a seguir".
-   Termine cada rótulo com dois-pontos.
-   Não atribua uma chave de acesso ao rótulo. Isso não é necessário e torna as outras chaves de acesso mais difíceis de atribuir.
-   Para uma seleção de uma ou mais opções dependentes, explique o requisito no rótulo.

    **Correto:**

    ![captura de tela do rótulo para dois controles: protocolos ](images/ctrl-check-boxes-image28.png)

    Neste exemplo, os usuários podem pensar que só podem fazer uma seleção.

    **Melhor:**

    ![captura de tela do rótulo: os protocolos selecionam um ou mais ](images/ctrl-check-boxes-image29.png)

    Neste exemplo, fica claro que os usuários podem fazer mais de uma seleção.

## <a name="documentation"></a>Documentação

Ao fazer referência às caixas de seleção:

-   Use o texto exato do rótulo, incluindo sua capitalização, mas não inclua o sublinhado ou dois-pontos da chave de acesso. Inclua a caixa de seleção palavra.
-   Veja uma caixa de seleção como uma caixa de seleção, não uma opção, uma caixa de seleção ou apenas uma caixa, pois a caixa é ambígua para localizadores.
-   Para descrever a interação do usuário, use selecionar e limpar.
-   Quando possível, forja o rótulo usando texto em negrito. Caso contrário, coloque o rótulo entre aspas somente se necessário para evitar confusão.

    Exemplo: marque a **caixa de seleção Sublinhado.**

