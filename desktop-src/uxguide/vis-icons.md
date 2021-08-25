---
title: Ícones (noções básicas de design)
description: Os ícones são representações gráficas de objetos, importantes não apenas por motivos éticos como parte da identidade visual de um programa, mas também por motivos utilitários como uma forma breve de transmitir o significado que os usuários agem quase instantaneamente.
ms.assetid: 6f88cb32-ecfe-4e6e-a41b-31891cf510cf
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: ad788338adc81bd9bc796412eebf4bef87ceca2b7a3855e024702a3e1bb23e49
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119841796"
---
# <a name="icons-design-basics"></a>Ícones (noções básicas de design)

> [!NOTE]
> Este guia de design foi criado para Windows 7 e não foi atualizado para versões mais recentes do Windows. Grande parte das diretrizes ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais.](/windows/uwp/design/)

Os ícones são representações gráficas de objetos, importantes não apenas por motivos éticos como parte da identidade visual de um programa, mas também por motivos utilitários como uma forma breve de transmitir o significado que os usuários agem quase instantaneamente. Windows O Vista apresenta um novo estilo de iconografia que traz um nível mais alto de detalhes e Windows.

**Observação:** Diretrizes [relacionadas a ícones padrão](vis-std-icons.md) são apresentadas em um artigo separado.

## <a name="design-concepts"></a>Conceitos de design

Aero é o nome para a experiência do usuário do Windows Vista, que representa os valores embodiados no design da filosofia, bem como a visão por trás da interface do usuário. Aero significa: authentic, authentic, reflect e open. O Aero tem como objetivo estabelecer um design que seja profissional e belo. A inserção aeroespacial cria uma experiência elegante e de alta qualidade que facilita a produtividade do usuário e até mesmo orienta uma resposta emocional.

Windows Os ícones do Vista diferem Windows ícones no estilo XP das seguintes maneiras:

-   O estilo é mais realista do que ilustrativo, mas não é muito fotorealístico. Os ícones são imagens simbólicas que devem ter uma aparência melhor do que a fotorealística!
-   Os ícones têm um tamanho máximo de 256 x 256 pixels, tornando-os adequados para exibições de alto dpi (pontos por polegada). Esses ícones de alta resolução permitem alta qualidade visual em exibições de lista com ícones grandes.
-   Sempre que os ícones de documento práticos e fixos são substituídos por miniaturas do conteúdo, facilitando a identificação e a identificação de documentos.
-   Os ícones da barra de ferramentas têm menos detalhes e nenhuma perspectiva, para otimizar para tamanhos menores e diferenciação visual.

Ícones bem projetados:

-   Melhorar a comunicação visual do programa.
-   Afetar fortemente a impressão geral dos usuários sobre o design visual do programa e a avaliação de seu ajuste e fim.
-   Melhore a usabilidade tornando programas, objetos e ações mais fáceis de identificar, aprender e encontrar.

As imagens a seguir ilustram o que torna o estilo aero de iconografia no Windows Vista diferente do usado no Windows XP.

![imagens de ícones de bloqueio e chave](images/vis-icons-image1.png)

Os Windows ícones do Vista (o bloqueio e a chave à esquerda) são autenticados, nítidos e detalhados. Elas são renderizadas em vez de desenhadas, mas não são completamente fotorealísticas.

![imagens de ícones de notebook de globo e notebook de livros](images/vis-icons-image2.png)

Os Windows ícones do Vista (os dois à esquerda) são profissionais e belos, com atenção aos detalhes que melhoram a qualidade de produção do ícone.

![imagens de notebook, bloqueio, monitor e papel](images/vis-icons-image3.png)

Esses Windows vista mostram o equilíbrio óptico e a precisão percebida na perspectiva e nos detalhes. Isso permite que eles pareçam grandes ou pequenos, de perto ou de uma distância. Além disso, esse estilo de iconografia funciona para telas de alta resolução.

![imagem de um ícone de roteador sem fio](images/vis-icons-image4.png)![imagem de uma planilha de ícone de papel](images/vis-icons-image5.png)![imagem de um ícone de seta para a direita grande e verde](images/vis-icons-image6.png)

