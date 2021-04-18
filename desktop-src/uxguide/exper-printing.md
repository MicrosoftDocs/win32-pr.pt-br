---
title: Impressão (noções básicas de Design)
description: A impressão é a experiência do usuário em papel. É fácil de ignorar, mas é uma parte importante da experiência geral do usuário.
ms.assetid: 26f5a8dc-27b2-4c2d-a05a-f942784c3cf9
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: a98bf29da1169ad43a3b1d16ab52298d62612037
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "104569948"
---
# <a name="printing-design-basics"></a>Impressão (noções básicas de Design)

> [!NOTE]
> Este guia de design foi criado para o Windows 7 e não foi atualizado para versões mais recentes do Windows. Grande parte da orientação ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais](/windows/uwp/design/).

A impressão é a experiência do usuário em papel. É fácil de ignorar, mas é uma parte importante da experiência geral do usuário.

Neste artigo, a *impressão* refere-se à experiência do usuário em papel, em que a saída é direcionada para o papel em vez da exibição da tela. O *formato amigável para impressoras* refere-se a modificações que o programa pode fazer para exibir a saída de tela, o que o torna mais adequado para a saída de papel.

Apesar da previsão de que a computação resultaria em "escritório sem papel", surpreendentemente, vamos imprimi-lo agora mesmo que nunca. Distribuímos cópias rígidas de apresentações de apresentação do Microsoft PowerPoint, imprimimos artigos que descobrimos online, mas desejamos Pesquisar mais atentamente mais tarde, imprimemos emails importantes ou retomamos que recebemos em formato eletrônico e assim por diante. Embora seja fácil ignorar a impressão durante a criação de uma interface do usuário, lembre-se de que a impressão é uma parte importante da experiência geral do usuário.

**Observação:** As diretrizes relacionadas a [caixas de diálogo comuns](win-common-dlg.md) são apresentadas em um artigo separado.

## <a name="is-this-the-right-user-interface"></a>Esta é a interface do usuário correta?

Para decidir se o programa precisa dar suporte à impressão, considere estas perguntas:

