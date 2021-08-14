---
description: A compactação de bloco é uma técnica de compactação de textura para reduzir o tamanho da textura.
ms.assetid: add98d8f-6846-4dd6-b0e2-a4b6e89cbcc5
title: Compactação de bloco (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edf93a9d475b21b54baa59f9324a7f69b043bb0c21787c0c2892bfdbe2f6c66d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118101213"
---
# <a name="block-compression-direct3d-10"></a>Compactação de bloco (Direct3D 10)

A compactação de bloco é uma técnica de compactação de textura para reduzir o tamanho da textura. Quando comparado com uma textura com 32 bits por cor, uma textura compactada em bloco pode ser até 75% menor. Os apps geralmente ganham um aumento no desempenho ao usar a compactação de bloco devido o menor volume de memória.

Mesmo com perdas, a compactação de bloco funciona bem e é recomendada para todas as texturas que são transformadas e filtradas pelo pipeline. Texturas que são mapeadas diretamente na tela (elementos de interface do usuário como ícones e texto) não são uma ótima opção para compactação porque os artefatos são mais perceptíveis.

Uma textura compactada em bloco deve ser criada como um múltiplo do tamanho de 4 em todas as dimensões e não pode ser usada como uma saída do pipeline.

-   [Como o bloqueio de compactação funciona?](#how-does-block-compression-work)
    -   [Armazenando dados descompactados](#storing-uncompressed-data)
    -   [Armazenando dados compactados](#storing-compressed-data)
-   [Usando compactação de bloco](#using-block-compression)
    -   [Tamanho virtual versus tamanho físico](#virtual-size-versus-physical-size)
-   [Algoritmos de compactação](#compression-algorithms)
    -   [BC1](#bc1)
    -   [BC2](#bc2)
    -   [BC3](#bc3)
    -   [BC4](#bc4)
    -   [BC5](#bc5)
-   [Conversão de formato usando o Direct3D 10,1](#format-conversion-using-direct3d-101)
-   [Tópicos relacionados](#related-topics)

## <a name="how-does-block-compression-work"></a>Como o bloqueio de compactação funciona?

A compactação de bloco é uma técnica para reduzir a quantidade de memória necessária para armazenar dados de cor. Armazenando algumas cores no tamanho original e outras cores usando um esquema de codificação, você pode reduzir significativamente a quantidade de memória necessária para armazenar a imagem. Como o hardware decodifica automaticamente os dados compactados, não há nenhuma penalidade de desempenho para o uso de texturas compactadas.

Para ver como funciona a compactação, examine os dois exemplos a seguir. O primeiro exemplo descreve a quantidade de memória usada para armazenar dados não compactados; o segundo exemplo descreve a quantidade de memória usada para armazenar dados compactados.

### <a name="storing-uncompressed-data"></a>Armazenando dados descompactados

A ilustração a seguir representa uma textura de 4 × 4 não compactada. Suponha que cada cor contenha um componente único de cor (vermelho, por exemplo) e é armazenado em um byte de memória.

![ilustração de uma textura 4x4 não compactada](images/d3d10-block-compress-1.png)

Os dados não compactados são dispostos na memória sequencialmente e exigem 16 bytes, conforme mostrado na ilustração a seguir.

![ilustração de dados descompactados na memória sequencial](images/d3d10-block-compress-2.png)

### <a name="storing-compressed-data"></a>Armazenando dados compactados

Agora que você já viu quanta memória uma imagem descompactada utiliza, dê uma olhada na quantidade de memória poupada por uma imagem compactada. O formato de compactação [BC4](#bc4) armazena 2 cores (1 byte cada) e índices de 16 3 bits (48 bits ou 6 bytes) que são usados para interpolar as cores originais na textura, conforme mostrado na ilustração a seguir.

![ilustração do formato de compactação BC4](images/d3d10-block-compress-3.png)

O espaço total obrigatório para armazenar os dados compactados é de 8 bytes, que é uma economia de memória de 50% em relação ao exemplo não compactado. A economia é ainda maior quando mais de um componente de cor é usado.

A economia de memória substancial proporcionada pelo compactação de bloco pode causar um aumento no desempenho. Esse desempenho impacta a qualidade da imagem (devido à interpolação de cores); no entanto, a baixa qualidade geralmente não é perceptível.

A próxima seção mostra como o Direct3D 10 torna mais fácil usar a compactação de bloco em seu aplicativo.

## <a name="using-block-compression"></a>Usando compactação de bloco

Crie uma textura compactada por bloco, assim como uma textura não compactada (consulte [criar uma textura de um arquivo](d3d10-graphics-programming-guide-resources-creating-textures.md)), exceto que você especificar um formato compactado por bloco.


```
loadInfo.Format = DXGI_FORMAT_BC1_UNORM;
D3DX10CreateTextureFromFile(...);
```



Em seguida, crie uma exibição para associar a textura ao pipeline. Como uma textura compactada por bloco pode ser usada somente como uma entrada para um estágio de sombreador, você deseja criar uma exibição de recurso de sombreador chamando [**CreateShaderResourceView**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createshaderresourceview).

Use uma textura compactada em bloco da mesma maneira que você usaria uma textura não compactada. Se seu aplicativo receberá um ponteiro de memória para dados compactados em bloco, você precisa levar em conta a memória preenchimento em uma minimapa que faz com que o tamanho declarado ser diferente do tamanho real.

### <a name="virtual-size-versus-physical-size"></a>Tamanho virtual versus tamanho físico

Se você tiver o código do app que usa um ponteiro de memória para percorrer a memória de um bloco de textura compactado, há uma consideração importante que pode exigir uma modificação no código do seu app. Uma textura compactada em bloco deve ser um múltiplo de 4 em todas as dimensões porque os algoritmos de compactação de bloco operam em blocos de texel de 4 x 4. Isso será um problema para um mipmap cujas dimensões iniciais são divisíveis por 4, mas os níveis subdivididos não são. O diagrama a seguir mostra a diferença na área entre o tamanho virtual (declarado) e o tamanho físico (real) de cada nível de mipmap.

![diagrama de níveis de mipmap não compactados e compactados](images/d3d10-block-compress-pad.png)

O lado esquerdo do diagrama mostra os tamanhos de nível de mipmap que são gerados para uma textura de 60 × 40 não compactada. O tamanho de nível superior é retirado da chamada de API que gera a textura; cada nível subsequente é metade do tamanho do nível anterior. Para uma textura descompactada, não há nenhuma diferença entre o tamanho virtual (declarado) e o tamanho físico (real).

O lado direito do diagrama mostra os tamanhos de nível de mipmap que são gerados para a mesma textura de 60 × 40 com compactação. Observe que o segundo e o terceiro nível possuem preenchimento de memória para gerar os fatores de tamanho 4 em cada nível. Isso é necessário para que os algoritmos possam operar em blocos de 4 × 4 texel. Isso é evidente se você considerar os níveis de mipmap menores que 4 × 4; o tamanho desses níveis muito pequenos de mipmap será arredondado para cima para o fator mais próximo de 4 quando a memória de textura for alocada.

O hardware de amostragem usa o tamanho virtual; quando é feito uma amostragem da textura, o preenchimento de memória é ignorado. Para níveis de mipmap menores que 4 × 4, somente os quatro primeiros texels são usados para um mapa 2 x 2, e apenas o primeiro texel é usado por um bloco 1 × 1. No entanto, não há nenhuma estrutura de API que expõe o tamanho físico (incluindo o preenchimento de memória).

Resumindo, tome cuidado ao usar blocos de memória alinhados ao copiar regiões que contêm dados compactados em bloco. Para fazer isso em um app que obtém um ponteiro de memória, certifique-se de que o ponteiro usa a densidade de superfície para levar em conta o tamanho da memória física.

## <a name="compression-algorithms"></a>Algoritmos de compactação

As técnicas de compactação de bloco no Direct3D dividem os dados de textura descompactados em blocos de 4 × 4, compactam cada bloco e armazenam os dados. Por esse motivo, as texturas a serem compactadas devem ter dimensões de textura que são múltiplas de 4.

![diagrama de compactação de bloco](images/d3d10-compression-1.png)

O diagrama acima mostra uma textura particionada em blocos de texel. O primeiro bloco mostra o layout de 16 texels rotulado como a-p, mas todos os blocos tem a mesma organização dos dados.

O Direct3D implementa vários esquemas de compactação, cada um implementa um equilíbrio diferente entre os vários componentes armazenados, o número de bits por componente e a quantidade de memória consumida. Use esta tabela para ajudar a escolher o formato que funciona melhor com o tipo de dados e a resolução de dados que melhor se adapta ao seu app.



| Dados de origem                     | Resolução de compactação de dados (em bits) | Escolha esse formato de compactação |
|---------------------------------|---------------------------------------|--------------------------------|
| Alfa e cor de três componentes | Cor (5:6:5), alfa (1) ou nenhum alfa  | BC1                            |
| Alfa e cor de três componentes | Cor (5:6:5), alfa (4)              | [BC2](#bc2)                    |
| Alfa e cor de três componentes | Cor (5:6:5), alfa (8)              | [BC3](#bc3)                    |
| Cor de um componente             | Um componente (8)                     | [BC4](#bc4)                    |
| Cor de dois componentes             | Dois componentes (8:8)                  | [BC5](#bc5)                    |



 

### <a name="bc1"></a>BC1

Use o primeiro formato de compactação de bloco (BC1) (o \_ formato dxgi \_ BC1 não \_ tipado, \_ formato DXGI \_ BC1 \_ UNORM ou dxgi \_ BC1 \_ UNORM \_ sRGB) para armazenar dados de três componentes coloridos usando uma cor 5:6:5 (5 bits vermelho, 6 bits verde, 5 bits azul). Isso vale até mesmo quando os dados também contêm alfa de 1 bit. Pressupondo uma textura de 4 × 4 usando o formato de dados maior possível, o formato BC1 reduz a memória necessária de 48 bytes (16 cores × 3 componentes/cor × 1 byte/componente) para 8 bytes de memória.

O algoritmo funciona em blocos de texels de 4 × 4. Em vez de armazenar 16 cores, o algoritmo salva 2 cores de referência (cor \_ 0 e cor \_ 1) e índices de cores de 16 2 bits (bloqueia a – p), conforme mostrado no diagrama a seguir.

![diagrama do layout da compactação BC1](images/d3d10-compression-bc1.png)

Os índices de cor (a–p) são usados para procurar as cores originais em uma tabela de cores. A tabela de cores contém 4 cores. As duas primeiras cores — cor \_ 0 e cor \_ 1 — são as cores mínimas e máximas. As outras duas cores, cor \_ 2 e cor \_ 3, são cores intermediárias calculadas com interpolação linear.


```
color_2 = 2/3*color_0 + 1/3*color_1
color_3 = 1/3*color_0 + 2/3*color_1
```



As quatro cores recebem valores de índice de 2 bits que serão salvos em blocos a–p.


```
color_0 = 00
color_1 = 01
color_2 = 10
color_3 = 11
```



Por fim, todas as cores nos blocos a–p são comparadas com as quatro cores na tabela de cores e o índice para a cor mais próxima é armazenado nos blocos de 2 bits.

Esse algoritmo se compromete a dados que também contêm alfa de 1 bit. A única diferença é que a cor \_ 3 é definida como 0 (que representa uma cor transparente) e \_ a cor 2 é uma mistura linear de cor \_ 0 e cor \_ 1.


```
color_2 = 1/2*color_0 + 1/2*color_1;
color_3 = 0;
```





<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Diferenças entre o Direct3D 9 e o Direct3D 10:<br/> Esse formato existe tanto no Direct3D 9 quanto no 10.<br/>
<ul>
<li>No Direct3D 9, o formato BC1 é chamado de D3DFMT_DXT1.</li>
<li>No Direct3D 10, o formato BC1 é representado por DXGI_FORMAT_BC1_UNORM ou DXGI_FORMAT_BC1_UNORM_SRGB.</li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="bc2"></a>BC2

Use o formato BC2 (um \_ formato dxgi \_ BC2 sem \_ tipo, \_ formato DXGI \_ BC2 \_ UNORM ou dxgi \_ BC2 \_ UNORM \_ sRGB) para armazenar dados que contêm dados de cor e alfa com coerência baixa (use [BC3](#bc3) para dados alfa altamente coerentes). O formato BC2 armazena dados RGB como uma cor 5:6:5 (5 bits de vermelho, 6 bits de verde, 5 bits de azul) e alfa como um valor de 4 bits separado. Pressupondo uma textura de 4 × 4 usando o formato de dados maior possível, essa técnica de compactação reduz a memória necessária de 64 bytes (16 cores × 4 componentes/cor × 1 byte/componente) para 16 bytes de memória.

O formato BC2 armazena cores com o mesmo número de bits e dados de layout como o formato [BC1](#bc1), no entanto, o BC2 requer 64-bits adicionais de memória para armazenar os dados alfa, conforme mostrado no diagrama a seguir.

![diagrama do layout da compactação BC2](images/d3d10-compression-bc2.png)

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Diferenças entre o Direct3D 9 e o Direct3D 10:<br/> Esse formato existe tanto no Direct3D 9 quanto no 10.<br/>
<ul>
<li>No Direct3D 9, o formato BC2 é chamado de D3DFMT_DXT2 e D3DFMT_DXT3.</li>
<li>No Direct3D 10, o formato BC2 é representado por DXGI_FORMAT_BC2_UNORM ou DXGI_FORMAT_BC2_UNORM_SRGB.</li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="bc3"></a>BC3

Use o formato BC3 (um \_ formato dxgi \_ BC3 sem \_ tipo, \_ formato DXGI \_ BC3 \_ UNORM ou dxgi \_ BC3 \_ UNORM \_ sRGB) para armazenar dados de cores altamente coerentes (use [BC2](#bc2) com dados alfa menos coerentes). O formato BC3 armazena dados de cor usando cor 5:6:5 (5 bits de vermelho, 6 bits de verde, 5 bits de azul) e dados alfa usando um byte. Pressupondo uma textura de 4 × 4 usando o formato de dados maior possível, essa técnica de compactação reduz a memória necessária de 64 bytes (16 cores × 4 componentes/cor × 1 byte/componente) para 16 bytes de memória.

O formato BC3 armazena cores com o mesmo número de bits e layout de dados que o formato [BC1](#bc1), no entanto, o BC3 requer 64 bits adicionais de memória para armazenar os dados alfa. O formato BC3 manipula o alfa armazenando dois valores de referência e interpolando entre eles (da mesma forma como o BC1 armazena cor RGB).

O algoritmo funciona em blocos de texels de 4 × 4. Em vez de armazenar 16 valores Alfa, o algoritmo armazena 2 Alfas de referência (alfa \_ 0 e alfa \_ 1) e índices de cores de 16 3 bits (alfa a até p), conforme mostrado no diagrama a seguir.

![diagrama do layout da compactação BC3](images/d3d10-compression-bc3.png)

O formato BC3 usa os índices de alfa (a–p) para procurar as cores originais em uma tabela de pesquisa que contém 8 valores. Os dois primeiros valores — Alfa \_ 0 e alfa \_ 1 — são os valores mínimo e máximo; os outros seis valores intermediários são calculados usando interpolação linear.

O algoritmo determina o número de valores alfa interpolados examinando os dois valores alfa de referência. Se alfa \_ 0 for maior que alfa \_ 1, BC3 interpolará 6 valores Alfa; caso contrário, ele interpolará 4. Quando o BC3 interpola apenas 4 valores alfa, ele define dois valores alfa adicionais (0 para totalmente transparente e 255 para totalmente opaco). O BC3 compacta os valores alfabéticos na área de texel de 4 × 4, armazenando o código de bit correspondente aos valores alfa interpolados que melhor correspondem ao alfa original para um determinado texel.


```
if( alpha_0 > alpha_1 )
{
  // 6 interpolated alpha values.
  alpha_2 = 6/7*alpha_0 + 1/7*alpha_1; // bit code 010
  alpha_3 = 5/7*alpha_0 + 2/7*alpha_1; // bit code 011
  alpha_4 = 4/7*alpha_0 + 3/7*alpha_1; // bit code 100
  alpha_5 = 3/7*alpha_0 + 4/7*alpha_1; // bit code 101
  alpha_6 = 2/7*alpha_0 + 5/7*alpha_1; // bit code 110
  alpha_7 = 1/7*alpha_0 + 6/7*alpha_1; // bit code 111
}
else
{
  // 4 interpolated alpha values.
  alpha_2 = 4/5*alpha_0 + 1/5*alpha_1; // bit code 010
  alpha_3 = 3/5*alpha_0 + 2/5*alpha_1; // bit code 011
  alpha_4 = 2/5*alpha_0 + 3/5*alpha_1; // bit code 100
  alpha_5 = 1/5*alpha_0 + 4/5*alpha_1; // bit code 101
  alpha_6 = 0;                         // bit code 110
  alpha_7 = 255;                       // bit code 111
}
```





<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Diferenças entre o Direct3D 9 e o Direct3D 10:<br/>
<ul>
<li>No Direct3D 9, o formato BC3 é chamado de D3DFMT_DXT4 e D3DFMT_DXT5.</li>
<li>No Direct3D 10, o formato BC3 é representado por DXGI_FORMAT_BC3_UNORM ou DXGI_FORMAT_BC3_UNORM_SRGB.</li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="bc4"></a>BC4

Use o formato BC4 para armazenar dados de cor de um componente usando 8 bits para cada cor. Como resultado da maior precisão (em comparação com [BC1](#bc1)), o BC4 é ideal para armazenar dados de ponto flutuante no intervalo de \[ 0 a 1 \] usando o formato dxgi \_ \_ BC4 \_ UNORM e \[ -1 a + 1 \] usando o formato dxgi \_ BC4 SNORM \_ \_ Format. Pressupondo uma textura de 4 × 4 usando o formato de dados maior possível, essa técnica de compactação reduz a memória necessária de 16 bytes (16 cores × 1 componentes/cor × 1 byte/componente) para 8 bytes.

O algoritmo funciona em blocos de texels de 4 × 4. Em vez de armazenar 16 cores, o algoritmo armazena 2 cores de referência (vermelho \_ 0 e vermelho \_ 1) e índices de cores de 16 3 bits (vermelho a por meio do Red p), conforme mostrado no diagrama a seguir.

![diagrama do layout da compactação BC4](images/d3d10-compression-bc4.png)

O algoritmo usa os índices de 3 bits para procurar as cores em uma tabela de cores que contém 8 cores. As duas primeiras cores — vermelho \_ 0 e vermelho \_ 1 — são as cores mínimas e máximas. O algoritmo calcula as cores restantes usando interpolação linear.

O algoritmo determina o número de valores de cor interpolados examinando os dois valores de referência. Se o vermelho \_ 0 for maior que o vermelho \_ 1, BC4 interpolará 6 valores de cor; caso contrário, ele interpolará 4. Quando o BC4 interpola apenas 4 valores de cor, ele define dois valores de cor adicional (0.0f para totalmente transparente e 1.0f para totalmente opaco). O BC4 compacta os valores alfabéticos na área de texel de 4 × 4, armazenando o código de bit correspondente aos valores alfa interpolados que melhor correspondem ao alfa original para um determinado texel.

-   [BC4 \_ UNORM](/windows)
-   [BC4 \_ SNORM](/windows)

### <a name="bc4_unorm"></a>BC4 \_ UNORM

A interpolação dos dados de componente único é feita como no exemplo de código a seguir.


```
unsigned word red_0, red_1;

if( red_0 > red_1 )
{
  // 6 interpolated color values
  red_2 = (6*red_0 + 1*red_1)/7.0f; // bit code 010
  red_3 = (5*red_0 + 2*red_1)/7.0f; // bit code 011
  red_4 = (4*red_0 + 3*red_1)/7.0f; // bit code 100
  red_5 = (3*red_0 + 4*red_1)/7.0f; // bit code 101
  red_6 = (2*red_0 + 5*red_1)/7.0f; // bit code 110
  red_7 = (1*red_0 + 6*red_1)/7.0f; // bit code 111
}
else
{
  // 4 interpolated color values
  red_2 = (4*red_0 + 1*red_1)/5.0f; // bit code 010
  red_3 = (3*red_0 + 2*red_1)/5.0f; // bit code 011
  red_4 = (2*red_0 + 3*red_1)/5.0f; // bit code 100
  red_5 = (1*red_0 + 4*red_1)/5.0f; // bit code 101
  red_6 = 0.0f;                     // bit code 110
  red_7 = 1.0f;                     // bit code 111
}
```



As cores de referência recebem índices de 3 bits (000 – 111, uma vez que há 8 valores), que serão salvos em blocos na cor vermelha a até a cor vermelha p durante a compactação.

### <a name="bc4_snorm"></a>BC4 \_ SNORM

O \_ formato dxgi \_ BC4 \_ SNORM é exatamente o mesmo, exceto que os dados são codificados no intervalo de SNORM e quando quatro valores de cor são interpolados. A interpolação dos dados de componente único é feita como no exemplo de código a seguir.


```
signed word red_0, red_1;

if( red_0 > red_1 )
{
  // 6 interpolated color values
  red_2 = (6*red_0 + 1*red_1)/7.0f; // bit code 010
  red_3 = (5*red_0 + 2*red_1)/7.0f; // bit code 011
  red_4 = (4*red_0 + 3*red_1)/7.0f; // bit code 100
  red_5 = (3*red_0 + 4*red_1)/7.0f; // bit code 101
  red_6 = (2*red_0 + 5*red_1)/7.0f; // bit code 110
  red_7 = (1*red_0 + 6*red_1)/7.0f; // bit code 111
}
else
{
  // 4 interpolated color values
  red_2 = (4*red_0 + 1*red_1)/5.0f; // bit code 010
  red_3 = (3*red_0 + 2*red_1)/5.0f; // bit code 011
  red_4 = (2*red_0 + 3*red_1)/5.0f; // bit code 100
  red_5 = (1*red_0 + 4*red_1)/5.0f; // bit code 101
  red_6 = -1.0f;                     // bit code 110
  red_7 =  1.0f;                     // bit code 111
}
```



As cores de referência recebem índices de 3 bits (000 – 111, uma vez que há 8 valores), que serão salvos em blocos na cor vermelha a até a cor vermelha p durante a compactação.

### <a name="bc5"></a>BC5

Use o formato BC5 para armazenar dados de cor de dois componentes usando 8 bits para cada cor. Como resultado da maior precisão (em comparação com [BC1](#bc1)), o BC5 é ideal para armazenar dados de ponto flutuante no intervalo de \[ 0 a 1 \] usando o formato dxgi \_ \_ BC5 \_ UNORM e \[ -1 a + 1 \] usando o formato dxgi \_ BC5 SNORM \_ \_ Format. Pressupondo uma textura de 4 × 4 usando o formato de dados maior possível, essa técnica de compactação reduz a memória necessária de 32 bytes (16 cores × 2 componentes/cor × 1 byte/componente) para 16 bytes.

O algoritmo funciona em blocos de texels de 4 × 4. Em vez de armazenar 16 cores para ambos os componentes, o algoritmo armazena 2 cores de referência para cada componente (vermelho \_ 0, vermelho \_ 1, verde \_ 0 e verde \_ 1) e índices de cores de 16 3 bits para cada componente (vermelho a por meio de p vermelho e verde a até verde p), conforme mostrado no diagrama a seguir.

![diagrama do layout da compactação Bc5](images/d3d10-compression-bc5.png)

O algoritmo usa os índices de 3 bits para procurar as cores em uma tabela de cores que contém 8 cores. As duas primeiras cores — vermelho \_ 0 e vermelho \_ 1 (ou verde \_ 0 e verde \_ 1) — são as cores mínimas e máximas. O algoritmo calcula as cores restantes usando interpolação linear.

O algoritmo determina o número de valores de cor interpolados examinando os dois valores de referência. Se o vermelho \_ 0 for maior que o vermelho \_ 1, BC5 interpolará 6 valores de cor; caso contrário, ele interpolará 4. Quando o BC5 interpola apenas 4 valores de cor, ele define os dois valores de cor restantes em 0.0f e 1.0f.

-   [BC5 \_ UNORM](/windows)
-   [BC5 \_ SNORM](/windows)

### <a name="bc5_unorm"></a>BC5 \_ UNORM

A interpolação dos dados de componente único é feita como no exemplo de código a seguir. Os cálculos para os componentes verdes são semelhantes.


```
unsigned word red_0, red_1;

if( red_0 > red_1 )
{
  // 6 interpolated color values
  red_2 = (6*red_0 + 1*red_1)/7.0f; // bit code 010
  red_3 = (5*red_0 + 2*red_1)/7.0f; // bit code 011
  red_4 = (4*red_0 + 3*red_1)/7.0f; // bit code 100
  red_5 = (3*red_0 + 4*red_1)/7.0f; // bit code 101
  red_6 = (2*red_0 + 5*red_1)/7.0f; // bit code 110
  red_7 = (1*red_0 + 6*red_1)/7.0f; // bit code 111
}
else
{
  // 4 interpolated color values
  red_2 = (4*red_0 + 1*red_1)/5.0f; // bit code 010
  red_3 = (3*red_0 + 2*red_1)/5.0f; // bit code 011
  red_4 = (2*red_0 + 3*red_1)/5.0f; // bit code 100
  red_5 = (1*red_0 + 4*red_1)/5.0f; // bit code 101
  red_6 = 0.0f;                     // bit code 110
  red_7 = 1.0f;                     // bit code 111
}
```



As cores de referência recebem índices de 3 bits (000 – 111, uma vez que há 8 valores), que serão salvos em blocos na cor vermelha a até a cor vermelha p durante a compactação.

### <a name="bc5_snorm"></a>BC5 \_ SNORM

O \_ formato dxgi \_ BC5 \_ SNORM é exatamente o mesmo, exceto que os dados são codificados no intervalo de SNORM e quando 4 valores de dados são interpolados, os dois valores adicionais são-1,0 f e 1,0 f. A interpolação dos dados de componente único é feita como no exemplo de código a seguir. Os cálculos para os componentes verdes são semelhantes.


```
signed word red_0, red_1;

if( red_0 > red_1 )
{
  // 6 interpolated color values
  red_2 = (6*red_0 + 1*red_1)/7.0f; // bit code 010
  red_3 = (5*red_0 + 2*red_1)/7.0f; // bit code 011
  red_4 = (4*red_0 + 3*red_1)/7.0f; // bit code 100
  red_5 = (3*red_0 + 4*red_1)/7.0f; // bit code 101
  red_6 = (2*red_0 + 5*red_1)/7.0f; // bit code 110
  red_7 = (1*red_0 + 6*red_1)/7.0f; // bit code 111
}
else
{
  // 4 interpolated color values
  red_2 = (4*red_0 + 1*red_1)/5.0f; // bit code 010
  red_3 = (3*red_0 + 2*red_1)/5.0f; // bit code 011
  red_4 = (2*red_0 + 3*red_1)/5.0f; // bit code 100
  red_5 = (1*red_0 + 4*red_1)/5.0f; // bit code 101
  red_6 = -1.0f;                    // bit code 110
  red_7 =  1.0f;                    // bit code 111
}
```



As cores de referência recebem índices de 3 bits (000 – 111, uma vez que há 8 valores), que serão salvos em blocos na cor vermelha a até a cor vermelha p durante a compactação.

## <a name="format-conversion-using-direct3d-101"></a>Conversão de formato usando o Direct3D 10,1

O Direct3D 10,1 permite cópias entre texturas de tipo preestruturadas e texturas compactadas de bloco das mesmas larguras de bits. As funções que podem fazer isso são [**CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) e [**CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion).

A partir do Direct3D 10,1, você pode usar [**CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) e [**CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion) para copiar entre alguns tipos de formato. Esse tipo de operação de cópia executa um tipo de conversão de formato que reinterpreta os dados de recursos como um tipo de formato diferente. Considere este exemplo que mostra a diferença entre a reinterpretação de dados com o comportamento de um tipo mais comum de conversão:


```
    FLOAT32 f = 1.0f;
    UINT32 u;
```



Para reinterpretar ' f ' como o tipo de ' u ', use [memcpy](/cpp/c-runtime-library/reference/memcpy-wmemcpy):


```
    memcpy( &u, &f, sizeof( f ) ); // ‘u’ becomes equal to 0x3F800000.
```



Na reinterpretação anterior, o valor subjacente dos dados não muda; [memcpy](/cpp/c-runtime-library/reference/memcpy-wmemcpy) reinterpreta o flutuante como um inteiro sem sinal.

Para executar o tipo mais comum de conversão, use a atribuição:


```
    u = f; // ‘u’ becomes 1.
```



Na conversão anterior, o valor subjacente dos dados muda.

A tabela a seguir lista os formatos de destino e origem permitidos que você pode usar nesse tipo de reinterpretação de conversão de formatos. Você deve codificar os valores corretamente para que a reinterpretação funcione conforme esperado.



| Largura de bit | Recurso não compactado                                                                                                                                               | Recurso compactado em bloco                                                                                                                                           |
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 32        | \_Formato dxgi \_ R32 \_ uint<br/> \_Formato dxgi \_ R32 \_ Santo<br/>                                                                                               | \_Formato dxgi \_ R9G9B9E5 \_ SHAREDEXP                                                                                                                                   |
| 64        | \_Formato dxgi \_ R16G16B16A16 \_ uint<br/> \_Formato dxgi \_ R16G16B16A16 \_ Santo<br/> \_Formato dxgi \_ R32G32 \_ uint<br/> \_Formato dxgi \_ R32G32 \_ Santo<br/> | \_Formato dxgi \_ BC1 \_ UNORM \[ \_ sRGB\]<br/> \_Formato dxgi \_ BC4 \_ UNORM<br/> \_Formato dxgi \_ BC4 \_ SNORM<br/>                                               |
| 128       | \_Formato dxgi \_ R32G32B32A32 \_ uint<br/> \_Formato dxgi \_ R32G32B32A32 \_ Santo<br/>                                                                             | \_Formato dxgi \_ BC2 \_ UNORM \[ \_ sRGB\]<br/> \_Formato dxgi \_ BC3 \_ UNORM \[ \_ sRGB\]<br/> \_Formato dxgi \_ BC5 \_ UNORM<br/> \_Formato dxgi \_ BC5 \_ SNORM<br/> |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Recursos (Direct3D 10)](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 
