---
title: Algoritmos de criação de transformação do WCS
description: Algoritmos de criação de transformação do WCS
ms.assetid: 526bbbfc-fb60-415d-b4f0-6a44a5d11a55
keywords:
- WCS (sistema de cores do Windows), criação de transformação
- WCS (sistema de cores do Windows), criação de transformação
- gerenciamento de cores de imagem, criação de transformação
- gerenciamento de cores, criação de transformação
- cores, criação de transformação
- criação de transformação
- Criação de transformação WCS
- algoritmos, criação de transformação
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 418596c0e57571f3e504727d4606921d36ff9461
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/03/2021
ms.locfileid: "104563080"
---
# <a name="wcs-transform-creation-algorithms"></a>Algoritmos de criação de transformação do WCS

[Criação de transformações](#creation-of-transforms)

 

[Execução de transformação sequencial](#sequential-transform-execution)

 

[Criação de transformações otimizadas](#creation-of-optimized-transforms)

 

[ICCProfileFromWCSProfile](#iccprofilefromwcsprofile)

 

[Preservação de preto e geração de preto](#black-preservation-and-black-generation)

 

[Gama de cheques](#checkgamut)

## <a name="creation-of-transforms"></a>Criação de transformações

Para explicar corretamente como as transformações de cores funcionam, é útil explicar o caminho completo de processamento por meio do ICM 2,0 e dos internos da CTE. A função ICM 2,0 [**CreateColorTransformW**](/windows/win32/api/icm/nf-icm-createcolortransformw) cria uma transformação de cor que os aplicativos podem usar para executar o gerenciamento de cores. Essa função cria um contexto de cor das entradas [**LOGCOLORSPACE**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea) e de intenção. As tentativas são mapeadas para o algoritmo de mapeamento de gamut de ICC de linha de base. Em seguida, a função chama o [**CreateMultiProfileTransform**](/windows/desktop/api/Wingdi/) da função ICM 2,0 para o processamento de cores consistente. A função **CreateColorTransform** geralmente copia dados para a estrutura de transformação otimizada interna.

A função ICM 2,0 CreateMultiProfileTransform aceita uma matriz de perfis e uma matriz de tentativas ou um único perfil de link de dispositivo e cria uma transformação de cor que os aplicativos podem usar para executar o mapeamento de cores. Ele processa os perfis de entrada e as intenções para criar modelos de dispositivo, modelos de aparência de cores, descrições de limites de gamut e modelos de mapeamento de gamut. Veja como isso é feito:

-   Os modelos de dispositivo são inicializados diretamente de perfis DM. Há um modelo de dispositivo criado para cada perfil na chamada para [**CreateMultiProfileTransform**](/windows/desktop/api/Wingdi/).
-   Os modelos de aparência de cores são inicializados diretamente de perfis CAM. Há um perfil CAM para cada perfil na chamada para [**CreateMultiProfileTransform**](/windows/desktop/api/Wingdi/). No entanto, o mesmo perfil CAM pode ser especificado para mais de um perfil.
-   As descrições de limites de gama são inicializadas a partir de um objeto de modelo de dispositivo e um objeto CAM. Há uma descrição de limite de gama para cada perfil na chamada para [**CreateMultiProfileTransform**](/windows/desktop/api/Wingdi/).
-   Os modelos de mapeamento de gamut são inicializados a partir de dois limites de gama e uma intenção. Você deve criar um modelo de mapeamento de gamut entre cada par de modelos de dispositivo criados na chamada para [**CreateMultiProfileTransform**](/windows/desktop/api/Wingdi/). Observe que isso significa que você usa um modelo de mapa de gama a menos do que o modelo de dispositivo. Como o número de tentativas corresponde ao número de modelos de dispositivo, também há mais uma intenção do que o necessário. A primeira tentativa na lista é ignorada. Você percorre a lista de modelos de dispositivo e as intenções, criando modelos de mapeamento de gamut. Pegue o primeiro e o segundo modelos de dispositivo e a segunda tentativa e, em seguida, inicialize o primeiro modelo de mapeamento de gama. Pegue o segundo e terceiro modelos de dispositivo e a terceira intenção e, em seguida, inicialize o segundo modelo de mapeamento de gama. Continue dessa maneira até que você tenha criado todos os modelos de mapeamento de gamut.

Quando os perfis tiverem sido processados corretamente e todos os objetos intermediários tiverem sido criados e inicializados, você poderá criar a transformação CITE com a chamada a seguir. Os *pDestCAM* e *pDestDM* são aqueles associados ao último perfil na chamada para [**CreateMultiProfileTransform**](/windows/desktop/api/Wingdi/).


```C++
HRESULT CreateCITEColorTransform(
 __inout     IDeviceModel          *pSourceDM,
 __inout     IColorAppearanceModel *pSourceCAM,
 __in        GamutMapArray         *pGamutMapArray,
 __inout     IColorAppearanceModel *pDestCAM,
 __inout     IDeviceModel          *pDestDM,
             EColorTransformMode    eTransformMode,
 __deref_out IColorTransform      **ppCTS
 );
```



## <a name="support-for-plug-ins"></a>Suporte para plug-ins

Um problema envolvido na configuração da lista de transformação é validar se um plug-in necessário está disponível. A opção de modelo a seguir fornece essa política para controlar esse comportamento. O gerenciamento dessa lista de transformação é um método na estrutura de transformação otimizada interna, mas cada método de modelo fornece o ponteiro para si mesmo e seu próprio conjunto de valores de parâmetro.

O modo deve ser um dos seguintes.

-   TfmRobust: se um perfil de medida especificar um plug-in preferencial e o plug-in não estiver disponível, o novo sistema de CTE usará o plug-in de linha de base. Se nenhum plug-in estiver disponível, a transformação relatará um erro.
-   TfmStrict: se ColorContext especificar um plug-in preferencial, o plug-in deverá estar disponível. Se nenhum plug-in preferencial for encontrado, o plug-in de linha de base será usado. Se nenhum plug-in estiver disponível, a transformação relatará um erro.
-   TfmBaseline: somente plug-ins de linha de base podem ser usados em AddMeasurementStep. Se ColorContext especificar um plug-in preferencial, o plug-in será ignorado. Se o plug-in de linha de base não estiver disponível, a transformação relatará um erro.

## <a name="transform-execution"></a>Execução de transformação

A função [**TranslateColors**](/windows/win32/api/icm/nf-icm-translatecolors) da API do ICM 2,0 converte uma matriz de cores do espaço de [cor](c.md) de origem para o espaço de cores de destino, conforme definido por uma transformação de cor. Essa função verifica internamente uma matriz de cores em cache para permitir a correspondência imediata de cores transformadas normalmente. Essa transformação dá suporte a matrizes de bytes por canal de 8 bits e a matrizes float de 32 bits por canal. Todos os outros formatos serão convertidos antes de serem transmitidos para a nova CTE.

A função [**TranslateBitmapBits**](/windows/win32/api/icm/nf-icm-translatebitmapbits) da API do ICM 2,0 converte as cores de um bitmap que tem um formato definido para produzir outro bitmap em um formato solicitado. Essa função verifica internamente uma matriz de cores em cache para permitir a correspondência imediata de cores transformadas normalmente. Para evitar muitos caminhos de código, suporte e complexidade de teste, apenas um número limitado de formatos de bitmap, na verdade, tem suporte no mecanismo de transformação e de interpolação. Essa função deve converter os formatos de bitmap de entrada e saída não nativos em formatos com suporte nativo para processamento. Essa transformação dá suporte apenas a bitmaps de 8 bits por byte de canal e bitmaps float de 32 bits por canal. Todos os outros formatos serão convertidos antes de serem transmitidos para a nova CTE.

 

### <a name="sequential-transform-execution"></a>Execução de transformação sequencial

Se o parâmetro *dwFlags* tiver o bit de transformação sequencial \_ definido quando as funções ICM [**CreateColorTransformW**](/windows/win32/api/icm/nf-icm-createcolortransformw) ou **CreateMultiProfileTransform** forem chamadas, as etapas de transformação serão executadas em sequência. Isso significa que o código percorre cada modelo de dispositivo, modelo de aparência de cor e modelo de mapeamento de gamut separadamente, conforme especificado pela chamada **CreateColorTransform** ou **CreateMultiProfileTransform** . Isso pode ser útil para depurar módulos de plug-in, mas é muito mais lento do que a execução por meio de uma transformação otimizada. A execução em modo sequencial, portanto, não é recomendada para software de produção. Além disso, pode haver pequenas diferenças nos resultados obtidos no modo sequencial e no modo otimizado. Isso ocorre devido a variações introduzidas quando as funções são concatenadas juntas.

### <a name="creation-of-optimized-transforms"></a>Criação de transformações otimizadas

Uma transformação otimizada é uma tabela de pesquisa multidimensional. A tabela pode ser processada por um mecanismo de interpolação multidimensional, como interpolação tetrahedral, que aplica as cores de entrada à transformação. A seção a seguir descreve como as tabelas de pesquisa otimizadas são criadas. A seção depois descreve como interpolar dentro das tabelas de pesquisa otimizadas.

## <a name="sparse-lookup-tables"></a>Tabelas de pesquisa esparsa

As impressoras convencionais têm tintas CMYK. Para estender a gama, uma abordagem é adicionar novas tintas ao sistema. As tintas normalmente adicionadas são cores que as tintas CMYK têm dificuldade de reproduzir. As opções comuns são laranja, verde, vermelho, azul etc. Para aumentar a "resolução aparente", as tintas com tons diferentes podem ser usadas, por exemplo, ciano claro, Magenta claro e assim por diante. Na verdade, o dispositivo de impressora tem mais de quatro canais.

Embora as impressoras sejam dispositivos de saída, elas também executam a conversão de cores do espaço do dispositivo para outro espaço de cores. No caso de uma impressora CMYK, essa seria uma transformação de CMYK para XYZ ou o "modelo de encaminhamento" da impressora. Ao combinar o modelo de encaminhamento com outras transformações, é possível emular uma impressão CMYK em outro dispositivo. Por exemplo, uma impressora CMYK para um monitor RGB tornaria possível um mecanismo de verificação que emulasse uma impressão da impressora CMYK em um monitor. Da mesma forma, o mesmo também se aplica a impressoras de Hi-Fi. Uma conversão de CMYKOG para RGB permite a prova da impressora CMYKOG em um monitor.

A abordagem convencional para implementar essa conversão de cores é usar um LUT uniforme. Por exemplo, em um perfil ICC para uma impressora CMYKOG, a especificação ICC exige uma marca A2B1 que armazena um LUT uniforme representando uma amostragem uniforme no espaço do dispositivo CMYKOG do modelo de encaminhamento, que passa de CMYKOG para o espaço de conexão do perfil ICC (CIELAB ou CIEXYZ). O perfil de link do dispositivo ICC permite uma transformação direta do espaço do dispositivo CMYKOG para qualquer espaço de cores, incluindo um espaço de dispositivo, também na forma de um LUT amostrado uniformemente no espaço CMYKOG. A amostragem nunca é feita com 256 níveis (profundidade de bit 8) devido ao enorme LUT resultante, exceto no caso de dispositivos monocromáticos (1 canal). Em vez disso, a amostragem com profundidade de bits inferior é usada; algumas opções típicas são 9 (profundidade de bits 3), 17 (profundidade de bits 4), 33 (profundidade de bit 5). Com o número de níveis inferior a 256 em cada canal, o LUT é usado em conjunto com um algoritmo de interpolação para produzir o resultado se um nível estiver entre dois níveis de amostra.

Embora um LUT uniforme seja conceitualmente simples de implementar, e a interpolação em um LUT uniforme é geralmente eficiente, o tamanho de LUT aumenta exponencialmente com a dimensão de entrada. Na verdade, se *d* for o número de etapas usadas no lut uniforme, e *n* for o número de canais no espaço de cores de origem, o número de nós no lut será ![ mostrado na variável para o número de nós em um lut. ](images/transformcreation-image002.gif) Claramente, o número de nós exige rapidamente tantos armazenamento na memória que até os sistemas de computação topo de linha tenham dificuldades para lidar com a demanda. Para dispositivos com seis ou oito canais, uma implementação de ICC do perfil de dispositivo requer o uso de algumas etapas no LUT, às vezes até cinco etapas na tabela A2B1 para manter o perfil em megabytes em vez de gigabytes. Claramente, o uso de um número menor de etapas aumenta o erro de interpolação, pois agora há menos amostras. Como o LUT deve ser uniforme, a precisão em todo o espaço de cores é degradada mesmo nas regiões do espaço em que uma diferença de cor significativa pode ser causada por pequenas alterações no valor do dispositivo.

Em dispositivos com mais de quatro colorants, determinados subespaços de todo o espaço do dispositivo são mais importantes do que outros. Por exemplo, no espaço de CMYKOG, as tintas ciano e verde raramente são usadas juntas porque seu matiz se sobrepõe em grande parte. Da mesma forma, as tintas amarela e laranja se sobrepõem em grande parte. Uma redução uniforme no número de etapas pode ser exibida como uma degradação geral na qualidade em todo o espaço de cores, que é algo que você pode pagar para as combinações de tinta impossíveis, mas não para as combinações prováveis ou importantes.

Embora um LUT uniformemente amostrado seja simples e eficiente para interpolação, ele impõe requisitos de memória enormes à medida que a dimensão aumenta. Na realidade, embora um dispositivo possa ter seis ou oito canais, eles raramente são usados simultaneamente. Na maioria dos casos, a cor de entrada para a transformação cor tem apenas algumas colorants "ativas" e, portanto, reside em um espaço de cor dimensional inferior. Isso também significa que a interpolação pode ser feita com mais eficiência nesse espaço dimensional inferior, pois a interpolação é mais rápida quando a dimensão é menor.

Portanto, a abordagem é estratificar todo o espaço do dispositivo em subespaços de várias dimensões. E como as dimensões inferiores (aquelas que combinam três ou quatro colorants) são mais importantes, por stratifying o espaço, você também pode aplicar taxas de amostragem diferentes; ou seja, um número diferente de etapas, para as partes; aumento das taxas de amostragem para dimensões inferiores, reduzindo-as para dimensões mais altas.

Para corrigir as notações, *n* é o número de canais no espaço de cor de origem da transformação de cor que você deseja obter. Você também pode fazer referência a *n* como a dimensão de entrada e ![ mostra n maior ou igual a 5.](images/transformcreation-image004.gif) , a menos que especificado de outra forma.

Os blocos de construção básicos são LUTs de várias *dimensões* e tamanhos de entrada, em vez de um lut uniforme com a dimensão de entrada *n*. Para ser mais preciso, um *lut* é um malha retangular imposto em um cubo de unidade; ou seja, todas as coordenadas do dispositivo são normalizadas para o intervalo de \[ 0, 1 \] ). Se é a dimensão de entrada do lut (Observe que não precisa ser igual a *n*, embora ![ mostre V menor ou igual a n.](images/transformcreation-image006.gif) é obrigatório), então ele consiste em grades de amostragem unidimensional ν:

SAMP *i*: ![ mostra uma grade de amostragem unidimensional.](images/transformcreation-image008.gif)

onde todos os *x <sub>j</sub>s* devem estar no intervalo de \[ 0, 1 \] , ![ mostra um sobrescrito d (i).](images/transformcreation-image010.gif) é o número de etapas para a amostragem de canal *i* que deve ser pelo menos 1 e ![ mostra um spuperscript de X (subscrito) d (i).](images/transformcreation-image012.gif) deve ser 1. Por outro lado, o ![ mostra um sobrescrito X (subscrito 1).](images/transformcreation-image014.gif) Não é necessário que seja 0.

Somente os dois casos especiais a seguir de LUT serão definidos.

*Closed lut*: esse é um lut com o requisito adicional que, para cada SAMP *<sub>i</sub>*, ![ mostra um sobrescrito X (subscrito 1) é igual a 0.](images/transformcreation-image016.gif) e ![ mostra um sobrescrito d (i) maior ou igual a 2.](images/transformcreation-image018.gif) . Um LUT fechado uniforme é um LUT fechado que tem o mesmo ![ mostra um sobrescrito d (i).](images/transformcreation-image010.gif) para cada canal, e os nós têm espaçamento uniforme entre 0 e 1.

*Abra lut*: esse é um lut com o requisito adicional que para cada SAMP *i*, ![ mostra um sobrescrito X (subscript 1) maior que 0.](images/transformcreation-image020.gif) . OK para ![ exibir um sobrescrito d (i) igual a 1.](images/transformcreation-image022.gif) .

O objetivo é estratificar o cubo de unidade \[ 0, 1 \] *n* em uma coleção de LUTs fechada e abrir Luts, de modo que a coleção inteira cubra o cubo de unidade. É conceitualmente mais simples organizar essas "LUT Strata" por suas dimensões, de modo que no nível superior:

![Mostra o nível superior para organizar L U T Strata por suas dimensões.](images/transformcreation-image024.png)

onde ![ mostra o subscrito Sigma k.](images/transformcreation-image026.gif) é a "coleção de Strata em *k* -dimensional". Observe que a dimensão Strata começa em 3, em vez de 0; ou seja, os pontos, porque a interpolação de combinações de três Colorant pode ser tratada sem muito requisito de memória.

## <a name="description-of-the-lut-strata"></a>Descrição do LUT Strata

Nesta implementação:

1. ![Mostra o subscript Sigma 3.](images/transformcreation-image028.gif) consiste em LUTs fechadas com três entradas, uma de cada combinação possível de três colorants escolhidas de *n* colorants.

2. ![Mostra o subscript 4 do Sigma.](images/transformcreation-image030.gif) consiste em um LUT fechado para a combinação CMYK (ou os quatro primeiros colorants), junto com ![Mostra (n em 4) menos 1.](images/transformcreation-image032.png) Abra LUTs para todas as outras combinações de quatro Colorant. Ao descobrir a combinação de CMYK, você reconhece que é uma combinação importante.

3. Para ![ mostra k igual a 5,..., n.](images/transformcreation-image034.gif) , ![ Mostra o subscrito Sigma k.](images/transformcreation-image026.gif) consiste em ![ Mostrar (n sobre k).](images/transformcreation-image037.gif) Abra LUTs, um para cada combinação possível de escolher *k* colorants do total de *n* colorants.

Ele permanece para especificar os tamanhos de LUTs. A principal diferença entre o LUTs aberto e o fechado é que os LUTs abertos não se sobrepõem e os LUTs fechados podem se sobrepor às faces de limite. O fato de que a amostragem unidimensional em um LUT aberto não contém 0, essencialmente significa que um LUT aberto não tem metade das faces de limite, portanto, o nome "aberto". Se dois LUTs não se sobrepõem, você pode usar um número diferente de etapas ou locais de nó em cada canal. O mesmo não será verdadeiro se duas sobreposição de LUTs. Nesse caso, se o número de etapas ou os locais de nó forem diferentes, um ponto de acordo com a interseção dos dois LUTs receberá um valor de interpolação diferente, dependendo de qual LUT é usado na interpolação. Uma solução simples para esse problema é usar a amostragem uniforme com o mesmo número de etapas, sempre que duas sobreposição de LUTs. Em outras palavras:

Todas as LUTs fechadas (todas as LUTs de três Colorant e a LUT CMYK nessa implementação) devem ser uniformes e ter o mesmo número de etapas, que são indicadas *d*.

Os dois algoritmos a seguir podem ser usados para determinar o número de etapas *d* para Luts fechadas e o número de etapas para abrir Luts.

## <a name="algorithm-1"></a>Algoritmo \# 1

Esse algoritmo não requer entrada externa.

Todos os LUTs fechados serão uniformes com o número de etapas *d* .

Todos os LUTs abertos da dimensão *k* terão o mesmo número de etapas ![ mostra d (k).](images/transformcreation-image039.gif) em cada canal de entrada, e os nós têm espaçamento uniforme; ou seja, para cada um ![ mostra igual a 1, 2,..., k.](images/transformcreation-image041.gif) .

SAMP *i*: ![ mostra o algoritmo SAMP i.](images/transformcreation-image043.png)

Por fim, especifique *d* e *d* (*k* ) na tabela 1 a seguir. Os três modos, "prova", "normal" e "melhor" são as configurações de qualidade ICM 2,0. Nessa implementação, o modo de prova tem a menor superfície de memória e o melhor modo tem o maior volume de memória.

Para implementar esse algoritmo, você deve chamar o seguinte algoritmo \# 2. Os usuários podem especificar seus próprios locais de amostragem, usando as tabelas como um guia.

## <a name="algorithm-2"></a>Algoritmo \# 2

Esse algoritmo requer entrada externa na forma de uma lista de locais de amostragem "importantes", mas é mais adaptável e pode economizar espaço de memória potencialmente.

A entrada necessária é uma matriz de valores de dispositivo fornecida pelo usuário. Esses valores de dispositivo indicam qual região do espaço de cores do dispositivo é importante; ou seja, qual região deve ser amostrada mais.

Todos os LUTs fechados serão uniformes com o número *d* de etapas, conforme descrito no algoritmo \# 1. Os valores para *d* são fornecidos na tabela 1.

*(a) LUT fechada uniforme*



|         | Modo de prova | Modo Normal | Modo melhor |
|---------|------------|-------------|-----------|
| ***d*** | 9          | 17          | 33        |



 

*(b) abrir LUT*



| Dimensão de entrada | Modo de prova | Modo Normal | Modo melhor |
|-----------------|------------|-------------|-----------|
| 4               | 5          | 7           | 9         |
| 5               | 2          | 3           | 3         |
| 6               | 2          | 3           | 3         |
| 7               | 2          | 2           | 2         |
| 8 ou mais       | 2          | 2           | 2         |



 

**Tabela 1:** Tamanhos de LUT usados no algoritmo

Cada LUT aberta pode ter um número diferente de etapas em cada canal de entrada, e os locais de amostragem não precisam ser igualmente espaçados. Para uma determinada camada de LUT aberta, há uma combinação Colorant associada, por exemplo, ![ mostra o c subscrito 1,..., c subscript k.](images/transformcreation-image045.gif) , em que ![ mostra o script C i.](images/transformcreation-image047.gif) s são inteiros distintos entre 1 e *n*. Eles são os índices de canal correspondentes ao colorants "ativo" neste Strata.

ETAPA 1: filtrar a matriz de entrada de valores de dispositivo que não estão contidos neste Strata. Um valor de dispositivo ![ mostra o x subscrito 1, x subscrito 2,..., X subscript n.](images/transformcreation-image049.gif) está contido no Strata, se e somente se ![ o mostrar um conjunto de valores para um canal.](images/transformcreation-image051.gif) e todos os outros canais são 0. Se o conjunto filtrado tiver *N* entradas, Let

![Mostra uma equação a ser usada se o conjunto filtrado tiver N entradas.](images/transformcreation-image053.png)

Para cada ![Mostra i igual a 1, 2,..., k.](images/transformcreation-image041.gif) , itere as seguintes etapas 2-5:

ETAPA 2: se ![ Mostrar d subscrito provisório (k) igual a 1.](images/transformcreation-image055.gif) , SAMP *i* tem apenas 1 ponto, que deve ser 1,0. Passe para o próximo *i*. Caso contrário, continue na etapa 3.

ETAPA 3: classificar os exemplos filtrados em ordem crescente no ![Mostra o script C i.](images/transformcreation-image047.gif) canal.

ETAPA 4: definir a grade de amostragem "provisória" usando os nós

![Mostra os nós usados para definir a grade de amostragem "provisória".](images/transformcreation-image057.png)

onde ![Mostra j igual a 1, 2,..., d subscrito provisório (k).](images/transformcreation-image059.gif) .

ETAPA 5: regularize a grade provisória para garantir que ela esteja em conformidade com monotônico estrita e também que termine com 1,0. Como a matriz já está classificada, os nós na grade provisória já são monotônico nondecreasing. No entanto, nós adjacentes podem ser idênticos. Você pode corrigir isso removendo nós idênticos, se necessário. Por fim, após esse procedimento, se o ponto de extremidade for menor que 1,0, substitua-o por 1,0.

Observe que a etapa 5 é o motivo pelo qual o LUT STRATA pode ter um número diferente de etapas em cada canal. Após a regularização, o número de etapas em um canal pode ser menor que ![Mostra o d subscrito provisório (k).](images/transformcreation-image061.gif) .

## <a name="interpolation"></a>Interpola

Você pode construir o estratificação do cubo de unidade abrindo LUT Strata e fechado LUT Strata. Para executar a interpolação usando essa "estrutura de LUT esparsa", siga estas etapas. Assumir um determinado valor de dispositivo de entrada ![Mostra (X subscript 1, X subscrito 2,..., X subscript n).](images/transformcreation-image049.gif) .

ETAPA 1: determinar o número de canais "ativos". Este é o número de canais diferentes de zero. Isso determina a dimensão de Strata *k* para pesquisar o estrato que o contém. Mais precisamente, a dimensão Strata será 3 se o número de canais ativos for ![ exibido menor ou igual a 3.](images/transformcreation-image063.gif) caso contrário, a dimensão Strata é igual ao número de canais ativos.

ETAPA 2: em ![Mostra o subscrito Sigma k.](images/transformcreation-image026.gif) , procure o estrato que o contém. Um valor de dispositivo estará contido em um estrato aberto se todos os canais correspondentes ao estrato tiverem um valor diferente de zero e todos os outros canais forem zero. Um valor de dispositivo estará contido em um estrato fechado se cada canal não representado pelo estrato for zero. Se nenhum estrato de contenção for encontrado, haverá uma condição de erro. Cancelar e relatar falha. Se um estrato que o contém for encontrado, vá para a próxima etapa.

ETAPA 3: se o estrato que o contém está fechado, a interpolação dentro do estrato pode ser feita por qualquer algoritmo de interpolação conhecido. Nessa implementação, a escolha do algoritmo é a interpolação tetrahedral. Se o estrato que o contém estiver aberto, e o valor do dispositivo estiver estritamente dentro do estrato, ou seja,

![Mostra o subscript X que é maior ou igual a... ](images/transformcreation-image065.gif) primeiro nó no canal *i* -ésimo

onde *eu* é um índice de canal para o estrato, então, o algoritmo de interpolação padrão, como interpolação tetrahedral, funciona.

Se ![ Mostrar um subscript i menor que... ](images/transformcreation-image067.gif) primeiro nó no canal *i* , em seguida , o valor do dispositivo entrará na "lacuna" entre os subespaços de estrato e de dimensão inferior. Esse MOI não se preocupa com um algoritmo de interpolação por si, portanto, qualquer algoritmo de interpolação pode ser usado para interpolar dentro dessa "lacuna", embora o algoritmo preferencial seja a seguinte interpolação transfinita.

A arquitetura do módulo de interpolação é ilustrada nas duas partes da Figura 1.

![Diagrama que mostra a parte um da arquitetura do módulo de interpolação.](images/transformcreation-image068.png)

![Diagrama que mostra a parte dois da arquitetura do módulo de interpolação.](images/transformcreation-image070.png)

**Figura 1:** Arquitetura do módulo Intepolation

Conforme explicado anteriormente, esse algoritmo é capaz de obter amostragem razoavelmente densa em regiões do espaço do dispositivo que contêm uma combinação importante de colorants, ao mesmo tempo em que minimiza o tamanho total de LUTs necessário. A tabela a seguir mostra uma comparação do número de nós necessários para a implementação de LUT esparsa (usando o algoritmo \# 1 e o modo normal) e a implementação de lut uniforme correspondente.



| **Número de canais de entrada** | **LUT esparsa** | **LUT uniforme** |
|------------------------------|----------------|-----------------|
| 5                            | 142498         | 1419857         |
| 6                            | 217582         | 24137567        |
| 7                            | 347444         | 410338673       |
| 8                            | 559618         | 6975757441      |



 

## <a name="interpolation-within-a-unit-cube"></a>Interpolação dentro de um cubo de unidade

Uma etapa básica no caso da grade retangular é a interpolação dentro de uma célula delimitadora. Para um ponto de entrada, você pode determinar a célula de fechamento facilmente. Em uma grade retangular, o valor de saída em cada um dos vértices (pontos de canto) da célula de circunscrição é especificado. Elas também são as únicas condições de limite (BCs) que uma interpolação deve satisfazer: a interpolação deve passar por todos esses pontos. Observe que essas condições de limite estão em pontos "discretos", nesse caso, os pontos de canto 2n da célula, em que n é a dimensão do espaço de cores.

É útil formalizar o conceito de condições de limite antes de prosseguir. Para qualquer subconjunto S do limite da célula delimitadora (o cubo de unidade em n dimensões), uma condição de limite em S é uma especificação de uma função BC: S → RM, em que m é a dimensão de saída. Em outras palavras, uma interpolação, que pode ser denotada interp: \[ 0, 1 \] n → RM, é necessária para satisfazer: interp (x) = BC (x) para todos os x em S.

No cenário padrão de interpolação no cubo de unidade, S é o conjunto de pontos discretos que são os vértices 2n do cubo.

Agora você pode generalizar as condições de limite para resolver os problemas descritos anteriormente e fornecer um novo algoritmo de interpolação dentro do cubo de unidade. Em vez de permitir apenas pontos de limite discretos, as condições de limite podem ser impostas em uma face de limite inteira do cubo. As suposições exatas são as seguintes:

(a) o ponto VN = (1, 1,..., 1) é especial e apenas uma condição de limite discreta é permitida. Em outras palavras, nenhuma condição de limite contínua pode ser imposta nas faces de limite de n XI = 1 (i = 1,..., n).

(b) para cada uma das n restantes faces de limite XI = 0 (i = 1,..., n), a condição de limite pode ser imposta em toda a face, com a condição de compatibilidade que se duas faces se interseccionam, as condições de limite nas faces devem concordar na interseção.

(c) todos os vértices não contidos nas faces com a condição de limite terão uma condição de limite individual (discreta).

Você pode se referir a uma condição de limite discreta como dados finitos e uma condição de limite contínua como dados transfinitos para discutir a interpolação em dados finitos e transfinitos.

Primeiro, examine a interpolação tetrahedral padrão (como a usada na patente do Sakamoto), que ajuda a definir as notações para essa formulação específica do problema. É conhecido que o cubo de unidade \[ 0, 1 \] n pode ser subdividido em n! tetrahedra, parametrizados pelo conjunto de permutações em símbolos n. Mais especificamente, cada tetraedro é definido por desigualdades

![Mostra a fórmula para o inequalites do tetrahedrons.](images/transformcreation-image073.gif)

em que σ: {1, 2,.., n} → {1, 2,..., n} é uma permutação de "Symbols" 1, 2,..., n, ou seja, é um mapeamento bijective do conjunto de n símbolos. Por exemplo, se n = 3 e σ = (3, 2, 1), significando σ (1) = 3, σ (2) = 2, σ (3) = 1, o tetraedro correspondente é definido por z ≥ y ≥ x, em que a notação comum x, y, z é usada para x1, X2, X3. Observe que esses tetrahedrons não são separados uns dos outros. Para fins de interpolação, os pontos que dependem de uma face comum de dois tetrahedrons distintos terão o mesmo valor de interpolação, independentemente de qual tetraedro é usado na interpolação. Ainda, no cenário padrão de interpolação em pontos finitos, para um determinado ponto de entrada (x1,..., Xn), primeiro determine em qual tetraedro ele se encontra ou, de modo equivalente, a permutação correspondente σ, então o tetrahedral interpolado é definido como

![Mostra a equação que define o tetrahedral interpolado.](images/transformcreation-image075.png)

onde ![Mostra a equação para os vetores de base padrão.](images/transformcreation-image077.png) para i = 1,..., n e E1,..., en são os vetores de base padrão. Antes de passar para a generalização, observe que V0, v1,..., vn são os vértices do tetraedro e ![Mostra as coordenadas de barycentric.](images/transformcreation-image079.png) são as "coordenadas barycentric".

Para o caso geral do BCs em rostos de limite, você pode usar o conceito de projeção barycentric. Como antes, para um determinado ponto de entrada (x1,..., Xn), primeiro determine em qual tetraedro ele se encontra ou, de forma equivalente, o σ de permutação correspondente. Em seguida, execute uma série de projeções barycentric, da seguinte maneira. A primeira projeção ![Mostra o subscript BProj 1 (x).](images/transformcreation-image081.gif) envia o ponto para o plano ![Mostra o Delta de subscript X (1) igual a 0.](images/transformcreation-image083.gif) apenas ![Mostra o X igual a V subscript n.](images/transformcreation-image085.gif) Nesse caso, ele não é alterado. A definição exata do BProj do mapa é definida da seguinte maneira:

![Mostra a equação para a definição exata do mapa BProj.](images/transformcreation-image087.png)

por ![Mostra a equação para o P subscript k.](images/transformcreation-image089.png) e k = 1, 2,..., n.

No caso ![Mostra X é igual a V subscript n.](images/transformcreation-image085.gif) , você pode parar, pois BC é definida em VN por pressuposição (a). No caso ![Mostra X não é igual a V subscript n.](images/transformcreation-image091.gif) , está claro que ![Mostra o subscript BProj 1 (X).](images/transformcreation-image081.gif) tem o σ (1) th Component Annihilated. Em outras palavras, ele está em uma das faces de limite. Ele está em uma face em que a BC é definida; nesse caso, você pode parar ou executar outra projeção barycentric ![Mostra o subscript BProj 2 (X ').](images/transformcreation-image093.gif) onde ![Mostra o X ' igual ao BProj 1 (X).](images/transformcreation-image095.gif) . E se ![Mostra o X ' ' = Bproj subscrito 1 (X ').](images/transformcreation-image097.gif) está em uma face em que a BC está definida, você pode parar; caso contrário, execute outra projeção ![Mostra o BProj subscript 3 (X ' ').](images/transformcreation-image099.gif) . Como cada projeção annihilates um componente, a dimensão efetiva diminui, portanto, você sabe que o processo deve eventualmente parar. No pior cenário, você executa n projeções à dimensão 0, ou seja, vértices no cubo, que de acordo com a suposição (c), você sabe que a BC será definida em.

Supondo que as projeções de K tenham sido executadas, com

![Mostra uma equação a ser usada supondo que a projeção K tenha sido executada.](images/transformcreation-image101.png)

x (0) = x, o ponto de entrada e BC é definido em x (k). Em seguida, desenrolar as projeções definindo uma série de vetores de saída:

![Mostra equações para uma série de vetores de saída.](images/transformcreation-image103.png)

onde ![Mostra a equação para o Y sobrescrito (K).](images/transformcreation-image105.gif) e, finalmente, obter a resposta

![Mostra interp (x) igual a y Superscript (0).](images/transformcreation-image107.gif)

## <a name="worked-example"></a>Exemplo trabalhado

![Diagrama que mostra um exemplo de interpolação trabalhado com um cubo de unidade.](images/transformcreation-image108.png)

**Figura 2:** Exemplo trabalhado

Considere a situação descrita na Figura 2, em que n = 3, m = 1, e você tem o seguinte BCs:

(a) quatro BCs discreto nos vértices

(0, 0, 1): β001

(0, 1, 1): β011

(1, 0, 1): β 101

(1, 1, 1): β 111

(b) uma BC contínua na face X3 = 0: F (x1, x2)

Computação \# 1: ponto de entrada x = (0,8, 0,5, 0,2). O tetraedro delimitador é associado à permutação &lt; 1, 2, 3 &gt; .

1ª projeção: ![Mostra a equação para a primeira projeção.](images/transformcreation-image110.png)

Isso já está na face X3 = 0, para que você possa parar. Em seguida, a substituição regressiva fornece

![Mostra a resposta para a primeira projeção.](images/transformcreation-image112.png) Qual é a resposta.

Computação \# 2: ponto de entrada x = (0,2, 0,5, 0,8). O tetraedro delimitador é associado à permutação &lt; 3, 2, 1 &gt; .

1ª projeção: ![Mostra a equação para a primeira projeção da computação 2.](images/transformcreation-image113.png)

2ª projeção: ![Mostra a equação para a segunda projeção da computação 2.](images/transformcreation-image115.png)

3ª projeção: ![Mostra a equação para a terceira projeção da computação 2.](images/transformcreation-image117.png) , que está na face X3 = 0. Em seguida, a substituição regressiva fornece

![Mostra as duas primeiras equações para a substituição retroativa.](images/transformcreation-image119.png)

![Mostra a terceira equação para a substituição retroativa.](images/transformcreation-image123.png), que é a resposta final.

## <a name="applications"></a>Aplicativos

*(a) interpolação tetrahedral sequencial*

![Diagrama que mostra a interpolação tetrahedral sequencial.](images/transformcreation-image124.png)

**Figura 3:** Interpolação tetrahedral sequencial

Consulte a Figura 3. Para interpolar entre dois planos nos quais as grades incompatíveis foram impostas, considere uma célula que está delimitando um determinado ponto P mostrado na figura. Os vértices "principais" da célula vêm diretamente da grade no plano superior. Os vértices na face inferior não são compatíveis com a grade no plano inferior, portanto, a face inteira é tratada como tendo uma BC com valores obtidos pela interpolação na grade no plano inferior. Em seguida, é claro que essa configuração atende às suposições (a), (b) e (c) acima, e você pode aplicar o algoritmo de interpolação.

Também é claro que o algoritmo reduziu a dimensão do problema de interpolação em 1, porque o resultado é uma combinação linear de valores nos vértices na grade superior e a interpolação no plano inferior, que tem a dimensão menos 1. Se uma configuração de plano de sanduíche semelhante existir no plano inferior, você poderá aplicar o procedimento nesse plano, reduzindo ainda mais a dimensão em 1. Este procedimento pode continuar até alcançar a dimensão 0. Essa cascata de projeções e interpolações pode ser chamada de "interpolação tetrahedral sequencial".

*(b) interpolação de lacunas*

![Diagrama que mostra a interpolação de lacunas.](images/transformcreation-image126.jpg)

**Figura 4:** Interpolação de lacunas

Essa é uma grade imposta em um cubo que fica estritamente dentro do quadrante positivo. O próprio cubo tem uma grade e cada plano de coordenadas tem grades que não são necessariamente compatíveis. A "lacuna" entre o cubo e os planos de coordenadas tem uma seção cruzada que é "em formato L" e não receptivos às técnicas padrão. No entanto, com a técnica apresentada aqui, você pode introduzir facilmente células que abordam essa lacuna. A Figura 4 descreve um deles. As grades nos planos de coordenadas dão suporte à interpolação que fornece o BCs necessário para todas as faces inferiores da célula, com um vértice restante cuja BC é fornecida pelo canto inferior do cubo.

## <a name="final-note-on-implementation"></a>Observação final sobre implementação

No aplicativo real, o "cubo de unidade" que é a configuração básica do algoritmo é extraído de lattices maiores, e os valores nos vértices podem exigir um cálculo caro. Por outro lado, também é claro que a interpolação tetrahedral requer apenas os valores nos vértices do tetraedro, que é um subconjunto de todos os vértices do cubo de unidade. Portanto, é mais eficiente implementar o que pode ser chamado de "avaliação adiada". Em uma implementação de software do algoritmo anterior, é comum ter uma sub-rotina que usa o cubo de unidade e os valores em seus vértices como entrada. A avaliação adiada significa que, em vez de passar os valores nos vértices, as informações necessárias para avaliar os valores dos vértices são passadas, sem realmente realizar a avaliação. Dentro da sub-rotina, a avaliação real desses valores será executada somente para os vértices que pertencem ao tetraedro delimitador, depois que a tetraedro de circunscrição for determinada.

## <a name="lookup-table-for-use-with-high-dynamic-range-virtual-rgb-source-devices"></a>Tabela de pesquisa para uso com dispositivos de origem RGB alta de intervalo dinâmico

No caso em que uma transformação é construída com um dispositivo de origem que é modelado como um dispositivo virtual RGB, é possível que os valores de Colorant de origem possam ser negativos ou maiores que Unity (1,0). Quando isso ocorre, o dispositivo de origem é referido como tendo um cabeçalho dinâmico alto (HDR). É feita uma consideração especial para esse caso.

No caso de transformações HDR, os valores mínimo e máximo para cada canal Colorant podem ser determinados a partir do limite de gama do dispositivo. Usando esses valores, um dimensionamento simples para cada canal de Colorant é aplicado de forma que os valores de Colorant iguais ao mínimo de Colorant sejam convertidos em 0,0, e os valores Colorant iguais ao máximo de Colorant seriam convertidos em 1,0, com um dimensionamento linear de valores entre o mapa linear entre 0,0 e 1,0.

### <a name="iccprofilefromwcsprofile"></a>ICCProfileFromWCSProfile

Como a principal finalidade desse recurso é oferecer suporte a versões anteriores ao vista do Windows, você deve gerar perfis ICC da versão 2,2, conforme definido em ICC de especificação ICC. 1:1998-09. Em determinados casos (consulte a tabela a seguir "dispositivo de linha de base para mapeamento de classe de perfil ICC"), você pode criar uma matriz ou um perfil ICC baseado em TRC de um perfil WCS. Em outros casos, o perfil ICC consiste em LUTs. O processo a seguir descreve como criar o AToB e o BToA LUTs. É claro que os perfis ICC também têm outros campos. Alguns dos dados podem ser derivados do perfil WCS. Para outros dados, você precisará desenvolver padrões inteligentes. Os direitos autorais serão atribuídos à Microsoft; Já que é a tecnologia da Microsoft que está sendo usada para criar o LUTs.

Esse design deve funcionar para todos os tipos de modelos de dispositivo, incluindo plug-ins. Desde que o plug-in tenha um modelo de dispositivo de linha de base associado, o tipo de dispositivo subjacente pode ser determinado.

A parte difícil de criar um perfil ICC é criar as tabelas de pesquisa AToB e BToA. Essas tabelas são mapeadas entre o espaço do dispositivo, por exemplo, RGB ou CMYK, e o espaço de conexão do perfil (PCS), que é uma variante de CIELAB. Isso é fundamentalmente o mesmo que o processo de gerenciamento de cores usado na transformação CITE para mapear do espaço do dispositivo para o espaço do dispositivo. No entanto, você deve ter as seguintes informações para fazer a transformação.

1) Referência as condições de exibição para os PCS.

2) Gama de PCS de referência.

3) O modelo de dispositivo que converte entre os valores de PCS e colorimetry.

O perfil WCS e seu CAM associado são fornecidos como parâmetros. Há dois modelos de dispositivo de linha de base que convertem entre colorimetry e a codificação de PCS. O motivo pelo qual você precisa de dois é explicado abaixo.

1) Você pode obter as condições de exibição de referência para os computadores da especificação de formato de perfil ICC. As informações fornecidas na especificação de formato de perfil ICC são suficientes para computar todos os dados necessários para inicializar o CAM usado pelo CMS. Para consistência e flexibilidade, essas informações são armazenadas em um perfil de cores WCS.

2) Você também pode usar um perfil WCS para armazenar amostras que definem a gama de referência dos PCS. O sistema de gerenciamento de cores CITE (CMS) tem duas maneiras de criar limites de gama. Uma é para obter uma amostra do espaço completo do dispositivo e usar o modelo do dispositivo para criar valores de medida. O segundo método é usar amostras medidas do perfil para criar um limite de gama de referência. Como a gama dos PCS ICC é muito grande para fazer uma gama de referência útil, o primeiro método é inadequado. Mas o segundo método é uma abordagem flexível e baseada em perfil. Para redefinir a gama dos PCS de referência, você pode alterar os dados de medida no perfil do dispositivo PCS.

3) Os PCS ICC são uma modelagem de um dispositivo ideal. Ao criar um modelo dos PCS como um dispositivo real, você pode aproveitar o processo de gerenciamento de cores usado no Smart CMM. Criar um modelo de dispositivo do colorimetry para a codificação de PCS é simples. Você simplesmente mapeia entre os valores colorimétrico verdadeiro e os valores codificados de PCS. Como a interface CMS para modelos de dispositivo oferece suporte apenas a valores XYZ, você também pode ter que mapear entre XYZ e LAB. Essa é uma transformação bem conhecida. Esse modelo é descrito no documento 2.2.02 "modelos de dispositivo de linha de base" nas seções 7,9 e 7,10.

Talvez seja necessário executar algum mapeamento de gama, se a gama do dispositivo for maior do que a gama dos PCS. O GMMs de linha de base pode ser usado para essa finalidade. Observe que um perfil ICC criado corretamente tem tabelas de pesquisa para as intenções de colorimétrico, perceptiva e saturação relativas, embora elas possam apontar para o mesmo LUT internamente.

![Diagrama que mostra a criação de um T o B L U T.](images/transformcreation-image128.png)

**Figura 5:** Criação de um AToB LUT

Esse processo é ilustrado na Figura 5. Primeiro, o modelo do dispositivo é inicializado a partir dos dados no perfil DM. Em seguida, construa um limite de gama de dispositivos da seguinte maneira. Uma amostragem de dados do modelo de dispositivo é executada por meio do modelo de dispositivo para obter dados colorimétrico. Os dados colorimétrico são executados por meio do CAM para criar dados de aparência. Os dados de aparência são usados para criar o limite de gama do dispositivo.

Em seguida, use dados do perfil de medição PCS de referência para criar um limite de gama para os PCS.

Use os dois limites de gama que acabamos de criar para inicializar um GMM. Em seguida, use o modelo de dispositivo, o GMM e o modelo de dispositivo de PCS para criar uma transformação. Execute uma amostragem do espaço do dispositivo por meio da transformação para criar um AToB LUT.

![Diagrama que mostra a criação de um T o B L U T usando uma amostragem do espaço P C S.](images/transformcreation-image130.png)

**Figura 6:** Criação de um BToA LUT

A Figura 6 ilustra a criação do BToA LUT. Isso é quase idêntico à criação de um AToB LUT, com as funções de origem e de destino trocadas. Além disso, você deve exemplificar a gama de PCS completos para criar o LUT.

Observe que, como o CAM (CIECAM02 no WCS) está envolvido no processo, a adaptação de desvio entre o ponto branco de mídia e o ponto branco dos PCS (exigido pelo ICC para ser o de D50) é afetada de forma transparente pelo CAM.

## <a name="hdr-virtual-rgb-devices"></a>Dispositivos do HDR virtual RGB

É necessário fornecer uma consideração especial ao gerar perfis para dispositivos do HDR virtual RGB; ou seja, dispositivos para os quais os valores de Colorant podem ser inferiores a 0,0 ou maiores que 1,0. Na geração do ATOB LUT, um conjunto maior de entrada 1D LUTs é criado. Os valores de Colorant são dimensionados e deslocados para o intervalo 0.. 1 usando os valores mínimo e máximo de Colorant no perfil WCS.

Como o espaço Colorant para dispositivos HDR não é provavelmente preenchido completamente, o suporte especial é fornecido no LUT 3-D para a marca também. Para lidar com cores na região preenchida de forma grosseira, os colorants são recodificados para que a extrapolação além de 0,0 e 1,0 possa ser obtida. O intervalo usado é-1.. + 4.

Devido ao redimensionamento aplicado para o LUT 3D, um conjunto de LUTs de saída 1D é criado para mapear o resultado de volta para o intervalo 0.. 1.

## <a name="more-than-one-pcs"></a>Mais de um PC

O ICC descobriu que um dos PCS não era suficientemente flexível para atender a todos os usos pretendidos de um CMS. Na versão 4 da especificação do perfil, o ICC esclareceu que há, na verdade, duas codificações de PCS. Um é usado para as intenções de colorimétrico; outro é usado para a intenção perceptiva. (Nenhum PC é especificado para a intenção de saturação. O ICC saiu dessa parte de forma ambígua.) Os PCS colorimétricos têm uma claridade mínima e máxima especificada, mas os valores de croma e de matiz variam de aproximadamente ± 127. Esse PCS é semelhante a um prisma retangular. Como mencionado anteriormente, o volume dos PCS perceptivas se assemelha à gama de uma impressora de jato de Radio.

Os dois PCSs ICC também têm duas codificações digitais diferentes. Nos PCS perceptiva, um valor de zero representa uma claridade de zero. Nos PCS colorimétricos, um valor de zero representa a claridade mínima dos PCS, que é maior que zero. Você pode resolver esse problema tendo um modelo de dispositivo diferente para cada uma das codificações de PCS.

## <a name="gamut-mapping"></a>Mapeamento de gamut

Para criar o AToB LUTs em um perfil ICC, você mapeia da gama do dispositivo para o espaço apropriado dos PCS. Para criar o BToA LUTs, você mapeia do espaço dos PCS para a gama do dispositivo. O mapeamento para o AToB LUTs é bastante semelhante ao usado em um CMS baseado em medição. Para os PCS perceptiva, mapeie a gama plausível do dispositivo para o limite de gama dos PCS perceptiva, usando recorte ou compactação para qualquer cor fora do gamut. Para as intenções de colorimétrico, talvez seja necessário recortar a claridade, mas os valores de croma e de matiz serão ajustados para a gama de PCS colorimétricos.

O mapeamento para o BToA LUTs é um pouco diferente. As intenções de colorimétrico ainda são fáceis; Você apenas corta os valores de PCS para a gama do dispositivo. Mas o ICC requer que todos os valores de PCS possíveis sejam mapeados para algum valor de dispositivo, não apenas aqueles dentro da gama de referência dos PCS perceptiva. Portanto, você deve garantir que o GMMs possa manipular as cores de origem que estão fora da gama de referência. Isso pode ser tratado recortando essas cores para o limite de gama do dispositivo.

## <a name="baseline-device-to-icc-profile-class-mapping"></a>Mapeamento de classe de dispositivo de linha de base para perfil ICC



| Tipo de dispositivo de linha de base              | Classe de perfil ICC       | Comentário                                                                      |
|-----------------------------------|-------------------------|-----------------------------------------------------------------------------|
| Dispositivo de captura RGB                | Dispositivo de entrada ("scnr")   | PCS é CIELAB. AToB0Tag é o dispositivo para computadores com a intenção colorimétrico relativa. |
| Monitor CRT, LCD                  | Dispositivo de vídeo ("MNTR") | PCS é CIEXYZ. Consulte o seguinte para a conversão de modelo.                      |
| Projetor RGB                     | Espaço de cores ("spac")    | PCS é CIELAB.                                                              |
| Impressora RGB e CMYK              | Dispositivo de saída ("PRTR")  | PCS é CIELAB.                                                              |
| Dispositivo virtual RGB (caso não HDR) | Dispositivo de vídeo ("MNTR") | PCS é CIEXYZ.                                                              |
| Dispositivo virtual RGB (caso HDR)     | Espaço de cores ("spac")    | PCS é CIELAB.                                                              |



 

A conversão de perfis de monitor não envolve a criação de LUTs, mas, em vez disso, consiste em criar um modelo de matriz ou TRC. O modelo usado em ICC é ligeiramente diferente daquele usado na modelagem CRT ou LCD do WCS, no qual o termo "correção preta" está ausente. Especificamente:

Modelo WCS: ![Mostra um modelo W C S.](images/transformcreation-image132.png)

Modelo ICC: ![Mostra um modelo C C.](images/transformcreation-image134.png)

A conversão do modelo WCS para o modelo ICC é feita da seguinte maneira.

Definir novas curvas:

![Mostra uma matriz para definir novas curvas.](images/transformcreation-image136.png)

Elas não são curvas de reprodução de Tom porque não mapeiam 1 para 1. Uma normalização vai conseguir isso. As definições finais do modelo ICC são:

![Mostra as definições finais do modelo C C.](images/transformcreation-image138.png)

![Mostra a matriz final para o modelo I c C.](images/transformcreation-image140.png)

Para dispositivos virtuais RGB não HDR, você também está gerando um perfil de vídeo ICC para a eficiência do espaço. Nesse caso, o ICC da matriz *M* triestímulo pode ser obtido diretamente dos primários do perfil WCS sem a conversão do modelo acima. Uma das finalidades, mas importante, é que essa matriz de triestímulo deve ser adaptada de acordo com o D50 para estar em conformidade com a especificação ICC dos PCS. Em outras palavras, as entradas em cada linha da matriz a ser codificada no perfil ICC devem ser somadas, respectivamente, a 96,42, 100 e 82,49. Na implementação atual, a adaptação de desvio é feita por CAT02, que também é a transformação de adaptação de desvio usada em CAM02.

## <a name="black-preservation-and-black-generation"></a>Preservação de preto e geração de preto

A implementação da preservação de preto está ligada junto à geração do canal preto em dispositivos que dão suporte a um canal preto. Para fazer isso, as informações sobre cada cor de origem são coletadas para permitir que os modelos de dispositivos que dão suporte a um canal preto determinem a melhor maneira de definir o canal preto na saída. Embora a preservação de preto seja pertinente para transformações de cor que convertem entre um dispositivo de canal preto em outro, a geração de preto é implementada para toda a transformação que envolve um dispositivo de destino de canal preto.

As informações do canal preto são registradas em uma estrutura de dados chamada [**BlackInformation**](/previous-versions/windows/desktop/api/WcsPlugIn/ns-wcsplugin-_blackinformation). A estrutura **BlackInformation** contém um booliano que indica se a cor contém apenas preto Colorant e um valor numérico que indica o grau de "preto" chamado peso preto. Para dispositivos de origem que dão suporte a um canal preto, o peso preto é a porcentagem de Colorant preta na cor de origem. Para dispositivos de origem que não contêm um canal preto, o peso preto é calculado usando o outro colorants e o valor de aparência. Um valor chamado "pureza de cores" é calculado com a diferença entre o valor máximo de Colorant e o valor de Colorant mínimo dividido pelo valor máximo de Colorant. Um valor chamado "claridade relativa" é calculado com a diferença entre a claridade da cor e a claridade mínima para o dispositivo de destino dividido pela diferença entre a claridade mínima e a máxima para o dispositivo de destino. Se o dispositivo de origem for um dispositivo aditivo (monitor ou projetor), o peso preto será determinado como 1,0 menos a pureza de cor multiplicada pela claridade relativa. Por exemplo, se o dispositivo de origem for um monitor RGB, o valor máximo e o valor mínimo de R, G e B para cada cor serão computados e o peso preto será determinado pela fórmula:

BW = (1,0 – (Max (R, G, B) – min (R, G, B))/Max (R, G, B)) \* claridade relativa

Se o dispositivo de origem oferecer suporte a coloração subtraíis, por exemplo, uma impressora CMY, os colorants individuais deverão ser "aqueles complementados" (subtraídos de 1,0) antes do uso na fórmula anterior. Portanto, para uma impressora CMY, R = 1,0 – C, G = 1,0 – M e B = 1,0 – Y.

As informações pretas para cada cor processada pela transformação de cor são determinadas durante o processo de tradução de cores. As informações somente em preto só serão determinadas se a preservação de preto for especificada. O peso preto é sempre determinado se o modelo do dispositivo de destino dá suporte a um Colorant preto. As informações pretas são passadas para o modelo de dispositivo de destino por meio do método [**ColorimetricToDeviceColorsWithBlack**](/previous-versions/windows/desktop/api/WcsPlugIn/nf-wcsplugin-idevicemodelplugin-colorimetrictodevicecolorswithblack) , que usa o lut resultante.

Observe que, devido à otimização de transformação de cor, o processo acima ocorre somente durante a criação do LUT de transformação otimizado, não durante a execução do método TranslateColors.

## <a name="optimization-for-transforms-with-more-than-three-source-channels"></a>Otimização para transformações com mais de três canais de origem

O tamanho da transformação otimizada é determinado por vários fatores: o número de canais de cores no dispositivo de origem, o número de etapas na tabela para cada canal de cor de origem e o número de canais de cores no dispositivo de saída. A fórmula para determinar o tamanho da tabela de transformação é:

Tamanho = número de etapas por fonte de canal <sub>\ dispositivo (número \ de \ canais \ no \ fonte \ dispositivo)</sub> x número de canais no dispositivo de saída

Como você pode ver, o tamanho da tabela aumenta exponencialmente dependendo do número de canais no dispositivo de origem. Muitos dispositivos de origem dão suporte a três canais de cores, por exemplo, vermelho, verde e azul. No entanto, se um dispositivo de origem dá suporte a quatro canais, como CMYK, o tamanho da tabela e o tempo necessário para construir a tabela crescem por um fator do número de etapas. Em um CMS baseado em medida em que as transformações são construídas imediatamente ", esse tempo pode ser bem inaceitável.

Para reduzir o tempo necessário para construir a tabela de conversão de cores, é possível tirar proveito de dois fatos. Primeiro, embora o dispositivo de origem possa dar suporte a mais de três canais de cores, o espaço de cores independente de dispositivo intermediário (CIECAM02 ja <sub>c</sub> b <sub>C</sub> ) tem apenas três canais de cor. Segundo, a parte mais demorada do processamento não é a modelagem de dispositivo (convertendo de coordenadas de cores do dispositivo em valores de triestímulo), mas o mapeamento de gamut. Usando esses fatos, você pode construir uma tabela de conversão de cores preliminar que converte cores no espaço de cores independente do dispositivo por meio das etapas de mapeamento de gamut e, finalmente, por meio do modelo de cores do dispositivo de saída. A construção dessa tabela é da dimensão três. Em seguida, construímos a tabela de conversão de cores final da dimensão convertendo as combinações de cores de origem em um espaço intermediário independente do dispositivo e, em seguida, usando a tabela de conversão de cores preliminar, conclua a conversão para o espaço de cores do dispositivo de saída. Portanto, você reduz da computação (número de etapas na tabela de pesquisa) <sub>número \ de \</sub> cálculos de mapeamento de gama de canais para o número de etapas na tabela intermediária ₃ cálculos de mapeamento de gamut. Mesmo que você precise executar o número de etapas na (tabela de pesquisa) <sub>número de</sub> computações de canais de modelagem de dispositivo e pesquisas de tabela tridimensionais, isso ainda é muito mais rápido do que o cálculo original.

O processo anterior funcionará bem, desde que não haja necessidade de informações a serem passadas entre o modelo do dispositivo de origem e qualquer outro componente na transformação de cores. No entanto, se o dispositivo de saída e o dispositivo de origem forem compatíveis com um Colorant preto e a Colorant preta de origem for usada para determinar a saída de Colorant preta, o processo não conseguirá comunicar corretamente as informações pretas de origem. Um processo alternativo é construir uma tabela de conversão de cores preliminar que converta as cores no espaço de cores independente do dispositivo somente por meio das etapas de mapeamento de gamut. Em seguida, construa a dimensão de quatro tabelas de conversão de cor final usando as seguintes etapas: a) converta as combinações de cores de origem para o espaço independente de dispositivo intermediário, b) execute as etapas de mapeamento de gama interpolando na tabela de cores preliminar em vez de aplicar os processos de mapeamento de gamut reais e c) Use os valores resultantes das etapas de mapeamento de gamut e qualquer informação de canal preto de origem para calcular o dispositivo de saída colorants usando o modelo de dispositivo de Esse processo também pode ser usado quando há informações transferidas entre os modelos de dispositivo de origem e saída, mesmo que não haja um canal preto; por exemplo, se os dois módulos forem implementados com uma arquitetura de plug-in que permita o intercâmbio de dados entre os módulos.

