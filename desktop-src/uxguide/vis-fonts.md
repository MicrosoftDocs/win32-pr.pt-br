---
title: Fontes
description: Os usuários interagem com texto mais do que com qualquer outro elemento no Microsoft Windows. Segoe UI (pronunciado \ 0034; SEE-go \ 0034;) é a Windows do sistema. O tamanho da fonte padrão foi aumentado para 9 pontos.
ms.assetid: 6d4f669d-d28c-4585-9bc3-ecda44de6df5
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 7ac9f725349433f1cd5f2070b0c80d86acb9d8b3f4d9537cc14375d977283620
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119816445"
---
# <a name="fonts"></a>Fontes

> [!NOTE]
> Este guia de design foi criado para Windows 7 e não foi atualizado para versões mais recentes do Windows. Grande parte das diretrizes ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais.](/windows/uwp/design/)

Os usuários interagem com texto mais do que com qualquer outro elemento no Microsoft Windows. Segoe UI (pronuncia-se "SEE-go") é a Windows do sistema. O tamanho da fonte padrão foi aumentado para 9 pontos.

![ilustração do alfabeto na fonte da interface do usuário do segoe ](images/vis-fonts-image1.png)

A Segoe UI fonte.

Segoe UI e Segoe não são a mesma fonte. Segoe UI é a fonte Windows para cadeias de caracteres de texto da interface do usuário. Segoe é uma fonte de identidade visual usada pela Microsoft e por parceiros para produzir material para impressão e publicidade.

Segoe UI é uma face de tipo acessível, aberta e amigável e, como resultado, tem melhor capacidade de leitura do que Toma, Microsoft Sans Serif e Arial. Ele tem as características de um serif sans humanista: as larguras variáveis de suas maiúsculas (E e S estreitas, por exemplo, em comparação com Helvetica, em que as larguras são mais semelhantes, razoavelmente largas); o estresse e as letras de suas letras minúsculas; e seu verdadeiro itálico (em vez de um "oblique" ou alfaiado, como muitos serifs sans de aparência industrial). A face de tipo deve dar o mesmo efeito visual na tela e na impressão. Ele foi projetado para ser um serif sans humanista sem nenhum caractere forte ou distração.

Segoe UI é otimizado para ClearType, que está on por padrão no Windows. Com ClearType habilitado, Segoe UI é uma fonte elegante e acessível. Sem ClearType habilitado, Segoe UI é apenas marginalmente aceitável. Esse fator determina quando você deve usar Segoe UI.

Segoe UI inclui caracteres latinos, gregos, cirílicos e árabe. Há novas fontes, também otimizadas para ClearType, criadas para outros conjuntos de caracteres e usos. Eles incluem Meiryo para japonês, Malgun Korean para coreano, Microsoft JhengHei para chinês (tradicional), Microsoft YaHei para chinês (simplificado), Gisha para hebraico e Leelawadee para tailandês e as fontes da Coleção ClearType projetadas para uso de documentos.

Meiryo inclui caracteres latinos baseados em Verdana. Malgun Também, Microsoft JhengHei e Microsoft YaHei usam um Segoe UI. O uso de versões itálico dessas fontes não é recomendado. Malgun Também, Microsoft JhengHei e Microsoft YaHei são fornecidos apenas em estilos regulares e em negrito, o que significa que os caracteres itálico são sintetizados com a redução dos estilos de estilo. Embora o Meiryo inclua itálico verdadeiros e itálico em negrito, esses estilos se aplicam somente aos caracteres latinos em que os caracteres japonês permanecem ressíntegros quando o estilo itálico é aplicado.

Uma variação do Meiryo, chamada interface do usuário do Meiryo, é preferencial na interface do usuário do comando [ribbons.](cmd-ribbons.md)

Para dar suporte a localidades que usam esses conjuntos de caracteres, Segoe UI é substituído por fontes corretas, dependendo de cada localidade durante o processo [de localização.](glossary.md)

