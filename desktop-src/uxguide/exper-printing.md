---
title: Impressão (noções básicas de Design)
description: A impressão é a experiência do usuário em papel. É fácil de ignorar, mas é uma parte importante da experiência geral do usuário.
ms.assetid: 26f5a8dc-27b2-4c2d-a05a-f942784c3cf9
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 73dbac58fe1a0b4f8486e3e1f3db43bdfe94c6b0e1475fa063390d23a4186cfd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119817993"
---
# <a name="printing-design-basics"></a>Impressão (noções básicas de Design)

> [!NOTE]
> este guia de design foi criado para o Windows 7 e não foi atualizado para versões mais recentes do Windows. Grande parte da orientação ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais](/windows/uwp/design/).

A impressão é a experiência do usuário em papel. É fácil de ignorar, mas é uma parte importante da experiência geral do usuário.

Neste artigo, a *impressão* refere-se à experiência do usuário em papel, em que a saída é direcionada para o papel em vez da exibição da tela. O *formato amigável para impressoras* refere-se a modificações que o programa pode fazer para exibir a saída de tela, o que o torna mais adequado para a saída de papel.

Apesar da previsão de que a computação resultaria em "escritório sem papel", surpreendentemente, vamos imprimi-lo agora mesmo que nunca. distribuímos cópias de hardware dos baralhos de apresentação da Microsoft PowerPoint, impressamos artigos que descobrimos online, mas desejamos pesquisar mais atentamente mais tarde, imprimemos emails importantes ou retomamos que recebemos em formato eletrônico e assim por diante. Embora seja fácil ignorar a impressão durante a criação de uma interface do usuário, lembre-se de que a impressão é uma parte importante da experiência geral do usuário.

**Observação:** As diretrizes relacionadas a [caixas de diálogo comuns](win-common-dlg.md) são apresentadas em um artigo separado.

## <a name="is-this-the-right-user-interface"></a>Esta é a interface do usuário correta?

Para decidir se o programa precisa dar suporte à impressão, considere estas perguntas:

