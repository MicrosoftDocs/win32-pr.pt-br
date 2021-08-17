---
description: Um bitmap é um dos objetos GDI que podem ser selecionados em um contexto de dispositivo (DC).
ms.assetid: 36afaabc-1334-42d1-8004-7952ce3c119e
title: Sobre bitmaps
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb155a2d96b32303c38438663cb7cc9b893a1560e8f33956ff894d309f055010
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119355506"
---
# <a name="about-bitmaps"></a>Sobre bitmaps

Um bitmap é um dos objetos GDI que podem ser selecionados em um *contexto de dispositivo* (DC). [Contextos de dispositivo](device-contexts.md) são estruturas que definem um conjunto de objetos gráficos e seus atributos associados, além de modos gráficos que afetam a saída. A tabela a seguir descreve os objetos GDI que podem ser selecionados em um contexto de dispositivo.



| Objeto gráfico                         | Descrição                                                                                                                                                                                          |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Bitmaps](bitmaps.md)                 | Cria, manipula (dimensiona, rola, gira e pinta) e armazena imagens como arquivos em um disco.                                                                                                       |
| [Pincéis](brushes.md)                 | Pinta o interior dos polígonos, das reticências e dos caminhos.                                                                                                                                                |
| [Fontes](fonts-and-text.md)            | Desenha texto em exibições de vídeo e outros dispositivos de saída.                                                                                                                                               |
| [Paleta lógica](logical-palette.md) | Uma paleta de cores criada por um aplicativo e associada a um determinado contexto de dispositivo.                                                                                                                |
| [Caminhos](paths.md)                     | Uma ou mais figuras (ou formas) que são preenchidas e/ou contornadas.                                                                                                                                     |
| [Canetas](pens.md)                       | Uma ferramenta de gráficos que um aplicativo usa para desenhar linhas e curvas.                                                                                                                                   |
| [Regiões](regions.md)                 | Um retângulo, polígono ou elipse (ou uma combinação de duas ou mais dessas formas) que pode ser preenchida, pintada, invertida, emoldurada e usada para executar testes de clique (testando o local do cursor). |



 

Da perspectiva de um desenvolvedor, um bitmap consiste em uma coleção de estruturas que especificam ou contêm os seguintes elementos:

-   Um cabeçalho que descreve a resolução do dispositivo no qual o retângulo de pixels foi criado, as dimensões do retângulo, o tamanho da matriz de bits e assim por diante.
-   Uma paleta lógica.
-   Uma matriz de bits que define a relação entre os pixels na imagem de bitmap e as entradas na paleta lógica.

Um tamanho de bitmap está relacionado ao tipo de imagem que ele contém. As imagens de bitmap podem ser monocromáticas ou coloridas. Em uma imagem, cada pixel corresponde a um ou mais bits em um bitmap. Imagens monocromáticas têm uma taxa de 1 bit por pixel (BPP). A geração de imagens coloridas é mais complexa. O número de cores que podem ser exibidas por um bitmap é igual a dois elevado ao número de bits por pixel. Portanto, um bitmap de cor de 256 requer 8 bpp (2 ^ 8 = 256).

Os aplicativos do painel de controle são exemplos de aplicativos que usam bitmaps. Ao selecionar um plano de fundo (ou papel de parede) para sua área de trabalho, você realmente seleciona um bitmap, que o sistema usa para pintar o plano de fundo da área de trabalho. O sistema cria o padrão de plano de fundo selecionado, desenhando repetidamente um padrão de pixel de 32 por 32 na área de trabalho.

A ilustração a seguir mostra a perspectiva do desenvolvedor do bitmap encontrado no arquivo Redbrick.bmp. Ele mostra uma matriz de paleta, um retângulo de pixel de 32 a 32 e a matriz de índice que mapeia as cores da paleta para pixels no retângulo.

![ilustração do retângulo de pixel, matriz de paleta e matriz de índice de redbrick.bmp](images/csbmp-01.png)

No exemplo anterior, o retângulo de pixels foi criado em um dispositivo de vídeo VGA usando uma paleta de 16 cores. Uma paleta de 16 cores requer índices de 4 bits; Portanto, a matriz que mapeia as cores da paleta para as cores de pixel também é composta por índices de 4 bits. (Para obter mais informações sobre paletas de cores lógicas, consulte [cores](colors.md).)

> [!Note]
>
> No bitmap acima, o sistema mapeia índices para pixels começando pela linha de verificação inferior da região retangular e terminando com a linha de varredura superior. Uma *linha de varredura* é uma linha única de pixels adjacentes em uma exibição de vídeo. Por exemplo, a primeira linha da matriz (linha 0) corresponde à linha inferior de pixels, a linha de verificação 31. Isso ocorre porque o bitmap acima é um bitmap independente de dispositivo (DIB) de baixo, um tipo comum de bitmap. No canto superior inferior e em bitmaps dependentes de dispositivo (BDD), o sistema mapeia índices para pixels começando com a linha de varredura superior.

 

Os tópicos a seguir descrevem áreas diferentes de bitmaps.

-   [Classificações de bitmap](bitmap-classifications.md)
-   [Tipos de cabeçalho de bitmap](bitmap-header-types.md)
-   [Extensões JPEG e PNG para estruturas e funções de bitmap específicas](jpeg-and-png-extensions-for-specific-bitmap-functions-and-structures.md)
-   [Bitmaps, contextos de dispositivo e superfícies de desenho](bitmaps--device-contexts--and-drawing-surfaces.md)
-   [Criação de bitmap](bitmap-creation.md)
-   [Rotação de bitmap](bitmap-rotation.md)
-   [Dimensionamento de bitmap](bitmap-scaling.md)
-   [Bitmaps como pincéis](bitmaps-as-brushes.md)
-   [Armazenamento de Bitmap](bitmap-storage.md)
-   [Compactação de bitmap](bitmap-compression.md)
-   [Mesclagem alfa](alpha-blending.md)
-   [Sombreamento suave](smooth-shading.md)
-   [funções de Bitmap habilitadas para ICM](icm-enabled-bitmap-functions.md)

 

 