Para licenciar Segoe UI e outras fontes da Microsoft para distribuição com um programa baseado em Windows, entre em contato com [Monotype](https://www.monotype.com/).

**Observação:** As diretrizes relacionadas [ao estilo e ao tom](text-style-tone.md) e ao texto da interface [do](text-ui.md) usuário são apresentadas em artigos separados.

## <a name="design-concepts"></a>Conceitos de design

### <a name="fonts-typefaces-point-sizes-and-attributes"></a>Fontes, face de tipo, tamanhos de ponto e atributos

Na tipografia tradicional, uma fonte descreve uma combinação de uma face de tipo, um tamanho de ponto e atributos. Uma face de tipo é a aparência da fonte. Segoe UI, Tahoma, Verdana e Arial são todas face de tipo. Tamanho do ponto refere-se ao tamanho da fonte, medido da parte superior dos ascendentes para a parte inferior dos descendentes, menos o espaçamento interno (chamado de à frente). Um ponto é de aproximadamente 1/72 polegada. Por fim, uma fonte pode ter atributos de negrito ou itálico.

Informalmente, as pessoas geralmente usam a fonte no lugar da face de tipo, conforme feito neste artigo, mas tecnicamente, Segoe UI é uma face de tipo, não uma fonte. Cada combinação de atributos é uma fonte exclusiva (por exemplo, 9 pontos Segoe UI regular, 10 pontos Segoe UI negrito e assim por diante).

### <a name="serif-and-sans-serif"></a>Serif e sans serif

As faces de tipo são serif ou sans serif. Serif refere-se a pequenos turnos que geralmente terminam os traços de letras em uma fonte. Uma face de tipo sans serif não tem serifs.

Os leitores geralmente preferem fontes serif usadas como texto do corpo em um documento. Os serifs fornecem uma sensação de formalidade e semelhança para um documento. Para o texto da interface do usuário, a necessidade de uma aparência limpa e a resolução mais baixa de monitores de computador torna o tipo sans serif faces a melhor opção.

### <a name="contrast"></a>Contraste

O texto é mais fácil de ler quando há uma grande diferença entre a luminância do texto e a tela de fundo. O texto preto em uma plano de fundo branco fornece o texto escuro de contraste mais alto em um plano de fundo muito claro também pode fornecer alto contraste. Essa combinação é melhor para superfícies de interface do usuário primárias.

Texto claro em um plano de fundo escuro oferece bom contraste, mas não tão bom quanto texto escuro em uma plano de fundo claro. Essa combinação funciona bem para superfícies de interface do usuário secundárias, como painéis de tarefas do Explorer, que você deseja des enfatizar em relação às superfícies de interface do usuário primárias.

**Se você quiser garantir que os usuários leiam seu texto, use texto escuro em uma plano de fundo claro.**

### <a name="affordances"></a>Affordances

O texto pode usar [as seguintes acessível para](glossary.md) indicar como ele é usado:

-   **Ponteiro.** O ponteiro da barra de I ("seleção de texto") indica que o texto é selecionável, enquanto o ponteiro de seta para a esquerda ("seleção normal") indica que o texto não é.
-   **Cursor.** Quando o texto tem o foco de entrada, o cursor é a barra vertical piscando que indica o ponto de inserção/seleção em texto selecionável ou editável.
-   **Caixa.** Uma caixa em torno do texto que indica que ele é editável. Para reduzir o peso da apresentação, a caixa pode ser exibida dinamicamente somente quando o texto editável é selecionado.
-   **Cor de primeiro plano.** Cinza claro indica que o texto está desabilitado. Cores não cinzas, especialmente azul e roxo, indicam que o texto é um link.
-   **Cor da tela de fundo.** Uma tela de fundo cinza claro sugere fracamente que o texto é somente leitura, mas, na prática, o texto somente leitura pode ter qualquer tela de fundo de cor.

Essas responsabilidades são combinadas para os seguintes significados:

-   **Editável.** Texto exibido em uma caixa, com um ponteiro de seleção de texto, um cursor (no foco de entrada) e, geralmente, em uma tela de fundo branca.
-   **Somente leitura, selecionável.** Texto com um ponteiro de seleção e um cursor (no foco de entrada).
-   **Somente leitura, não selecionável.** Texto com um ponteiro de seta.
-   **Desabilitado.** Texto cinza claro com um ponteiro de seta, às vezes em uma plano de fundo cinza.

O texto somente leitura tradicionalmente tem uma plano de fundo cinza, mas uma plano de fundo cinza não é necessária. Na verdade, uma tela de fundo cinza pode ser indesejável, especialmente para grandes blocos de texto, porque sugere que o texto está desabilitado e não recomenda a leitura.

### <a name="accessibility-and-the-system-font-sizes-and-colors"></a>Acessibilidade e a fonte, tamanhos e cores do sistema

As diretrizes para tornar o texto acessível a usuários com deficiências ou deficiências podem ser resumidas a uma regra simples: Respeitar as configurações do usuário sempre usando a fonte, os tamanhos e as cores do sistema.

**Se você fizer apenas uma coisa...**

Respeitar as configurações do usuário sempre usando a fonte, os tamanhos e as cores do sistema.

**Desenvolvedores:** No código, você pode determinar as propriedades da fonte do sistema (incluindo seu tamanho) usando a função de API GetThemeFont. Você pode determinar as cores do sistema usando a função de API GetThemeSysColor.

Como você não pode fazer suposições sobre as configurações de tema do sistema dos usuários, você deve:

-   Sempre basear as cores da fonte e as plano de fundo das cores do tema do sistema. Nunca faça suas próprias cores com base em valores RGB fixos (vermelho, verde, azul).
-   Sempre corresponda às cores do texto do sistema com suas cores de plano de fundo correspondentes. Por exemplo, se você escolher COLOR STATICTEXT para a cor do texto, também deverá \_ escolher COR ESTÁTICA para a cor da tela de \_ fundo.
-   Sempre crie novas fontes com base em variações proporcionais da fonte do sistema. Considerando as métricas de fonte do sistema, você pode criar variações em negrito, itálico, maiores e menores.

**Uma maneira simples de garantir que seu programa respeita as configurações dos usuários é testar usando um tamanho de fonte diferente e um esquema de cores de alto contraste.** Todo o texto deve ser reessado e exibido corretamente no esquema de cores escolhido.

## <a name="usage-patterns"></a>Padrões de uso

O texto tem vários padrões de uso:



|    Uso                                         |    Descrição                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Texto da barra de título**<br/> Texto na barra de título que identifica a janela.<br/>                                                                                                                                                                | ![exemplo de fonte de texto da barra de título ](images/vis-fonts-image2.png)<br/>                                                                            |
| **Instruções principais**<br/> Texto que explica o que fazer em uma página, janela ou caixa de diálogo. <br/>                                                                                                                                              | ![exemplo de fonte de texto de instruções principais ](images/vis-fonts-image3.png)<br/>                                                                    |
| **Instruções secundárias**<br/> Texto complementar que explica o que fazer em uma página, janela ou caixa de diálogo. <br/>                                                                                                                            | ![exemplo de fonte de texto de instruções secundárias ](images/vis-fonts-image4.png)<br/>                                                               |
| **Texto normal**<br/> Texto comum (somente leitura) exibido em uma interface do usuário. <br/>                                                                                                                                                           | ![exemplo de fonte de texto normal ](images/vis-fonts-image5.png)<br/>                                                                               |
| **Texto enfatizado**<br/> O texto em negrito é usado para facilitar a análise do texto e para chamar a atenção para o texto que os usuários devem ler. O texto itálico é usado para se referir ao texto literalmente (em vez de aspas) e enfatizar palavras específicas. <br/> | ![exemplo de fonte de texto enfatizada ](images/vis-fonts-image6.png)<br/>                                                                           |
| **Texto editável**<br/> O texto que os usuários podem editar é mostrado em uma caixa. para reduzir o peso da apresentação, a caixa pode ser exibida somente quando o texto editável é selecionado. <br/>                                                          | ![exemplo de fonte de texto editável ](images/vis-fonts-image7.png)<br/>                                                                             |
| **Texto desabilitado**<br/> Texto que não se aplica ao contexto atual, como rótulos para controles desabilitados. texto desabilitado indica que os usuários (normalmente) não devem se preocupar com a leitura do texto. <br/>                                           | ![exemplo de fonte de texto desabilitada ](images/vis-fonts-image8.png)<br/>                                                                             |
| **Links**<br/> Texto usado para navegar para outra página, janela ou tópico de ajuda ou iniciar um comando. <br/>                                                                                                                                     | ![exemplo de fonte de texto de link ](images/vis-fonts-image9.png)<br/> ![exemplo de fonte de texto links (foco) ](images/vis-fonts-image10.png)<br/> |
| **Header de grupo**<br/> Texto usado para agrupar itens em uma exibição de lista. <br/>                                                                                                                                                                          | ![exemplo de fonte de texto de header de grupo ](images/vis-fonts-image11.png)<br/>                                                                        |
| **Nome do arquivo**<br/> Texto do nome do arquivo (somente na exibição de conteúdo). <br/>                                                                                                                                                                               | ![exemplo de fonte de texto de nome de arquivo (na exibição de conteúdo) ](images/vis-fonts-image12.png)<br/>                                                         |
| **Texto do documento**<br/> Texto usado em documentos (em vez de texto da interface do usuário). <br/>                                                                                                                                                                  | ![exemplo de fonte de texto do documento ](images/vis-fonts-image13.png)<br/>                                                                            |
| **Títulos de documento**<br/> Texto usado como um título dentro de um documento. <br/>                                                                                                                                                                    | ![exemplo de fonte de texto de títulos de documento ](images/vis-fonts-image14.png)<br/>                                                                   |



 

## <a name="guidelines"></a>Diretrizes

### <a name="fonts-and-colors"></a>Fontes e cores

-   **As fontes e as cores a seguir são padrões para Windows Vista e Windows 7.**



| Padrão | Símbolo de tema | Fonte, Cor |
|-----------------------------------------------------------------------------------------------|-----------------------------|------------------------------------------------------------|
| ![exemplo de fonte de texto da barra de título ](images/vis-fonts-image2.png)<br/>                    | CaptionFont<br/>      | 9 pt. preto ( \# 000000) Segoe UI<br/>                 |
| ![exemplo de fonte de texto de instruções principais ](images/vis-fonts-image3.png)<br/>            | MainInstruction<br/>  | 12 pt. blue ( \# 003399) Segoe UI<br/>                 |
| ![exemplo de fonte de texto de instruções secundárias ](images/vis-fonts-image4.png)<br/>       | Instrução<br/>      | 9 pt. preto ( \# 000000) Segoe UI<br/>                 |
| ![exemplo de fonte de texto normal ](images/vis-fonts-image5.png)<br/>                       | Bodytext<br/>         | 9 pt. preto ( \# 000000) Segoe UI<br/>                 |
| ![exemplo de fonte de texto enfatizada ](images/vis-fonts-image6.png)<br/>                   | Bodytext<br/>         | 9 pt. preto ( \# 000000) Segoe UI, negrito ou itálico<br/> |
| ![exemplo de fonte de texto editável ](images/vis-fonts-image7.png)<br/>                     | Bodytext<br/>         | 9 pt. preto ( \# 000000) Segoe UI, em uma caixa<br/>       |
| ![exemplo de fonte de texto desabilitada ](images/vis-fonts-image8.png)<br/>                     | Desabilitado<br/>         | 9 pt. cinza-escuro \# (323232) Segoe UI<br/>             |
| ![exemplo de fonte de texto de link ](images/vis-fonts-image9.png)<br/>                         | HyperLinkText<br/>    | 9 pt. blue ( \# 0066CC) Segoe UI<br/>                  |
| ![exemplo de fonte de texto links (foco) ](images/vis-fonts-image10.png)<br/>               | Frequente<br/>              | 9 pt. azul-claro ( \# 3399FF) Segoe UI<br/>            |
| ![exemplo de fonte de texto de header de grupo ](images/vis-fonts-image11.png)<br/>                |                             | 11 pt. blue ( \# 003399) Segoe UI<br/>                 |
| ![exemplo de fonte de texto de nome de arquivo (na exibição de conteúdo) ](images/vis-fonts-image12.png)<br/> |                             | 11 pt. preto ( \# 000000) Segoe UI<br/>                |
| ![exemplo de fonte de texto do documento ](images/vis-fonts-image13.png)<br/>                    | (nenhum)<br/>           | 9 pt. black ( \# 000000) Californiabri<br/>                  |
| ![exemplo de fonte de texto de títulos de documento ](images/vis-fonts-image14.png)<br/>           | (nenhum)<br/>           | 17 pt. black ( \# 000000) Californiabri<br/>                 |



 

-   **Escolha fontes e otimize layouts de janela com base na tecnologia de interface do usuário e na versão de destino Windows:**



| Tecnologia de interface do usuário | versão de Windows de destino | Fontes a serem usadas e otimizadas para |
|--------------------------------------------|-------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows Presentation Foundation<br/> | Tudo<br/>                                        | Use as partes do tema do WPF.<br/>                                                                                                                                                                                                                                                                                                                                  |
| Win32 ou WinForms<br/>               | Windows Vista ou posterior<br/>                     | Use a fonte de Segoe UI apropriada.<br/>                                                                                                                                                                                                                                                                                                                    |
|                                            | componentes extensíveis ou pré Windows Vista<br/> | para direcionar Windows XP e Windows 2000, use a pseudo-fonte MS Shell de 8 pontos Dlg 2, que é mapeada para Tahoma.<br/> para direcionar versões anteriores do Windows, use 8 pontos MS Shell Dlg pseudo fonte, que é mapeado para Tahoma em Windows 2000 e Windows XP, e para MS Sans Serif no Windows 95, Windows 98, Windows Millennium Edition e Windows NT 4,0.<br/> |



 

-   **Programa**
    -   para elementos que usam layout fixo (como Windows modelos de diálogo e winforms), codifique a fonte apropriada da tabela anterior.
    -   para elementos que usam layout dinâmico (como Windows Presentation Foundation), use as fontes de tema. Use APIs de tema como DrawThemeText para desenhar texto com base no símbolo de tema. Certifique-se de ter uma alternativa com base nas métricas do sistema caso o serviço tema não esteja em execução.
-   **Por Segoe UI, use um tamanho de fonte de 9 pontos ou maior.** A fonte Segoe UI é otimizada para esses tamanhos, portanto evite usar tamanhos menores.
-   **Sempre corresponder as cores de texto do sistema com suas cores de plano de fundo correspondentes.** Por exemplo, se você escolher COLOR \_ STATICTEXT para a cor do texto, você também deverá escolher Color \_ static para a cor do plano de fundo.
-   **Sempre crie novas fontes com base em variações de tamanho proporcional da fonte do sistema.** Dadas as métricas de fonte do sistema, você pode criar variações em negrito, itálico, maior e menor.
-   Exibe grandes blocos de texto somente leitura (como termos de licença) em um plano de fundo leve em vez de um plano de fundo cinza. Os planos de fundo em cinza sugerem que o texto está desabilitado e não incentiva a leitura.
-   **Considere um comprimento máximo de linha de 65 caracteres** para facilitar a leitura do texto. (Os caracteres incluem letras, pontuação e espaços.)

### <a name="attributes"></a>Atributos

-   A maior parte do texto da interface do usuário deve ser simples sem nenhum atributo. Os atributos podem ser usados da seguinte maneira:
    -   **Aplique.** Use em rótulos de controle para facilitar a análise do texto. Use com moderação para chamar a atenção para que os usuários de texto precisem ler. Usar muito mais negrito diminui seu impacto.
    -   **Colocadas.** Use para fazer referência ao texto literalmente, em vez de aspas. Use com moderação para enfatizar palavras específicas. Use para [prompts](glossary.md) em [caixas de texto](ctrl-text-boxes.md) e [listas suspensas editáveis](/windows/desktop/uxguide/ctrl-drop).
    -   **Negrito itálico.** Não use.
    -   **Aplicar.** Não use, exceto para links. Use itálico em vez de ênfase.
-   Nem todas as fontes dão suporte a negrito e itálico, portanto, elas nunca devem ser cruciais para entender o texto.