Esses exemplos mostram diferentes tipos de ícones, incluindo um objeto tridimensional em perspectiva, um ícone voltado para a frente (simples) e um ícone de barra de ferramentas.

## <a name="guidelines"></a>Diretrizes

### <a name="perspective"></a>Perspectiva

-   **Ícones no Windows Vista são tridimensionais e mostrados em perspectiva como objetos sólidos ou objetos bidimensionais mostrados diretamente.** Use ícones simples para arquivos e para objetos que são realmente simples, como documentos ou partes de papel.

    ![imagens de computador 3d e papel 2d simples ](images/vis-icons-image7.png)

    Ícones 3D e simples típicos.

-   **Objetos tridimensionais são representados em perspectiva como objetos sólidos, vistos de uma exibição de olho de pássaros com dois pontos de partida.**

    ![imagem do notebook com linhas mostrando a perspectiva](images/vis-icons-image8.png)

    Este exemplo mostra a perspectiva e os pontos de partida típicos de ícones 3D.

-   **Nos tamanhos menores, o mesmo ícone pode mudar de perspectiva para direta.** No tamanho de 16x16 pixels e menor, renderizar ícones diretamente (voltados para a frente). Para ícones maiores, use a perspectiva.

    -   **Exceção:** Os ícones da barra de ferramentas são sempre voltados para a frente, mesmo em tamanhos maiores.

    ![imagem de computador 3d grande e computador 2d pequeno ](images/vis-icons-image9.png)

    Este exemplo mostra como o mesmo ícone é tratado de forma diferente, dependendo do tamanho.

### <a name="light-source"></a>Fonte de luz

-   **A fonte de luz para objetos dentro da grade de perspectiva está acima, ligeiramente à frente e ligeiramente à esquerda do objeto.**
-   **A fonte de luz lança sombras ligeiramente para a parte traseira e direita da base do objeto.**
-   **Todos os raios de luz são paralelos e atingem o objeto ao longo do mesmo ângulo (como o sol).** A meta é ter uma aparência de iluminação uniforme em todos os ícones e efeitos de destaque. Raios de luz paralelos produzem sombras que têm o mesmo comprimento e densidade, fornecendo mais unidade em vários ícones.

### <a name="shadows"></a>Sombras

**Geral**

-   **Use sombras para retirar objetos visualmente da plano de fundo e fazer com que objetos 3D pareçam estar em terra, em vez de flutuação incorretamente no espaço.**
-   **Use um intervalo de opacidade de 30 a 50% para sombras.** Às vezes, um nível diferente de sombra deve ser usado, dependendo da forma ou da cor de um ícone.
-   **Reduza ou reduza a sombra, se necessário, para impedir que ela seja cortada pelo tamanho da caixa de ícone.**
-   **Não use sombras em ícones em tamanhos 24x24 ou menores.**

    ![imagens de ícones 3d com sombras ](images/vis-icons-image10.png)

    Sombras típicas do ícone.

**Ícones simples**

-   **Ícones simples geralmente são usados para ícones de** arquivo e objetos simples do mundo real, como um documento ou um papel.
-   **A iluminação de ícone simples vem do canto superior esquerdo em 130 graus.**
-   **Ícones menores (por exemplo, 16x16 e 32x32) são simplificados para a leitura.** No entanto, se elas contêm uma reflexão dentro do ícone (geralmente simplificada), elas podem ter uma sombra forte. A sombra de soltar varia de 30 a 50% em opacidade.
-   **Os efeitos de camada podem ser usados para ícones simples, mas devem ser comparados com outros ícones simples.** As sombras para objetos variam um pouco, de acordo com o que tem melhor aparência e é mais consistente dentro do conjunto de tamanhos e com os outros ícones no Windows Vista. Em algumas ocasiões, pode até ser necessário modificar as sombras. Isso será especialmente verdadeiro quando objetos são colocados sobre outras pessoas.
-   **Um intervalo sutil de cores pode ser usado para obter o resultado desejado.** As sombras ajudam os objetos a ficar no espaço. A cor afeta o peso percebido da sombra e pode distorcer a imagem se ela for muito pesada.

