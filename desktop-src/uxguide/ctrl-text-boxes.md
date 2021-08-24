---
title: Caixas de texto
description: Com uma caixa de texto, os usuários podem exibir, inserir ou editar um texto ou valor numérico.
ms.assetid: fb8ed262-1451-496d-a3f4-a29af39763bb
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 63418b3f72691e5ac23638291b9ec8aa83bc78d2f89815e093f5a04850a3d9ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119819245"
---
# <a name="text-boxes"></a>Caixas de texto

> [!NOTE]
> Este guia de design foi criado para Windows 7 e não foi atualizado para versões mais recentes do Windows. Grande parte das diretrizes ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais.](/windows/uwp/design/)

Com uma caixa de texto, os usuários podem exibir, inserir ou editar um texto ou valor numérico.

![captura de tela de uma caixa de texto e rótulo típicos ](images/ctrl-text-boxes-image1.png)

Uma caixa de texto típica.

> [!Note]  
> Diretrizes relacionadas [ao layout,](vis-layout.md) [fontes](vis-fonts.md)e [balão são apresentadas](ctrl-balloons.md) em artigos separados.

 

## <a name="is-this-the-right-control"></a>Esse é o controle correto?

Para decidir, considere estas perguntas:

-   **É prático enumerar todos os valores válidos com eficiência?** Em caso afirmaível, considere uma [lista](ctrl-list-boxes.md)de seleção [única,](ctrl-list-views.md)exibição de [lista,](/windows/desktop/uxguide/ctrl-drop)lista de lista, lista de listas listadas editáveis, ou [controle deslizante.](ctrl-sliders.md)
-   **Os dados válidos não estão totalmente restritos? Ou os dados válidos são restritos somente por formato (tipos de caracteres ou comprimento restritos)?** Se sim, use uma caixa de texto.
-   **O valor representa um tipo de dados que tem um controle comum especializado?** Os exemplos incluem data, hora ou endereço IPv4 ou IPv6. Nesse caso, use o controle apropriado, como um controle de data em vez de uma caixa de texto.
-   Se os dados são numéricos:
    -   **Os usuários percebe a configuração como uma quantidade relativa?** Se sim, use um controle deslizante.
    -   **O usuário se beneficiaria com um feedback instantâneo sobre o efeito das alterações de configuração?** Nesse caso, use um controle deslizante, possivelmente junto com uma caixa de texto. Por exemplo, os usuários podem escolher facilmente uma cor usando um controle deslizante porque podem ver imediatamente o efeito das alterações nos valores de matiz, saturação ou luminosidade.

## <a name="design-concepts"></a>Conceitos de design

Embora as caixas de texto tenham o benefício de serem muito flexíveis, elas têm a desvantagem de ter restrições mínimas. As únicas restrições em uma caixa de texto editável são:

-   Opcionalmente, você pode definir o número máximo de caracteres.
-   Opcionalmente, você pode restringir a entrada somente a caracteres numéricos (0 9).
-   Se você usar um [controle de rotação](ctrl-spin-controls.md), poderá limitar as opções de controle de rotação a valores válidos.

Além do comprimento e da presença opcional de um controle de rotação, as caixas de texto não têm nenhuma dica visual que sugira os valores válidos ou seu formato. Isso significa contar com rótulos para transmitir essas informações aos usuários. Se os usuários inserirem um texto que não seja válido, você deverá tratar o erro com uma mensagem de erro.

Como regra geral, **você deve usar o controle mais restrito que você pode**. Use controles irr pouco restritos, como caixas de texto como último recurso. Dito isso, quando você estiver considerando restrições, tenha em mente as necessidades de usuários globais. Por exemplo, um controle restrito a Estados Unidos ZIP Não é globalizado, mas uma caixa de texto irr pouco restrita que aceita qualquer formato de código postal é.

## <a name="usage-patterns"></a>Padrões de uso