-   **Que tipo de programa você está projetando?** O tipo de programa é um bom indicador do nível apropriado de suporte à impressão. Os programas de criação, exibição e navegação de documentos e imagens precisam de suporte de impressão excelente, enquanto outros tipos de programas podem precisar apenas de suporte de impressão para um nível menor. (Para obter uma lista de tipos de programa, consulte a seção [padrões de impressão](#printing-patterns) deste artigo.)
-   **O programa é usado em cenários que se beneficiam da saída direta do papel?** Nesse caso, é mais conveniente adicionar suporte de impressão ao seu programa do que exigir que os usuários copiem os dados para outro programa para impressão.

## <a name="design-concepts"></a>Conceitos de design

### <a name="design-your-program-to-eliminate-unnecessary-printing"></a>Projete seu programa para eliminar a impressão desnecessária

Há muitas razões pelas quais os usuários precisam imprimir alguns que são bons, alguns que são menos assim. Os usuários devem imprimir porque desejam, não porque eles devem. Exigir que os usuários imprimam pode ser um sinal de recursos ausentes. por exemplo, nos últimos usuários tinham que imprimir documentos para fazer comentários e sugerir revisões, mas agora os usuários podem fazer essas tarefas diretamente dentro de Microsoft Word documentos. **Examine os cenários do programa que envolvem a impressão e, na melhor medida possível, verifique se a necessidade de impressão é opcional e não o resultado dos recursos ausentes.**

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
-   Selecione o intervalo de páginas, o número de cópias e a colagem.
-   Use ambos os lados do papel.

Seu programa pode exigir opções adicionais, como opções de conteúdo do documento (qual conteúdo imprimir), opções de formato (como imprimir, incluindo qualidade de impressão, tamanhos de imagem, ajuste ao quadro) e opções de cores. Se você precisar fornecer opções adicionais, faça isso estendendo a caixa de diálogo Comum Opções de impressão. Não crie uma caixa de diálogo Imprimir personalizada.

Ao projetar as opções imprimir, considere a experiência ao imprimir vários documentos. É provável que o próximo trabalho de impressão seja muito semelhante ao último trabalho de impressão. Otimizar as configurações padrão para reprints e trabalhos de impressão semelhantes não fazem com que os usuários comecem completamente a cada vez.

### <a name="design-print-preview-for-performance-and-usability"></a>Visualização de impressão de design para desempenho e usabilidade

**Um trabalho de impressão incorreto perde tempo e dinheiro. Para programas de criação de documentos, os usuários devem ser capazes de avaliar os resultados antes de fazer a impressão real.** Uma visualização de impressão deve permitir que os usuários:

-   Avalie margens, quebras de página, orientação de página, headers e rodapés.
-   Navegue por todas as páginas.
-   Imprima diretamente da visualização de impressão.

Alguns documentos complexos (como desenhos CAD de design auxiliado por computador) podem levar muito tempo para \[ \] renderizar. O desempenho da versão prévia é importante, uma visualização de impressão pode se tornar bastante entediante se levar algum tempo para renderizar cada página. **Consequentemente, é melhor ter uma visualização de impressão que renderiza rapidamente e é precisa o suficiente para permitir que os usuários avaliem os resultados da impressão do que ter uma visualização completamente precisa que renderiza lentamente.**

Ao projetar a visualização de impressão, considere toda a tarefa de preparação para impressão. O que os usuários vão procurar? O que eles vão alterar? Os programas de criação de documentos devem fornecer uma visualização de impressão interativa para que os usuários possam ajustar as configurações alteradas com frequência, como margens e quebras de linha na versão prévia.

No entanto, na melhor medida possível, seu programa deve fazer a coisa certa por padrão. Quando necessário, avisar sobre situações de impressão que são improváveis de serem o que o usuário pretendia. Não confie em usuários encontrando problemas usando a visualização de impressão. Por exemplo, suponha que uma planilha tenha muitas colunas para imprimir em uma única página no modo retrato. Embora o programa possa apresentar uma caixa de diálogo de confirmação, uma solução melhor é imprimir automaticamente no modo paisagem.

**Se você fizer apenas cinco coisas...**

1.  Projete uma experiência de impressão apropriada para o tipo de programa.
2.  Revise os cenários do programa que envolvem impressão e, na melhor medida possível, tornar a necessidade de imprimir opcional.
3.  Forneça extensões de impressão úteis personalização da caixa de diálogo Comum imprimir. Não crie uma caixa de diálogo Imprimir personalizada para essa finalidade.
4.  Otimize as opções imprimir para reprints e trabalhos de impressão semelhantes.
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
<td><strong>Criação avançada de documentos</strong><br/> Usado para criar, exibir e imprimir documentos de alto nível. A capacidade de criar impressões de alta qualidade é um dos principais motivos pelos quais o programa existe. Direcionado a usuários especialistas. <br/></td>
<td><strong>Metas do usuário:</strong> Controle detalhado dos resultados perfeitos sobre a saída de impressão.<br/> <strong>Exemplo:</strong> Microsoft Word<br/> <strong>Experiência de impressão recomendada:</strong><br/>
<ul>
<li>Saída otimizada para impressão (WYSIWYG).</li>
<li>Recursos avançados de formatação de documento, com opções para imprimir objetos grandes.</li>
<li>Opções de impressão avançadas, incluindo os rodapés e os rodapés. As opções de impressão relacionadas ao documento são salvas no próprio documento.</li>
<li>Visualizações de impressão rápidas, precisas e poderosas.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Criação intermediária de documentos</strong><br/> Usado para criar e exibir documentos mais complexos. A capacidade de criar impressões de boa qualidade é importante, mas não necessariamente um dos principais motivos pelos quais o programa existe. Direcionado a usuários intermediários. <br/></td>
<td><strong>Metas do usuário:</strong> Bons resultados com esforço mínimo. Algum controle sobre a saída de impressão.<br/> <strong>Exemplos:</strong> A maioria Microsoft Office programas, como Outlook e Excel.<br/> <strong>Experiência de impressão recomendada:</strong><br/>
<ul>
<li>Saída otimizada para impressão (WYSIWYG).</li>
<li>Alguns recursos de formatação de documento, com capacidade de imprimir objetos grandes sem truncamento.</li>
<li>Algumas opções de impressão personalizadas, incluindo os rodapés e os rodapés.</li>
<li>Visualizações precisas e fáceis de usar.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Criação de documento simples</strong><br/> Usado para criar e exibir documentos simples. Direcionado a todos os usuários. <br/></td>
<td><strong>Metas do usuário:</strong> Suporte à impressão básica com opções de impressão padrão. Os usuários esperam bons resultados sem nenhum ajuste.<br/> <strong>Exemplos:</strong> WordPad, Paint.<br/> <strong>Experiência de impressão recomendada:</strong><br/>
<ul>
<li>A saída pode ser otimizada para impressão (WYSIWYG), mas isso não é necessário.</li>
<li>Alguns recursos de formatação de documento, com capacidade de imprimir objetos grandes sem truncamento.</li>
<li>Opções de impressão padrão; as opções de impressão personalizadas são opcionais.</li>
<li>Visualizações simples ou sem impressão.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Visualizadores de documentos</strong><br/> Usado para exibir documentos. Os usuários não podem alterar o conteúdo ou o formato do documento. <br/></td>
<td><strong>Metas do usuário:</strong> Suporte à impressão básica com opções de impressão padrão. Os usuários esperam bons resultados sem nenhum ajuste. Problemas de impressão são tratados automaticamente porque os usuários não podem modificar o documento.<br/> <strong>Exemplo:</strong> Windows Internet Explorer<br/> <strong>Experiência de impressão recomendada:</strong><br/>
<ul>
<li>A saída pode ser otimizada para impressão (WYSIWYG), mas isso não é necessário.</li>
<li>O programa lida automaticamente com quebras de página, elimina páginas em branco, trata objetos grandes e remove telas de fundo e outros elementos de design.</li>
<li>Opções de impressão padrão; as opções de impressão personalizadas são opcionais.</li>
<li>Visualizações simples ou sem impressão.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Utilitários ou aplicativos de linha de negócios</strong><br/> Usado para executar tarefas simples e específicas. Direcionado a todos os usuários. <br/></td>
<td><strong>Metas do usuário:</strong> Capacidade de exportar dados selecionados com eficiência. Os usuários esperam bons resultados sem nenhum ajuste. Geralmente, para esses programas, os usuários ficam muito surpresas em encontrar qualquer suporte de impressão.<br/> <strong>Experiência de impressão recomendada:</strong><br/>
<ul>
<li>O suporte à impressão é opcional dependendo dos cenários com suporte.</li>
<li>A saída pode ser otimizada para impressão (WYSIWYG), mas isso não é necessário.</li>
<li>Alguns recursos de formatação de documento. Pode ser aceitável se objetos grandes são truncados.</li>
<li>Opções de impressão padrão.</li>
<li>Imprimir visualizações opcionais.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="guidelines"></a>Diretrizes

### <a name="general"></a>Geral

-   **Não imprima páginas em branco ou páginas com apenas os rodapés e os rodapés.** No entanto, imprima páginas em branco se os rodapés ou os rodapés contêm números de página e esses números de página podem ser referenciados em outro lugar.
-   **Fazer o spool completo de todos os trabalhos de impressão pendentes antes de desligar um programa.**

### <a name="formatting-pages"></a>Páginas de formatação

-   **Reformate o layout de texto para se ajustar ao tamanho da página de destino.** Nunca truncar texto.
-   Se os usuários não controlarem o formato do documento:
    -   **Manipular automaticamente objetos grandes dimensionando, girando ou dividindo entre páginas.** Para obter mais diretrizes sobre como imprimir objetos grandes, consulte [Objetos superestados.](#oversized-objects)
    -   **Otimize as quebras de página para eliminar páginas em branco e quase em branco.**
    -   **Converta texto claro em uma plano de fundo escuro em texto escuro em uma plano de fundo branco.**
    -   **Remova os backgrounds e outros elementos de design,** especialmente se eles não são adequados para uma impressora em preto e branco.
-   **Se o programa apresentar documentos parciais separados, forneça uma opção de formato amigável para impressora para consolá-los em um único documento para impressão.**
-   **Remover elementos interativos:**
    -   Remova os controles de navegação e os botões de comando.
    -   Certifique-se de que todos os dados estão visíveis sem barras de rolagem.
    -   Substitua os links pelo equivalente de texto.

        **Aceitável:**

        Para obter mais informações, consulte Guia de UX.

        **Otimizado para impressão:**

        Para obter mais informações, consulte Guia de UX ( https://msdn.microsoft.com/windowsvista/uxguide) .

        Neste exemplo, o link é substituído por seu texto equivalente entre parênteses.

    -   Mova informações úteis exibidas ao passar o mouse para em linha.

### <a name="oversized-objects"></a>Objetos sobresstados

Lidar com objetos grandes, como planilhas, gráficos e fotos, é um problema exclusivo da impressão. Escolha uma das seguintes abordagens:

-   **Dimensione o objeto para caber na página.** Essa abordagem funcionará bem se o objeto for apenas um pouco grande demais para imprimir, manter o objeto em uma única página é importante e o objeto ainda é legível quando escalado para baixo.

    ![captura de tela da foto dimensionada para metade de uma página ](images/exper-printing-image3.png)

    Neste exemplo, a imagem grande é dimensionada para caber na página.

-   **Gire a página.** Essa abordagem funciona bem quando algumas páginas são impressas melhor no modo paisagem quando no modo retrato (e vice-versa).

    ![captura de tela da foto paisagem girada para retrato ](images/exper-printing-image4.png)

    Neste exemplo, a imagem grande é girada para se ajustar melhor à página.

-   **Imprima o objeto em várias páginas.** A abordagem funciona bem quando o objeto não pode ser dimensionado ou não deve ser dimensionado e girar a página não ajuda ou não é procurado. Se o objeto tiver limites internos (como os divisores de coluna e linha em uma planilha), divida as páginas nesses limites em vez de dentro do conteúdo. Além disso, repita todos os elementos necessários para entender a página, como legendas ou headers de coluna. Ao dividir um objeto em várias páginas, atribua os números de página na ordem de leitura (da esquerda para a direita, de cima para baixo).

    ![captura de tela de cabeceadas de coluna repetidas na próxima página ](images/exper-printing-image5.png)

    Neste exemplo, a tabela grande é impressa em duas páginas. Os headers de coluna persistem de página em página para facilitar a compreensão rápida.

-   **Truncar o objeto** (imprimindo apenas a parte do objeto ainda visível após o truncamento). Essa abordagem é a solução mais simples de implementar, mas provavelmente é a menos aceitável. Observe também que o truncando nunca é aceitável para texto.

    ![captura de tela da metade da foto larga na página retrato ](images/exper-printing-image6.png)

    Neste exemplo, a imagem grande é truncada.

### <a name="headers-and-footers"></a>Cabeçalhos e rodapés

-   **Forneça os rodapés e os rodapés para programas de criação de documentos avançados e intermediários.** Considere fornecer os rodapés e os rodapés para outros tipos de programas se eles são usados para documentos de várias páginas.
-   **Tornar os rodapés e os rodapés personalizáveis.** Permitir que os usuários definam as partes esquerda, centro e direita.
    -   Para os headers, coloque o nome do documento no lado esquerdo por padrão.
    -   Para rodapés, coloque o documento de direitos autorais ou fonte no lado esquerdo e o número da página no lado direito, por padrão.
-   **Use URLs e caminho de arquivo amigável.** Exibe espaços como espaços, não "%20".

### <a name="print-commands"></a>Comandos de impressão

-   **Para barras de menu e menus de atalho, use o comando Imprimir que exibe a caixa de diálogo Opções de impressão comuns.** Use uma reellipse para indicar que informações adicionais são necessárias.

    ![captura de tela do menu arquivo, comando de impressão selecionado ](images/exper-printing-image7.png)

    Neste exemplo, o comando Imprimir tem reellipses para indicar que ele exibirá a caixa de diálogo Opções de impressão comuns para obter mais informações.

-   **Para barras de ferramentas usadas com uma barra de menus, use um comando Print imediato.** Clicar no botão imprime uma única cópia do documento na impressora padrão. Esses comandos da barra de ferramentas devem ser imediatos. Para indicar que o comando é imediato, coloque a impressora padrão na dica de ferramenta. Os usuários podem acessar o comando Imprimir completo na barra de menus.

    ![captura de tela do ícone de impressora e sua dica de ferramenta ](images/exper-printing-image8.png)

    Neste exemplo, o comando Imprimir em uma barra de ferramentas imprime imediatamente em vez de exibir a caixa de diálogo Comum Opções de impressão. Colocar a impressora padrão na dica de ferramenta fornece um reforço textual de que o usuário está ignorando a caixa de diálogo.

-   **Para barras de ferramentas usadas sem uma barra de menus, use um botão Imprimir divisão.** Clicar no botão imprime uma única cópia do documento na impressora padrão. Clicar na parte de seta do botão descarta um menu com os comandos Imprimir, Imprimir versão prévia e Configuração de página completos.

    ![captura de tela do ícone de impressora no botão dividir ](images/exper-printing-image9.png)

    Neste exemplo, a barra de Windows Internet Explorer de ferramentas usa um controle de botão de divisão para fornecer todos os comandos de impressão.

-   **Para a interface do usuário do comando da faixa de opções, coloque o comando Imprimir no menu do aplicativo.**

    ![captura de tela de comandos colocados verticalmente à esquerda ](images/exper-printing-image10.png)

    Para faixas de opções, o comando Imprimir é acessado usando o menu do aplicativo.

### <a name="print-options"></a>Opções de impressão

-   **Não crie uma caixa de diálogo Opções de impressão personalizadas.** Se você precisa fornecer opções adicionais, estenda a caixa de diálogo Comum Opções de impressão. Não use uma caixa de diálogo separada para opções de impressão adicionais.

**Incorreto:**

![captura de tela da caixa de diálogo opções de impressão personalizadas ](images/exper-printing-image11.png)

Neste exemplo, a Fabrikam usa incorretamente uma caixa de diálogo separada para opções de impressão adicionais.

**Desenvolvedores:** Para obter informações sobre como estender a caixa de diálogo Comum de Impressão, consulte [Estrutura PRINTDLGEX](/windows/win32/api/commdlg/ns-commdlg-printdlgexa).

-   **Ao estender a caixa de diálogo comum Opções de impressão, não duplique os recursos já fornecidos.**
-   **Se os usuários provavelmente manterem as configurações de um trabalho de impressão para o próximo, faça com que essas configurações sejam os padrões.** Para o primeiro trabalho de impressão após a iniciação do programa, use os valores padrão, incluindo a impressora padrão. Para trabalhos de impressão subsequentes na instância [do programa](glossary.md), preserve a última impressora selecionada e o tamanho do papel. Não preserve o número de cópias ou intervalos de páginas, pois elas têm muito menos probabilidade de serem reeseledas posteriormente.
-   **Otimize as configurações removendo as opções que atualmente não se aplicam.** Remova opções inconsistentes com os recursos da impressora ou características selecionadas do documento atual. Por exemplo, um aplicativo de impressão de fotos pode limitar as combinações de tamanho de papel, tipo de papel e qualidade de impressão que dão os melhores resultados, portanto, escolher uma opção de papel de glossário pode remover envelopes dos formatos de papel. Se, por algum motivo, os usuários quiserem ver todas as opções, você poderá fornecer essa capacidade por meio de um controle, como uma caixa de seleção.

**Desenvolvedores:** Para saber como determinar os recursos da impressora selecionada, consulte [Imprimir Esquema](../printdocs/print-schema.md).

-   **Para programas de criação de documentos avançados, salve as opções de impressão relacionadas a documentos dentro do próprio documento.** Para esses programas, as opções de impressão são uma parte integrante do documento.
-   **Para outros tipos de programas, salve as configurações por usuário.**
-   **Considere selecionar uma impressora não padrão para impressão especializada.** Por exemplo, um aplicativo de impressão de fotos sempre pode selecionar a impressora usada pela última vez pelo programa, independentemente da impressora padrão do sistema. Isso pressu que a impressora padrão do sistema provavelmente não seja uma impressora de fotos. Esses programas devem salvar a configuração da última impressora selecionada.
-   **Não bloqueie seu programa durante a detecção de funcionalidades de impressora.** Isso apresenta uma experiência de usuário ruim. Em vez disso, qualquer uma das duas:
    -   Execute a detecção de funcionalidade de impressora em um thread separado.
    -   Tempo decor entre 10 segundos.
    -   Forneça uma caixa de diálogo para permitir que os usuários cancelem.

![captura de tela da caixa de diálogo 'conectando-se a' ](images/exper-printing-image12.png)

Neste exemplo, a caixa de diálogo facilita o cancelamento da detecção de funcionalidades da impressora se o usuário decidir que a tarefa está demorando muito.

### <a name="print-previews"></a>Visualizações de impressão

-   **Forneça um recurso de visualização de impressão sempre que apropriado.** Todos os programas de criação de documentos se beneficiam de visualizações de impressão, mas os usuários não os esperam em programas simples de criação de documentos. Para programas de criação de documentos avançados, considere ter suporte de visualização de impressão diretamente dentro da janela principal do programa.

![captura de tela da página exibida na visualização de impressão ](images/exper-printing-image13.png)

Neste exemplo, o Word tem suporte para visualização de impressão dentro da janela principal do programa.

-   Forneça recursos de visualização de impressão que permitem aos usuários:
    -   Avalie margens, quebras de página, orientação de página, headers e rodapés.
    -   Navegue por todas as páginas.
    -   Imprima diretamente da visualização de impressão.

Considere fornecer uma visualização de impressão interativa para que os usuários possam ajustar as configurações alteradas com frequência, como margens e quebras de linha diretamente na versão prévia.

-   **Fazer com que as páginas de visualização de impressão renderizarem dentro de um segundo.** É melhor ter uma visualização de impressão que renderiza rapidamente e é precisa o suficiente para permitir que os usuários avaliem os resultados da impressão do que ter uma visualização completamente precisa que renderiza lentamente.
-   **Para programas de criação de documentos avançados,** considere estender a caixa de diálogo Imprimir padrão incorporando a funcionalidade de visualização diretamente dentro dela, em vez de criar um diálogo separado para ela.
-   **Forneça um botão óbvio para fechar o modo de visualização.**

![captura de tela do ícone e rótulo de visualização de impressão de fechamento ](images/exper-printing-image14.png)

O modo de Visualização de Impressão no Word tem um comando de visualização de fechamento óbvio.

### <a name="printing-errors"></a>Erros de impressão

**Observação:** Depois que o trabalho de impressão tiver sido em spool para a impressora, Windows será responsável por quaisquer erros subsequentes. Seu programa só precisa lidar com erros que ocorrem antes que o trabalho de impressão seja em spool.

-   **Antes de fazer o spool de um trabalho de impressão, verifique se há possíveis problemas de impressão que o usuário possa corrigir.** Apresente uma confirmação clara e concisa antes de continuar a imprimir. Sempre que possível, ofereça para corrigir o problema automaticamente. Isso pode impedir um desperdício de tempo e dinheiro.

## <a name="text"></a>Texto

-   Para a opção de imprimir em ambos os lados do papel, rotule a opção Imprimir de lado duplo. Não use a frase Duplex Manual.

## <a name="documentation"></a>Documentação

-   Use print, não print out, como um verbo.
-   É aceitável usar printout para se referir ao resultado de um trabalho de impressão.
-   Use a fila de impressão, não a fila da impressora.