![captura de tela da caixa de diálogo com a sombra de soltar marcada ](images/vis-icons-image11.png)![captura de tela do ícone de papel com sombra estreita ](images/vis-icons-image12.png)

A opção Drop Shadow na caixa de diálogo Estilo de Camada e uma sombra típica para um ícone simples.

**Intervalos de sombra de ícone simples básicos**



| Característica                              | Intervalo                                                         |
|-------------------------------|----------------------------------------------------------|
| Color<br/>              | Preto<br/>                                         |
| Modo Blend<br/>         | Multiplicar<br/>                                      |
| Opacidade<br/>            | 22 a 50%, dependendo da cor do item<br/> |
| Ângulo<br/>              | 120-130 (usar luz global)<br/>                    |
| Distância<br/>           | 3 para 256x256, variando até 1 para 32x32<br/>    |
| Visualização<br/>             | 0<br/>                                             |
| Tamanho<br/>               | 7 para 256x256, variando para 2 para 32x32<br/>    |



 

**Ícones tridimensionais**

-   Crie sombras para ícones 3D caso a caso, com um esforço para se ajustar em um intervalo de distância de conversão e difusão para totalmente transparente. Crie imagens com um tamanho um pouco menor do que as demandas de tamanho de ícone geral para permitir espaço para uma sombra suspensa (para os tamanhos que exigirão uma). Verifique se a sombra não termina abruptamente na borda do ícone.

![Ilustração da criação de sombras no Photoshop](images/vis_icons_image13.jpeg)

![Ilustração de quatro objetos com sombras variadas](images/vis_icons_image14.jpeg)

Esses exemplos ajudam a demonstrar variações criadas com base na forma e na posição do próprio objeto. Às vezes, a sombra precisa ser difusa ou reduzida para impedir que ela seja cortada pelo tamanho da caixa de ícone.

### <a name="color-and-saturation"></a>Cor e saturação

-   **as cores geralmente são menos saturadas do que eram Windows XP.**
-   **Use gradientes para criar uma imagem de aparência mais realista.**
-   **Embora não haja nenhuma paleta de cores específica para ícones padrão, lembre-se de que eles precisam trabalhar bem juntos em muitos contextos e temas.** Prefira o conjunto padrão de cores; Não Recolorir ícones padrão, como ícones de aviso, pois isso interrompe a capacidade dos usuários de interpretar o significado. Para obter mais diretrizes, consulte [Color](vis-color.md).
-   **Os arquivos de ícone exigem versões de paleta de 8 e de 4 bits também,** para dar suporte à configuração padrão em uma área de trabalho remota. Esses arquivos podem ser criados por meio de um processo em lote, mas devem ser revisados, pois alguns exigirão o retoque para melhor legibilidade.

    ![captura de tela da caixa de diálogo Seletor de cor ](images/vis-icons-image15.png)

    Não há nenhuma restrição de paleta de cores estrita. Somente a saturação completa (parte superior direita) é evitada.

-   Níveis de bits: design de ICO para 32 bits (alfa incluído) + 8 bits + 4 bits (dificando o pixel automaticamente, somente examinar o mais crítico). Somente uma cópia de 32 bits da imagem de pixel 256x256 deve ser incluída e somente a imagem de pixel 256x256 deve ser compactada para manter o tamanho do arquivo inativo. várias ferramentas de ícone oferecem compactação para o Windows Vista.
-   Níveis de bits: barras de ferramentas de 24 bits + alfa (máscara de 1 bit), de 8 bits e de 4 bits.
-   Barras de ferramentas ou arquivos AVI: Use magenta (R255 G0 B255) como a cor de transparência do plano de fundo.

### <a name="size-requirements"></a>Requisitos de tamanho

**Geral**

