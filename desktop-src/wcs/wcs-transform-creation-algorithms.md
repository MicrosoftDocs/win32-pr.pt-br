---
title: Algoritmos de criação de transformação do WCS
description: Algoritmos de criação de transformação do WCS
ms.assetid: 526bbbfc-fb60-415d-b4f0-6a44a5d11a55
keywords:
- Windows Sistema de cores (WCS), criação de transformação
- WCS (Windows sistema de cores), criação de transformação
- gerenciamento de cores de imagem, criação de transformação
- gerenciamento de cores, criação de transformação
- cores, criação de transformação
- criação de transformação
- Criação de transformação WCS
- algoritmos, criação de transformação
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df199f0fa649e7ce545a7b371f1caba65686746766f5572bac8e43b47413eace
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118445417"
---
# <a name="wcs-transform-creation-algorithms"></a>Algoritmos de criação de transformação do WCS

[Criação de transformações](#creation-of-transforms)

 

[Execução de transformação sequencial](#sequential-transform-execution)

 

[Criação de transformações otimizadas](#creation-of-optimized-transforms)

 

[ICCProfileFromWCSProfile](#iccprofilefromwcsprofile)

 

[Preservação de preto e geração de preto](#black-preservation-and-black-generation)

 

[Gama de cheques](#checkgamut)

## <a name="creation-of-transforms"></a>Criação de transformações

para explicar corretamente como as transformações de cores funcionam, é útil explicar o caminho completo de processamento por meio do ICM 2,0 e dos internos da CTE. a função ICM 2,0 [**CreateColorTransformW**](/windows/win32/api/icm/nf-icm-createcolortransformw) cria uma transformação de cor que os aplicativos podem usar para executar o gerenciamento de cores. Essa função cria um contexto de cor das entradas [**LOGCOLORSPACE**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea) e de intenção. As tentativas são mapeadas para o algoritmo de mapeamento de gamut de ICC de linha de base. em seguida, a função chama ICM função 2,0 [**CreateMultiProfileTransform**](/windows/desktop/api/Wingdi/) para processamento de cores consistente. A função **CreateColorTransform** geralmente copia dados para a estrutura de transformação otimizada interna.

a função ICM 2,0 CreateMultiProfileTransform aceita uma matriz de perfis e uma matriz de tentativas ou um único perfil de link de dispositivo e cria uma transformação de cor que os aplicativos podem usar para executar o mapeamento de cores. Ele processa os perfis de entrada e as intenções para criar modelos de dispositivo, modelos de aparência de cores, descrições de limites de gamut e modelos de mapeamento de gamut. Veja como isso é feito:

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

a função [**TranslateColors**](/windows/win32/api/icm/nf-icm-translatecolors) da API do ICM 2,0 converte uma matriz de cores do espaço de [cor](c.md) de origem para o espaço de cores de destino, conforme definido por uma transformação de cor. Essa função verifica internamente uma matriz de cores em cache para permitir a correspondência imediata de cores transformadas normalmente. Essa transformação dá suporte a matrizes de bytes por canal de 8 bits e a matrizes float de 32 bits por canal. Todos os outros formatos serão convertidos antes de serem transmitidos para a nova CTE.

a função [**TranslateBitmapBits**](/windows/win32/api/icm/nf-icm-translatebitmapbits) da API do ICM 2,0 converte as cores de um bitmap que tem um formato definido para produzir outro bitmap em um formato solicitado. Essa função verifica internamente uma matriz de cores em cache para permitir a correspondência imediata de cores transformadas normalmente. Para evitar muitos caminhos de código, suporte e complexidade de teste, apenas um número limitado de formatos de bitmap, na verdade, tem suporte no mecanismo de transformação e de interpolação. Essa função deve converter os formatos de bitmap de entrada e saída não nativos em formatos com suporte nativo para processamento. Essa transformação dá suporte apenas a bitmaps de 8 bits por byte de canal e bitmaps float de 32 bits por canal. Todos os outros formatos serão convertidos antes de serem transmitidos para a nova CTE.

 

### <a name="sequential-transform-execution"></a>Execução de transformação sequencial

se o parâmetro *dwFlags* tiver o bit de transformação sequencial \_ definido quando as funções de ICM [**CreateColorTransformW**](/windows/win32/api/icm/nf-icm-createcolortransformw) ou **CreateMultiProfileTransform** forem chamadas, as etapas de transformação serão executadas em sequência. Isso significa que o código percorre cada modelo de dispositivo, modelo de aparência de cor e modelo de mapeamento de gamut separadamente, conforme especificado pela chamada **CreateColorTransform** ou **CreateMultiProfileTransform** . Isso pode ser útil para depurar módulos de plug-in, mas é muito mais lento do que a execução por meio de uma transformação otimizada. A execução em modo sequencial, portanto, não é recomendada para software de produção. Além disso, pode haver pequenas diferenças nos resultados obtidos no modo sequencial e no modo otimizado. Isso ocorre devido a variações introduzidas quando as funções são concatenadas juntas.

### <a name="creation-of-optimized-transforms"></a>Criação de transformações otimizadas

Uma transformação otimizada é uma tabela de pesquisa multidimensional. A tabela pode ser processada por um mecanismo de interpolação multidimensional, como interpolação tetrahedral, que aplica as cores de entrada à transformação. A seção a seguir descreve como as tabelas de pesquisa otimizadas são criadas. A seção depois descreve como interpolar dentro das tabelas de pesquisa otimizadas.

## <a name="sparse-lookup-tables"></a>Tabelas de pesquisa esparsa

As impressoras convencionais têm tintas CMYK. Para estender a gama, uma abordagem é adicionar novas tintas ao sistema. As tintas normalmente adicionadas são cores que as tintas CMYK têm dificuldade de reproduzir. As opções comuns são laranja, verde, vermelho, azul etc. Para aumentar a "resolução aparente", as tintas com tons diferentes podem ser usadas, por exemplo, ciano claro, Magenta claro e assim por diante. Na verdade, o dispositivo de impressora tem mais de quatro canais.

Embora as impressoras sejam dispositivos de saída, elas também executam a conversão de cores do espaço do dispositivo para outro espaço de cores. No caso de uma impressora CMYK, essa seria uma transformação de CMYK para XYZ ou o "modelo de encaminhamento" da impressora. Ao combinar o modelo de encaminhamento com outras transformações, é possível emular uma impressão CMYK em outro dispositivo. Por exemplo, uma impressora CMYK para um monitor RGB tornaria possível um mecanismo de verificação que emulasse uma impressão da impressora CMYK em um monitor. Da mesma forma, o mesmo também se aplica a impressoras de Hi-Fi. Uma conversão de CMYKOG para RGB permite a prova da impressora CMYKOG em um monitor.

A abordagem convencional para implementar essa conversão de cores é usar um LUT uniforme. Por exemplo, em um perfil ICC para uma impressora CMYKOG, a especificação ICC exige uma marca A2B1 que armazena um LUT uniforme representando uma amostragem uniforme no espaço do dispositivo CMYKOG do modelo de encaminhamento, que passa de CMYKOG para o espaço de conexão do perfil ICC (CIELAB ou CIEXYZ). O perfil de link do dispositivo ICC permite uma transformação direta do espaço do dispositivo CMYKOG para qualquer espaço de cores, incluindo um espaço de dispositivo, também na forma de um LUT amostrado uniformemente no espaço CMYKOG. A amostragem nunca é feita com 256 níveis (profundidade de bit 8) devido ao enorme LUT resultante, exceto no caso de dispositivos monocromáticos (1 canal). Em vez disso, a amostragem com profundidade de bits inferior é usada; algumas opções típicas são 9 (profundidade de bits 3), 17 (profundidade de bits 4), 33 (profundidade de bit 5). Com o número de níveis inferior a 256 em cada canal, o LUT é usado em conjunto com um algoritmo de interpolação para produzir o resultado se um nível estiver entre dois níveis de amostra.

Embora um LUT uniforme seja conceitualmente simples de implementar, e a interpolação em um LUT uniforme é geralmente eficiente, o tamanho de LUT aumenta exponencialmente com a dimensão de entrada. Na verdade, se *d* for o número de etapas usadas no LUT uniforme e *n* for o número de canais no espaço de cores de origem, o número de nós no LUT será Mostrar a variável para o número de nós em um ![ ](images/transformcreation-image002.gif) LUT. . Claramente, o número de nós exige rapidamente tanto armazenamento na memória que até mesmo sistemas de computação de ponta têm dificuldade para lidar com a demanda. Para dispositivos com seis ou oito canais, uma implementação de ICC do perfil de dispositivo requer o uso de algumas etapas no LUT, às vezes até mesmo até cinco etapas na tabela A2B1 para manter o perfil em megabytes em vez de gigabytes. Claramente, o uso de um número menor de etapas aumenta o erro de interpolação, porque agora há menos amostras. Como o LUT deve ser uniforme, a precisão sobre todo o espaço de cores é degradada mesmo nessas regiões do espaço em que uma diferença de cor significativa pode ser causada por pequena alteração no valor do dispositivo.

Em dispositivos com mais de quatro colorantes, determinados subespaços de todo o espaço do dispositivo são mais importantes do que outros. Por exemplo, no espaço CMYKOG, tintas ciano e verde raramente são usadas juntas porque seus matizes se sobrepõem em grande parte uns aos outros. Da mesma forma, tintas amarelas e laranjas se sobrepõem em grande parte umas às outras. Uma redução uniforme no número de etapas pode ser vista como uma degradação geral na qualidade em todo o espaço de cores, que é algo que você pode dar às combinações de tinta improbáveis, mas não para combinações prováveis ou importantes.

Embora um LUT com amostra uniforme seja simples e eficiente para interpolação, ele impõe grandes requisitos de memória à medida que a dimensão aumenta. Na realidade, embora um dispositivo possa ter seis ou oito canais, eles raramente são usados simultaneamente. Na maioria dos casos, a transformação de cor de entrada para cor tem apenas alguns colorantes "ativos" e, portanto, reside em um espaço de cores dimensional inferior. Isso também significa que a interpolação pode ser feita com mais eficiência nesse espaço dimensional inferior porque a interpolação é mais rápida quando a dimensão é menor.

Portanto, a abordagem é estatizar todo o espaço do dispositivo em subespaços de várias dimensões. E como dimensões inferiores (que combinam três ou quatro colorantes) são mais importantes, ao retificar o espaço, você também pode aplicar taxas de amostragem diferentes; ou seja, um número diferente de etapas, para as partes; aumentando as taxas de amostragem para dimensões mais baixas, reduzindo-as para dimensões mais altas.

Para corrigir as notações, *n* é o número de canais no espaço de cor de origem da transformação de cores que você deseja amostrar. Você também pode se referir a *n* como a dimensão de entrada e ![ Mostra n maior ou igual a 5.](images/transformcreation-image004.gif) , a menos que especificado de outra forma.

Os blocos de construção básicos são LUTs de várias dimensões e *tamanhos* de entrada, em vez de um LUT uniforme com a dimensão de entrada *n*. Para ser mais preciso, um *LUT* é uma rede retangular imposta a um cubo de unidade; ou seja, todas as coordenadas do dispositivo são normalizadas para o intervalo \[ 0, 1 \] ). se for a dimensão de entrada do lut (observe que não precisa ser igual a *n*, embora Mostre V menor ![ ou igual a n.](images/transformcreation-image006.gif) é necessário), em seguida, ele consiste em grades de amostragem unidimensionais:

Samp *i:* ![ mostra uma grade de amostragem unidimensional.](images/transformcreation-image008.gif)

em que todos *os x <sub>j</sub>s* devem estar no intervalo \[ 0, 1 \] , mostra um ![ superscrito d(i).](images/transformcreation-image010.gif) é o número de etapas para a *amostragem de i* canal que deve ser pelo menos 1 e Mostra um ![ spuperscript de X (subscrito) d(i).](images/transformcreation-image012.gif) deve ser 1. Por outro lado, Mostra ![ um superscrito X (subscrito 1).](images/transformcreation-image014.gif) não é necessário ser 0.

Somente os dois casos especiais de LUT a seguir serão definidos.

*LUT fechado:* esse é um LUT com o requisito adicional de que para cada Samp *<sub>i</sub>*, Mostra um X de sobrescrito ![ (subscrito 1) igual a 0.](images/transformcreation-image016.gif) e Mostra ![ um superscrito d(i) maior ou igual a 2.](images/transformcreation-image018.gif) . Um LUT fechado uniforme é um LUT fechado que tem o mesmo ![ Show a superscript d(i).](images/transformcreation-image010.gif) para cada canal e os nós têm um espaço uniforme entre 0 e 1.

*Abrir LUT:* este é um LUT com o requisito adicional de que para cada Samp *i*, ![ SHows a superscript X (subscript 1) maior que 0.](images/transformcreation-image020.gif) . Não há problema em mostrar ![ um superscrito d(i) igual a 1.](images/transformcreation-image022.gif) .

A meta é estatizar o cubo de unidade 0, 1 n em uma coleção de LUTs fechados e \[ \]  abrir LUTs, de forma que toda a coleção cobrirá o cubo de unidade. Conceitualmente, é mais simples organizar essas "camadas LUT" por suas dimensões, de modo que, no nível superior:

![Mostra o nível superior para organizar as camadas de L U T por suas dimensões.](images/transformcreation-image024.png)

em ![ que Mostra o subscrito sigma k.](images/transformcreation-image026.gif) é a "*coleção de camadas* k-dimensional". Observe que a dimensão de camadas começa em 3 em vez de 0; ou seja, pontos, porque a interpolação de combinações de três cores pode ser tratada sem muitos requisitos de memória.

## <a name="description-of-the-lut-strata"></a>Descrição da camada LUT

Nesta implementação:

1. ![Mostra o subscrito sigma 3.](images/transformcreation-image028.gif) consiste em LUTs fechados com três entradas, uma de cada combinação possível de três colorantes escolhidos entre os *n colorantes.*

2. ![Mostra o subscrito sigma 4.](images/transformcreation-image030.gif) consiste em um LUT fechado para a combinação de CMYK (ou os quatro primeiros colorantes), junto com ![Mostra (n sobre 4) menos 1.](images/transformcreation-image032.png) abra LUTs para todas as outras combinações de quatro cores. Ao destacar a combinação de CMYK, você reconhece que é uma combinação importante.

3. Para ![ Mostra k igual a 5, ..., n.](images/transformcreation-image034.gif) , ![ mostra o subscrito sigma k.](images/transformcreation-image026.gif) consiste em ![ Mostra (n sobre k).](images/transformcreation-image037.gif) abra LUTs, um para cada combinação possível de escolher *k* colorantes do total de *n colorantes.*

Ele permanece para especificar os tamanhos dos LUTs. A principal diferença entre LUTs abertos e fechados é que LUTs abertos não se sobrepõem e LUTs fechados podem se sobrepor às faces de limite. O fato de que a amostragem unidimensional em um LUT aberto não contém 0, essencialmente significa que um LUT aberto não tem metade das faces de limite, portanto, o nome "aberto". Se dois LUTs não se sobrepõem, você pode usar um número diferente de etapas ou locais de nó em cada canal. O mesmo não será verdadeiro se dois LUTs se sobrepõem. Nesse caso, se o número de etapas ou os locais de nó são diferentes, um ponto na interseção dos dois LUTs receberá um valor de interpolação diferente, dependendo de qual LUT é usado na interpolação. Uma solução simples para esse problema é usar a amostragem uniforme com o mesmo número de etapas sempre que dois LUTs se sobrepõem. Em outras palavras:

Todos os LUTs fechados (todos os LUTs de três cores e o LUT do CMYK nesta implementação) devem ser uniformes e ter o mesmo número de etapas, que são denotadas *d*.

Os dois algoritmos a seguir podem ser usados para determinar o número de etapas *d* para LUTs fechados e o número de etapas para LUTs abertos.

## <a name="algorithm-1"></a>Algoritmo \# 1

Esse algoritmo não requer entrada externa.

Todos os LUTs fechados serão uniformes com *o número* d de etapas.

Todos os LUTs abertos da dimensão *k* terão o mesmo número de etapas ![ Mostra d(k).](images/transformcreation-image039.gif) em cada canal de entrada, e os nós são espamados igualmente; ou seja, para cada ![ Mostra i igual a 1, 2, ..., k.](images/transformcreation-image041.gif) .

Samp *i:* ![ mostra o algoritmo samp i.](images/transformcreation-image043.png)

Por fim, *especifique* d e *d* (*k* ) na Tabela 1 a seguir. Os três modos, "proof", "normal" e "best" são as ICM de qualidade 2.0. Nessa implementação, o modo de prova tem o menor volume de memória e o melhor modo tem o maior volume de memória.

Para implementar esse algoritmo, você deve chamar o algoritmo \# 2 a seguir. Os usuários podem especificar seus próprios locais de amostragem, usando as tabelas como um guia.

## <a name="algorithm-2"></a>Algoritmo \# 2

Esse algoritmo requer entrada externa na forma de uma lista de locais de amostragem "importantes", mas é mais adaptável e pode economizar espaço de memória potencialmente.

A entrada necessária é uma matriz de valores de dispositivo fornecidos pelo usuário. Esses valores de dispositivo indicam qual região do espaço de cores do dispositivo é importante; ou seja, qual região deve ser amostrada mais.

Todos os LUTs fechados serão uniformes com *o número d* de etapas, conforme descrito no Algoritmo \# 1. Os valores *para d* são fornecidos na Tabela 1.

*(a) LUT fechado uniforme*



|         | Modo de prova | Modo Normal | Melhor modo |
|---------|------------|-------------|-----------|
| ***d*** | 9          | 17          | 33        |



 

*(b) Abrir LUT*



| Dimensão de entrada | Modo de prova | Modo Normal | Melhor modo |
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

## <a name="interpolation"></a>Interpolação

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

É útil formalizar o conceito de condições de limite antes de continuar. Para qualquer subconjunto S do limite da célula delimitada (o cubo de unidade em n dimensões), uma condição de limite em S é uma especificação de uma função BC: S → Rm, em que m é a dimensão de saída. Em outras palavras, um interpolador, que pode ser denotado Interp: \[ 0,1 n→ Rm, é necessário para \] satisfazer: Interp(x) = BC(x) para todos os x em S.

No cenário padrão de interpolação no cubo de unidade, S é o conjunto de pontos discretos que são os vértices 2n do cubo.

Agora você pode generalizar as condições de limite para resolver os problemas descritos anteriormente e fornecer um novo algoritmo de interpolação dentro do cubo de unidade. Em vez de permitir apenas pontos de limite discretos, as condições de limite podem ser impostas em uma face de limite inteira do cubo. As suposições precisas são as seguinte:

(a) O ponto vn =(1,1,...,1) é especial e apenas uma condição de limite discreto é permitida. Em outras palavras, nenhuma condição de limite contínua pode ser imposta nos n rostos de limite xi=1 (i=1,...,n).

(b) Para cada um dos n limites restantes faces xi=0 (i=1,...,n), a condição de limite pode ser imposta em todo o rosto, com a condição de compatibilidade de que, se duas faces intersecção, as condições de limite nos rostos devem concordar com a interseção.

(c) Quaisquer vértices não contidos nas faces com condição de limite terão uma condição de limite individual (discreta).

Você pode se referir a uma condição de limite discreto como dados finitos e a uma condição de limite contínua como dados transfinitos ao discutir interpolação em dados finitos e transfinitos.

Primeiro, revise a interpolação padrão dehedral (como a usada na patente de Sakaaka), que ajuda a definir as notações para essa formulação específica do problema. É conhecido que o cubo de \[ unidade 0,1 \] n pode ser subdividido em n! hedra, parametrizado pelo conjunto de permutações em n símbolos. Mais especificamente, cada talhedron é definido por desigualdades

![Mostra a fórmula para as desigualdades doshedrons.](images/transformcreation-image073.gif)

em que σ:{1,2,..,n}→{1,2,...,n} é uma permutação de "símbolos" 1, 2, ..., n, ou seja, é um mapeamento telesectivo do conjunto de n símbolos. Por exemplo, se n = 3 e σ = (3, 2, 1), o que significa σ(1)=3, σ(2)=2, σ(3)=1, ohedron correspondente é definido por z≥y≥x, em que a notação comum x, y, z é usada para x1, x2, x3. Observe que esseshedrons não são desconconfiados uns dos outros. Para fins de interpolação, os pontos em um rosto comum de dois nós distintos terão o mesmo valor de interpolação, independentemente de qualhedron é usado na interpolação. Ainda assim, no cenário padrão de interpolação em pontos finitos, para um determinado ponto de entrada (x1, ..., xn), primeiro determine em qualhedron ele está ou equivalentemente no σ de permutação correspondente e, em seguida, o interpolantehedral será definido como

![Mostra a equação que define o interpolante dehedral.](images/transformcreation-image075.png)

onde ![Mostra a equação para os vetores de base padrão.](images/transformcreation-image077.png) para i=1, ..., n e e1, ..., en são os vetores de base padrão. Antes de passar para a generalização, observe que v0, v1, ..., vn são os vtices dohedron e ![Mostra as coordenadas centradas em barras.](images/transformcreation-image079.png) são as "coordenadas barycentric".

Para o caso geral de BCs em faces de limite, você pode usar o conceito de projeção centrada em barras. Como antes, para um determinado ponto de entrada (x1, ..., xn), primeiro determine em qualhedron ele se encontra, ou equivalentemente, o valor de permutação correspondente σ. Em seguida, execute uma série de projeções centradas em barras, da seguinte forma. A primeira projeção ![Mostra o subscrito BProj 1 (x).](images/transformcreation-image081.gif) envia o ponto para o plano ![Mostra x delta de subscrito (1) igual a 0.](images/transformcreation-image083.gif) Se ![Mostra X igual ao subscrito V n.](images/transformcreation-image085.gif) nesse caso, ele não é alterado. A definição precisa do mapa BProj é definida da seguinte maneira:

![Mostra a equação para a definição precisa do mapa BProj.](images/transformcreation-image087.png)

por ![Mostra a equação do subscrito P k.](images/transformcreation-image089.png) e k = 1, 2, ..., n.

No caso ![Mostra que X é igual ao subscrito V n.](images/transformcreation-image085.gif) , você pode parar, porque BC é definido em vn por Suposição (a). No caso ![Mostra que X não é igual ao subscrito V n.](images/transformcreation-image091.gif) , está claro que ![Mostra o subscrito BProj 1 (X).](images/transformcreation-image081.gif) tem o σ(1)o componente anilado. Em outras palavras, ele está em uma das faces de limite. Ele está em um rosto no qual BC está definido, nesse caso, você pode parar ou executar outra projeção centrada em barras ![Mostra o subscrito BProj 2 (X').](images/transformcreation-image093.gif) onde ![Mostra X' igual ao subscrito BProj 1 (X).](images/transformcreation-image095.gif) . E se ![Mostra X''= Bproj subscrito 1 (X').](images/transformcreation-image097.gif) está em um rosto no qual BC está definido, você pode parar; caso contrário, execute ainda outra projeção ![Mostra o subscrito BProj 3 (X'').](images/transformcreation-image099.gif) . Como cada projeção anila um componente, a dimensão efetiva diminui, para que você saiba que o processo deve parar eventualmente. No pior cenário, você executa n projeções até a dimensão 0, ou seja, vértices no cubo, que, de acordo com a Suposição (c), você sabe que BC será definido.

Supondo que as projeções K foram executadas, com

![Mostra uma equação a ser usada supondo que a projeção K tenha sido executada.](images/transformcreation-image101.png)

x(0)= x, o ponto de entrada e BC é definido em x(k). Em seguida, desenrola as projeções definindo uma série de vetores de saída:

![Mostra equações para uma série de vetores de saída.](images/transformcreation-image103.png)

onde ![Mostra a equação do K (sobrescrito Y).](images/transformcreation-image105.gif) e você finalmente obtém a resposta

![Mostra Interp(x) igual a y superscript (0).](images/transformcreation-image107.gif)

## <a name="worked-example"></a>Exemplo trabalhado

![Diagrama que mostra um exemplo trabalhado de interpolação com um cubo de unidade.](images/transformcreation-image108.png)

**Figura 2:** Exemplo trabalhado

Considere a situação descrita na Figura 2, em que n = 3, m = 1 e você tem os seguintes BCs:

(a) Quatro BCs discretos nos vértices

(0, 0, 1): β001

(0, 1, 1): β011

(1, 0, 1): β101

(1, 1, 1): β111

(b) Um BC contínuo na face x3=0: F(x1, x2)

Computação \# 1: ponto de entrada x = (0,8, 0,5, 0,2). Ohedron delimitado está associado à permutação &lt; 1, 2, 3 &gt; .

1ª projeção: ![Mostra a equação para a primeira projeção.](images/transformcreation-image110.png)

Isso já está no rosto x3=0, portanto, você pode parar. A substituição regressiva, em seguida, fornece

![Mostra a resposta para a primeira projeção.](images/transformcreation-image112.png) que é a resposta.

Computação \# 2: ponto de entrada x = (0,2, 0,5, 0,8). Ohedron delimitado está associado à permutação &lt; 3, 2, 1 &gt; .

1ª projeção: ![Mostra a equação para a primeira projeção da computação 2.](images/transformcreation-image113.png)

2ª projeção: ![Mostra a equação para a segunda projeção da computação 2.](images/transformcreation-image115.png)

Terceira projeção: ![Mostra a equação para a terceira projeção da computação 2.](images/transformcreation-image117.png) , que está no rosto x3=0. A substituição regressiva, em seguida, fornece

![Mostra as duas primeiras equações para a substituição regressiva.](images/transformcreation-image119.png)

![Mostra a terceira equação para a substituição regressiva.](images/transformcreation-image123.png), que é a resposta final.

## <a name="applications"></a>Aplicativos

*(a) Interpolação sequencial dehedral*

![Diagrama que mostra interpolação sequencial dehedral.](images/transformcreation-image124.png)

**Figura 3:** Interpolação sequencial dehedral

Consulte a Figura 3. Para interpolar entre dois planos nos quais grades incompatíveis foram impostas, considere uma célula que inclui um determinado ponto P mostrado na figura. Os vértices "superior" da célula vêm diretamente da grade no plano superior. Os vértices na face inferior não são compatíveis com a grade no plano inferior, portanto, o rosto inteiro é tratado como tendo um BC com valores obtidos pela interpolação na grade no plano inferior. Em seguida, fica claro que essa configuração satisfaz suposições (a), (b) e (c) acima e você pode aplicar o algoritmo de interpolação.

Também é claro que o algoritmo reduziu a dimensão do problema de interpolação em 1, porque o resultado é uma combinação linear de valores nos vértices na grade superior e interpolação no plano inferior, que tem dimensão menor que 1. Se houver uma configuração de plano de sanduíche semelhante no plano inferior, você poderá aplicar o procedimento nesse plano, reduzindo ainda mais a dimensão em 1. Esse procedimento pode continuar até que você alcance a dimensão 0. Essa cascata de projeções e interpolações pode ser chamada de "Interpolação Sequencial deHedral".

*(b) Interpolação de lacunas*

![Diagrama que mostra interpolação de lacuna.](images/transformcreation-image126.jpg)

**Figura 4:** Interpolação de lacunas

Essa é uma grade imposta a um cubo que está estritamente dentro do quadrante positivo. O cubo em si tem uma grade e cada plano de coordenadas tem grades que não são necessariamente compatíveis. A "lacuna" entre o cubo e os planos de coordenadas tem uma seção cruzada que é "em forma de L" e não é acessível a técnicas padrão. No entanto, com a técnica introduzida aqui, você pode introduzir facilmente células que abrangem essa lacuna. A Figura 4 ilustra um deles. As grades nos planos de coordenadas suportam interpolação que fornece os BCs necessários para todas as faces inferiores da célula, com um vértice restante cujo BC é fornecido pelo canto inferior do cubo.

## <a name="final-note-on-implementation"></a>Observação final sobre a implementação

No aplicativo real, o "cubo de unidade" que é a configuração básica do algoritmo é extraído de grades maiores, e os valores nos vértices podem exigir um cálculo caro. Por outro lado, também fica claro que a interpolação dehedral requer apenas os valores nos vértices dohedron, que é um subconjunto de todos os vértices do cubo de unidade. Portanto, é mais eficiente implementar o que pode ser chamado de "avaliação adiada". Em uma implementação de software do algoritmo anterior, é comum ter uma sub-rotina que leva o cubo de unidade e os valores em seus vértices como entrada. A avaliação adiada significa que, em vez de passar os valores nos vértices, as informações necessárias para avaliar os valores dos vértices são passadas, sem realmente realizar a avaliação. Dentro da sub-rotina, a avaliação real desses valores será executada somente para os vértices que pertencem aohedron delimitado, depois que ohedron delimitado for determinado.

## <a name="lookup-table-for-use-with-high-dynamic-range-virtual-rgb-source-devices"></a>Tabela de busca para uso com dispositivos de origem RGB virtuais de alto intervalo dinâmico

No caso em que uma transformação é construída com um dispositivo de origem modelado como um dispositivo RGB virtual, é possível que os valores de coloração de origem possam ser negativos ou maiores que unity (1,0). Quando isso ocorre, o dispositivo de origem é chamado de HDR (alto intervalo dinâmico). É feita uma consideração especial para esse caso.

No caso de transformaçãos do HDR, os valores mínimo e máximo para cada canal colorido podem ser determinados no limite de jogos do dispositivo. Usando esses valores, um dimensionamento simples para cada canal colorido é aplicado para que os valores colorantes iguais ao colorante mínimo sejam convertidos em 0,0 e valores de coloração iguais ao máximo colorante seriam convertidos em 1,0, com um dimensionamento linear de valores entre para mapear linearmente entre 0,0 e 1,0.

### <a name="iccprofilefromwcsprofile"></a>ICCProfileFromWCSProfile

Como a principal finalidade desse recurso é dar suporte a versões anteriores ao Vista do Windows, você deve gerar perfis ICC da versão 2.2 conforme definido na Especificação ICC.1:1998-09. Em determinados casos (consulte a tabela a seguir "Mapeamento de classe de perfil do dispositivo de linha de base para o ICC"), você pode criar um perfil ICC baseado em matriz ou TRC de um perfil WCS. Em outros casos, o perfil ICC consiste em LUTs. O processo a seguir descreve como criar os LUTs AToB e BToA. É claro que os perfis ICC também têm outros campos. Alguns dos dados podem ser derivados do perfil do WCS. Para outros dados, você terá que desenvolver padrões inteligentes. Os direitos autorais serão atribuídos à Microsoft; uma vez que é a tecnologia da Microsoft que está sendo usada para criar os LUTs.

Esse design deve funcionar para todos os tipos de modelos de dispositivo, incluindo plug-ins. Desde que o plug-in tenha um modelo de dispositivo de linha de base associado, o tipo de dispositivo subjacente pode ser determinado.

A parte difícil da criação de um perfil ICC é criar as tabelas de AToB e de lookup BToA. Essas tabelas são mapeadas entre o espaço do dispositivo, por exemplo, RGB ou CMYK e o PCS (Espaço de Conexão de Perfil), que é uma variante do CIELAB. Isso é fundamentalmente o mesmo que o processo de gerenciamento de cores usado na transformação CITE para mapear do espaço do dispositivo para o espaço do dispositivo. No entanto, você deve ter as informações a seguir para fazer a transformação.

1) Condições de exibição de referência para o PCS.

2) Referência de jogos do PCS.

3) Modelo de dispositivo que é convertido entre valores de PCS e coloribilidade.

O perfil do WCS e seu CAM associado são fornecidos como parâmetros. Há dois modelos de dispositivo de linha de base que convertem entre colorimetry e a codificação PCS. O motivo pelo qual você precisa de dois é explicado abaixo.

1) Você pode obter as condições de exibição de referência para o PCS na especificação de formato de perfil ICC. As informações fornecidas na especificação de formato de perfil ICC são suficientes para calcular todos os dados necessários para inicializar o CAM usado pelo CMS. Para consistência e flexibilidade, essas informações são armazenadas em um perfil de cor do WCS.

2) Você também pode usar um perfil WCS para armazenar exemplos que definem a gama de referência do PCS. O CMS (sistema de gerenciamento de cores) CITE tem duas maneiras de criar limites de jogos. Uma delas é amostrar o espaço completo do dispositivo e usar o modelo de dispositivo para criar valores de medição. O segundo método é usar exemplos medidos do perfil para criar um limite de referência de jogos. Como o gamut do PCS ICC é muito grande para fazer uma referência útil, o primeiro método é inadequado. Mas o segundo método é uma abordagem flexível baseada em perfil. Para redefinir a gama de PCS de referência, você pode alterar os dados de medição no perfil do dispositivo PCS.

3) O ICC PCS é uma modelagem de um dispositivo ideal. Ao criar um modelo do PCS como um dispositivo real, você pode aproveitar o processo de gerenciamento de cores usado no CMM Inteligente. A criação de um modelo de dispositivo da colorimetria para a codificação do PCS é simples. Você simplesmente mapeia entre os valores colorimétricos verdadeiros e os valores codificados por PCS. Como a interface CMS para modelos de dispositivo dá suporte apenas a valores XYZ, talvez você também tenha que mapear entre XYZ e LAB. Essa é uma transformação conhecida. Esse modelo é descrito no documento 2.2.02 "Modelos de dispositivo de linha de base" nas seções 7.9 e 7.10.

Talvez seja preciso executar algum mapeamento de jogos se a gama do dispositivo for maior do que a gama do PCS. Os GMMs de linha de base podem ser usados para essa finalidade. Observe que um perfil ICC criado corretamente tem tabelas de análise para as intenções Colorimetric, Perceptual e Saturação Relativas, embora tudo isso possa apontar para o mesmo LUT internamente.

![Diagrama que mostra a criação de um A T o B L U T.](images/transformcreation-image128.png)

**Figura 5:** Criação de um LUT AToB

Esse processo é ilustrado na Figura 5. Primeiro, o modelo de dispositivo é inicializado a partir dos dados no perfil de DM. Em seguida, construa um limite de jogos de dispositivo da seguinte forma. Uma amostragem de dados do modelo de dispositivo é executado por meio do modelo de dispositivo para obter dados colorimétricos. Os dados colorimétricos são executados por meio do CAM para criar dados de aparência. Os dados de aparência são usados para criar o limite de jogos do dispositivo.

Em seguida, use dados do perfil de medição do PCS de referência para criar um limite de jogos para o PCS.

Use os dois limites de jogos criados para inicializar um GMM. Em seguida, use o modelo de dispositivo, o GMM e o modelo de dispositivo PCS para criar uma transformação. Execute uma amostragem do espaço do dispositivo por meio da transformação para criar um LUT AToB.

![Diagrama que mostra a criação de um A T o B L U T usando uma amostragem de espaço P C S.](images/transformcreation-image130.png)

**Figura 6:** Criação de um LUT BToA

A Figura 6 ilustra a criação do LUT BToA. Isso é quase idêntico à criação de um LUT AToB, com as funções de origem e destino trocadas. Além disso, você deve experimentar a gama completa de PCS para criar o LUT.

Observe que, como a CAM (CIECAM02 no WCS) está envolvida no processo, a adaptação chromatic entre o ponto branco de mídia e o ponto branco do PCS (determinado pelo ICC para ser o de D50) é efetivada de forma transparente pelo CAM.

## <a name="hdr-virtual-rgb-devices"></a>Dispositivos RGB virtuais do HDR

Uma consideração especial deve ser dada ao gerar perfis para dispositivos RGB virtuais HDR; ou seja, dispositivos para os quais os valores de coloração podem ser menores que 0,0 ou maior que 1,0. Na geração do ATOB LUT, um conjunto maior de LUTs de entrada 1D é criado. Os valores de coloração são dimensionados e deslocadas para o intervalo 0 .. 1 usando os valores de coloração mínimo e máximo no perfil WCS.

Como o espaço colorido para dispositivos HDR provavelmente não será preenchido completamente, o suporte especial também é fornecido no LUT 3D para a marca. Para manipular cores na região populada esparsamente, os colorantes são recodificados para que a extrapolação além de 0,0 e 1,0 possa ser alcançada. O intervalo usado é -1 .. +4.

Devido ao recalque aplicado para o LUT 3D, um conjunto de LUTs de saída 1D é criado para mapear o resultado de volta para o intervalo 0 .. 1.

## <a name="more-than-one-pcs"></a>Mais de um PCS

O ICC descobriu que um PCS não era suficientemente flexível para atender a todos os usos pretendido de um CMS. Na versão 4 da Especificação de Perfil, o ICC esclareceu que há, na verdade, duas codificações PCS. Um é usado para as intenções colorimétricas; outro é usado para a intenção perceptual. (Nenhum PCS é especificado para a intenção saturação. O ICC deixou essa parte ambígua.) O PCS colorimétrico tem uma leveza mínima e máxima especificada, mas os valores de chroma e matiz variam para aproximadamente ± 127. Esse PCS se parece com um prisma retangular. Conforme mencionado anteriormente, o volume de PCS perceptual é semelhante à gama de uma impressora inkjet.

Os dois PCSs ICC também têm duas codificações digitais diferentes. No PCS perceptível, um valor de zero representa uma leveza de zero. No PCS colorimétrico, um valor de zero representa a luz mínima do PCS, que é maior que zero. Você pode resolver esse problema tendo um modelo de dispositivo diferente para cada uma das codificações do PCS.

## <a name="gamut-mapping"></a>Mapeamento de jogos

Para criar os LUTs AToB em um perfil ICC, mapeie do dispositivo para o espaço do PCS apropriado. Para criar os LUTs BToA, você mapeia do espaço PCS para a gama de dispositivos. O mapeamento para LUTs AToB é bastante semelhante ao usado em um CMS baseado em medida. Para o PCS perceptual, mapeie a gama de dispositivos insustância para o limite de jogos pcs perceptível, usando recorte ou compactação para qualquer cor fora de jogo. Para as intenções colorimétricas, talvez seja preciso cortar a luz, mas os valores de chroma e matiz vão caber na gama de PCS colorimétrica.

O mapeamento para os LUTs BToA é um pouco diferente. As intenções colorimétricas ainda são fáceis; você apenas reclipe os valores de PCS para a gama de dispositivos. Mas o ICC requer que todos os valores de PCS possíveis mapeiem para algum valor de dispositivo, não apenas aqueles dentro da gama de referência do PCS perceptual. Portanto, você deve garantir que os GMMs possam manipular as cores de origem que estão fora da gama de referência. Isso pode ser tratado com o recorte dessas cores para o limite de jogos do dispositivo.

## <a name="baseline-device-to-icc-profile-class-mapping"></a>Mapeamento de classe de perfil do dispositivo de linha de base para o ICC



| Tipo de dispositivo de linha de base              | Classe de perfil ICC       | Comentário                                                                      |
|-----------------------------------|-------------------------|-----------------------------------------------------------------------------|
| Dispositivo de captura RGB                | Dispositivo de entrada ("scnr")   | PCS é CIELAB. AToB0Tag é Dispositivo para PCS com intenção colorimétrica relativa. |
| CRT, monitor de LCD                  | Exibir Dispositivo ("mntr") | PCS é CIEXYZ. Consulte o seguinte para conversão de modelo.                      |
| Projetor RGB                     | Espaço de Cores ("spac")    | PCS é CIELAB.                                                              |
| Impressora RGB e CMYK              | Dispositivo de saída ("prtr")  | PCS é CIELAB.                                                              |
| Dispositivo Virtual RGB (caso não HDR) | Exibir Dispositivo ("mntr") | PCS é CIEXYZ.                                                              |
| Dispositivo Virtual RGB (caso HDR)     | Espaço de Cores ("spac")    | PCS é CIELAB.                                                              |



 

A conversão de perfis de monitor não envolve a criação de LUTs, mas consiste na criação de uma matriz ou modelo TRC. O modelo usado no ICC é ligeiramente diferente do usado na modelagem CRT ou LCD do WCS, já que o termo "correção preta" está ausente. Especificamente:

Modelo do WCS: ![Mostra um modelo W C S.](images/transformcreation-image132.png)

Modelo ICC: ![Mostra um modelo de I C C.](images/transformcreation-image134.png)

A conversão do modelo do WCS para o modelo ICC é feita da seguinte forma.

Definir novas curvas:

![Mostra uma matriz para definir novas curvas.](images/transformcreation-image136.png)

Essas não são curvas de reprodução de tom porque não mapeiam 1 para 1. Uma normalização fará isso. As definições finais do modelo ICC são:

![Mostra as definições finais do modelo de I C C.](images/transformcreation-image138.png)

![Mostra a matriz final para o modelo de I C C.](images/transformcreation-image140.png)

Para dispositivos virtuais RGB não HDR, você também está gerando um perfil ICC de exibição para eficiência de espaço. Nesse caso, a matriz de trístimulo *M ICC* pode ser obtida diretamente dos primários do perfil WCS sem a conversão do modelo acima. Uma última, mas importante, observe que essa matriz de trístimulo deve ser adaptada de forma cromática a D50 para estar em conformidade com a especificação de ICC do PCS. Em outras palavras, as entradas em cada linha da matriz a ser codificada no perfil ICC devem somar respectivamente a 96,42, 100 e 82,49. Na implementação atual, a adaptação chromatic é feita pelo CAT02, que também é a transformação de adaptação chromatic usada no CAM02.

## <a name="black-preservation-and-black-generation"></a>Preservação de preto e geração de preto

A implementação da preservação de preto está vinculada à geração do canal preto em dispositivos que suportam um canal preto. Para fazer isso, as informações sobre cada cor de origem são coletadas para permitir que modelos de dispositivo que deem suporte a um canal preto determinem a melhor maneira de definir o canal preto na saída. Embora a preservação de preto seja pertinente para as transformaçãos de cores que convertem entre um dispositivo de canal preto em outro, a geração preta é implementada para toda a transformação que envolve um dispositivo de destino de canal preto.

As informações de canal preto são registradas em uma estrutura de dados chamada [**BlackInformation**](/previous-versions/windows/desktop/api/WcsPlugIn/ns-wcsplugin-_blackinformation). A **estrutura BlackInformation** contém um booliana que indica se a cor contém apenas coloração preta e um valor numérico que indica o grau de "negritude" chamado peso preto. Para dispositivos de origem que suportam um canal preto, o peso preto é o percentual de coloração preta na cor de origem. Para dispositivos de origem que não contêm um canal preto, o peso preto é calculado usando os outros colorantes e o valor de aparência. Um valor chamado " puridade de cor" é calculado com a diferença entre o valor de coloração máximo e o valor de colorante mínimo dividido pelo valor máximo do colorante. Um valor chamado "leveza relativa" é calculado pela diferença entre a luz da cor e a leveza mínima para o dispositivo de destino dividido pela diferença entre a luz mínima e a máxima para o dispositivo de destino. Se o dispositivo de origem for um dispositivo aditivo (monitor ou projetor), o peso preto será determinado como o 1,0 menos a luminosidade da cor multiplicada pela luz relativa. Por exemplo, se o dispositivo de origem for um monitor RGB, o valor máximo e o valor mínimo de R, G e B para cada cor serão computados e o peso preto será determinado pela fórmula:

BW = (1.0 – (max(R,G,B) – min(R,G,B)) / max(R, G, B)) \* leveza relativa

Se o dispositivo de origem for compatível com a coloração subtrativa, por exemplo, uma impressora CMY, os colorantes individuais deverão ser "complementos" (subtraídos de 1,0) antes do uso na fórmula anterior. Portanto, para uma impressora CMY, R = 1,0 – C, G = 1,0 – M e B = 1,0 – Y.

As informações pretas para cada cor processada pela transformação de cor são determinadas durante o processo de conversão de cores. As informações somente pretas só são determinadas se a preservação de preto for especificada. O peso preto é sempre determinado se o modelo de dispositivo de destino é suportado por um colorido preto. As informações pretas são passadas para o modelo de dispositivo de destino por meio do [**método ColorimetricToDeviceColorsWithBlack,**](/previous-versions/windows/desktop/api/WcsPlugIn/nf-wcsplugin-idevicemodelplugin-colorimetrictodevicecolorswithblack) que usa o LUT resultante.

Observe que, devido à otimização da transformação de cor, o processo acima ocorre somente durante a criação do LUT de transformação otimizado, não durante a execução do método TranslateColors.

## <a name="optimization-for-transforms-with-more-than-three-source-channels"></a>Otimização para transformação com mais de três canais de origem

O tamanho da transformação otimizada é determinado por vários fatores: o número de canais de cores no dispositivo de origem, o número de etapas na tabela para cada canal de cor de origem e o número de canais de cores no dispositivo de saída. A fórmula para determinar o tamanho da tabela de transformação é:

Tamanho = Número de etapas por origem de <sub>canal\ dispositivo (Número\ de\ canais\ in\ dispositivo de origem\ )</sub> x número de canais no dispositivo de saída

Como você pode ver, o tamanho da tabela aumenta exponencialmente dependendo do número de canais no dispositivo de origem. Muitos dispositivos de origem são compatíveis com três canais de cores, por exemplo, Vermelho, Verde e Azul. No entanto, se um dispositivo de origem dá suporte a quatro canais, como CMYK, o tamanho da tabela e o tempo necessário para construir a tabela aumentarão em um fator do número de etapas. Em um CMS baseado em medida em que as transformação são construídas "em tempo real", esse momento pode ser inaceitável.

Para reduzir o tempo necessário para construir a tabela de conversão de cores, é possível aproveitar dois fatos. Primeiro, embora o dispositivo de origem possa dar suporte a mais de três canais de cores, o espaço de cores intermediário independente do dispositivo (CIECAM02 Ja <sub>C</sub> b <sub>C</sub> ) tem apenas três canais de cores. Em segundo lugar, a parte mais demorada do processamento não é a modelagem do dispositivo (convertendo de coordenadas de cor do dispositivo em valores de trítulo), mas o mapeamento de jogos. Usando esses fatos, você pode construir uma tabela de conversão de cores preliminar que converte cores no espaço de cores independente do dispositivo por meio das etapas de mapeamento de jogos e, por fim, por meio do modelo de cor do dispositivo de saída. A construção dessa tabela é da dimensão três. Em seguida, construiremos a tabela de conversão de cores final da dimensão quatro convertendo as combinações de cores de origem em espaço intermediário independente do dispositivo e, em seguida, usando a tabela preliminar de conversão de cores, concluiremos a conversão no espaço de cores do dispositivo de saída. Portanto, você reduz da computação (número de etapas na tabela de pesquisa) <sub>number\ of\ channels</sub> gamut mapping computations to the number of steps in the intermediate table gamut mapping computations." Embora você tenha que executar várias etapas na (tabela de lookup) <sub>number\ of\ channels</sub> computations of device modeling and three-dimensional table lookups, isso ainda é muito mais rápido do que o cálculo original.

O processo anterior funcionará bem desde que não haja necessidade de passar informações entre o modelo de dispositivo de origem e qualquer outro componente na transformação de cores. No entanto, se o dispositivo de saída e o dispositivo de origem deem suporte a um colorante preto de origem e o colorante preto de origem for usado para determinar o colorante preto de saída, o processo não comunicará corretamente as informações pretas de origem. Um processo alternativo é construir uma tabela de conversão de cores preliminar que converte cores no espaço de cores independente do dispositivo apenas por meio das etapas de mapeamento de jogos. Em seguida, construa a tabela de conversão de cores final da dimensão quatro usando as seguintes etapas: a) converter as combinações de cores de origem em espaço independente de dispositivo intermediário, b) execute as etapas de mapeamento de jogos interpolando na tabela de cores preliminares em vez de aplicar os processos reais de mapeamento de gamut e c) use os valores resultantes das etapas de mapeamento de jogos e qualquer informação de canal preto de origem para calcular os colorantes do dispositivo de saída usando o modelo de dispositivo de saída. Esse processo também pode ser usado quando há informações transferidas entre os modelos de dispositivo de origem e saída, mesmo se não houver nenhum canal preto; por exemplo, se os dois módulos são implementados com uma arquitetura de plug-in que permite o intercâmbio de dados entre módulos.

