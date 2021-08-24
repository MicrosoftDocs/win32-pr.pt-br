---
title: Fontes
description: Os usuários interagem com texto mais do que com qualquer outro elemento no Microsoft Windows. Segoe UI (pronuncia-se \ 0034; CONSULTE-go \ 0034;) é a fonte do sistema Windows. O tamanho da fonte padrão foi aumentado para 9 pontos.
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
> este guia de design foi criado para o Windows 7 e não foi atualizado para versões mais recentes do Windows. Grande parte da orientação ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais](/windows/uwp/design/).

Os usuários interagem com texto mais do que com qualquer outro elemento no Microsoft Windows. Segoe UI (pronuncia-se "veja-go") é a fonte do sistema Windows. O tamanho da fonte padrão foi aumentado para 9 pontos.

![ilustração do alfabeto na fonte da interface do usuário do amsegoe ](images/vis-fonts-image1.png)

A fonte Segoe UI.

Segoe UI e Segoe não são da mesma fonte. Segoe UI é a fonte Windows destinada a cadeias de caracteres de texto da interface do usuário. Segoe é uma fonte de identidade visual usada pela Microsoft e por parceiros para produzir material para impressão e publicidade.

Segoe UI é um tipo acessível, aberto e amigável e, como resultado, tem melhor legibilidade do que Tahoma, Microsoft Sans Serif e Arial. Ele tem as características de um Humanist Sans Serif: as larguras variadas de suas letras maiúsculas (e/S estreitas, por exemplo, comparadas com Helvetica, em que as larguras são mais semelhantes, bastante amplas); o estresse e o Letterforms de sua letra minúscula; e seu itálico verdadeiro (em vez de um "oblíquo" ou um romano inclinado, como muitos Sans Serif de aparência industrial). A face de tipos destina-se a dar o mesmo efeito visual na tela e na impressão. Ele foi projetado para ser um Humanist Sans Serif sem caracteres fortes ou atrapalhando a peculiaridade.

O Segoe UI é otimizado para ClearType, que é ativado por padrão no Windows. Com o ClearType habilitado, Segoe UI é uma fonte elegante e legível. Sem o ClearType habilitado, Segoe UI é apenas marginalmente aceitável. Esse fator determina quando você deve usar Segoe UI.

Segoe UI inclui caracteres latino, grego, cirílico e árabe. Há novas fontes, também otimizadas para ClearType, criadas para outros conjuntos de caracteres e usos. Isso inclui Meiryo para japonês, Malgun Gothic para coreano, Microsoft JhengHei para chinês (tradicional), Microsoft YaHei para chinês (simplificado), Gisha para Hebraico e Leelawadee para tailandês e as fontes de coleção de ClearType projetadas para uso de documentos.

Meiryo inclui caracteres latinos com base em Verdana. Malgun Gothic, Microsoft JhengHei e Microsoft YaHei usam um Segoe UI personalizado. O uso de versões em itálico dessas fontes não é recomendado. Malgun Gothic, Microsoft JhengHei e Microsoft YaHei são fornecidos apenas em estilos regulares e em negrito, o que significa que caracteres em itálico são sintetizados inclinando os estilos verticais. Embora Meiryo inclua itálico real e negrito em itálico, esses estilos se aplicam somente aos caracteres latinos que os caracteres japoneses permanecem verticais quando o estilo em itálico é aplicado.

Uma variação de Meiryo, chamada UI de Meiryo, é preferida na interface do usuário do comando de [faixas](cmd-ribbons.md) de as.

Para dar suporte a localidades usando esses conjuntos de caracteres, Segoe UI é substituída pelas fontes corretas dependendo de cada localidade durante o processo de [localização](glossary.md) .