-   **preste atenção especial aos ícones de alta visibilidade,** como ícones de aplicativos principais, ícones de arquivos que podem aparecer no Windows Explorer e ícones que aparecem no Menu iniciar ou na área de trabalho.
    -   **Ícones de aplicativo e itens do painel de controle:** O conjunto completo inclui 16x16, 32x32, 48x48 e 256x256 (o código é dimensionado entre 32 e 256). O formato de arquivo. ico é necessário. Para o modo clássico, o conjunto completo é 16x16, 24x24, 32x32, 48x48 e 64 x 64.
    -   **Opções de ícone de item de lista:** Use miniaturas dinâmicas ou ícones de arquivo do tipo de arquivo (por exemplo, .doc); conjunto completo.
    -   **Ícones da barra de ferramentas:** 16x16, 24x24, 32x32. Observe que os ícones da barra de ferramentas são sempre simples, e não 3D, mesmo no tamanho de 32x32.
    -   **Ícones de caixa de diálogo e assistente:** 32x32 e 48x48.
    -   **Sobreposições:** Código do Shell de núcleo (por exemplo, um atalho) 10x10 (para 16x16), 16x16 (para 32x32), 24x24 (para 48x48), 128x128 (para 256x256). Observe que alguns deles são ligeiramente menores, mas estão próximos desse tamanho, dependendo da forma e do saldo óptico.
    -   **Área de início rápido:** Os ícones serão reduzidos de 48x48 em sobreposições dinâmicas em Alt + Tab, mas para uma versão mais nítida, adicione um 40x40 ao arquivo. ico.
    -   **Ícones de balão:** 32x32 e 40x40.
    -   **Tamanhos adicionais:** É útil ter disponível como recursos para fazer outros arquivos (por exemplo, anotações, faixas da barra de ferramentas, sobreposições, DPI alto e casos especiais): 128x128, 96x96, 64 x 64, 40x40, 24x24, 22x22, 14x14, 10x10 e 8x8. Você pode usar. ico, .png, .bmp ou outros formatos de arquivo, dependendo do código nessa área.

**Para DPI alto**

-   Windows O Vista tem como alvo 96 dpi e 120 dpi.

As tabelas a seguir mostram exemplos de taxas de dimensionamento aplicadas a dois tamanhos de ícone comuns. Observe que nem todos esses tamanhos devem ser incluídos no arquivo. ico. O código reduzirá os maiores.



| dpi                   | Tamanho do ícone                         | Fator de escala                            |
|--------------------|--------------------------|-----------------------------|
| 96<br/>      | 16x16<br/>         | 1,0 (100%)<br/>       |
| 120<br/>     | 20x20<br/>         | 1,25 (125%)<br/>      |
| 144<br/>     | 24x24<br/>         | 1,5 (150%)<br/>       |
| 192<br/>     | 32x32<br/>         | 2,0 (200%)<br/>       |



 



| dpi                   | Tamanho do ícone                         | Fator de escala                            |
|--------------------|--------------------------|-----------------------------|
| 96<br/>      | 32x32<br/>         | 1,0 (100%)<br/>       |
| 120<br/>     | 40x40<br/>         | 1,25 (125%)<br/>      |
| 144<br/>     | 48 x 48<br/>         | 1,5 (150%)<br/>       |
| 192<br/>     | 64x64<br/>         | 2,0 (200%)<br/>       |



 

**tamanhos de arquivo. ico (Standard)**

![Diagrama que mostra ícones de roteadores de tamanho padrão diferentes.](images/vis-icons-image16.png)

**tamanhos de arquivo. ico (casos especiais)**

![ilustração de ícones de roteador de tamanho diferente ](images/vis-icons-image17.png)

**Anotações e sobreposições**

-   As anotações ficam no canto inferior direito do ícone e devem preencher 25 por cento da área de ícones.
    -   **Exceção:** ícones 16x16 têm anotações 10x10s.
-   Não use mais de uma anotação em um ícone.
-   As sobreposições ficam no canto inferior esquerdo do ícone e devem preencher 25 por cento da área de ícones.
    -   **Exceção:** ícones 16x16 têm sobreposições de 10x10.

### <a name="level-of-detail"></a>Nível de detalhes