Os dois processos anteriores podem ser usados para melhorar efetivamente o tempo necessário para construir a tabela de transformação de cores quatrodimensionais.

### <a name="checkgamut"></a>CheckGamut

As ICM chamadas CreateTransform e **CreateMultiProfileTransform** levam uma palavra de valores de sinalizador, um dos quais é ENABLE \_ GAMUT \_ CHECKING. Quando esse sinalizador é definido, o CITE deve criar a transformação de maneira diferente. As etapas iniciais são as mesmas: os CAMs de origem e de destino devem ser inicializados e, em seguida, os descritores de limite de gama de origem e destino devem ser inicializados. Independentemente da intenção especificada, o GMM CheckGamut deve ser usado. O GMM CheckGamut deve ser inicializado usando os modelos de dispositivo de origem e de destino e descritores de limite de gama. No entanto, a transformação deve criar uma transformação truncada que inclui o modelo de dispositivo de origem, o CAM de origem, os GMMs intermediárias e o GMM CheckGamut. Isso garante que os valores delta J, delta C e delta h saída pelo CMM CheckGamut se tornem os valores finais resultantes.

O significado de CheckGamut fica claro quando há apenas dois perfis de dispositivo na transformação. Quando há mais de dois perfis de dispositivo e mais de dois GMMs, CheckGamut informa se as cores que foram transformadas por meio do primeiro modelo de dispositivo e todos, menos o último GMM, se enquadram no gamut do dispositivo de destino.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conceitos básicos de gerenciamento de cores](basic-color-management-concepts.md)
</dt> <dt>

[Algoritmos e esquemas do sistema de cores do Windows](windows-color-system-schemas-and-algorithms.md)
</dt> </dl>

 

 