Uma caixa de texto é um controle flexível com vários usos possíveis.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Entrada de dados</strong><br/> Uma caixa de texto de linha única e irr pouco restrita usada para inserir ou editar cadeias de caracteres curtas.<br/></td>
<td><img src="images/ctrl-text-boxes-image2.png" alt="Screen shot of a text box with Display name label " /><br/> Uma caixa de texto de linha única e irr pouco restrita.<br/></td>
</tr>
<tr class="even">
<td><strong>Entrada de dados formatados</strong><br/> Um conjunto de caixas de texto de linha única de tamanho curto e fixo usado para inserir dados com um formato específico. <br/></td>
<td><img src="images/ctrl-text-boxes-image3.png" alt="Screen shot of a Product key text box " /><br/> Uma caixa de texto usada para entrada de dados formatada.<br/>
<blockquote>
[!Note]<br />
O <a href="glossary.md">recurso de saída</a> automática avança automaticamente o foco de entrada de uma caixa de texto para a próxima. Uma desvantagem dessa abordagem é que os dados não podem ser copiados ou copiados como uma única unidade.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><strong>Entrada de dados assistida</strong><br/> Uma caixa de texto de linha única e irr pouco restrita usada para inserir ou editar cadeias de caracteres, combinada com um botão de comando que ajuda os usuários a selecionar valores válidos.<br/></td>
<td><img src="images/ctrl-text-boxes-image4.png" alt="Screen shot of text box with Browse button" /><br/> Neste exemplo, o comando Procurar ajuda os usuários a selecionar valores válidos.<br/></td>
</tr>
<tr class="even">
<td><strong>Entrada textual</strong><br/> Uma caixa de texto sem restrição de várias linhas usada para inserir ou editar cadeias de caracteres longas. <br/></td>
<td><img src="images/ctrl-text-boxes-image5.png" alt="Screen shot of an Address text box " /><br/> Uma caixa de texto sem restrição de várias linhas.<br/></td>
</tr>
<tr class="odd">
<td><strong>Entrada numérica</strong><br/> Uma caixa de texto somente numérica de linha única usada <a href="ctrl-spin-controls.md"></a> para inserir ou editar números, com um controle de rotação opcional para facilitar a entrada baseada em mouse. <br/></td>
<td><img src="images/ctrl-text-boxes-image6.png" alt="Screen shot of a text box for entering a wait time " /><br/> Uma caixa de texto usada para entrada numérica.<br/> A combinação de uma caixa de texto e seu controle de rotação associado é chamada de caixa <a href="ctrl-spin-controls.md">de rotação</a>.<br/></td>
</tr>
<tr class="even">
<td><strong>Senha e entrada de PIN</strong><br/> Uma caixa de texto de linha única e irr pouco restrita usada para inserir senhas e PINs com segurança.<br/></td>
<td><img src="images/ctrl-text-boxes-image7.png" alt="Screen shot of a Password text box " /><br/> Uma caixa de texto usada para inserir senhas.<br/></td>
</tr>
<tr class="odd">
<td><strong>Saída de dados</strong><br/> Uma caixa de texto somente leitura de linha única, sempre exibida sem uma borda, usada para exibir cadeias de caracteres curtas. <br/></td>
<td>Ao contrário do texto estático, os dados exibidos usando uma caixa de texto podem ser rolados (útil se os dados forem maiores do que o controle), selecionados e copiados.<br/> <img src="images/ctrl-text-boxes-image8.png" alt="Screen shot of a text box showing path to a folder " /><br/> Uma caixa de texto somente leitura de linha única usada para exibir dados.<br/></td>
</tr>
<tr class="even">
<td><strong>Saída textual</strong><br/> Uma caixa de texto somente leitura de várias linhas usada para exibir cadeias de caracteres longas. <br/></td>
<td><img src="images/ctrl-text-boxes-image9.png" alt="Screen shot of a Privacy information text box " /><br/> Uma caixa de texto somente leitura usada para exibir dados.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="guidelines"></a>Diretrizes

### <a name="general"></a>Geral

-   **Ao desabilitar uma caixa de texto, desabilite também quaisquer rótulos associados, rótulos de instrução, controles de rotação e botões de comando.**
-   **Use o auto-complete para ajudar os usuários a inserir dados que provavelmente serão usados repetidamente.** Os exemplos incluem nomes de usuário, endereços e nomes de arquivo. No entanto, não use a conclusão automática para caixas de texto que podem conter informações confidenciais, como senhas, PINs, números de cartão de crédito ou informações médicas.
-   **Não faça os usuários rolarem desnecessariamente.** Se você espera que os dados sejam maiores do que a caixa de texto e pode facilmente tornar a caixa de texto maior sem prejudicar o layout, tamanho da caixa para eliminar a necessidade de rolagem.

    **Incorreto:**

    ![captura de tela de uma caixa de texto de nome de computador ](images/ctrl-text-boxes-image10.png)

    Neste exemplo, a caixa de texto deve ficar muito mais longa para lidar com seus dados.