-   o tamanho de 16x16 de muitos desses ícones ainda é amplamente usado e, portanto, importante.
-   Os detalhes em um ícone desse tamanho devem mostrar claramente o ponto-chave do ícone.
-   Como um ícone é menor, a transparência e alguns detalhes especiais encontrados em tamanhos maiores devem ser sacrificados para simplificar e chegar ao ponto.
-   Os atributos e as cores devem ser exagerados e usados para enfatizar os principais formulários.

    ![ilustração de um grande e dois dispositivos pequenos ](images/vis-icons-image18.png)

    Em 16x16, o ícone do dispositivo de áudio portátil poderia ser facilmente confundido para um telefone celular, de modo que a parte Ear é um detalhe Visual importante a ser mostrado.

-   Simplesmente reduzir verticalmente do tamanho do 256x256 não funciona.
-   Todos os tamanhos precisam de nível de detalhe relevante; Quanto menor o ícone, mais você precisará exagerar os detalhes de definição.

    ![ilustração de telefones celulares com detalhes claros ](images/vis-icons-image19.png)

    ![ilustração de telefones celulares com detalhes borrados ](images/vis-icons-image20.png)

### <a name="icon-development"></a>Desenvolvimento de ícone

**Criando e produzindo ícones**

-   **Contrate um designer gráfico experiente.** Para grandes elementos gráficos, imagens e ícones funcionam com especialistas. É recomendável ter experiência em ilustrações usando arte vetorial ou programas 3D.
-   **Planeje a série de iterações,** desde os esboços de conceito iniciais até as simulações no contexto, até a análise final da produção e o ajuste e a conclusão de ícones no produto em funcionamento.
-   **A criação de ícones antecipados pode ser cara.** Reunir todos os detalhes e requisitos existentes, como: o conjunto completo de ícones necessários; a função principal e o significado de cada um; famílias ou clusters no conjunto que você deseja que sejam aparentes; requisitos da marca; os nomes de arquivo exatos; formatos de imagem usados em seu código; e requisitos de tamanho. Verifique antecipadamente que você pode aproveitar ao máximo seu tempo com o designer.
-   **Lembre-se de que o designer pode não estar familiarizado com seu produto, portanto, forneça informações funcionais, capturas de tela e seções de especificações, conforme apropriado.**
-   **Planeje geopolítica e análises legais conforme apropriado.**
-   **Mapeie um período de tempo e tenha comunicação regular.**

**Do esboço do conceito para o produto final**

![ilustração do desenvolvimento de esboços de telefones celulares ](images/vis-icons-image21.png)

-   Crie esboços de conceito.
-   Experimente o conceito em tamanhos diferentes.
-   Renderizar em 3D, se necessário.
-   Tamanhos de teste em cores de segundo plano diferentes.
-   Avalie os ícones no contexto da interface do usuário real.
-   Produza o arquivo. ico final ou outros formatos de recursos gráficos.

**Ferramentas**

-   **Lápis e papel:** Ideias de conceito inicial, listadas e esboçadas.
-   **3D Studio máx:** Renderizar objetos 3D em perspectiva.
-   **Adobe Photoshop:** Esboço e iteração, simulação em contexto e finalizar detalhes.
-   **Adobe Illustrator/Macromedia FreeHand:** Esboço e iteração, finalizar detalhes.
-   **Engrenagem de filme gif Gamani:** Produza o arquivo. ico (com compactação, se necessário).
-   **Workshop de ícone de axial:** Produza o arquivo. ico (com compactação, se necessário).
-   Microsoft Visual Studio não dá suporte a ícones do Windows Vista (não há suporte para o canal alfa ou mais de 256 cores).

**Produção**

> [!TIP]
> Siga estas etapas para criar um único arquivo. ico que contenha vários tamanhos de imagem e profundidades de cor.

**Etapa 1: conceituar**

