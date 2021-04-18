---
title: Caixas de texto
description: Com uma caixa de texto, os usuários podem exibir, inserir ou editar um texto ou valor numérico.
ms.assetid: fb8ed262-1451-496d-a3f4-a29af39763bb
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 2b5257e9772465f26815abb0f6ecbe0ff357ba4b
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "104506321"
---
# <a name="text-boxes"></a>Caixas de texto

> [!NOTE]
> Este guia de design foi criado para o Windows 7 e não foi atualizado para versões mais recentes do Windows. Grande parte da orientação ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais](/windows/uwp/design/).

Com uma caixa de texto, os usuários podem exibir, inserir ou editar um texto ou valor numérico.

![captura de tela de uma caixa de texto e rótulo típicos ](images/ctrl-text-boxes-image1.png)

Uma caixa de texto típica.

> [!Note]  
> As diretrizes relacionadas ao [layout](vis-layout.md), às [fontes](vis-fonts.md)e aos [balões](ctrl-balloons.md) são apresentadas em artigos separados.

 

## <a name="is-this-the-right-control"></a>Esse é o controle correto?

Para decidir, considere estas perguntas:

-   **É prático enumerar todos os valores válidos com eficiência?** Nesse caso, considere uma [lista de seleção única](ctrl-list-boxes.md), [exibição de lista](ctrl-list-views.md), [lista suspensa](/windows/desktop/uxguide/ctrl-drop), lista suspensa editável ou [controle deslizante](ctrl-sliders.md) em vez disso.
-   **Os dados válidos são completamente irrestrito? Ou os dados válidos são restritos apenas por formato (comprimento ou tipos de caracteres restritos)?** Nesse caso, use uma caixa de texto.
-   **O valor representa um tipo de dados que tem um controle comum especializado?** Os exemplos incluem data, hora ou endereço IPv4 ou IPv6. Nesse caso, use o controle apropriado, como um controle de data, em vez de uma caixa de texto.
-   Se os dados forem numéricos:
    -   **Os usuários percebem a configuração como uma quantidade relativa?** Se sim, use um controle deslizante.
    -   **O usuário se beneficiaria com um feedback instantâneo sobre o efeito das alterações de configuração?** Nesse caso, use um controle deslizante, possivelmente junto com uma caixa de texto. Por exemplo, os usuários podem escolher facilmente uma cor usando um controle deslizante, pois eles podem ver imediatamente o efeito das alterações nos valores de matiz, saturação ou luminosidade.

## <a name="design-concepts"></a>Conceitos de design

Embora as caixas de texto tenham o benefício de ser muito flexível, elas têm a desvantagem de ter restrições mínimas. As únicas restrições em uma caixa de texto editável são:

-   Opcionalmente, você pode definir o número máximo de caracteres.
-   Opcionalmente, você pode restringir a entrada para caracteres numéricos (0 9).
-   Se você usar um [controle de rotação](ctrl-spin-controls.md), poderá limitar as opções de controle de giro a valores válidos.

Além da sua duração e da presença opcional de um controle de rotação, as caixas de texto não têm nenhuma pista visual que sugira os valores válidos ou seu formato. Isso significa depender dos rótulos para transmitir essas informações aos usuários. Se os usuários digitarem texto que não seja válido, você deverá manipular o erro com uma mensagem de erro.

Como regra geral, **você deve usar o controle mais restrito que pode**. Use controles irrestrito como caixas de texto como último recurso. Dito isso, quando você estiver considerando restrições, tenha em mente as necessidades de usuários globais. Por exemplo, um controle que é restrito a Estados Unidos CEPs não é globalizado, mas uma caixa de texto irrestrita que aceita qualquer formato de código postal é.

## <a name="usage-patterns"></a>Padrões de uso