-   Barras de rolagem:
    -   **Não coloque barras de rolagem horizontais em caixas de texto de várias linhas.** Em vez disso, use rolagem vertical e quebra de linha.
    -   **Não coloque nenhuma barra de rolagem em caixas de texto de linha única.**
-   **Para entrada numérica, você pode usar um controle de rotação.** Para entrada textual, use uma lista de listas listadas ou lista de listas listadas editáveis em vez disso.
-   **Não use o recurso de saída automática, exceto a entrada de dados formatada.** A mudança automática de foco pode surpresar os usuários.

### <a name="editable-text-boxes"></a>Caixas de texto editáveis

-   **Limite o comprimento do texto de entrada quando possível.** Por exemplo, se a entrada válida for um número entre 0 e 999, use uma caixa de texto numérica limitada a três caracteres. Todas as partes das caixas de texto que usam a entrada de dados formatada devem ter um comprimento curto e fixo.
-   **Seja flexível com formatos de dados.** Se os usuários provavelmente inserirem texto usando uma ampla variedade de formatos, tente lidar com todos os mais comuns. Por exemplo, muitos nomes, números e identificadores podem ser inseridos com espaços opcionais e pontuação, e a capitalização geralmente não importa.
-   Se você não puder lidar com os formatos prováveis, exigir um formato específico usando a entrada de dados formatada ou indicar os formatos válidos no rótulo.

    **Aceitável:**

    ![captura de tela de uma caixa de texto para entrada numérica ](images/ctrl-text-boxes-image11.png)

    Neste exemplo, uma caixa de texto requer entrada em um formato específico.

    **Melhor:**

    ![captura de tela da caixa de texto de entrada de dados formatada ](images/ctrl-text-boxes-image12.png)

    Neste exemplo, o padrão de entrada de dados formatado é usado para exigir um formato específico.

    **Melhor:**

    ![captura de tela de uma caixa de texto irr pouco restrita ](images/ctrl-text-boxes-image13.png)

    Neste exemplo, uma caixa de texto lida com todos os formatos prováveis.

-   Considere a flexibilidade de formato ao escolher o comprimento máximo de entrada. Por exemplo, um número de cartão de crédito válido pode usar até 19 caracteres, portanto, limitar o comprimento a qualquer coisa mais curta dificultaria a entrada de números usando os formatos mais longos.
-   **Não use o padrão de entrada de dados formatados se os usuários têm maior probabilidade de colar dados longos e complexos.** Em vez disso, reserve o padrão de entrada de dados formatado para situações em que os usuários têm maior probabilidade de digitar os dados.

    ![captura de tela de uma caixa de texto com rótulo: endereço ipv6 ](images/ctrl-text-boxes-image14.png)

    Neste exemplo, o padrão de entrada de dados formatado não é usado, para que os usuários possam colar endereços IPv6.

-   **Se os usuários provavelmente inserirão o valor inteiro novamente, selecione todo o texto no foco de entrada.** Se os usuários têm maior probabilidade de editar, coloque o ai no final do texto.

    ![captura de tela de uma caixa de texto de senha ](images/ctrl-text-boxes-image15.png)

    Neste exemplo, os usuários têm maior probabilidade de substituir do que editar, portanto, o valor inteiro é selecionado no foco de entrada.

    ![captura de tela de uma caixa de texto para inserir palavras-chave ](images/ctrl-text-boxes-image16.png)

    Neste exemplo, os usuários têm maior probabilidade de adicionar palavras-chave do que substituir o texto, portanto, o acento de acento é colocado no final do texto.

-   **Sempre use uma caixa de texto de várias linhas se caracteres de nova linha são entrada válida.**
-   **Quando a caixa de texto for para um arquivo ou caminho, sempre forneça um botão Procurar.**

### <a name="numeric-text-boxes"></a>Caixas de texto numéricas

-   **Escolha a unidade mais conveniente e rotule as unidades.** Por exemplo, considere usar mililiters em vez de liters (ou vice-versa), percentuais em vez de valores diretos (ou vice-versa) e assim por diante.

    **Correto:**

    ![captura de tela da caixa de texto com liters como unidade ](images/ctrl-text-boxes-image17.png)

    Neste exemplo, a unidade é rotulada, mas exige que os usuários insiram números decimais.

    **Melhor:**

    ![captura de tela da caixa de texto com mililitros como unidade ](images/ctrl-text-boxes-image18.png)

    Neste exemplo, a caixa de texto usa uma unidade mais conveniente.