-   Use os conceitos estabelecidos sempre que possível, para garantir a consistência de significados para o ícone e sua relevância para outros usos.
-   Considere como o ícone aparecerá no contexto da interface do usuário e como ele pode funcionar como parte de um conjunto de ícones.
-   Se estiver revisando um ícone existente, considere se a complexidade pode ser reduzida.
-   Considere o impacto cultural de seus elementos gráficos. Evite usar letras, palavras, mãos ou rostos em ícones. Descreve representações de pessoas ou usuários da forma mais genérica possível, se necessário.
-   Se combinar vários objetos em uma única imagem em um ícone, considere como a imagem será dimensionada para tamanhos menores. Use no máximo três objetos em um ícone (dois é preferencial). Para o tamanho de 16x16, considere remover objetos ou simplificar a imagem para melhorar o reconhecimento.
-   não use o sinalizador Windows em ícones.

**Etapa 2: ilustrar**

-   para ilustrar Windows ícones de estilo Aero, use uma ferramenta de vetor, como o Macromedia Freehand ou o Adobe illustrator. Use as características de paleta e estilo conforme descrito anteriormente neste artigo.
-   Ilustrar imagem usando o FreeHand ou o Illustrator. Copie e cole as imagens de vetor no Adobe Photoshop.
-   Faça e use uma camada de modelo no Photoshop para garantir que o trabalho seja feito em regiões quadradas dos tamanhos regulamentados.
-   Crie imagens em um tamanho um pouco menores do que as demandas de tamanho de ícone geral para permitir espaço para uma sombra suspensa (para os tamanhos que exigem uma).
-   Coloque as imagens na parte inferior dos quadrados, para que todos os ícones em um diretório sejam posicionados de forma consistente. Evite cortar sombras.
-   Se você estiver adicionando outro objeto a uma imagem ou série, mantenha o objeto principal em uma posição fixa e coloque imagens planas de tamanho menor em uma posição fixa, como a parte inferior esquerda ou superior direita, dependendo do caso.

**Etapa 3: criar as imagens de 24 bits**

-   Depois de ter colado os tamanhos no Photoshop, verifique a legibilidade das imagens, especialmente em 16x16 e em tamanhos menores. Pode ser necessária a investigar pixels usando porcentagens de cores. A redução da transparência também pode ser necessária. É comum exagerar aspectos em tamanhos menores e também para eliminar aspectos, a fim de se concentrar no ponto principal.
-   Os ícones de 8 bits serão exibidos em qualquer modo de cores inferior a 32 bits e não terão o canal alfa de 8 bits, portanto, eles podem precisar ter suas bordas ou mais limpas porque não há uma suavização (as bordas podem ser denteadas e a imagem pode ser difícil de ler).
-   No Photoshop, duplique a camada de imagem de 24 bits e renomeie a camada para imagens de 4 bits. indexe imagens de 4 bits para a Windows paleta de 16 cores.
-   Limpe as imagens usando apenas as cores da paleta de 16 cores. Os contornos feitos de versões mais escuras ou mais claras das cores do objeto geralmente são preferíveis a cinza ou preto.
-   Se estiver trabalhando em um bitmap, certifique-se de que a cor do plano de fundo não seja usada na própria imagem, pois essa cor será a cor transparente. O magenta (R255 G0 B255) geralmente é usado como a cor de transparência do plano de fundo.

**Etapa 4: criar as imagens de 8 e de 4 bits**

-   Agora que as imagens de 24 bits estão prontas para serem feitas em ícones de 32 bits, as versões de 8 bits precisam ser criadas.
-   Esse é um ótimo momento para testar capturas de tela contextuais. É incrível o que pode ser descoberto exibindo outros ícones ou uma família de ícones no contexto. Essa etapa pode economizar tempo e dinheiro. É muito melhor detectar problemas antes que os arquivos passem pela produção e sejam entregues.
-   Adicione a sombra projetada às imagens em tamanhos que as exigem.
-   Mescle a sombra projetada e as imagens de 24 bits juntas.
-   Crie um novo arquivo do Photoshop para cada tamanho. Copie e cole a imagem apropriada. Salve cada arquivo como um arquivo de .psd.
-   Não mescle a camada de imagem com a camada de plano de fundo. É útil incluir o tamanho e a intensidade de cor no nome do arquivo enquanto estiver funcionando, mas o arquivo pode, em última instância, precisar ser renomeado.

**Etapa 5: criar o arquivo. ico**