Uma caixa de texto é um controle flexível com vários usos possíveis.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Entrada de dados</strong><br/> Uma caixa de texto de linha única e irrestrita usada para inserir ou editar cadeias de caracteres curtas.<br/></td>
<td><img src="images/ctrl-text-boxes-image2.png" alt="Screen shot of a text box with Display name label " /><br/> Uma caixa de texto de linha única e irrestrita.<br/></td>
</tr>
<tr class="even">
<td><strong>Entrada de dados formatados</strong><br/> Um conjunto de caixas de texto de linha simples, com tamanho fixo e curto usado para inserir dados com um formato específico. <br/></td>
<td><img src="images/ctrl-text-boxes-image3.png" alt="Screen shot of a Product key text box " /><br/> Uma caixa de texto usada para entrada de dados formatados.<br/>
<blockquote>
[!Note]<br />
O recurso de <a href="glossary.md">saída automática</a> avança automaticamente o foco de entrada de uma caixa de texto para a próxima. Uma desvantagem dessa abordagem é que os dados não podem ser copiados ou colados como uma única unidade.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><strong>Entrada de dados assistida</strong><br/> Uma caixa de texto de linha única e irrestrita usada para inserir ou editar cadeias de caracteres, combinadas com um botão de comando que ajuda os usuários a selecionar valores válidos.<br/></td>
<td><img src="images/ctrl-text-boxes-image4.png" alt="Screen shot of text box with Browse button" /><br/> Neste exemplo, o comando procurar ajuda os usuários a selecionar valores válidos.<br/></td>
</tr>
<tr class="even">
<td><strong>Entrada textual</strong><br/> Uma caixa de texto de várias linhas e irrestrita usada para inserir ou editar cadeias de caracteres longas. <br/></td>
<td><img src="images/ctrl-text-boxes-image5.png" alt="Screen shot of an Address text box " /><br/> Uma caixa de texto de várias linhas e irrestrita.<br/></td>
</tr>
<tr class="odd">
<td><strong>Entrada numérica</strong><br/> Uma caixa de texto de linha única, somente numérica, usada para inserir ou editar números, com um <a href="ctrl-spin-controls.md">controle de rotação</a> opcional para facilitar a entrada baseada no mouse. <br/></td>
<td><img src="images/ctrl-text-boxes-image6.png" alt="Screen shot of a text box for entering a wait time " /><br/> Uma caixa de texto usada para entrada numérica.<br/> A combinação de uma caixa de texto e seu controle de rotação associado é chamada de <a href="ctrl-spin-controls.md">caixa de rotação</a>.<br/></td>
</tr>
<tr class="even">
<td><strong>Senha e PIN de entrada</strong><br/> Uma caixa de texto de linha única e irrestrita usada para inserir senhas e PINs com segurança.<br/></td>
<td><img src="images/ctrl-text-boxes-image7.png" alt="Screen shot of a Password text box " /><br/> Uma caixa de texto usada para inserir senhas.<br/></td>
</tr>
<tr class="odd">
<td><strong>Saída de dados</strong><br/> Uma caixa de texto de linha única, somente leitura, sempre exibida sem uma borda, usada para exibir cadeias de caracteres curtas. <br/></td>
<td>Diferentemente do texto estático, os dados exibidos usando uma caixa de texto podem ser rolados (útil se os dados forem mais largos do que o controle), selecionados e copiados.<br/> <img src="images/ctrl-text-boxes-image8.png" alt="Screen shot of a text box showing path to a folder " /><br/> Uma caixa de texto somente leitura de linha única usada para exibir dados.<br/></td>
</tr>
<tr class="even">
<td><strong>Saída textual</strong><br/> Uma caixa de texto somente leitura de várias linhas usada para exibir cadeias de caracteres longas. <br/></td>
<td><img src="images/ctrl-text-boxes-image9.png" alt="Screen shot of a Privacy information text box " /><br/> Uma caixa de texto somente leitura usada para exibir dados.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="guidelines"></a>Diretrizes

### <a name="general"></a>Geral

-   **Ao desabilitar uma caixa de texto, também desabilite quaisquer rótulos associados, rótulos de instrução, controles de rotação e botões de comando.**
-   **Use o preenchimento automático para ajudar os usuários a inserir dados que provavelmente serão usados repetidamente**. Os exemplos incluem nomes de usuário, endereços e nomes de arquivo. No entanto, não use o preenchimento automático para caixas de texto que possam conter informações confidenciais, como senhas, PINs, números de cartão de crédito ou informações médicas.
-   **Não faça os usuários rolarem desnecessariamente.** Se você espera que os dados sejam maiores do que a caixa de texto e você pode rapidamente tornar a caixa de texto maior sem prejudicar o layout, dimensione a caixa para eliminar a necessidade de rolagem.

    **Incorreto:**

    ![captura de tela de uma caixa de texto de nome do computador ](images/ctrl-text-boxes-image10.png)

    Neste exemplo, a caixa de texto deve se tornar muito mais demorada para lidar com seus dados.

-   Barras de rolagem:
    -   **Não coloque barras de rolagem horizontais em caixas de texto de várias linhas.** Em vez disso, use a rolagem vertical e a quebra de linha.
    -   **Não coloque nenhuma barra de rolagem em caixas de texto de linha única.**
-   **Para entrada numérica, você pode usar um controle de rotação.** Para entrada textual, use uma lista suspensa ou lista suspensa editável em vez disso.
-   **Não use o recurso de saída automática, exceto para entrada de dados formatados.** A mudança automática de foco pode surpreender os usuários.

### <a name="editable-text-boxes"></a>Caixas de texto editáveis

