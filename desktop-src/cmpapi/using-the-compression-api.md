---
description: Muitos aplicativos precisam usar compactação e descompactação de dados sem perdas. A API de compactação simplifica isso expondo algoritmos de compactação do Windows por meio de uma API pública.
ms.assetid: D603A7DE-D4A1-4515-9702-B03C81504661
title: Usando a API de compactação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01eff163f4ea1ccf03e1cd4ac9cb16a26afeb265
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089503"
---
# <a name="using-the-compression-api"></a>Usando a API de compactação

Muitos aplicativos precisam usar compactação e descompactação de dados sem perdas. A API de compactação simplifica isso expondo algoritmos de compactação do Windows por meio de uma API pública. Cada algoritmo de compactação tem um conjunto de propriedades que controla seu comportamento. A API de compactação expõe uma interface que permite ao desenvolvedor definir ou consultar os valores dessas propriedades. Todas as propriedades dos algoritmos de compactação com suporte têm valores padrão que representam valores comumente usados dessas propriedades. Se uma propriedade for necessária para compactação e descompactação, os valores padrão serão idênticos, garantindo que valores idênticos sejam usados para compactação e descompactação.

## <a name="selecting-the-compression-algorithm"></a>Selecionando o algoritmo de compactação

Depois que um desenvolvedor decidir que um aplicativo precisa compactar ou descompactar dados, a próxima etapa será escolher um algoritmo de compactação. Isso pode depender de testes para encontrar a melhor combinação de velocidade, taxa de compactação e requisito de memória para um aplicativo específico. A lista a seguir fornece uma comparação relativa dos algoritmos de compactação com suporte no momento pela API de compactação. Nem todas as opções estão disponíveis para todos os algoritmos de compactação, e a comparação é aproximada porque o desempenho pode depender dos dados de entrada.

XPRESS (**algoritmo de compactação \_ \_ Xpress**)

-   Muito rápido com requisitos de recursos baixos
-   Taxa de compactação média
-   Altas velocidades de compactação e descompactação
-   Requisito de memória insuficiente
-   Dá suporte à opção de **\_ nível de classe de informações \_ \_ de compactação** disponível na enumeração de [**\_ \_ classe Compact Information**](/windows/desktop/api/compressapi/ne-compressapi-compress_information_class) . O valor padrão é **(DWORD) 0**. Para alguns dados, o valor **(DWORD) 1** pode melhorar a taxa de compactação com uma velocidade de compactação ligeiramente mais lenta.

XPRESS com codificação Huffman (**compactar \_ algoritmo \_ Xpress \_ Huff**)

-   A taxa de compactação é maior do que o **algoritmo de compactação \_ \_ Xpress**
-   Taxa de compactação média
-   Média para alta compactação e velocidades de descompactação
-   Requisito de memória insuficiente
-   Dá suporte à opção de **\_ nível de classe de informações \_ \_ de compactação** na enumeração de [**\_ \_ classe Compact Information**](/windows/desktop/api/compressapi/ne-compressapi-compress_information_class) . O valor padrão é **(DWORD) 0**. Para alguns dados, o valor **(DWORD) 1** pode melhorar a taxa de compactação com uma velocidade de compactação ligeiramente mais lenta.

MSZIP (**compactar \_ algoritmo \_ MSZIP**)

-   Usa mais recursos do que o **algoritmo de compactação \_ \_ Xpress \_ Huff**
-   Gera um bloco compactado semelhante ao RFC 1951.
-   Taxa de compactação média a alta
-   Velocidade de compactação média e alta velocidade de descompactação
-   Requisito de memória média

LZMS (**compactar \_ algoritmo \_ LZMS**)

-   Bom algoritmo se o tamanho dos dados a serem compactados for mais de 2 MB.
-   Alta taxa de compactação
-   Baixa velocidade de compactação e alta velocidade de descompactação
-   Requisito de memória média a alta
-   Dá suporte à opção de **tamanho de bloco de classe de informações de compactação \_ \_ \_ \_** na enumeração de [**\_ \_ classe Compact Information**](/windows/desktop/api/compressapi/ne-compressapi-compress_information_class) . Um tamanho mínimo de 1 MB é sugerido para obter uma melhor taxa de compactação.