Os dois processos anteriores podem ser usados para melhorar efetivamente o tempo necessário para construir a tabela de transformação de cor de quatro dimensões.

### <a name="checkgamut"></a>CheckGamut

O ICM chama CreateTransform e **CreateMultiProfileTransform** pegar uma palavra de valores de sinalizador, uma das quais é habilitar a \_ verificação de GAMUT \_ . Quando esse sinalizador é definido, CITE deve criar a transformação de forma diferente. As etapas iniciais são as mesmas: o câmeras de origem e o de destino devem ser inicializados, e os descritores de limite de gamut de origem e destino devem ser inicializados. Independentemente da intenção especificada, o CheckGamut GMM deve ser usado. O CheckGamut GMM deve ser inicializado usando os modelos de dispositivo de origem e de destino e os descritores de limite de gamut. No entanto, a transformação deve criar uma transformação truncada que inclui o modelo do dispositivo de origem, a CAM de origem, qualquer GMMs intermediária e CheckGamut GMM. Isso garante que os valores Delta J, Delta C e Delta h sejam impressos pelo CheckGamut CMM se tornarem os valores finais resultantes.

O significado de CheckGamut é claro quando há apenas dois perfis de dispositivo na transformação. Quando há mais de dois perfis de dispositivo e mais de dois GMMs, o CheckGamut relata se as cores que foram transformadas por meio do primeiro modelo de dispositivo e todos os últimos GMM estão dentro da gama do dispositivo de destino.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conceitos básicos de gerenciamento de cores](basic-color-management-concepts.md)
</dt> <dt>

[Algoritmos e esquemas do sistema de cores do Windows](windows-color-system-schemas-and-algorithms.md)
</dt> </dl>

 

 