-   **Limite o tamanho do texto de entrada quando possível.** Por exemplo, se a entrada válida for um número entre 0 e 999, use uma caixa de texto numérica que esteja limitada a três caracteres. Todas as partes de caixas de texto que usam entrada de dados formatados devem ter um tamanho curto e fixo.
-   **Seja flexível com formatos de dados.** Se for provável que os usuários insiram texto usando uma ampla variedade de formatos, tente lidar com todos os mais comuns. Por exemplo, muitos nomes, números e identificadores podem ser inseridos com espaços e pontuação opcionais, e a capitalização geralmente não importa.
-   Se você não puder lidar com os formatos prováveis, exija um formato específico usando a entrada de dados formatados ou indique os formatos válidos no rótulo.

    **Aceitável:**

    ![captura de tela de uma caixa de texto para entrada numérica ](images/ctrl-text-boxes-image11.png)

    Neste exemplo, uma caixa de texto requer entrada em um formato específico.

    **Melhor:**

    ![captura de tela da caixa de texto de entrada de dados formatados ](images/ctrl-text-boxes-image12.png)

    Neste exemplo, o padrão de entrada de dados formatados é usado para exigir um formato específico.

    **Recomendá**

    ![captura de tela de uma caixa de texto irrestrita ](images/ctrl-text-boxes-image13.png)

    Neste exemplo, uma caixa de texto lida com todos os formatos prováveis.

-   Considere a flexibilidade de formato ao escolher o comprimento máximo de entrada. Por exemplo, um número de cartão de crédito válido pode usar até 19 caracteres, portanto, limitar o comprimento a algo mais curto dificultaria a inserção de números usando os formatos mais longos.
-   **Não use o padrão de entrada de dados formatado se for mais provável que os usuários colem dados longos e complexos.** Em vez disso, Reserve o padrão de entrada de dados formatado para situações em que os usuários têm mais probabilidade de digitar os dados.

    ![captura de tela de uma caixa de texto com rótulo: endereço IPv6 ](images/ctrl-text-boxes-image14.png)

    Neste exemplo, o padrão de entrada de dados formatado não é usado, para que os usuários possam colar os endereços IPv6.

-   **Se for mais provável que os usuários reinsiram o valor inteiro, selecione todo o texto no foco de entrada.** Se for mais provável que os usuários editem, coloque o cursor no final do texto.

    ![captura de tela de uma caixa de texto de senha ](images/ctrl-text-boxes-image15.png)

    Neste exemplo, é mais provável que os usuários substituam de editar, portanto, o valor inteiro é selecionado no foco de entrada.

    ![captura de tela de uma caixa de texto para inserir palavras-chave ](images/ctrl-text-boxes-image16.png)

    Neste exemplo, é mais provável que os usuários adicionem palavras-chave do que substituir o texto, portanto, o cursor é colocado no final do texto.

-   **Sempre use uma caixa de texto de várias linhas se os caracteres de nova linha forem de entrada válida.**
-   **Quando a caixa de texto for para um arquivo ou caminho, sempre forneça um botão procurar.**

### <a name="numeric-text-boxes"></a>Caixas de texto numéricas

-   **Escolha a unidade mais conveniente e etiquete as unidades.** Por exemplo, considere usar milliliters em vez de litros (ou vice-versa), percentuais em vez de valores diretos (ou vice-versa) e assim por diante.

    **Correto:**

    ![captura de tela da caixa de texto com litros como unidade ](images/ctrl-text-boxes-image17.png)

    Neste exemplo, a unidade é rotulada, mas requer que os usuários insiram números decimais.

    **Melhor:**

    ![captura de tela da caixa de texto com milliliters como unidade ](images/ctrl-text-boxes-image18.png)

    Neste exemplo, a caixa de texto usa uma unidade mais conveniente.

-   **Use um controle de rotação sempre que for útil.** No entanto, às vezes, os controles de rotação não são práticos, como quando os usuários precisam inserir muitos números grandes. Use controles de rotação quando:
    -   A entrada provavelmente será um número pequeno, normalmente em 100.
    -   É provável que os usuários façam uma pequena alteração em um número existente.
    -   É mais provável que os usuários estejam usando o mouse do que o teclado.
-   **Alinhar texto numérico à direita sempre que:**

    -   Há mais de uma caixa de texto numérica.
    -   As caixas de texto são alinhadas verticalmente.
    -   É provável que os usuários adicionem ou comparem os valores.

    **Correto:**

    ![captura de tela de caixas de texto de despesas (Hotel, etc.) ](images/ctrl-text-boxes-image19.png)

    Neste exemplo, o texto numérico é alinhado à direita para facilitar a comparação de valores.

    **Incorreto:**

    ![captura de tela de caixas de texto para valores RGB ](images/ctrl-text-boxes-image20.png)

    Neste exemplo, o texto numérico está alinhado à esquerda incorretamente.