para licenciar Segoe UI e outras fontes da Microsoft para distribuição com um programa baseado em Windows, entre em contato com [Monotype](https://www.monotype.com/).

**Observação:** As diretrizes relacionadas ao [estilo e](text-style-tone.md) ao [texto da interface do usuário](text-ui.md) e do Tom são apresentadas em artigos separados.

## <a name="design-concepts"></a>Conceitos de design

### <a name="fonts-typefaces-point-sizes-and-attributes"></a>Fontes, tipos, tamanhos de pontos e atributos

Na tipografia tradicional, uma fonte descreve uma combinação de uma face de tipos, um tamanho de ponto e atributos. Uma face de tipos é a aparência da fonte. Segoe UI, Tahoma, Verdana e Arial são todos os tipos. Tamanho do ponto refere-se ao tamanho da fonte, medido a partir da parte superior dos ascendentes até a parte inferior dos descendentes, menos o espaçamento interno (chamado à esquerda). Um ponto é aproximadamente 1/72 polegadas. Por fim, uma fonte pode ter atributos de negrito ou itálico.

Informalmente, as pessoas geralmente usam a fonte no lugar da face de tipos, como feito neste artigo, mas tecnicamente, Segoe UI é uma face de tipos, não uma fonte. Cada combinação de atributos é uma fonte exclusiva (por exemplo, 9 pontos Segoe UI regular, 10 pontos Segoe UI negrito e assim por diante).

### <a name="serif-and-sans-serif"></a>Serif e Sans Serif

Os tipos de letra são Serif ou sans serif. O serif se refere a pequenas transformações que geralmente finalizam os traços de letras em uma fonte. Um tipo de Sans Serif não tem serifas.

Os leitores geralmente preferem fontes serif usadas como corpo de texto em um documento. As serifas fornecem uma sensação de formalização e elegância a um documento. Para o texto da interface do usuário, a necessidade de uma aparência limpa e a resolução mais baixa dos monitores de computador faz com que os tipos de Sans Serif sejam a melhor opção.

### <a name="contrast"></a>Contraste

O texto é mais fácil de ler quando há uma grande diferença entre a luminância do texto e o plano de fundo. O texto preto em um plano de fundo branco fornece o texto escuro de contraste mais alto em um plano de fundo muito leve também pode fornecer alto contraste. Essa combinação é melhor para as principais superfícies da interface do usuário.

O texto claro em um plano de fundo escuro oferece bom contraste, mas não tão bom quanto o texto escuro em um plano de fundo claro. Essa combinação funciona bem para superfícies de interface do usuário secundárias, como painéis de tarefas do Explorer, que você deseja realçar em relação às superfícies da interface do usuário primária.

**Se você quiser garantir que os usuários leiam o texto, use o texto escuro em um plano de fundo claro.**

### <a name="affordances"></a>Capacidades

O texto pode usar o seguinte [capacidades](glossary.md) para indicar como ele é usado:

-   **Refere.** O ponteiro I-bar ("Text Select") indica que o texto é selecionável, enquanto o ponteiro de seta para a esquerda ("Select normal") indica que o texto não é.
-   **Acento.** Quando o texto tem o foco de entrada, o cursor é a barra vertical piscando que indica o ponto de inserção/seleção em texto selecionável ou editável.
-   **Quadro.** Uma caixa ao contrário do texto que indica que ele é editável. Para reduzir o peso da apresentação, a caixa poderá ser exibida dinamicamente somente quando o texto editável for selecionado.
-   **Cor do primeiro plano.** Cinza-claro indica que o texto está desabilitado. Cores não cinzas, especialmente azuis e roxas, indicam que o texto é um link.
-   **Cor do plano de fundo.** Um plano de fundo cinza claro sugere que o texto é somente leitura, mas na prática, o texto somente leitura pode ter qualquer plano de fundo colorido.

Esses capacidades são combinados pelos seguintes significados:

-   **Edit.** Texto exibido em uma caixa, com um ponteiro de seleção de texto, um cursor (no foco de entrada) e geralmente em um plano de fundo branco.
-   **Somente leitura, selecionável.** Texto com um ponteiro de seleção e um cursor (no foco de entrada).
-   **Somente leitura, não selecionável.** Texto com um ponteiro de seta.
-   **Desabilitado.** Texto cinza claro com um ponteiro de seta, às vezes em um plano de fundo cinza.

Texto somente leitura tradicionalmente tem um plano de fundo cinza, mas não é necessário um plano de fundo cinza. Na verdade, um plano de fundo cinza pode ser indesejável, especialmente para grandes blocos de texto, porque ele sugere que o texto está desabilitado e não incentiva a leitura.

### <a name="accessibility-and-the-system-font-sizes-and-colors"></a>Acessibilidade e a fonte, os tamanhos e as cores do sistema

As diretrizes para tornar o texto acessível aos usuários com deficiências ou deficiências podem ser preparadas para uma regra simples: respeite as configurações do usuário sempre usando a fonte, os tamanhos e as cores do sistema.

**Se você fizer apenas uma coisa...**

Respeite as configurações do usuário sempre usando a fonte, os tamanhos e as cores do sistema.

**Desenvolvedores:** No código, você pode determinar as propriedades de fonte do sistema (incluindo seu tamanho) usando a função de API GetThemeFont. Você pode determinar as cores do sistema usando a função da API GetThemeSysColor.

Como não é possível fazer suposições sobre as configurações de tema do sistema dos usuários, você deve:

-   Sempre baseie suas cores de fonte e planos de fundo fora das cores do tema do sistema. Nunca faça suas próprias cores com base em valores RGB (vermelho, verde e azul) fixos.
-   Sempre corresponder as cores de texto do sistema com suas cores de plano de fundo correspondentes. Por exemplo, se você escolher COLOR \_ STATICTEXT para a cor do texto, você também deverá escolher Color \_ static para a cor do plano de fundo.
-   Sempre crie novas fontes com base em variações de tamanho proporcional da fonte do sistema. Dadas as métricas de fonte do sistema, você pode criar variações em negrito, itálico, maior e menor.

**Uma maneira simples de garantir que o programa respeita as configurações dos usuários é testar usando um tamanho de fonte diferente e um esquema de cores de alto contraste.** Todo o texto deve ser redimensionado e exibido corretamente no esquema de cores escolhido.

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



| Tecnologia de interface do usuário | Versão Windows destino | Fontes para usar e otimizar para |
|--------------------------------------------|-------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows Presentation Foundation<br/> | Tudo<br/>                                        | Use partes de tema do WPF.<br/>                                                                                                                                                                                                                                                                                                                                  |
| Win32 ou WinForms<br/>               | Windows Vista ou posterior<br/>                     | Use a fonte Segoe UI apropriada.<br/>                                                                                                                                                                                                                                                                                                                    |
|                                            | Componentes extensíveis ou pré-Windows Vista<br/> | Para direcionar Windows XP e Windows 2000, use a pseudo-fonte Dlg 2 do MS Shell de 8 pontos, que mapeia para Toma.<br/> Para direcionar versões anteriores do Windows, use a pseudo-fonte Dlg do MS Shell de 8 pontos, que mapeia para o Toma no Windows 2000 e no Windows XP e para o MS Sans Serif no Windows 95, Windows 98, Windows Edition do Windows e Windows NT 4.0.<br/> |



 

-   **Desenvolvedores:**
    -   Para elementos que usam layout fixo (como Windows modelos de caixa de diálogo e WinForms), codifica em código a fonte apropriada da tabela anterior.
    -   Para elementos que usam layout dinâmico (como Windows Presentation Foundation), use as fontes de tema. Use APIs de tema como DrawThemeText para desenhar texto com base no símbolo de tema. Certifique-se de ter uma alternativa com base nas métricas do sistema caso o serviço de tema não seja executado.
-   **Por Segoe UI, use um tamanho de fonte de 9 pontos ou maior.** A Segoe UI fonte é otimizada para esses tamanhos, portanto, evite usar tamanhos menores.
-   **Sempre corresponda às cores do texto do sistema com suas cores de plano de fundo correspondentes.** Por exemplo, se você escolher COLOR STATICTEXT para a cor do texto, também deverá \_ escolher COR ESTÁTICA para a cor da tela de \_ fundo.
-   **Sempre crie novas fontes com base em variações proporcionais da fonte do sistema.** Considerando as métricas de fonte do sistema, você pode criar variações em negrito, itálico, maiores e menores.
-   Exibir grandes blocos de texto somente leitura (como termos de licença) em uma tela de fundo clara em vez de uma tela de fundo cinza. As plano de fundo cinza sugerem que o texto está desabilitado e não recomenda a leitura.
-   **Considere um comprimento máximo de linha de 65 caracteres** para facilitar a leitura do texto. (Os caracteres incluem letras, pontuação e espaços.)

### <a name="attributes"></a>Atributos

-   A maioria dos textos da interface do usuário deve ser simples sem nenhum atributos. Os atributos podem ser usados da seguinte forma:
    -   **Negrito.** Use em rótulos de controle para facilitar a análise do texto. Use com moderação para chamar a atenção para o texto que os usuários devem ler. O uso de negrito demais diminui seu impacto.
    -   **Itálico.** Use para se referir ao texto literalmente em vez de aspas. Use com moderação para enfatizar palavras específicas. Use para [prompts](glossary.md) em [caixas de texto](ctrl-text-boxes.md) e listas de listas [listadas editáveis.](/windows/desktop/uxguide/ctrl-drop)
    -   **Itálico em negrito.** Não use.
    -   **Sublinhar.** Não use, exceto para links. Use itálico em vez disso para ênfase.
-   Nem todas as fontes são suportadas em negrito e itálico, portanto, elas nunca devem ser cruciais para entender o texto.