-   **Que tipo de programa você está projetando?** O tipo de programa é um bom indicador do nível apropriado de suporte à impressão. Os programas de criação, exibição e navegação de documentos e imagens precisam de suporte de impressão excelente, enquanto outros tipos de programas podem precisar apenas de suporte de impressão para um nível menor. (Para obter uma lista de tipos de programa, consulte a seção [padrões de impressão](#printing-patterns) deste artigo.)
-   **O programa é usado em cenários que se beneficiam da saída direta do papel?** Nesse caso, é mais conveniente adicionar suporte de impressão ao seu programa do que exigir que os usuários copiem os dados para outro programa para impressão.

## <a name="design-concepts"></a>Conceitos de design

### <a name="design-your-program-to-eliminate-unnecessary-printing"></a>Projete seu programa para eliminar a impressão desnecessária

Há muitas razões pelas quais os usuários precisam imprimir alguns que são bons, alguns que são menos assim. Os usuários devem imprimir porque desejam, não porque eles devem. Exigir que os usuários imprimam pode ser um sinal de recursos ausentes. Por exemplo, nos últimos usuários tinham que imprimir documentos para fazer comentários e sugerir revisões, mas agora os usuários podem executar essas tarefas diretamente nos documentos do Microsoft Word. **Examine os cenários do programa que envolvem a impressão e, na melhor medida possível, verifique se a necessidade de impressão é opcional e não o resultado dos recursos ausentes.**

Também vale a pena lembrar que conservar recursos, como papel e tinta, é útil em ambiente e economiza o dinheiro das organizações em longa execução.

### <a name="understand-the-differences-between-screen-display-and-print"></a>Entender as diferenças entre exibição e impressão da tela

Embora haja muitas semelhanças entre a saída de exibição e a impressão, também há muitas diferenças. Saída de impressão:

-   **Tem um DPI alto.** A saída de exibição geralmente é de 96 ou 120 pontos por polegada (DPI), enquanto a saída da impressora geralmente é de 600 dpi ou maior.
-   **Tem diferentes fontes ideais.** Embora fontes bem projetadas funcionem bem para exibição e impressão, as fontes serif são mais legíveis em altas resoluções para grandes quantidades de texto que as fontes de Sans Serif. Assim, grandes quantidades de texto especialmente pretendidas para impressão devem usar uma fonte em serif, enquanto o texto destinado principalmente para exibição deve usar uma fonte sans serif. Para obter mais informações, consulte [fontes](vis-fonts.md) (Segoe UI).
-   **Tem taxa de proporção.** A exibição geralmente tem uma [taxa de proporção](glossary.md) baixa (4:3 ou 5:4), enquanto Print usa uma taxa de proporção alta (8,5:11 ou 1:1.4142 com base nos tamanhos de página padrão). Isso ocorre porque a impressão do [modo retrato](glossary.md) é mais comum do que o [modo paisagem](glossary.md).
-   **Tem páginas.** Consequentemente, saída de impressão:
    -   Tem tamanhos de página padrão. O padrão na Estados Unidos e no Canadá é um documento de 8,5 "X11"; o padrão em qualquer outro lugar é o papel A4.
    -   Tem quebras de página.
    -   Tem margens de página.
    -   Tem cabeçalhos e rodapés.
    -   Tem saída de um ou dois lados.
    -   Pode ter várias cópias.
    -   Pode ser impresso fora de ordem ou seletivamente.
-   **Tem muitas opções.** Os usuários talvez queiram escolher um tamanho de impressora e papel, opções de impressora (como qualidade de impressão, impressão dupla e grampeamento), número de cópias, intervalos de páginas, agrupamento e formato de impressão.
-   **Leva tempo e dinheiro.** Pode levar um tempo significativo para imprimir um documento grande ou uma foto de alta qualidade, e o custo do papel e da tinta aumenta ao longo do tempo. Por outro lado, a saída de exibição é instantânea e, essencialmente, gratuita.
-   **Pode ser preto e branco.** Muitas impressoras hoje são pretas e brancas, enquanto algumas telas são monocromáticas.
-   **Não é interativo.** Os usuários não podem rolar páginas ou controles para ver mais conteúdo. Eles não podem clicar em links ou botões ou focalizar os controles. O conteúdo interativo não tem nenhum valor quando impresso.
-   **Pode ficar sem papel, tinta ou toner ou estar offline.** Consequentemente, a saída de papel precisa de mais tratamento de erros e solução de problemas.

Essas diferenças podem afetar o design de impressão. A criação de uma boa experiência de impressão requer mais do que apenas direcionar a saída do seu programa para a impressora.

### <a name="wysiwyg-and-the-evolving-requirements-of-screen-display"></a>Os requisitos WYSIWYG e em evolução da tela de exibição

Historicamente, o princípio mais fundamental para a experiência do usuário de impressão é conhecido como WYSIWYG ("o que você vê é o que você obtém"). Esse princípio sugere que deve haver uma relação forte entre o que é visto na exibição e o que é impresso. Antes de o WYSIWYG se tornar uma prática padrão, geralmente não havia nenhuma relação entre as versões de exibição e impressão de um documento. Os usuários precisaram imprimir para ver o que o documento realmente parecia no papel. O uso de WYSIWYG foi uma grande melhoria na produtividade, pois a maioria dos programas no momento foi projetada principalmente para criação e impressão de documentos.

Hoje, é comum que os sites da Web otimizem para a exibição, e seu formato amigável de impressora pode parecer muito diferente. Além disso, temos diversos dispositivos de computação (por exemplo, Smart Phones e assistentes pessoais digitais) que muitas vezes precisam de saída otimizadas para pequenas exibições. Embora o WYSIWYG ainda seja a melhor abordagem para os programas de criação de documentos, para outros programas, geralmente faz mais sentido otimizar para uma variedade de dispositivos de destino. Para esses programas, o que você vê em uma exibição de PC pode ser diferente do que você vê em outros monitores de dispositivo, o que pode ser diferente do que você obtém na página impressa.

### <a name="optimize-for-printing"></a>Otimizar para impressão

Os programas que não empregam uma experiência de impressão WYSIWYG estrita ainda podem ser otimizados para impressão das seguintes maneiras:

-   Reformate o layout para o tamanho da página de destino.
-   Forneça visualização de impressão, preferivelmente com opções de personalização fáceis, permitindo que os usuários testem diretamente na caixa de diálogo de impressão (por exemplo, arrastando margens).
-   Se apropriado, forneça uma opção de formato amigável para impressora.
    -   Consolide documentos parciais separados em um único documento.
    -   Remova planos de fundo e outros elementos de design, como anúncios, especialmente se eles não forem adequados para uma impressora em preto e branco.
    -   Remova elementos interativos, como controles de navegação e botões de comando.
    -   Certifique-se de que todos os dados estejam visíveis sem barras de rolagem ou passe o mouse.

        **Versão de exibição:**

        ![captura de tela de relatório otimizado para tela ](images/exper-printing-image1.png)

        **Versão amigável para impressora:**

        ![captura de tela do mesmo relatório otimizado para impressão ](images/exper-printing-image2.png)

        Na versão amigável da impressora, todos os dados ficam visíveis na página impressa e os elementos interativos são removidos.

    -   Substitua os links pelo texto equivalente.

        **Aceitável:**

        Para obter mais informações, consulte Guia do UX.

        **Otimizado para impressão:**

        Para obter mais informações, consulte Guia do UX ( https://msdn.microsoft.com/windowsvista/uxguide) .

-   Converta o texto claro em um plano de fundo escuro em texto escuro em um plano de fundo branco.

### <a name="include-the-right-print-options"></a>Incluir as opções de impressão corretas

A caixa de diálogo opções de impressão comum fornece opções para:

-   Selecione a impressora e o tamanho do papel.
-   Definir propriedades da impressora.
-   Selecione o intervalo de páginas, o número de cópias e o agrupamento.
-   Use ambos os lados do papel.

Seu programa pode exigir opções adicionais, como opções de conteúdo do documento (que conteúdo imprimir), opções de formato (como imprimir, incluindo qualidade de impressão, tamanhos de imagem, ajuste ao quadro) e opções de cores. Se você precisar fornecer opções adicionais, faça isso estendendo a caixa de diálogo opções de impressão comum. Não crie uma caixa de diálogo de impressão personalizada.

Ao criar as opções de impressão, considere a experiência ao imprimir vários documentos. As chances são o próximo trabalho de impressão que será muito semelhante ao último trabalho de impressão. Otimizar as configurações padrão para reimpressões e trabalhos de impressão semelhantes não fazem com que os usuários recomecem completamente a cada vez.

### <a name="design-print-preview-for-performance-and-usability"></a>Visualização de impressão de design para desempenho e usabilidade

**Um trabalho de impressão incorreto desperdiça tempo e dinheiro. Para programas de criação de documentos, os usuários devem ser capazes de avaliar os resultados antes de fazer a impressão real.** Uma visualização de impressão deve permitir que os usuários:

-   Avalie as margens, as quebras de página, a orientação da página, os cabeçalhos e os rodapés.
-   Navegue por todas as páginas.
-   Imprima diretamente da visualização de impressão.

Alguns documentos complexos (como desenhos de CAD de design auxiliados por computador \[ \] ) podem levar muito tempo para serem renderizados. O desempenho da visualização é importante, uma visualização de impressão pode se tornar bastante entediante se levar algum tempo para renderizar cada página. **Consequentemente, é melhor ter uma visualização de impressão que seja processada rapidamente e seja preciso o suficiente para permitir que os usuários avaliem os resultados impressos do que ter uma visualização completamente precisa que se torne lento.**

Ao criar a visualização de impressão, considere toda a tarefa de preparação para impressão. O que os usuários vão procurar? O que eles vão mudar? Os programas de criação de documentos devem fornecer uma visualização de impressão interativa para que os usuários possam ajustar as configurações alteradas com frequência, como margens e quebras de linha na visualização.

No entanto, para a melhor extensão possível, o programa deve fazer a coisa certa por padrão. Quando necessário, avise sobre as situações de impressão que são improváveis de serem as pretendidas pelo usuário. Não confie nos usuários encontrando problemas usando a visualização de impressão. Por exemplo, suponha que uma planilha tenha muitas colunas para imprimir em uma única página no modo retrato. Embora o programa possa apresentar uma caixa de diálogo de confirmação, uma solução melhor é imprimir automaticamente no modo paisagem.

**Se você fizer apenas cinco coisas...**

1.  Crie uma experiência de impressão apropriada para o tipo de programa.
2.  Examine os cenários do programa que envolvem a impressão e, na melhor medida possível, faça a necessidade de imprimir opcional.
3.  Forneça extensões de impressão úteis Personalizando a caixa de diálogo Imprimir comum. Não crie uma caixa de diálogo de impressão personalizada para essa finalidade.
4.  Otimize as opções de impressão para reimpressões e trabalhos de impressão semelhantes.
5.  Forneça um recurso de visualização sempre que apropriado.

## <a name="printing-patterns"></a>Padrões de impressão

O tipo de programa é o principal indicador da experiência de impressão apropriada:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Criação avançada de documentos</strong><br/> Usado para criar, exibir e imprimir documentos de high-end. A capacidade de criar impressões de alta qualidade é uma das principais razões pelas quais o programa existe. Direcionado a usuários avançados. <br/></td>
<td><strong>Objetivos do usuário:</strong> Resultados perfeitos controle detalhado sobre a saída de impressão.<br/> <strong>Exemplo:</strong> Microsoft Word<br/> <strong>Experiência de impressão recomendada:</strong><br/>
<ul>
<li>Saída otimizada para impressão (WYSIWYG).</li>
<li>Recursos avançados de formatação de documentos, com opções para imprimir objetos grandes.</li>
<li>Opções avançadas de impressão, incluindo cabeçalhos e rodapés. As opções de impressão relacionadas a documentos são salvas no próprio documento.</li>
<li>Visualizações de impressão rápidas, precisas e poderosas.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Criação de documento intermediário</strong><br/> Usado para criar e exibir documentos mais complexos. A capacidade de criar impressões de boa qualidade é importante, mas não necessariamente uma das principais razões pelas quais o programa existe. Direcionado a usuários intermediários. <br/></td>
<td><strong>Objetivos do usuário:</strong> Bons resultados com esforço mínimo. Algum controle sobre a saída de impressão.<br/> <strong>Exemplos:</strong> A maioria dos programas Microsoft Office, como o Outlook e o Excel.<br/> <strong>Experiência de impressão recomendada:</strong><br/>
<ul>
<li>Saída otimizada para impressão (WYSIWYG).</li>
<li>Alguns recursos de formatação de documentos, com a capacidade de Imprimir objetos grandes sem truncamento.</li>
<li>Algumas opções de impressão personalizadas, incluindo cabeçalhos e rodapés.</li>
<li>Visualizações de impressão precisas e fáceis de usar.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Criação de documento simples</strong><br/> Usado para criar e exibir documentos simples. Destinado a todos os usuários. <br/></td>
<td><strong>Objetivos do usuário:</strong> Suporte de impressão básica com opções de impressão padrão. Os usuários esperam bons resultados sem qualquer ajuste.<br/> <strong>Exemplos:</strong> WordPad, Paint.<br/> <strong>Experiência de impressão recomendada:</strong><br/>
<ul>
<li>A saída pode ser otimizada para impressão (WYSIWYG), mas isso não é necessário.</li>
<li>Alguns recursos de formatação de documentos, com a capacidade de Imprimir objetos grandes sem truncamento.</li>
<li>Opções de impressão padrão; as opções de impressão personalizadas são opcionais.</li>
<li>Visualização simples ou sem impressão.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Visualizadores de documentos</strong><br/> Usado para exibir documentos. Os usuários não podem alterar o formato ou o conteúdo do documento. <br/></td>
<td><strong>Objetivos do usuário:</strong> Suporte de impressão básica com opções de impressão padrão. Os usuários esperam bons resultados sem qualquer ajuste. Os problemas de impressão são tratados automaticamente porque os usuários não podem modificar o documento.<br/> <strong>Exemplo:</strong> Internet Explorer do Windows<br/> <strong>Experiência de impressão recomendada:</strong><br/>
<ul>
<li>A saída pode ser otimizada para impressão (WYSIWYG), mas isso não é necessário.</li>
<li>O programa manipula automaticamente as quebras de página, elimina páginas em branco, manipula objetos grandes e remove planos de fundo e outros elementos de design.</li>
<li>Opções de impressão padrão; as opções de impressão personalizadas são opcionais.</li>
<li>Visualização simples ou sem impressão.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Utilitários ou aplicativos de linha de negócios</strong><br/> Usado para executar tarefas simples e específicas. Destinado a todos os usuários. <br/></td>
<td><strong>Objetivos do usuário:</strong> Capacidade de exportar dados selecionados com eficiência. Os usuários esperam bons resultados sem qualquer ajuste. Geralmente, para esses programas, os usuários têm uma surpresa agradável para encontrar qualquer suporte à impressão.<br/> <strong>Experiência de impressão recomendada:</strong><br/>
<ul>
<li>O suporte à impressão é opcional, dependendo dos cenários com suporte.</li>
<li>A saída pode ser otimizada para impressão (WYSIWYG), mas isso não é necessário.</li>
<li>Alguns recursos de formatação de documentos. Poderá ser aceitável se os objetos grandes estiverem truncados.</li>
<li>Opções de impressão padrão.</li>
<li>Imprimir visualizações opcionais.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="guidelines"></a>Diretrizes

### <a name="general"></a>Geral

-   **Não imprima páginas em branco ou páginas com apenas cabeçalhos e rodapés.** No entanto, imprima páginas em branco se os cabeçalhos ou rodapés contiverem números de página e esses números de página forem referenciados em outro lugar.
-   **Faça o spool completo de todos os trabalhos de impressão pendentes antes de desligar um programa.**

### <a name="formatting-pages"></a>Formatando páginas

-   **Reformate o layout de texto para ajustá-lo no tamanho da página de destino.** Nunca truncar texto.
-   Se os usuários não controlam o formato do documento:
    -   **Manipule objetos grandes automaticamente dimensionando, girando ou dividindo em páginas.** Para obter mais diretrizes sobre a impressão de objetos grandes, consulte [objetos superdimensionados](#oversized-objects).
    -   **Otimize as quebras de página para eliminar páginas em branco e quase em branco.**
    -   **Converta o texto claro em um plano de fundo escuro em texto escuro em um plano de fundo branco.**
    -   **Remova planos de fundo e outros elementos de design,** especialmente se eles não forem adequados para uma impressora em preto e branco.
-   **Se o seu programa apresentar documentos parciais separados, forneça uma opção de formato amigável para a impressora para consolidá-los em um único documento para impressão.**
-   **Remover elementos interativos:**
    -   Remover controles de navegação e botões de comando.
    -   Verifique se todos os dados estão visíveis sem barras de rolagem.
    -   Substitua os links pelo texto equivalente.

        **Aceitável:**

        Para obter mais informações, consulte Guia do UX.

        **Otimizado para impressão:**

        Para obter mais informações, consulte Guia do UX ( https://msdn.microsoft.com/windowsvista/uxguide) .

        Neste exemplo, o link é substituído por seu texto equivalente entre parênteses.

    -   Mova informações úteis exibidas ao passar o mouse para embutido.

### <a name="oversized-objects"></a>Objetos superdimensionados

Lidar com objetos grandes, como planilhas, gráficos e fotos, é um problema exclusivo para a impressão. Escolha uma das seguintes abordagens:

-   **Dimensione o objeto para caber na página.** Essa abordagem funciona bem se o objeto é apenas um pouco grande para ser impresso, manter o objeto em uma única página é importante e o objeto ainda é legível quando reduzido.

    ![captura de tela da foto dimensionada para a metade de uma página ](images/exper-printing-image3.png)

    Neste exemplo, a imagem grande é dimensionada para caber na página.

-   **Girar a página.** Essa abordagem funciona bem quando algumas páginas são mais impressas no modo paisagem no modo retrato (e vice-versa).

    ![captura de tela da foto em paisagem girada para retrato ](images/exper-printing-image4.png)

    Neste exemplo, a imagem grande é girada para se ajustar melhor à página.

-   **Imprima o objeto em várias páginas.** A abordagem funciona bem quando o objeto não pode ser dimensionado, ou não deve ser dimensionado, e a rotação da página não ajuda ou não é desejada. Se o objeto tiver limites internos (como os divisores de coluna e linha em uma planilha), quebre as páginas nesses limites em vez de dentro do conteúdo. Além disso, repita os elementos necessários para entender a página, como legendas ou cabeçalhos de coluna. Ao dividir um objeto em várias páginas, atribua os números de página na ordem de leitura (da esquerda para a direita, de cima para baixo).

    ![captura de tela de títulos de coluna repetidos na próxima página ](images/exper-printing-image5.png)

    Neste exemplo, a tabela grande é impressa em duas páginas. Os cabeçalhos de coluna persistem da página para a página para facilitar a compreensão rápida.

-   **Truncar o objeto** (imprimindo apenas a parte do objeto ainda fica visível após o truncamento). Essa abordagem é a solução mais simples para implementar, mas provavelmente será a menos aceitável. Observe também que o truncamento nunca é aceitável para texto.

    ![captura de tela da metade da largura da foto na página retrato ](images/exper-printing-image6.png)

    Neste exemplo, a imagem grande está truncada.

### <a name="headers-and-footers"></a>Cabeçalhos e rodapés

-   **Forneça cabeçalhos e rodapés para programas de criação de documentos avançados e intermediários.** Considere fornecer cabeçalhos e rodapés para outros tipos de programas se eles forem usados para documentos com multipáginas.
-   **Tornar os cabeçalhos e os rodapés personalizáveis.** Permitir que os usuários definam as partes esquerda, Central e direita.
    -   Para cabeçalhos, coloque o nome do documento no lado esquerdo por padrão.
    -   Para os rodapés, coloque o documento de direitos autorais ou origem no lado esquerdo e o número da página à direita, por padrão.
-   **Use caminho e URLs de arquivo amigável.** Exibir espaços como espaços, não "%20".

### <a name="print-commands"></a>Comandos de impressão

-   **Para barras de menus e menus de atalho, use o comando Imprimir que exibe a caixa de diálogo opções de impressão comum.** Use uma elipse para indicar que informações adicionais são necessárias.

    ![captura de tela do menu arquivo, comando Imprimir selecionado ](images/exper-printing-image7.png)

    Neste exemplo, o comando Print tem reticências para indicar que ele exibirá a caixa de diálogo opções de impressão comum para obter mais informações.

-   **Para barras de ferramentas usadas com uma barra de menus, use um comando de impressão imediato.** Clicar no botão imprime uma única cópia do documento para a impressora padrão. Esses comandos de barra de ferramentas devem ser imediatos. Para indicar que o comando é imediato, coloque a impressora padrão na dica de ferramenta. Os usuários podem acessar o comando impressão completa na barra de menus.

    ![captura de tela do ícone de impressora e sua dica de ferramenta ](images/exper-printing-image8.png)

    Neste exemplo, o comando Imprimir em uma barra de ferramentas é impresso imediatamente em vez de exibir a caixa de diálogo opções de impressão comum. Colocar a impressora padrão na dica de ferramenta fornece reforço textual que o usuário está ignorando a caixa de diálogo.

-   **Para barras de ferramentas usadas sem uma barra de menus, use um botão Imprimir divisão.** Clicar no botão imprime uma única cópia do documento para a impressora padrão. Clicar na parte de seta do botão remove um menu com os comandos de impressão completa, visualização de impressão e configuração de página.

    ![captura de tela do ícone de impressora no botão de divisão ](images/exper-printing-image9.png)

    Neste exemplo, a barra de ferramentas do Windows Internet Explorer usa um controle de botão de divisão para fornecer todos os comandos de impressão.

-   **Para a interface do usuário do comando da faixa de Ribbon, coloque o comando Imprimir no menu do aplicativo.**

    ![captura de tela de comandos colocados verticalmente à esquerda ](images/exper-printing-image10.png)

    Para as faixas de faixa, o comando Print é acessado usando o menu Application.

### <a name="print-options"></a>Opções de impressão

-   **Não crie uma caixa de diálogo opções de impressão personalizadas.** Se você precisar fornecer opções adicionais, estenda a caixa de diálogo opções de impressão comum. Não use uma caixa de diálogo separada para opções de impressão adicionais.

**Incorreto:**

![captura de tela da caixa de diálogo opções de impressão personalizadas ](images/exper-printing-image11.png)

Neste exemplo, a Fabrikam usa incorretamente uma caixa de diálogo separada para opções de impressão adicionais.

**Desenvolvedores:** Para obter informações sobre como estender a caixa de diálogo Imprimir comum, consulte [estrutura PRINTDLGEX](/windows/win32/api/commdlg/ns-commdlg-printdlgexa).

-   **Ao estender a caixa de diálogo opções de impressão comum, não duplique nenhum recurso já fornecido.**
-   **Se for provável que os usuários mantenham as configurações de um trabalho de impressão para o próximo, torne essas configurações os padrões.** Para o primeiro trabalho de impressão após a inicialização do programa, use os valores padrão standard, incluindo a impressora padrão. Para trabalhos de impressão subsequentes na [instância](glossary.md)do programa, preserve a última impressora selecionada e o tamanho do papel. Não preserve o número de cópias ou intervalos de páginas, pois elas têm muito menos probabilidade de serem remarcadas mais tarde.
-   **Otimize as configurações removendo as opções que não se aplicam atualmente.** Remova as opções que estão inconsistentes com os recursos da impressora selecionada ou características do documento atual. Por exemplo, um aplicativo de impressão de fotos pode limitar as combinações de tamanho de papel, tipo de papel e qualidade de impressão que fornecem os melhores resultados, portanto, escolher uma opção de papel brilhante pode remover envelopes dos formatos de papel. Se, por qualquer motivo, os usuários desejarem ver todas as opções, você poderá fornecer essa capacidade por meio de um controle como uma caixa de seleção.

**Desenvolvedores:** Para saber como determinar os recursos da impressora selecionada, consulte [Imprimir esquema](../printdocs/print-schema.md).

-   **Para programas de criação de documentos avançados, salve as opções de impressão relacionadas ao documento no próprio documento.** Para esses programas, as opções de impressão são parte integrante do documento.
-   **Para outros tipos de programas, salve as configurações em uma base por usuário.**
-   **Considere a seleção de uma impressora não padrão para impressão especializada.** Por exemplo, um aplicativo de impressão de fotos sempre poderia selecionar a impressora usada pela última vez pelo programa, independentemente da impressora padrão do sistema. Isso pressupõe que a impressora padrão do sistema não é provavelmente uma impressora de fotos. Esses programas devem salvar a configuração da última impressora selecionada.
-   **Não bloqueie seu programa ao detectar recursos de impressora.** Isso apresenta uma experiência de usuário ruim. Em vez disso, seja:
    -   Execute a detecção de capacidade da impressora em um thread separado.
    -   Tempo limite após 10 segundos.
    -   Forneça uma caixa de diálogo para permitir que os usuários cancelem.

![captura de tela da caixa de diálogo "conectando-se a" ](images/exper-printing-image12.png)

Neste exemplo, a caixa de diálogo torna fácil cancelar a detecção de capacidade da impressora se o usuário decidir que a tarefa está demorando muito.

### <a name="print-previews"></a>Visualizações de impressão

-   **Forneça um recurso de visualização de impressão sempre que apropriado.** Todos os programas de criação de documentos se beneficiam das visualizações de impressão, mas os usuários não as esperam em programas simples de criação de documentos. Para programas avançados de criação de documentos, considere o suporte à visualização de impressão diretamente na janela principal do programa.

![captura de tela da página exibida na visualização de impressão ](images/exper-printing-image13.png)

Neste exemplo, o Word tem suporte à visualização de impressão na janela principal do programa.

-   Fornecer recursos de visualização de impressão que permitem aos usuários:
    -   Avalie as margens, as quebras de página, a orientação da página, os cabeçalhos e os rodapés.
    -   Navegue por todas as páginas.
    -   Imprima diretamente da visualização de impressão.

Considere fornecer uma visualização de impressão interativa para que os usuários possam ajustar as configurações com frequência alteradas, como margens e quebras de linha diretamente dentro da versão prévia.

-   **Fazer com que as páginas de visualização de impressão sejam renderizadas em um segundo.** É melhor ter uma visualização de impressão que seja renderizada rapidamente e seja preciso o suficiente para permitir que os usuários avaliem os resultados impressos do que para ter uma visualização completamente precisa que se torne lenta.
-   **Para programas avançados de criação de documentos, considere estender a caixa de diálogo de impressão padrão incorporando a funcionalidade de visualização diretamente dentro dela,** em vez de criar uma caixa de diálogo separada para ela.
-   **Forneça um botão óbvio para fechar o modo de visualização.**

![captura de tela do ícone e rótulo de visualização de impressão fechar ](images/exper-printing-image14.png)

O modo de visualização de impressão no Word tem um comando fechar visualização óbvia.

### <a name="printing-errors"></a>Erros de impressão

**Observação:** Depois que o trabalho de impressão tiver sido colocado em spool na impressora, o Windows será responsável por quaisquer erros subsequentes. Seu programa precisa apenas tratar os erros que ocorrem antes que o trabalho de impressão seja colocado em spool.

-   **Antes de colocar em spool um trabalho de impressão, verifique se há possíveis problemas de impressão que o usuário pode corrigir.** Apresente uma confirmação clara e concisa antes de continuar a impressão. Sempre que possível, ofereça para corrigir o problema automaticamente. Isso pode evitar um desperdício de tempo e dinheiro.

## <a name="text"></a>Texto

-   Para a opção de imprimir em ambos os lados do papel, rotule a opção imprimir lado e verso. Não use a frase duplex manual.

## <a name="documentation"></a>Documentação

-   Use imprimir, não imprimir, como um verbo.
-   É aceitável usar a impressão impressa para fazer referência ao resultado de um trabalho de impressão.
-   Use fila de impressão, não fila de impressora.