-   **Use um controle de rotação sempre que for útil.** No entanto, às vezes, controles de rotação não são práticos, como quando os usuários precisam inserir muitos números grandes. Use controles de rotação quando:
    -   A entrada provavelmente será um número pequeno, normalmente abaixo de 100.
    -   É provável que os usuários façam uma pequena alteração em um número existente.
    -   É mais provável que os usuários usem o mouse do que o teclado.
-   **Alinhe o texto numérico à direita sempre que:**

    -   Há mais de uma caixa de texto numérica.
    -   As caixas de texto são alinhadas verticalmente.
    -   É provável que os usuários adicionem ou comparem os valores.

    **Correto:**

    ![captura de tela de caixas de texto de despesas (hotel, etc.) ](images/ctrl-text-boxes-image19.png)

    Neste exemplo, o texto numérico é alinhado à direita para facilitar a comparação de valores.

    **Incorreto:**

    ![captura de tela de caixas de texto para valores rgb ](images/ctrl-text-boxes-image20.png)

    Neste exemplo, o texto numérico é alinhado incorretamente à esquerda.

-   **Sempre alinhe valores monetários com a direita.**
-   **Não atribua significados especiais a valores numéricos específicos,** mesmo que esses significados especiais sejam usados internamente pelo seu aplicativo. Em vez disso, use caixas de seleção ou botões de opção para uma seleção explícita de usuário.

    **Incorreto:**

    ![captura de tela do rótulo: use -1 para desabilitar o cache ](images/ctrl-text-boxes-image21.png)

    Neste exemplo, o valor -1 tem um significado especial.

    **Correto:**

    ![captura de tela do rótulo da caixa de seleção: cache ](images/ctrl-text-boxes-image22.png)

    Neste exemplo, uma caixa de seleção torna a opção explícita.

### <a name="password-and-pin-input"></a>Senha e entrada de PIN

-   **Sempre use o controle comum de senha em vez de criar seu próprio.** Senhas e PINs exigem tratamento especial para serem tratados com segurança.

Para obter mais diretrizes e exemplos, consulte [Balão.](ctrl-balloons.md)

### <a name="textual-output"></a>Saída textual

-   **Considere usar a cor do sistema de tela de fundo branca para texto grande e somente leitura de várias linhas.** Uma plano de fundo em branco facilita a leitura do texto. Muito texto em uma plano de fundo cinza não desanimo a leitura.

Para obter mais informações sobre cores da plano de fundo, consulte [Fontes](vis-fonts.md).

### <a name="data-output"></a>Saída de dados

-   **Não use uma borda para caixas de texto somente leitura de linha única.** A borda é uma dica visual de que o texto é editável.
-   **Não desabilite caixas de texto somente leitura de linha única.** Isso impede que os usuários selecionem e copiem o texto para a área de transferência. Ele também impede que os usuários rolem os dados se excederem o tamanho de seus limites.
-   **Não de definir uma parada de tabulação em uma única linha, caixa de texto somente leitura, a menos que o usuário provavelmente precise rolar ou copiar o texto.**

## <a name="input-validation-and-error-handling"></a>Validação de entrada e tratamento de erros

Como as caixas de texto geralmente não são restritas para aceitar apenas a entrada válida, talvez seja necessário validar a entrada e lidar com problemas. Valide os vários tipos de problemas de entrada da seguinte forma:

-   Se o usuário inserir um caractere que não é válido, ignore o caractere e exibe um balão de problema de entrada que explica os caracteres válidos. [](ctrl-balloons.md)

    ![captura de tela da caixa de texto chave do produto (Product Key)](images/ctrl-text-boxes-image23.png)

    Neste exemplo, um balão relata um caractere de entrada incorreto.

-   Se os dados de entrada têm um valor ou formato que não é válido, exibe um balão de problema de entrada quando a caixa de texto perde o foco de entrada.
-   Se os dados de entrada estão inconsistentes com outros controles na janela, dê uma mensagem de erro quando toda a entrada for concluída, como quando os usuários clicarem em OK para uma caixa de diálogo modal.

**Não limpe dados de entrada inválidos, a menos que os usuários não sejam capazes de corrigir erros facilmente.** Isso permite que os usuários corrijam erros sem começar de novo. Por exemplo, você deve limpar senhas incorretas e PINs porque os usuários não podem corrigi-las facilmente.

Para obter mais diretrizes e exemplos, consulte [Mensagens de erro](mess-error.md) e [balão.](ctrl-balloons.md)

## <a name="prompts"></a>Solicitações