## <a name="deciding-which-compression-api-mode-to-use"></a>Decidindo qual modo de API de compactação usar

Depois que um desenvolvedor seleciona o algoritmo de compactação, a próxima decisão é qual dos dois modos da API de compactação usar: modo de buffer ou modo de bloqueio. O modo de buffer foi desenvolvido para facilitar o uso e é recomendado para a maioria dos casos.

O modo de buffer divide automaticamente o buffer de entrada em blocos de um tamanho que é apropriado para o algoritmo de compactação selecionado. O modo de buffer formata e armazena automaticamente o tamanho do buffer descompactado no buffer compactado. O tamanho do buffer compactado não é salvo automaticamente e o aplicativo precisa salvá-lo para descompactação. Não inclua o sinalizador **compactar \_ RAW** no parâmetro *Algorithm* ao chamar [**createcompactár**](/windows/desktop/api/compressapi/nf-compressapi-createcompressor) e [**CreateDecompressor**](/windows/desktop/api/compressapi/nf-compressapi-createdecompressor) para usar o modo de buffer. Para obter um exemplo de código de um aplicativo de modo de buffer, consulte a seção [usando a API de compactação no modo de buffer](using-the-compression-api-in-buffer-mode.md) .

O modo de bloqueio permite que o desenvolvedor controle o tamanho do bloco, mas requer que mais trabalho seja feito pelo aplicativo. Ao usar o modo de bloco, o aplicativo precisa dividir os dados de entrada em pedaços adequadamente ao compactar e, em seguida, colocar as peças de volta ao serem descompactadas. O modo de bloqueio falhará se o tamanho do buffer de entrada for maior que o tamanho do bloco interno do algoritmo de compactação. O tamanho do bloco interno é 32 KB para MSZIP e 1GB para os algoritmos de compactação do XPRESS. O tamanho do bloco interno para LZMS é configurável até 64 GB com um aumento correspondente no uso de memória. O tamanho do buffer compactado não é salvo automaticamente e o aplicativo também precisa salvá-lo para descompactação. O valor do parâmetro *UncompressedBufferSize* de [**descompactação**](/windows/desktop/api/compressapi/nf-compressapi-decompress) deve ser exatamente igual ao tamanho original dos dados descompactados e não apenas ao tamanho do buffer de saída. Isso significa que o aplicativo deve salvar o tamanho original exato dos dados descompactados, bem como os dados compactados e o tamanho compactado, ao usar o modo de bloqueio. Inclua o sinalizador de **compactação \_ bruta** no parâmetro de *algoritmo* ao chamar o [**createcompacter**](/windows/desktop/api/compressapi/nf-compressapi-createcompressor) e o [**CreateDecompressor**](/windows/desktop/api/compressapi/nf-compressapi-createdecompressor) para usar o modo de bloqueio. Para obter um exemplo de código de um aplicativo de modo de bloco, consulte a seção [usando a API de compactação no modo de bloco](using-the-compression-api-in-block-mode.md) .

## <a name="custom-memory-allocation"></a>Alocação de memória personalizada

Os aplicativos de modo de bloco e de buffer têm a opção de especificar uma rotina de alocação de memória personalizada quando chamam [**Createcompactár**](/windows/desktop/api/compressapi/nf-compressapi-createcompressor) e [**CreateDecompressor**](/windows/desktop/api/compressapi/nf-compressapi-createdecompressor). O parâmetro *AllocationRoutines* especifica a estrutura de [**\_ \_ rotinas de alocação de compactação**](/windows/desktop/api/compressapi/ns-compressapi-compress_allocation_routines) que contém a rotina de alocação de memória. Em seguida, o aplicativo pode definir o tamanho do bloco para o compressor usando [**SetCompressorInformation**](/windows/desktop/api/compressapi/nf-compressapi-setcompressorinformation). Consulte a seção [usando a API de compactação em modo de bloco](using-the-compression-api-in-block-mode.md) para obter um exemplo de uma rotina de alocação personalizada simples.

 

 