-   Escolha o aplicativo que melhor atende às necessidades e às habilidades dos artistas. Lembre-se de que os ícones a serem usados em um produto de remessa devem ser criados em uma ferramenta que tenha sido adquirida ou licenciada. Isso significa que as versões de avaliação não podem ser usadas.
-   os dois produtos listados abaixo foram usados por designers que produziram ícones para Windows Vista, e cada um deles oferece a capacidade de exportar para o Adobe Photoshop CS.
    -   Engrenagem de filme gif Gamani: produzir arquivo. ico
    -   Ícone de axial-Workshop: produzir arquivo. ico
-   Visual Studio não dá suporte a ícones do Windows Vista (não há suporte para o canal alfa ou mais de 256 cores), portanto, seu uso não é recomendado.
-   Os arquivos de ícone (formato. ico) devem conter as versões de 4 e 8 bits, bem como o de 24 bits + alfa.
-   salve os arquivos como um "ícone de Windows (. ico)", independentemente do programa de criação de ícones que você escolher usar.
-   Alguns ativos de iconographic podem realmente ser faixas de bitmap, que também exigem um canal alfa (por exemplo, para barras de ferramentas) ou .png arquivos salvos com transparência. Nem todos são necessariamente. formato ICO; Verifique se há suporte para o formato no código.

**Etapa 6: avaliar**

-   Examine todos os tamanhos.
-   Veja a família em conjunto para avaliar a aparência da família, o equilíbrio óptico e a distinção.
-   Examine no contexto para avaliar os pesos e a visibilidade relativos (certifique-se de que um não seja dominado).
-   Considere os casos que podem não ser usados agora, mas que podem estar em um futuro próximo. Esse ícone pode ser anotado ou ter uma sobreposição?
-   Examine no código.

### <a name="icons-in-the-context-of-list-views-toolbars-and-tree-views"></a>Ícones no contexto de exibições de lista, barras de ferramentas e exibições de árvore

**Modos de exibição de lista**

-   para o Windows Vista, use miniaturas para arquivos que contêm conteúdo que é visualmente distinto em pequena escala, de modo que os usuários possam reconhecer diretamente o arquivo que estão procurando. (Use o Windows interface de programação de aplicativo de miniatura para isso.)

    ![captura de tela do Windows Explorer com ícones de pasta ](images/vis-icons-image22.png)

-   As sobreposições de ícone de aplicativo (não mostradas aqui) em miniaturas ajudam a associação com o aplicativo para o tipo de arquivo, além de mostrar a visualização do arquivo.

**Observação:** Para arquivos sem conteúdo visualmente distinto, não use miniaturas. Em vez disso, use ícones de arquivo simbólico tradicional mostrando a representação de objeto e o aplicativo ou tipo associado.

**Barras de Ferramentas**

-   Os ícones que aparecem em uma barra de ferramentas devem ter um equilíbrio óptico em tamanho, cor e complexidade.
-   Teste possíveis ícones em uma captura de tela contextual para evitar predominância ou desequilíbrios indesejados.
-   O teste em capturas de tela ajuda facilmente a evitar iterações caras no código.
-   Examine também os ícones no código. O movimento e outros fatores podem afetar o sucesso de um ícone; em alguns casos, outras iterações podem ser necessárias.

![captura de tela da barra de ferramentas com ícones e rótulos pequenos ](images/vis-icons-image23.png)

No exemplo acima, o equilíbrio óptico ainda não foi atingido.

![ilustração de ícones em diferentes planos de fundo ](images/vis-icons-image24.png)

Experimente iterações no contexto.

**Modos de exibição de árvore**

-   O equilíbrio óptico é necessário para preservar a hierarquia em um controle de exibição de árvore.
-   Portanto, os ícones que são normalmente usados neste contexto devem ser avaliados lá. Às vezes, um ícone de 16x16 específico deve ser menor porque sua forma tem um predominância óptico sobre outros.
-   A compensação para desequilíbrios ópticos é uma parte importante da produção de ícones de alta qualidade.

![Figura de dois conjuntos de pastas no modo de exibição de árvore ](images/vis-icons-image25.png)

 