Um prompt é um rótulo ou uma instrução curta colocada dentro de uma caixa de texto como seu valor padrão. Ao contrário do texto estático, os prompts desaparecem da tela quando os usuários digitam algo na caixa de texto ou ele obtém o foco de entrada.

![captura de tela da caixa de texto do prompt com rótulo: pesquisa ](images/ctrl-text-boxes-image24.png)

Um prompt típico.

Use um prompt quando:

-   O espaço na tela é tão premium que usar um rótulo ou instrução é indesejável, como em uma barra de ferramentas.
-   O prompt serve principalmente para identificar a finalidade da caixa de texto de maneira compacta. Não deve ser informações cruciais que o usuário precisa ver ao usar a caixa de texto.

Não use prompts apenas para direcionar os usuários a digitar algo ou clicar em botões. Por exemplo, não escreva texto de prompt que diz Enter a filename e clique em Enviar.

Ao usar prompts:

-   Desenhe o texto do prompt em cinza itálico e o texto de entrada real em preto normal. O texto do prompt não deve ser confundido com texto real.
-   Mantenha o texto do prompt conciso. Você pode usar fragmentos em vez de frases completas.
-   Use a capitalização com estilo de frase.
-   Não use a pontuação final ou as reticpses.
-   O texto do prompt não deve ser editável e deve desaparecer depois que os usuários clicarem na guia ou na caixa de texto.
    -   **Exceção:** Se a caixa de texto tiver o foco de entrada padrão, o prompt será exibido e desaparecerá depois que o usuário começar a digitar.
-   O texto do prompt será restaurado se a caixa de texto ainda estiver vazia quando perder o foco de entrada.

## <a name="recommended-sizing-and-spacing"></a>Dimensionamento e espaçamento recomendados

![Figura de caixas de texto de uma linha e de duas linhas ](images/ctrl-text-boxes-image25.png)

Dimensionamento e espaçamento recomendados para caixas de texto.

A largura de uma caixa de texto é uma pista visual do tamanho de entrada esperado. Ao dimensionar caixas de texto:

-   **Escolha uma largura apropriada para os dados válidos mais longos.** Na maioria das situações, os usuários não precisam rolar a cadeia de caracteres mais longa provável que eles inserirão ou exibirão.
-   **Inclua mais 30%** (até 200 por cento para texto mais curto) para qualquer texto (mas não números) que serão localizados.
-   **Se a entrada esperada não tiver um tamanho específico, escolha uma largura consistente com as outras caixas de texto ou controles na janela.**
-   **Dimensione as caixas de texto de várias linhas para exibir um número integral de linhas de texto.**

## <a name="labels"></a>Rótulos

### <a name="text-box-labels"></a>Rótulos da caixa de texto

-   Todas as caixas de texto precisam de rótulos. Grave o rótulo como uma palavra ou frase, não como uma frase, terminando com dois-pontos e usando [texto estático](glossary.md).

    **Exceções:**

    -   Caixas de texto com prompts localizados onde o espaço está em uma parte Premium.
    -   Para rotulagem, um grupo de caixas de texto usado para **entrada de dados formatados** deve ser tratado como uma única caixa de texto.
    -   Se uma caixa de texto for subordinada a um botão de opção ou caixa de seleção e for introduzida por seu rótulo que termina com dois-pontos, não coloque um rótulo adicional na caixa de texto.
    -   **Omita os rótulos de controle que redefinem a instrução principal.** Nesse caso, a instrução principal leva os dois-pontos (a menos que seja uma pergunta) e a chave de acesso.

        **Aceitável:**

        ![captura de tela da caixa de texto com o rótulo redundante](images/ctrl-text-boxes-image26.png)

        Neste exemplo, o rótulo da caixa de texto é apenas uma recondição da instrução principal.

        **Melhor:**

        ![captura de tela da caixa de texto com a instrução Main somente ](images/ctrl-text-boxes-image27.png)

        Neste exemplo, o rótulo redundante é removido e, portanto, a instrução Main usa a tecla de acesso e os dois-pontos.