-   **Sempre alinhar valores monetários à direita.**
-   **Não atribua significados especiais a valores numéricos específicos**, mesmo se esses significados especiais forem usados internamente pelo seu aplicativo. Em vez disso, use caixas de seleção ou botões de opção para uma seleção de usuário explícita.

    **Incorreto:**

    ![captura de tela do rótulo: use-1 para desabilitar o cache ](images/ctrl-text-boxes-image21.png)

    Neste exemplo, o valor-1 tem um significado especial.

    **Correto:**

    ![captura de tela do rótulo da caixa de seleção: Caching ](images/ctrl-text-boxes-image22.png)

    Neste exemplo, uma caixa de seleção torna a opção Explicit.

### <a name="password-and-pin-input"></a>Senha e PIN de entrada

-   **Sempre use o controle comum de senha em vez de criar o seu próprio.** Senhas e PINs exigem tratamento especial para serem manipulados com segurança.

Para obter mais diretrizes e exemplos, consulte [balões](ctrl-balloons.md).

### <a name="textual-output"></a>Saída textual

-   **Considere o uso da cor do sistema de plano de fundo branco para texto grande somente leitura de várias linhas.** Um plano de fundo branco torna o texto mais fácil de ler. Muitos textos em um plano de fundo cinza desencorajam a leitura.

Para obter mais informações sobre cores de plano de fundo, consulte [fontes](vis-fonts.md).

### <a name="data-output"></a>Saída de dados

-   **Não use uma borda para caixas de texto somente leitura de linha única.** A borda é uma pista visual de que o texto é editável.
-   **Não desabilite caixas de texto somente leitura de linha única.** Isso impede que os usuários selecionem e copiem o texto para a área de transferência. Ele também impede que os usuários rolem os dados se excederem o tamanho de seus limites.
-   **Não defina uma parada de tabulação na caixa de texto somente leitura de linha única, a menos que o usuário provavelmente precise rolar ou copiar o texto.**

## <a name="input-validation-and-error-handling"></a>Validação de entrada e tratamento de erro

Como as caixas de texto geralmente não são restritas para aceitar apenas uma entrada válida, talvez seja necessário validar a entrada e lidar com quaisquer problemas. Valide os vários tipos de problemas de entrada da seguinte maneira:

-   Se o usuário inserir um caractere que não é válido, ignore o caractere e exiba um [balão de problema de entrada](ctrl-balloons.md) que explique os caracteres válidos.

    ![captura de tela da caixa de texto da chave do produto](images/ctrl-text-boxes-image23.png)

    Neste exemplo, um balão relata um caractere de entrada incorreto.

-   Se os dados de entrada tiverem um valor ou formato que não é válido, exiba um balão de problema de entrada quando a caixa de texto perder o foco de entrada.
-   Se os dados de entrada estiverem inconsistentes com outros controles na janela, forneça uma mensagem de erro quando a entrada inteira for concluída, por exemplo, quando os usuários clicarem em OK para uma caixa de diálogo modal.

**Não limpe dados de entrada inválidos, a menos que os usuários não possam corrigir erros facilmente.** Isso permite que os usuários corrijam os erros sem começar de novo. Por exemplo, você deve limpar senhas e PINs incorretos, pois os usuários não podem corrigi-los facilmente.

Para obter mais diretrizes e exemplos, consulte [mensagens de erro](mess-error.md) e [balões](ctrl-balloons.md).

## <a name="prompts"></a>Solicitações

Um prompt é um rótulo ou uma instrução curta colocada dentro de uma caixa de texto como seu valor padrão. Ao contrário do texto estático, os prompts desaparecem da tela quando os usuários digitam algo na caixa de texto ou recebem o foco de entrada.

![captura de tela da caixa de texto de aviso com o rótulo: Pesquisar ](images/ctrl-text-boxes-image24.png)

Um prompt típico.

Use um prompt quando:

-   O espaço na tela é um tanto que usar um rótulo ou instrução é indesejável, como em uma barra de ferramentas.
-   O prompt destina-se principalmente à identificação da finalidade da caixa de texto de forma compactada. Elas não devem ser informações cruciais que o usuário precisa ver ao usar a caixa de texto.

Não use prompts apenas para direcionar os usuários para digitar algo ou clicar em botões. Por exemplo, não escreva o texto do prompt que diga inserir um nome de arquivo e, em seguida, clique em enviar.

Ao usar prompts:

-   Desenhe o texto do prompt em cinza itálico e o texto de entrada real em preto normal. O texto do prompt não deve ser confundido com texto real.
-   Mantenha o texto do prompt conciso. Você pode usar fragmentos em vez de frases completas.
-   Use a capitalização com estilo de frase.
-   Não use pontuação final ou reticências.
-   O texto do prompt não deve ser editável e deve desaparecer quando os usuários clicarem na guia ou na caixa de texto.
    -   **Exceção:** Se a caixa de texto tiver o foco de entrada padrão, o prompt será exibido e desaparece quando o usuário começa a digitar.
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

    **Exceção**

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