-   Atribua uma chave de acesso exclusiva. Para obter diretrizes de atribuição de chave de acesso, consulte [teclado](inter-keyboard.md).
-   Use a capitalização com estilo de frase.
-   Posicione o rótulo à esquerda ou acima da caixa de texto e alinhe o rótulo à borda esquerda da caixa de texto. Se o rótulo estiver à esquerda, alinhe verticalmente o texto do rótulo com o texto da caixa de texto.

    **Correto:**

    ![captura de tela do rótulo alinhado à esquerda acima da caixa de texto ](images/ctrl-text-boxes-image28.png)

    ![captura de tela do rótulo alinhado por texto à esquerda da caixa de texto ](images/ctrl-text-boxes-image29.png)

    Nesses exemplos, o rótulo na parte superior alinha com a borda esquerda da caixa de texto e o rótulo à esquerda é alinhado com o texto na caixa de texto.

    **Incorreto:**

    ![captura de tela de rótulo alinhado por texto acima da caixa de texto ](images/ctrl-text-boxes-image30.png)

    ![captura de tela do rótulo alinhado na parte superior esquerda da caixa de texto ](images/ctrl-text-boxes-image31.png)

    Nesses exemplos incorretos, o rótulo na parte superior alinha com o texto na caixa de texto e o rótulo à esquerda é alinhado com a parte superior da caixa de texto.

-   Você pode especificar unidades (por exemplo, segundos ou conexões) entre parênteses após o rótulo.
-   Se uma caixa de texto aceitar um número máximo de caracteres arbitrariamente pequeno, você poderá indicar a entrada máxima no rótulo. A largura da caixa de texto também deve sugerir o tamanho máximo.

    ![captura de tela da caixa de texto de senha ](images/ctrl-text-boxes-image32.png)

    Neste exemplo, o rótulo fornece o número máximo de caracteres.

-   Não faça com que o conteúdo da caixa de texto (ou seu rótulo de unidade) faça parte de uma frase, pois isso não é localizável.
-   Se a caixa de texto puder ser usada para inserir vários itens, deixe claro como separar os itens no rótulo.

    ![captura de tela de nomes separados por rótulo com ponto e vírgula ](images/ctrl-text-boxes-image33.png)

    Neste exemplo, o separador de item é fornecido no rótulo.

-   Para obter diretrizes sobre como indicar a entrada necessária, consulte entrada necessária nas [caixas de diálogo](win-dialog-box.md).

### <a name="instruction-labels"></a>Rótulos de instrução

-   Se você precisar adicionar texto de instrução sobre uma caixa de texto, adicione-a acima do rótulo. Use frases completas com pontuação final.
-   Use a capitalização com estilo de frase.
-   Informações adicionais que são úteis, mas não necessárias, devem ser mantidas curtas. Coloque essas informações entre parênteses entre o rótulo e os dois-pontos ou sem parênteses abaixo da caixa de texto.

    ![captura de tela de informações adicionadas abaixo da caixa de texto ](images/ctrl-text-boxes-image34.png)

    Neste exemplo, informações adicionais são colocadas abaixo da caixa de texto.

### <a name="prompt-labels"></a>Rótulos de prompt

-   Mantenha o texto do prompt conciso. Você pode usar fragmentos em vez de frases completas.
-   Use a capitalização com estilo de frase.
-   Não use pontuação final ou reticências.
-   Se o prompt instrui os usuários a inserir informações que serão acionadas por um botão ao lado da caixa de texto, basta posicionar o botão ao lado da caixa de texto. Não use o prompt para direcionar os usuários a clicar no botão (por exemplo, não escreva o texto do prompt que diz, arraste um arquivo e clique em enviar).

## <a name="documentation"></a>Documentação

Ao fazer referência a caixas de texto:

-   Use tipo para se referir a interações do usuário que exigem digitação ou colagem; caso contrário, use Enter se os usuários puderem colocar informações na caixa de texto usando outros meios, como selecionar o valor de uma lista ou usar um botão de procura.
-   Use Selecionar para se referir a uma entrada em uma caixa de texto somente leitura.
-   Use o texto exato do rótulo, incluindo sua capitalização e inclua a caixa palavra. Não inclua a tecla de acesso sublinhado ou dois-pontos. Não faça referência a uma caixa de texto como uma caixa de texto ou um campo.
-   Quando possível, formate o rótulo usando texto em negrito. Caso contrário, coloque o rótulo entre aspas somente se necessário para evitar confusão.

    Exemplo: digite sua senha na caixa **senha** e clique em **OK**.

-   Se a caixa de texto exigir um formato específico, documente apenas o formato aceitável mais comumente usado. Permita que os usuários descubram outros formatos por conta própria. Você deseja ser flexível com formatos de dados, mas fazer isso não deve resultar em documentação complexa.

    **Correto:**

    Insira o número de série da parte usando o formato 1234-56-7890.

    **Incorreto:**

    Insira o número de série da parte usando qualquer um dos seguintes formatos:

    1234567890

    1234-56-7890

    1234 56 7890

