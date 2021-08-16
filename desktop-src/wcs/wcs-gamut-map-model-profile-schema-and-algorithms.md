---
title: Algoritmo e esquema do perfil do modelo de mapa de gamut do WCS
description: Algoritmo e esquema do perfil do modelo de mapa de gamut do WCS
ms.assetid: 64b9871a-1b4f-4e9a-be4d-4c25b3198b91
keywords:
- Windows Sistema de cores (WCS), perfil de modelo de mapa de gamut (GMMP)
- WCS (Windows sistema de cores), perfil de modelo de mapa de gamut (GMMP)
- gerenciamento de cores de imagem, perfil de modelo de mapa de gamut (GMMP)
- gerenciamento de cores, perfil de modelo de mapa de gamut (GMMP)
- cores, perfil de modelo de mapa de gamut (GMMP)
- Windows Sistema de cores (WCS), perfis
- WCS (Windows sistema de cores), perfis
- gerenciamento de cores de imagem, perfis
- gerenciamento de cores, perfis
- cores, perfis
- Perfil de modelo de mapa de gamut (GMMP)
- GMMP (perfil de modelo de mapa de gamut)
- Perfil do modelo de mapa de gamut WCS
- esquemas, perfil de modelo de mapa de gamut (GMMP)
- algoritmos, perfil de modelo de mapa de gamut (GMMP)
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7db5b7a26fe5832fe33095c5785e90ad0a6938649878ff279e101a7e5817cc4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118037149"
---
# <a name="wcs-gamut-map-model-profile-schema-and-algorithms"></a>Algoritmo e esquema do perfil do modelo de mapa de gamut do WCS

-   [Visão geral](#overview)
-   [Arquitetura de perfil de modelo de mapa de gamut](#gamut-map-model-profile-architecture)
-   [Geração do limite de gama](#generation-of-the-gamut-boundary)
-   [O esquema GMMP](#the-gmmp-schema)
-   [Os elementos do esquema GMMP](#the-gmmp-schema-elements)
-   [GamutMapModel](#defaultbaselinegamutmapmodel-type)
    -   [Namespace](#namespace)
    -   [Versão](#version)
    -   [Documentação](#documentation)
    -   [Tipo de DefaultBaselineGamutMapModel](#defaultbaselinegamutmapmodel-type)
    -   [PlugInGamutMapType](#plugingamutmaptype)
    -   [ExtensionType](#extensiontype)
-   [Os algoritmos de linha de base GMMP](#the-gmmp-baseline-algorithms)
-   [Alinhando os eixos neutros](#aligning-the-neutral-axes)
    -   [Diferença mínima de cor (MinCD)](#minimum-color-difference-mincd)
    -   [BasicPhoto](#basicphoto)
    -   [Visão geral](#overview)
    -   [O caso de um único Shell de gamut](#the-case-of-single-gamut-shell)
    -   [Aprimoramento preto](#black-enhancement)
    -   [O caso de shells de gama dupla](#the-case-of-dual-gamut-shells)
    -   [Motivos para alterações das recomendações de CIE TC8-03](#reasons-for-changes-from-the-cie-tc8-03-recommendations)
    -   [Mapeamento de matiz](#hue-mapping)
-   [Descrição de limite de gama e algoritmos de Shell de gamut](#gamut-boundary-description-and-gamut-shell-algorithms)
    -   [Triangulação do limite de gama](#triangulation-of-the-gamut-boundary)
    -   [Elementos de linha de limite](#boundary-line-elements)
    -   [Operação de gama: CheckGamut](#gamut-operation-checkgamut)
    -   [Plano de matiz completo: Intersect](#full-hue-plane-intersect)
    -   [Operação de gama: CheckGamut (continuação)](#gamut-operation-checkgamut-continued)
    -   [Mapeamento de gama da diferença de cor mínima](#minimum-color-difference-gamut-mapping)
    -   [Suavização de matiz](#hue-smoothing)
    -   [Definindo primárias e secundárias na descrição do limite de gama](#setting-primaries-and-secondaries-in-the-gamut-boundary-description)
    -   [Definindo o eixo neutro na descrição do limite de gama](#setting-the-neutral-axis-in-the-gamut-boundary-description)
-   [Tópicos relacionados](#related-topics)

## <a name="overview"></a>Visão geral

Esse esquema é usado para especificar o conteúdo de um perfil de modelo de mapa de gamut (GMMP). Os algoritmos de linha de base associados são descritos no tópico a seguir.

O esquema GMMP básico consiste em informações de cabeçalho comuns, uma referência opcional a um plug-in de modelo de mapa de gamut preferencial e marcas de extensão.

Além disso, o GMMP fornece informações explícitas sobre o modelo de mapa de gamut de destino e fornece uma política sobre o modelo de mapa de gamut de fallback de linha de base a ser usado se o modelo de destino não estiver disponível. O esquema pode incluir informações de extensão particulares, mas não incluirá nenhuma outra informação estranha.

## <a name="gamut-map-model-profile-architecture"></a>Arquitetura de perfil de modelo de mapa de gamut

![Diagrama que mostra o perfil de modelo de mapa de gamut.](images/gmmp-image002.png)

A amostragem do espaço de Colorant do dispositivo de saída é feita com a iteração pela colorants de 0,0 para 1,0 com uma etapa fracionária, acumulando todas as combinações de cada Colorant em cada etapa e, em seguida, convertendo-as do espaço de Colorant de dispositivo para o espaço de aparência de cores usando o método DM::D seguido pelo método CAM:: Evicetocolorimetriccolors. Veja a seguir um exemplo de como isso é feito para RGB.


```C++
For (red= 0.0; red <= 1.0; red += redStep) {

     For (green = 0.0; green <= 1.0; green += greenStep) {

          For (blue = 0.0; blue <= 1.0; blue += blueStep) {

               Colorants[0] = red; colorants[1] = green; colorants[2] = blue;

               pRGBDM->DeviceToColorimetricColors(1, colorants, &amp;XYZ);

               pCAM->ColorimetricToAppearanceColors(1, &amp;XYZ, &amp;JCh);

          }

     }

}

```



## <a name="generation-of-the-gamut-boundary"></a>Geração do limite de gama

Há três componentes para o limite de gama: os primários, os exemplos neutros e os shells. Os primários são gerados pela obtenção de primárias de dispositivo e aplicação da transformação DeviceToColorimetric/ColorimetricToAppearance. Os exemplos neutros são gerados pela amostragem do espaço do dispositivo Colorant na área neutra e pela aplicação da mesma transformação. Para três dispositivos Colorant (RGB ou CMY), os exemplos neutros são definidos como tendo todas as colorants iguais, por exemplo, R = = G = = B. Para CMYK, as amostras neutras são definidas como tendo C = = M = = Y = = 0.

Os fatores que influenciam os dados usados para criar o limite de gama são os exemplos de dados (somente dispositivos de linha de base) e as condições de exibição. O tamanho da etapa usada para fazer a amostragem completa do espaço Colorant (para monitores e para o Shell plausível) é uma constante interna e não está disponível para manipulação externa. Alterar as condições de exibição altera o comportamento do CAM (modelo de aparência de cor) e altera a forma do limite de gama, portanto, você deve gerar um limite de gama associado ao perfil de condições de exibição. Se os dados de exemplo forem usados, como no caso de impressoras de linha de base e dispositivos de captura, os exemplos terão um grande impacto na forma da gama de referência e afetarão o comportamento do próprio modelo.

Para dispositivos de entrada, como câmeras e scanners, diferentes amostras são usadas para gerar o Shell de referência e o Shell plausível. O Shell de referência é gerado a partir das medidas usadas para inicializar o modelo do dispositivo. O Shell plausível é gerado de forma semelhante à ilustração anterior para dispositivos de saída. A diferença que quando você insere um destino típico, você não obtém valores totalmente saturados (em que R, G ou B = 255). Você deve extrapolar usando o modelo de dispositivo para estimar esses valores.

## <a name="the-gmmp-schema"></a>O esquema GMMP


```C++
<?xml version="1.0" encoding="UTF-8"?>
<xs:schema 
  xmlns:gmm="http://schemas.microsoft.com/windows/2005/02/color/GamutMapModel"
  xmlns:wcs="http://schemas.microsoft.com/windows/2005/02/color/WcsCommonProfileTypes"
  targetNamespace="http://schemas.microsoft.com/windows/2005/02/color/GamutMapModel"
  xmlns:xs="http://www.w3.org/2001/XMLSchema"
  elementFormDefault="qualified"
  attributeFormDefault="unqualified"
  blockDefault="#all"
  version="1.0">

  <xs:annotation>
    <xs:documentation>
      Gamut Map Model profile schema.
      Copyright (C) Microsoft. All rights reserved.
    </xs:documentation>
  </xs:annotation>

  <xs:import namespace="http://schemas.microsoft.com/windows/2005/02/color/WcsCommonProfileTypes" />

  <xs:element name="GamutMapModel">
    <xs:complexType>
      <xs:sequence>
        <xs:element name="ProfileName" type="wcs:MultiLocalizedTextType"/>
        <xs:element name="Description" type="wcs:MultiLocalizedTextType" minOccurs="0"/>
        <xs:element name="Author" type="wcs:MultiLocalizedTextType" minOccurs="0"/>
        <xs:element name="DefaultBaselineGamutMapModel">
          <xs:simpleType>
            <xs:restriction base="xs:string">
              <xs:enumeration value="HPMinCD_Absolute"/>
              <xs:enumeration value="HPMinCD_Relative"/>
              <xs:enumeration value="SGCK"/>
              <xs:enumeration value="HueMap"/>
            </xs:restriction>
          </xs:simpleType>
        </xs:element>
        <xs:element name="PlugInGamutMapModel" minOccurs="0">
          <xs:complexType>
            <xs:sequence>
              <xs:any namespace="##other" processContents="skip"
                minOccurs="0" maxOccurs="unbounded" />
            </xs:sequence>
            <xs:attribute name="GUID" type="wcs:GUIDType" use="required"/>
          </xs:complexType>
        </xs:element>
      </xs:sequence>
      <xs:attribute name="ID" type="xs:string" use="optional" />
    </xs:complexType>
  </xs:element>
</xs:schema>
```



## <a name="the-gmmp-schema-elements"></a>Os elementos do esquema GMMP

## <a name="gamutmapmodel"></a>GamutMapModel

Esse elemento é uma sequência dos seguintes subelementos:

1.  Cadeia de caracteres ProfileName,
2.  DefaultBaselineGamutMapModel,
3.  Cadeia de caracteres de descrição opcional,
4.  Cadeia de caracteres de autor opcional,
5.  Opcional PlugInGamutMap e
6.  ExtensionType opcional.

**Condições de validação** : cada subelemento é validado por seu próprio tipo.

### <a name="namespace"></a>Namespace

xmlns: GMM = " http://schemas.microsoft.com/windows/2005/02/color/GamutMapModel "

targetNamespace = " http://schemas.microsoft.com/windows/2005/02/color/GamutMapModel "

### <a name="version"></a>Versão

versão "1,0" com a primeira versão do Windows Vista.

**condições de validação** : 1,0 no Windows Vista. As versões &lt; 2,0 também são válidas para oferecer suporte a alterações não significativas no formato.

### <a name="documentation"></a>Documentação

Esquema de perfil de modelo de mapa de gamut.

Copyright (C) Microsoft. All rights reserved.

**Condições de validação** : cada subelemento é validado por seu próprio tipo.

### <a name="defaultbaselinegamutmapmodel-type"></a>Tipo de DefaultBaselineGamutMapModel

Tipo UINT

Valores de enumeração:

<dl> "MinCD \_ Absolute"  
"MinCD \_ Relative"  
"SIG \_ KNEE"  
"HueMap"  
</dl>

**Condições de** validação: os valores devem corresponder a uma das enumerações acima.

### <a name="plugingamutmaptype"></a>PlugInGamutMapType

Esse elemento é uma sequência de um GUIDType GUID e qualquer subconjunto.

**Condições de** validação: o GUID é usado para corresponder ao GUID de DLL do PlugIn GMM. Há um máximo de 100.000 subconjunto personalizados.

### <a name="extensiontype"></a>Extensiontype

Esse elemento é uma sequência opcional de qualquer subconjunto.

**Condições de** validação: pode haver um máximo de 100.000 subconjunto.

## <a name="the-gmmp-baseline-algorithms"></a>Os algoritmos de linha de base GMMP

## <a name="aligning-the-neutral-axes"></a>Alinhando os eixos neutros

A maioria dos algoritmos de mapeamento de jogos tem a meta de mapear o eixo neutro do dispositivo de origem para o eixo neutro do dispositivo de destino: ou seja, branco vai para branco, preto para preto e cinza para cinza. Isso é abordado, em parte, dimensionando a luz das cores de origem para corresponder ao intervalo de luz do dispositivo de destino. Mas isso não aborda completamente o problema.

É uma propriedade física da maioria dos dispositivos de imagens que a chromaticidade do dispositivo branco não combina exatamente com a chromaticidade do dispositivo preto. Por exemplo, monitorar branco depende da soma das chromaticities e das luminâncias relativas dos três primários, enquanto o monitor preto depende da reflexão da superfície de exibição. A impressora branca depende da chromaticidade do papel, enquanto a impressora preta depende da tinta ou do toner usado. Um modelo de aparência que mapeia o dispositivo branco exatamente para o eixo neutro do espaço de aparência (chroma exatamente igual a zero) não mapeará o dispositivo preto para o eixo neutro. Como o olho é mais sensível às diferenças de chroma à medida que a luz aumenta, os cinzas médios serão representados como ainda mais chromatic do que o preto do dispositivo. (A Figura 1 ilustra a curvatura dos eixos neutros em duas dimensões. Na verdade, os eixos neutros formam uma curva mais complexa em três dimensões.)

Embora o CAM prevee que essas cores neutras do dispositivo aparecerão chromatic, os observadores reais parecem compensar isso. A maioria das pessoas não considera esses valores neutros do dispositivo como chromatic. Para a maioria dos modelos de mapeamento de jogos, portanto, você deve continuar mapeando os neutros de origem para os neutros do dispositivo.

Para mapear os neutros de origem para os neutros do dispositivo, ajuste os limites de jogos de origem e destino e cada pixel ao aplicar o algoritmo de mapeamento de jogos. Primeiro, ajuste cada valor na cor de origem para que o eixo neutro do dispositivo de origem na luz da cor de origem caia diretamente no eixo neutro do espaço de aparência. (Consulte o lado esquerdo da Figura 1.) Em seguida, ajuste a descrição do limite de jogos do dispositivo de destino para que cada cor no eixo neutro do dispositivo de destino na cor da cor do limite de jogos do dispositivo de destino caia diretamente no eixo neutro do espaço de aparência. (Consulte o lado direito da Figura 1.)

![Diagrama que mostra o grafo Limite de Jogos de Origem à esquerda e o Limite de Jogos de Destino à direita.](images/gmmp-image004.png)

**Figura 1:** alinhamento dos eixos neutros ilustrados. Esquerda: ajuste dos pontos de origem em relação ao eixo neutro do dispositivo de origem. Direito: ajustando a descrição do limite de jogos de destino em relação à descrição do limite de jogos de destino.

Observe que você ajusta cada valor de pixel de origem em relação ao eixo neutro nesse valor de luz. Isso garante que os neutros do dispositivo de origem se enquadram no eixo neutro do modelo de aparência. Você também desloca todas as outras cores nessa luz pela mesma quantidade, para que não haja descontinuidades na representação da gama de origem. Você precisa mudar por diferentes quantidades em diferentes níveis de luz, porque os neutros do dispositivo de origem não são representados como igualmente chromatic nos diferentes níveis de luz. Claramente, essa não é uma transformação trivial.

Lidar com os valores do dispositivo de destino é um pouco mais complicado. Inicialmente, você ajusta todo o limite de jogos de destino de maneira semelhante, mas em relação ao eixo neutro do dispositivo de destino. Isso é ilustrado na Figura 1 no lado direito. Esse ajuste garante que os valores cinza de origem serão mapeados para valores cinza de destino. Esse é o espaço no qual os algoritmos de mapeamento de jogos operam.

No entanto, esse espaço não descreve com precisão o comportamento verdadeiro do dispositivo de destino. Você deve inverter o mapeamento antes que as cores mapeadas de jogos sejam entregues ao modelo de aparência e ao modelo de dispositivo de destino. Você desloca todos os valores mapeados pelo oposto do deslocamento aplicado anteriormente ao eixo neutro do dispositivo de destino. Isso mapeia o eixo neutro de destino de volta para o valor representado originalmente pelo CAM. Ele faz o mesmo para o limite de jogos e todos os valores intermediários.

![Diagrama que mostra um grafo para desfazer o alinhamento do eixo neutro do dispositivo de destino.](images/gmmp-image008.png)

**Figura 2:** Desfazer o alinhamento do eixo neutro do dispositivo de destino

### <a name="minimum-color-difference-mincd"></a>Diferença mínima de cor (MinCD)

Versões Mínimas de Diferença de Cores (MinCD) Relativas e Absolutas – equivalentes à intenção colorimétrica ICC.

> [!Note]  
> O GMM MinCD é adequado para mapear elementos gráficos e linhas que contêm cores de "logotipo" (cores spot), gradientes de cores do logotipo com algumas cores fora de jogo e para o estágio final das transformaçãos de prova. Embora o GMM MinCD possa ser usado para imagens de fotos que estão inteiramente dentro do gamut de destino, não é recomendável para renderização geral de imagens de imagens de fotos. O mapeamento de cores fora de jogo para cores na superfície de jogos de destino pode resultar em artefatos indesejados, como anomalias de tom ou de chroma em gradientes suaves que cruzam o limite de jogos. BasicPhoto é recomendado para imagens de fotos. Se uma imagem falsa ou contona exigir um mapeamento de jogos diferente de BasicPhoto, a alternativa deverá ser criar um GMM plug-in implementando esse mapeamento, em vez de usar MinCD.

 

As cores em jogos são deixadas inalteradas. Para cores fora de jogo, a leveza e a chroma são ajustadas encontrando o ponto na gama de destino que tem a distância mínima da cor dos pontos de entrada fora de jogos. A distância da cor é calculada no espaço JCh. No entanto, você pondera a distância em leveza (J) e a distância em chroma (C) ou matiz (h) de forma diferente. Uma função de peso dependente de chroma é usada para a distância em leveidade, de modo que o peso seja menor para chroma pequena e maior para uma chroma grande até que um limite de chroma seja atingido, após o qual o peso permanece em 1, ou seja, o mesmo peso que a distância em chroma ou matiz. Isso segue o uso recomendado para CMC e CIEDE2000. Há duas variantes: colorimetric relativo e colorimetric absoluto.

**Colorimetric relativo:** Primeiro, alinhe os eixos neutros de origem e destino, conforme descrito anteriormente. Em seguida, clip the adjusted source color to the adjusted destination gamut boundary. (Consulte a Figura 4. Mapeamento de Chroma ao longo da luz constante.) Reajuste os valores do dispositivo de destino, conforme descrito anteriormente. No caso de um limite de jogos de destino monocromático, o recorte de chroma significa que o valor de chroma (C) é definido como zero (0,0).

**Colorimétrica absoluta:** Isso é semelhante à colorimétrica relativa, mas sem o alinhamento do eixo neutro de origem e destino. O valor de origem é recortado diretamente para o eixo neutro de destino. Observe que, se os limites de jogos de origem e destino são monocromáticos, o comportamento é idêntico à variante colorimétrica relativa; ou seja, o alinhamento de eixos neutros é executado e, em seguida, o chroma é recortado para zero. Isso garante que uma saída razoável seja atingida mesmo que a mídia e os colorantes sejam significativamente diferentes.

![Diagrama que mostra um grafo para recorte minCD para a gama ajustada.](images/gmmp-image010.png)

**Figura 3:** Recorte minCD para a gama ajustada

### <a name="basicphoto"></a>BasicPhoto

### <a name="overview"></a>Visão geral

BasicPhoto – equivalente à intenção de ICC preferencial, pictorial ou perceptual.

Esse algoritmo é uma variante do mapeamento de luminosidade sigmoidal dependente de chroma e do SGCK (dimensionamento de rótula) descrito por CIE TC8-03 em CIE156:2004. Esse algoritmo de variante dá suporte a GBDs (descritores de limite de jogos) com shells de jogos duplos; ou seja, GBDs com um shell de referência e um shell frágil. O algoritmo SGCK, que assume originalmente apenas um shell de gamut no GBD, baseia-se no algoritmo SIGOID (1999), que incorpora o mapeamento de leveza sigmoidal e o dimensionamento de função de rótula proposto por Clara e Fairchild (1999), combinado com a dependência de \_ chroma de GCUSP (1998). Ele mantém a constante de matiz percebida, por exemplo, o ângulo de matiz em Hue-corrected Hue e usa um dimensionamento de luz sigmoidal genérico (independente de imagem), que é aplicado de maneira dependente de chroma e uma função de 90% de chroma. A variante é dimensiona ao longo de linhas de luz constante.

### <a name="the-case-of-single-gamut-shell"></a>O caso de um shell de jogos único

É útil revisar o algoritmo caso os GBDs de origem e de destino tenham apenas um shell de jogos. Nesse caso, o algoritmo consiste nos cálculos a seguir.

Primeiro, execute o mapeamento de leveza inicial usando a seguinte fórmula:

![Mostra a fórmula para o mapeamento de leveza inicial.](images/gmmp-image012.png) (1)

em *que J* é a leveza original e J *<sub>R</sub>* é a luz de reprodução.

![Mostra a segunda fórmula de mapeamento de leveza.](images/gmmp-image014.png) (2)

Quando o limite de gamut de origem for monocromático, o valor de chroma será zero para o limite monocromático devido ao alinhamento do eixo neutro. Isso resultará no caso degenere em que C é igual a zero. Nesse caso, *p <sub>C</sub>* é definido como 1.

*p <sub>C</sub>* é um fator de ponderação dependente de chroma (Semprevic, 1998) que depende do chroma da cor original, C e *J <sub>S</sub>* são o resultado da leveza original que está sendo mapeada usando uma função sigmoidal.

 

Para calcular *J <sub>S</sub>* (Sk e Fairchild, 1999), uma LUT (tabela de pesquisa unidimensional) entre os valores originais e de luz de reprodução é configurada primeiro com base em uma função normal cumulativa discreta (S).

![Mostra uma fórmula para calcular J s.](images/gmmp-image016.png) (3)

onde x ₀ e S são a média e o desvio padrão da distribuição normal, respectivamente, e *eu* = 0, 1, 2... *m*,*m* é o número de pontos usados no lut. *S <sub>i</sub>* é o valor da função normal cumulativa para *i*  / *m* %. Os parâmetros dependem da claridade do ponto preto da gama de reprodução e podem ser interpolados da tabela 1. Para obter detalhes sobre como calcular esses parâmetros, consulte Braun e Fairchild (1999, p. 391).

:::row:::
    :::column:::
        <sub>MinOut</sub> J
    :::column-end:::
    :::column:::
       5.0
    :::column-end:::
    :::column:::
        10.0
    :::column-end:::
    :::column:::
        15.0
    :::column-end:::
    :::column:::
        20,0
    :::column-end:::
:::row-end:::
:::row:::
    :::column:::
        x ₀
    :::column-end:::
    :::column:::
       53,7
    :::column-end:::
    :::column:::
        56,8
    :::column-end:::
    :::column:::
        58,2
    :::column-end:::
    :::column:::
        60,6
    :::column-end:::
:::row-end:::
:::row:::
    :::column:::
        S
    :::column-end:::
    :::column:::
       43.0
    :::column-end:::
    :::column:::
        49.0
    :::column-end:::
    :::column:::
        35,0
    :::column-end:::
    :::column:::
        34,5
    :::column-end:::
:::row-end:::


**Tabela 1** : cálculo do parâmetro de compactação de claridade BasicPhoto

Para usar S como um mapeamento de claridade LUT (S <sub>lut</sub> ), ele deve ser normalizado primeiro no intervalo de claridade de \[ 0100 \] . Os dados normalizados são então dimensionados para o intervalo dinâmico do dispositivo de destino, conforme mostrado na equação 4, em que *j*<sub>min \ *out*</sub> e *j*<sub>Max \ *out*</sub> são os valores de luminosidade do ponto preto e do ponto branco da mídia de reprodução, respectivamente.

![Mostra a fórmula para S como um mapeamento de claridade LUT.](images/gmmp-image018.png) (4)

Neste ponto, os valores de *j s* podem ser obtidos na <sub>lut</sub> de s, interpolando entre os pontos *m* dos valores de *j O* e *j s* correspondentes que ele contém e usando a equação a seguir como entrada.

![Mostra a fórmula para obter os valores de J S.](images/gmmp-image020.png) (5)

J <sub>Mini</sub> é o valor de claridade do ponto preto da mídia original, j é o valor de claridade do ponto branco do meio original, <sub>e j</sub> <sub>o é a</sub> claridade original do. Para referência posterior, você pode indicar por *S* a função sigmoidal definida da maneira que acabou de ser descrita, conforme ilustrado na Figura 4 a seguir.

![Diagrama que mostra o grafo para o mapeamento de croma ao longo da luminosidade constante.](images/gmmp-image024.png)

**Figura 4** : mapeamento de croma ao longo da luminosidade constante

Em segundo lugar, se o limite de gama de destino for desvio, compacte croma junto com as linhas de luminosidade constante (l) e execute a compactação da seguinte maneira.

![Mostra a fórmula para executar a compactação croma.](images/gmmp-image026.png)  (6)

onde *d* representa a distância de *E* em *l*; *g* representa o limite médio de gama; *r* representa a reprodução; e *o* original Figura 5.

![Diagrama que mostra o grafo para compactação croma e claridade em BasicPhoto.](images/gmmp-image028.png)

**Figura 5** : compactação de croma e claridade no BasicPhoto

Se o limite de gama de destino for monocromático, o valor de croma será recortado para zero.

Em terceiro lugar, use um clipe MinCD (descrito anteriormente) para eliminar qualquer erro residual.

### <a name="black-enhancement"></a>Aprimoramento preto

O algoritmo anterior pode ser modificado para melhorar o preto quando o destino é um dispositivo de impressora. O problema tem a ver com a escolha de *J <sub>minOut</sub>*, que geralmente não corresponde à cor mais escura que uma impressora pode produzir.

Mais especificamente, a cor com densidade mais alta, obtida com a colocação de tintas de 100% (ou cobertura máxima possível, se a limitação de GCR/tinta estiver em vigor), geralmente não é "neutra" no espaço de aparência da cor. Consulte a Figura 6. Em outras palavras, se a claridade mínima neutra for usada para o dispositivo de destino, o dimensionador de luminosidade construído será mapeado para uma claridade mínima que não seja a maior densidade que pode ser obtida pela impressora. Considere o caso de uso adicional do monitor para a impressora. O monitor preto, R = G = B = 0, será impresso como não a densidade mais alta. O impacto na qualidade da imagem é que há uma falta de profundidade e contraste.

![Diagrama que mostra como o ponto preto do dispositivo pode ser mais escuro do que a claridade mínima neutra.](images/gmmp-seqfigure01.png)

**Figura 6** : o ponto preto do dispositivo pode ser mais escuro do que a claridade mínima neutra.

Suponha que o "ponto preto do dispositivo" de destino seja Jkakbk/JkCkh k. Se C k não for zero, o ponto preto do dispositivo não será neutro em relação a CAM02. Se você usar J k para o destino "claridade mínima neutra" na construção do dimensionador de claridade; ou seja, definindo

*J <sub>minOut</sub> = JK*

e aplicá-lo ao Shell de gamut de origem, você obtém a configuração descrita na Figura 7. Na figura, o plano de matiz corresponde a h k.

![Diagrama que mostra o dimensionador de claridade modificado com o ponto preto do dispositivo de destino.](images/gmmp-seqfigure02.png)

**Figura 7** : geometria usando o dimensionador de claridade modificado com o ponto preto do dispositivo de destino

Para permitir que o algoritmo de compactação de croma subsequente prossiga, você deseja alinhar o máximo e o mínimo de lightnesses nos shells de origem e de destino. Isso pode ser feito ajustando o Shell de destino entre J <sub>neutralMin</sub> e j k ao deslocar pontos para a esquerda. Além disso, essa transformação deve ser aplicada em todo o espaço jab, não apenas no plano de matiz correspondente a h k.

A transformação é

![Mostra a fórmula da transformação.](images/gmmp-seqfigure03.png)

A Figura 8 mostra o efeito da transformação.

![Diagrama que mostra o efeito do dimensionador de claridade modificado com o ponto preto do dispositivo de destino.](images/gmmp-seqfigure04.png)

**Figura 8** : geometria usando o dimensionador de claridade modificado com o ponto preto do dispositivo de destino

Depois de aplicar o algoritmo de compactação croma usual, o ponto deve ser "deslocado;" ou seja, a transformação inversa deve ser aplicada para obter a cor final mapeada.

![Mostra a fórmula da transformação inversa para obter a cor final mapeada.](images/gmmp-seqfigure05.png)

### <a name="the-case-of-dual-gamut-shells"></a>O caso de shells de gama dupla

O objetivo é generalizar o SIG \_ joelho para o Shell de gamut único para o caso em que o dispositivo de origem gbd ou o dispositivo de destino gbd tem uma estrutura de dois shells. O Shell interno será chamado de Shell de referência, enquanto o Shell externo será chamado de shell plausível. Você deseja considerar os casos a seguir.

(a) o GBD de origem e o GBD de destino têm uma estrutura de dois shells.

(b) a fonte GBD tem uma estrutura de dois shells; o GBD de destino tem apenas um shell.

(c) a fonte GBD tem apenas um shell; o GBD de destino tem uma estrutura de dois shells.

(d) tanto o GBD de origem quanto o GBD de destino têm apenas um shell.

Case (d) é o caso de um único Shell de gamut que foi discutido anteriormente. Para casos (a), (b) e (c), você pode generalizar o redimensionamento de claridade para usar as informações extras da estrutura de shell dupla. Nos casos (b) e (c) em que a origem ou o destino tem apenas um shell, você introduz um "Shell de referência induzido" que será discutido em uma seção subsequente, "Shell de referência induzido". O algoritmo geral para dois shells será descrito para o caso (a). Depois que a construção do Shell de referência induzida é explicada, o algoritmo também pode ser aplicado a Case (b) e (c). Para a compactação croma, a taxa de compactação será determinada pelos maiores shells disponíveis. Em outras palavras, se o Shell plausível e o Shell de referência estiverem disponíveis, o Shell plausível será usado; caso contrário, o Shell de referência será usado.

*Redimensionamento de luminosidade generalizado*

A existência de dois shells para GBD de origem e de destino significa que você deve mapear um conjunto de quatro pontos do GBD de origem para um conjunto correspondente no GBD de destino.

![Mostra como mapear um conjunto de quatro pontos para um conjunto correspondente.](images/gmmp-image030.png)

Os subscritos têm os seguintes significados.

o ou r: "original" (origem) ou "reprodução" (destino)

min ou Max: claridade mínima neutra ou claridade máxima neutra

PLA ou ref: Shell plausível ou Shell de referência

A ordenação em cada quádruplo também é a magnitude relativa esperada desses pontos.

O mapa de redimensionamento de claridade usa as mesmas primeiras equações que o Shell único, mas *J S* é definida de forma piecewise da seguinte maneira.

![Mostra a fórmula para J S de uma maneira piecewise.](images/gmmp-image032.png) (7)

Em outras palavras, ele é sigmoidal dentro do Shell de referência e linear externo. Consulte a Figura 9.

![Diagrama que mostra um grafo para a função de redimensionamento de claridade para GBDs de dois shells.](images/gmmp-image033.png)

**Figura 9:** Função de recalque de leveza para GBDs de dois shells

**SHELL DE REFERÊNCIA INDUZIDO**

Em que um GBD tem um shell e o outro GBD tem dois shells, você deve criar um "Shell de Referência" para o GBD com apenas um shell. O shell existente, que seria chamado de Shell de Referência, será alterado para o "Shell Desaúso". Na verdade, na verdade, você não precisa criar um shell no espaço full Dem. Como o recalque de leveidade usa apenas *J max* e *J min,* você só precisa fazer esses valores para o Shell de Referência induzido. Há dois casos, dependendo de qual GBD tem dois shells.

Caso 1: o GBD de origem tem dois shells; O GBD de destino tem um shell.

Determine o Shell de Referência induzido de destino no eixo neutro; ou seja, o J <sub>r,\ min,\ ref</sub> e J <sub>r,\ max,\ ref</sub> do shell. Isso é feito usando o algoritmo a seguir.

![Mostra o algoritmo para determinar o Shell de Referência induzido de destino.](images/gmmp-induced01.png)

Os fatores ? <sub>baixo</sub> e ? <sub>controle</sub> alto a separação entre o Shell Desilusão e o Shell de Referência. Um valor de 1 significa que os valores de J <sub>min</sub> ou J m coincidem. Seus valores são "induzidos" do Shell de Referência de origem e do Shell De origem.

![Mostra a fórmula para os valores do Shell de Referência de origem e o Shell De origem.](images/gmmp-induced02.png)

Os "fatores de trabalho" F <sub>baixo</sub> e F <sub>alto</sub> são *parâmetros* que devem estar entre 0 e 1. Se o valor for 0, os J <sub>min</sub> ou J m serão induzidos diretamente dos shells de origem. Nesse caso, escolha F <sub>baixo</sub> = 0,95 e F <sub>alto</sub> = 0,1.

Caso 2: o GBD de origem tem um shell; O GBD de destino tem dois shells.

Determine o Shell de Referência induzido de origem no eixo neutro; ou seja, o J <sub>o,\ min,\ ref</sub> e J <sub>o,\ max,\ ref</sub> do shell. Isso é feito usando o algoritmo a seguir.

![Mostra o algoritmo para determinar o Shell de Referência induzido de destino no eixo neutro.](images/gmmp-induced03.png)

Novamente, os fatores ? <sub>baixo</sub> e ? <sub>controle</sub> alto a separação entre o Shell de Negação e o Shell de Referência. Um valor de 1 significa que os <sub>valores</sub> mínimos J ou J m coincidem. Seus valores são "induzidos" do Shell de Referência de origem e do Shell De origem De origem:

![Mostra o algoritmo para controlar a separação entre o Shell de Referência e o Shell De origem.](images/gmmp-induced04.png)

### <a name="reasons-for-changes-from-the-cie-tc8-03-recommendations"></a>Motivos para alterações das recomendações do CIE TC8-03

BasicPhoto difere das recomendações do CIE TC8-03 das seguintes maneiras.

1.  O Chroma não é compactado em direção ao cume, mas ao longo de linhas de luz constante.
2.  O intervalo de leveza usa a luz da cor mais escura na gama, em vez do ponto em que o limite de jogos cruza o eixo neutro.
3.  BasicPhoto dá suporte a um shell de jogos de referência e a um shell de jogos inentente, se qualquer limite de gamut na transformação tiver dois shells.
4.  BasicPhoto usa CIECAM02; em vez de usar CIECAM97s para converter em D65 a 400 cd/m2 e, em seguida, usar o espaço de cor IPT RIT.

A primeira alteração foi feita para evitar problemas de inversão de tom que podem ocorrer ao usar a compactação em direção a um manifest. Conforme mostrado na Figura 10, a compactação de ltda pode causar inversões de tom. Isso pode acontecer quando as cores de chroma alta são mais claras do que as cores de chroma inferior. Como o SGCK compacta cada pixel independentemente na leveidade e no chroma, não há garantia de preservar a relação de leveza entre os valores de pixel após a compactação. A desvantagem conhecida dessa decisão de compactar linhas de luz constante é que você pode sofrer perdas de chroma, especialmente em áreas em que o limite de jogos de destino é muito simples, como acontece com amarelos brilhante.

![Diagrama que mostra a inversão de tom causada pelo SGCK.](images/gmmp-toneinversion.png)

**Figura 10:** Inversão de tom causada por SGCK

![Mostra uma imagem original de um bule.](images/originalteapot.jpg)![Mostra o resultado SGCK da imagem de bule.](images/badteapot.jpg)![Mostra o resultado BasicPhoto da imagem de bule.](images/betterteapot.jpg)

**Figura 11:** imagem original, resultado SGCK e resultado de BasicPhoto

A Figura 11 ilustra essa inversão de tom. À esquerda está uma imagem original capturada por uma câmera digital; no centro, a imagem como reproduzida pelo SGCK; e à direita, a imagem reproduzida por BasicPhoto. A imagem à esquerda está no espaço de cores da câmera digital, as imagens central e direita estão no espaço de cores de uma exibição de vídeo do LCD. Na imagem original, a parte superior do bule é mais escura do que a parte inferior, porque a parte inferior está refletindo a peça de tabela em que ela está. Na imagem SGCK, a parte superior é, na verdade, mais leve do que a parte inferior, devido à inversão de tom. Além disso, é difícil ver os itens refletidos na parte inferior do bule. À direita, BasicPhoto corrigiu a inversão de tom e os artigos refletidos são mais claramente distinguíveis.

A segunda alteração foi feita para melhorar a reprodução de cores quase pretas em impressoras em que o preto mais preto não se enquadra diretamente no eixo neutro CIECAM02. A Figura 12 a seguir mostra uma imagem convertida em sRGB; reproduzido para uma impressora de inkjet RGB usando SGCK; e reproduzidos para a mesma impressora usando BasicPhoto. A imagem no centro não está usando o dispositivo completo preto e, portanto, não tem o contraste visto no original. O contraste é restaurado com BasicPhoto.

![Mostra a imagem original de um playset.](images/playstructure.jpg)![Mostra a imagem do playset reproduzida para uma impressora de inkjet R G B usando SGCK.](images/playstructurebad.jpg)![Mostra a imagem do playset reproduzida para uma impressora de inkjet do R G B usando BasicPhoto.](images/betterplaystructure.jpg)

**Figura 12:** Preto aprimorado

A terceira alteração foi feita para melhorar a reprodução de cores para câmeras digitais. Especialmente nos casos em que a câmera digital foi criada usando um destino de referência, uma descrição de limite de jogos criada com base em cores medidas pode não incluir todas as cores que podem ser capturadas em uma cena do mundo real. Em vez de cortar todas as cores para o gamut do destino de cor medido, você permite que a extrapolação produza um limite de jogos inaceitável. O algoritmo BasicPhoto foi projetado para dar suporte a esse limite de jogos extrapolado.

A quarta alteração foi feita porque o CIECAM02 funciona bem para o mapeamento de gamut. O processo recomendado pelo TC8-03 de conversão de cores do dispositivo em D65 a 400 cd/m2 e, em seguida, o uso do espaço de cores de IPT RIT é demorado e demorado.

### <a name="hue-mapping"></a>Mapeamento de matiz

HueMap é o equivalente da intenção de saturação do ICC.

Se o limite de jogos de origem ou o limite de jogos de destino não contiver primários, esse modelo será reverta para o modelo MinCD (relativo) descrito em uma seção anterior; por exemplo, dispositivos para os quais os primários não podem ser determinados (perfis ICC com mais de quatro canais) ou perfis ICC monocromáticos.

Esse algoritmo primeiro ajusta o matiz do valor da cor de entrada. Em seguida, ele ajusta simultaneamente a luminosidade e a chroma, usando um mapeamento de cingar. Por fim, ele clipes de valor de cor para garantir que ele está dentro do gamut.

A primeira etapa é determinar as "Hue Wheels". Encontre os valores JCh para cores primárias e secundárias para o dispositivo de origem e de destino. Você está considerando apenas os componentes de matiz. Isso resulta em uma roda de matiz primária ou secundária com seis pontos de cor para cada dispositivo. (Consulte a Figura 13.)

![Diagrama que mostra as engrenagens de matiz com seis pontos de cor.](images/gmmp-figure12.png)

**Figura 13:** Roda de matiz

Melhores resultados poderão ser obtidos se o primário azul de origem não for girado para o primário azul de destino. Em vez disso, o ângulo de matiz primário azul de origem é usado como o ângulo de matiz primário azul de destino.

Em seguida, execute as rotações de matiz para cada cor de entrada da imagem de origem,

a)Usando o ângulo de matiz da cor de entrada, determine o local da cor na roda de matiz de origem em relação às duas cores primária ou secundária adjacentes. O local pode ser pensado como uma porcentagem da distância entre as primárias. Por exemplo, o matiz de cor de entrada é 40% do caminho do valor de matiz de Magenta para o valor de matiz de Vermelho.

b)Na roda de matiz de destino, localize o ângulo de matiz associado, por exemplo, 40% de Magenta para Vermelho. Esse valor será o ângulo de matiz de destino.

Em geral, os primários e secundários de origem não estarão nos mesmos ângulos de matiz que os primários e secundários de destino; ou seja, o ângulo de matiz de destino geralmente será diferente do ângulo de matiz de origem.

Por exemplo, suponha que as engrenagens de matiz produzam os seguintes valores:

Origem M = 295 graus, Origem R = 355 graus.

Destino M = 290 graus, Destino R = 346 graus.

Se o ângulo de matiz da cor de entrada for 319 graus, ele será 40% do ângulo (24 graus) da fonte M para o R de origem. O ângulo de M para R é de 60 graus e o ângulo de M para o matiz de entrada é de 24 graus. Calcule o ângulo no destino que é 40% do destino M para o destino R (22 graus), portanto, o ângulo de matiz da cor de destino é de 312 graus.

Em seguida, calcule os pontos de referência de matiz para o matiz de origem e o matiz de destino. Para calcular o ponto de referência de matiz para um valor h (matiz) específico, você deseja encontrar o valor J (leveza) e o valor C (chroma).

-   Localize o valor J do ponto de referência de matiz interpolando entre os valores J para os pontos primários ou secundários adjacentes, usando a posição relativa do matiz; por exemplo, 40% neste exemplo.
-   Localize o valor máximo de C neste valor J e h. Agora você tem o JCh do ponto de referência de matiz para esse matiz.

![Diagrama que mostra uma folha de matiz.](images/gmmp-figure13.png)

**Figura 14** : uma folha de matiz (visualização de uma fatia de limite de gamut em um matiz específico)

A próxima etapa é computar o mapeamento de distorção para cada pixel. Primeiro, visualize uma folha de matiz da gama de origem para o ângulo de matiz da cor de origem e uma folha de matiz da gama de destino para o ângulo de matiz de destino calculado durante a rotação de matiz. As folhas de matiz são criadas por meio de uma "fatia" da superfície de limite de gama de JCh em um ângulo de matiz específico (consulte a Figura 14).

Observação: para fins de otimização de desempenho, as folhas de matiz não são realmente criadas; Eles são descritos e mostrados aqui apenas para fins de visualização. As operações são executadas diretamente na superfície de limite da gama no matiz especificado. Em seguida, você computa os pontos de referência de matiz para determinar o mapeamento de distorção.

-   Execute um redimensionamento de claridade para mapear os pontos pretos e brancos da folha de origem para a folha de destino (veja a Figura 15). Os pontos pretos e brancos da folha de matiz de origem são mapeados linearmente para os pontos pretos e brancos da folha de matiz de destino, dimensionando todas as coordenadas J do limite de origem. O valor de cor de entrada mapeada para matiz é dimensionado da mesma maneira.

![Diagrama que mostra o mapeamento de claridade.](images/gmmp-figure14.png)

**Figura 15** : mapeamento de luminosidade

-   Determine os pontos de referência de matiz para cada folha de matiz. Aplique um mapeamento de distorção à folha de origem para que os pontos de referência de origem e destino coincidam (consulte a Figura 16). O ponto de referência para uma gama em um matiz específico é o ponto de referência de matiz interpolado entre os primários adjacentes. O ponto de referência da folha de matiz de origem é mapeado linearmente para o ponto de referência da folha de matiz de destino, usando uma operação de "distorção" que bloqueia o eixo J, mantendo os pontos pretos e os pontos brancos fixos. Os pontos pretos, os pontos brancos e os pontos de referência das folhas de matiz de origem e de destino devem coincidir.
-   Aplique o mapeamento de distorção ao valor de cor de entrada com ajuste de luminosidade. As coordenadas J e C do valor da cor de origem são proporcionalmente dimensionadas, em relação à sua distância do eixo J.
-   Em seguida, uma compactação sutil dependente de croma em direção ao J-Value do ponto de referência de matiz é executada no ponto de cores mapeado para distorção. A compactação para referência de matiz J é feita de maneira semelhante a gama, em que branco, preto, cinza e pontos na referência de matiz J não são afetados. Todos os outros pontos tendem a fazer a referência de matiz J de maneira suave, o que é um pouco próximo da referência de matiz J, com constante croma restante. A dependência croma garante que as cores neutras não sejam afetadas e que o efeito seja aumentado em cores com croma maiores.

Veja a seguir uma descrição matemática da compactação de claridade em direção à referência de matiz J ou ajuste do J-Value do ponto de destino. Ele é chamado de ponto de destino porque foi mapeado para a gama de destino.

Primeiro, COMPUTE "factorC" (fator de dependência croma) para o ponto de destino, que determina a quantidade de efeito que a compactação de claridade terá. Pontos próximos ou no eixo J terão pouca ou nenhuma compactação; pontos distantes do eixo J (alta croma) terão mais compactação aplicada. Multiplique por 0,5 para garantir que factorC seja menor que 1, porque é possível que sourceC possa ser um pouco maior do que referenceC, mas não duas vezes tão grande.

factorC = (destinationC/referenceC)? 0,5

em que:

destinationC é o valor C do ponto de destino.

referenceC é o valor C do ponto de referência de matiz.

Em seguida, determine se o ponto de destino J está acima ou abaixo da referência de matiz J. Se estiver acima, faça o seguinte:

1.  Compute "factorJ" para o ponto de destino em relação ao referenceJ. Esse valor de factorJ estará entre 0 e 1 (0 se estiver no referenceJ; 1 se em maxJ).
2.  factorJ = (destinationJ-referenceJ)/(maxJ-referenceJ)

    em que:

    destinationJ é o J-Value do ponto de destino.

    referenceJ é o J-Value do ponto de referência de matiz.

    maxJ é o valor J máximo da gama.

3.  Aplique uma função de energia do tipo gama ao factorJ, o que reduzirá o factorJ por um determinado valor. Este exemplo usa a potência de 2 (o quadrado). Subtraia o factorJ reduzido do factorJ original e multiplique o resultado pelo intervalo J total acima do referenceJ primário para localizar o "deltaJ", que representa a alteração em J após a compactação de claridade, mas não incluindo a dependência croma.
4.  deltaJ = (factorJ-(factorJ? factorJ)) ? (maxJ - referenceJ)

5.  Aplique factorC ao deltaJ (quanto maior o croma, maior o efeito) e calcule o novo J-Value para o ponto de destino.
6.  destinationJ = destinationJ-(deltaJ? factorC)

Se J-Value para o ponto de destino estiver abaixo de referenceJ, uma computação semelhante às etapas anteriores a-C será executada, usando minJ em vez de maxJ para encontrar o intervalo em J para computar o factorJ e levar em conta a polaridade das operações "embaixo" da referenceJ.

factorJ = (referenceJ-destinationJ)/(referenceJ-minJ)

deltaJ = (factorJ-(factorJ? factorJ)) ? (referenceJ - minJ)

destinationJ = destinationJ + (deltaJ? factorC)

em que:

minJ é o valor J mínimo da gama.

O croma para pontos de cor de entrada é expandido linearmente (quando possível) ao longo da luminosidade constante proporcional ao valor máximo de croma das gamas de origem e de destino no matiz e na claridade. Combinado com a compactação de luminosidade dependente de croma, isso ajuda a preservar a saturação porque o mapeamento de distorção usando os pontos de referência às vezes faz com que o ponto de origem seja supercompactado em croma (consulte a Figura 16).

![Diagrama que mostra o mapeamento de distorção para corresponder pontos de referência de matiz, antes da distorção à esquerda, depois de distorcer à direita.](images/gmmp-shearmapping.png)

**Figura 16** : mapeamento de distorção, compactação de claridade para referência de matiz J e expansão de croma

Veja a seguir uma descrição matemática do processo de expansão croma ou ajuste do valor C do ponto de destino. Ele é chamado de ponto de destino porque foi mapeado por distorção e luminosidade compactado na gama de destino.

1.  Antes do mapeamento de distorção, determine sourceExtentC (a extensão croma na claridade e no matiz do ponto de origem).
2.  Após o mapeamento de distorção e a compactação de claridade que transforma o ponto de origem no ponto de destino, determine o destExtentC (a extensão croma na claridade e no matiz do ponto de destino).
3.  Se o sourceExtentC for maior que o destExtentC, nenhum ajuste de croma para o ponto de destino será necessário e você poderá ignorar a próxima etapa.
4.  Ajuste destinationC (o croma do ponto de destino) para caber na extensão de croma de destino nessa luminosidade e matiz.
5.  destinationC = destinationC? (destExtentC / sourceExtentC)

    em que:

    destinationC é o ponto de destino C-Value.

    sourceExtentC é o valor C máximo da gama de origem na claridade e no matiz do ponto de origem.

    destExtentC é o valor C máximo da gama de destino na claridade e no matiz do ponto de destino.

Por fim, execute o recorte de distância mínimo. Se a cor de entrada de matiz-girado, com ajuste de luminosidade e com mapeamento de distorção ainda estiver ligeiramente fora da gama de destino, recorte-a (Mova-a) para o ponto mais próximo no limite de gama de destino (veja a figura 17).

![Diagrama que mostra o recorte de distância mínimo.](images/gmmp-figure15.png)

**Figura 17** : recorte de distância mínimo

## <a name="gamut-boundary-description-and-gamut-shell-algorithms"></a>Descrição de limite de gama e algoritmos de Shell de gamut

A função de limite de gama de dispositivos usa o mecanismo de modelo de dispositivo e os parâmetros analíticos para derivar um limite de gama de dispositivos de cores, descrito como uma lista de vértices indexados do envoltória da gama do dispositivo. O envoltória é calculado de forma diferente, dependendo se você está trabalhando com dispositivos aditivos, como monitores e projetores ou dispositivos subtraíis. A lista de vértices indexados é armazenada em CIEJab. A estrutura da lista de vértices indexados é otimizada para aceleração de hardware pelo DirectX.

Essa abordagem tem muitas soluções conhecidas. Se você Pesquisar "convexa envoltória DirectX" na Web, obterá mais de 100 ocorrências. Por exemplo, há uma referência de 1983 neste tópico específico (teoria e aplicativo de gráficos de computador, "Shiphulls, superfícies b-spline e CADCAM", pp. 34-49) com referências de 1970 a 1982 no tópico.

A coleção de pontos pode ser determinada de informações externamente disponíveis, da seguinte maneira:

-   Os pontos para o Shell de referência para monitores são gerados usando uma amostragem do cubo de cores no espaço de Colorant do dispositivo.
-   Os pontos para o Shell de referência para impressoras e dispositivos de captura são obtidos dos dados de exemplo usados para inicializar o modelo.
-   Pontos para o Shell de referência para scRGB e sRGB são gerados usando uma amostragem do cubo de cor para sRGB.
-   Os pontos para o Shell plausível para dispositivos de captura são gerados usando uma amostragem do cubo de cores no espaço de Colorant do dispositivo.
-   Pontos para o Shell de referência para projetores são gerados usando uma amostragem de um poliedro no cubo de cores no espaço Colorant do dispositivo.
-   Os pontos para o possível Shell de espaços de cores de intervalo dinâmico amplos são gerados usando uma amostragem do cubo de cores no próprio espaço.

Você pode criar uma lista de vértices que descreve com eficiência a gama do dispositivo de cores, dado um perfil de dispositivo e serviços de suporte do sistema.

Para dispositivos de saída, o limite de gama descreve o intervalo de cores que podem ser exibidas pelo dispositivo. Um limite de gama é gerado a partir dos mesmos dados usados para modelar o comportamento do dispositivo. Conceitualmente, você produz uma amostra do intervalo de cores que o dispositivo pode produzir, mede as cores, converte as medidas em espaço de aparência e, em seguida, usa os resultados para criar o limite de gama.

Os dispositivos de entrada são mais complicados. Cada pixel em uma imagem de entrada deve ter algum valor. Cada pixel deve ser capaz de representar qualquer cor encontrada no mundo real de alguma forma. Nesse sentido, nenhuma cor é "fora da gama" para um dispositivo de entrada, pois eles sempre podem ser representados.

Todos os formatos de imagem digital têm algum intervalo dinâmico fixo. Devido a essa limitação, sempre há alguns estímulos distintos que mapeiam para o mesmo valor digital. Portanto, você não pode estabelecer um mapeamento de um para um entre cores do mundo real e valores de câmera digital. Em vez disso, o limite de gama é formado por meio da estimativa de uma variedade de cores do mundo real que podem produzir as respostas digitais da câmera. Você usa esse intervalo estimado como a gama do dispositivo de entrada.

Os primários estão incluídos para fornecer mapeamento de gamut de tipo de intenção de gráficos comerciais.

No estilo real orientado a objeto, você abstrai a representação subjacente do limite de gama. Isso permite que você tenha a flexibilidade de alterar a representação no futuro. Para entender o GBD (descritor de limite de gama) usado na nova CTE, primeiro você deve entender como o GMAs (algoritmos de mapeamento de gamut) funciona. Tradicionalmente, o GMAs foi projetado para atender às necessidades da comunidade de arte gráfica; ou seja, para reproduzir as imagens que já foram processadas corretamente para o dispositivo no qual a imagem de entrada foi criada. O objetivo da GMAs de artes gráficas é fazer a melhor reprodução possível da imagem de entrada no dispositivo de saída. A nova CTE GBD foi projetada para resolver quatro problemas principais.

Como a imagem de entrada é renderizada para o dispositivo de entrada, todas as cores se ajustam dentro do intervalo entre o ponto branco médio e o ponto preto. Suponha que a imagem seja uma fotografia de uma cena na qual há um branco difuso, como uma pessoa em uma camisa de baixo branco e um realce especulativo, como a reflexão clara de uma janela ou um amortecedor de cromo. A cena será renderizada para o meio de entrada para que o realce de especulação seja mapeado para o ponto branco médio e o branco difuso seja mapeado para uma cor neutra mais escura do que o ponto branco médio. A escolha de como mapear cores da cena para a mídia de entrada é uma decisão dependente de cena e uma decisão estética. Se o realce especular estava ausente da cena original, o branco difuso provavelmente será mapeado para o ponto branco médio. Em uma cena com muitos detalhes de realce, mais intervalo seria deixado entre o branco especular e o branco difuso. Em uma cena em que o realce não é significativo, um intervalo muito pequeno pode ser deixado.

Para imagens previamente renderizadas, o mapeamento de gamut é relativamente simples. Basicamente, o ponto branco da média original é mapeado para o ponto branco da média de reprodução, o ponto preto de origem é mapeado para o ponto preto de destino e a maior parte do mapeamento é concluída. Os diferentes GMAs de existência fornecem variações para mapear outros pontos na escala de tons da média de origem e diferentes maneiras de lidar com valores de croma fora do gamut. Mas o mapeamento de branco para branco e preto para preto é consistente em todas essas variações. Essa implementação exige que o branco esteja acima de um J \* de 50 e preto abaixo de um j \* de 50.

Nem todas as codificações de cores limitam os intervalos de cores para imagens de entrada. A scRGB de codificação de cores padrão IEC (IEC 61966-2-2) fornece 16 bits para cada um dos três canais de cores vermelho, verde e azul (RGB). Nessa codificação, a referência preta não é codificada como o triplo RGB (0, 0, 0), mas como (4096, 4096, 4096). A referência branca é codificada como (12288, 12288, 12288). A codificação scRGB pode ser usada para representar realces especulares e detalhes de sombra. Ele inclui corridas RGB que não são fisicamente possíveis porque exigem quantidades negativas de luz e codificações que estão fora do local de CIE Spectral. Claramente, nenhum dispositivo pode produzir todas as cores na gama de scRGB. Na verdade, nenhum dispositivo pode produzir todas as cores que um humano pode ver. Portanto, os dispositivos não podem preencher a gama de scRGB, e seria útil ser capaz de representar a parte da gama de preenchimento. Cada dispositivo tem um intervalo de valores no espaço scRGB que ele pode produzir. Essas são as cores "esperadas" para o dispositivo; seria surpreendente que o dispositivo produza cores fora desta gama. Há uma transformação definida do espaço de scRGB para o espaço de aparência; portanto, cada dispositivo também tem um intervalo de valores de aparência que espera-se reproduzir.

Em scRGB e entrada de dispositivos de captura caracterizados com um destino fixo, é possível obter um valor fora do intervalo de valores esperados. Se alguém calibrar uma câmera para um destino de teste; e, em seguida, captura uma cena com destaques especulares, pode haver pixels mais brilhantes do que o ponto branco do destino. A mesma coisa pode acontecer se um vermelho ocorrido naturalmente for mais desvio do que o vermelho de destino. Se alguém usar uma imagem scRGB de um dispositivo e editar manualmente as cores na imagem, será possível criar pixels que se enquadram fora do intervalo esperado da gama do dispositivo, mesmo que estejam dentro da gama completa do scRGB.

Um segundo problema pode não, à primeira, parecer estar relacionado a isso. Surge quando você usa um destino de cor para caracterizar um dispositivo de entrada, como uma câmera ou um scanner. Os destinos refletiis normalmente são produzidos em papel e contêm vários patches coloridos. O manufaturers fornece arquivos de dados com medidas de cores tomadas sob uma condição de exibição fixa para cada patch de cor. Ferramentas de criação de perfil de cores crie um mapeamento entre esses valores medidos e os valores retornados pelos sensores de cor nos dispositivos. O problema é que geralmente esses destinos de cor não cobrem o intervalo completo de valores de dispositivo. Por exemplo, o scanner ou a câmera pode retornar um valor de (253, 253, 253) para o ponto branco de referência e um patch vermelho de referência pode ter um valor RGB de (254, 12, 4). Elas representam o intervalo de valores esperados para o dispositivo de entrada, com base nos valores de destino. Se você caracterizar o dispositivo de entrada com base nas respostas para o destino, esperará apenas as cores dentro desse intervalo estreito. Esse intervalo não é apenas menor do que o intervalo de cores que as pessoas podem ver, é menor do que o intervalo de cores que o dispositivo pode produzir.

Em ambos os casos, é difícil estimar a gama do dispositivo ou da imagem de entrada, apesar da existência de uma gama de referência ou medidas. No primeiro problema, a gama plausível do dispositivo de entrada é menor do que a gama completa de scRGB. No segundo problema, a gama de referência do destino é menor que a gama total possível do dispositivo de entrada.

O terceiro problema envolve o mapeamento de Tom. Muitos modelos de limites de gama que podem representar adequadamente imagens previamente renderizadas usadas nas artes gráficas foram propostas, por exemplo, o Braun e Fairchild Mountain Range GBD (Braun \[ 97 \] ) e o descritor de limite Morovic de segmento de máximo (Morovic \[ 98 \] ). Mas esses modelos fornecem apenas informações sobre os extremos da gama do dispositivo; estão faltando informações sobre outros pontos no mapeamento de tons. Sem essas informações, o GMAs só pode fazer estimativas aproximadas do mapeamento de Tom ideal. Pior, esses modelos não fornecem ajuda para o intervalo dinâmico estendido em scRGB e em imagens de câmera digital.

Como esse problema é resolvido nos setores fotográficos e videographic? A câmera captura uma imagem. Os especialistas podem debater quanto o processamento ocorre no dispositivo de captura; Mas eles concordam que não é uma quantidade significativa. Ambas as tecnologias não mapeiam um branco difuso em uma cena capturada para o ponto branco da média. Da mesma forma, eles não mapeiam o ponto preto da cena para o ponto preto da média. O comportamento do filme fotográfico é descrito em espaço de densidade usando uma curva de característica, geralmente chamada de um Prejudicador e Driffield, ou a curva de H&D. A curva mostra a densidade da cena original e a densidade resultante no filme. A Figura 18 mostra uma curva típica de H&D. O eixo x representa o aumento da exposição do log. O eixo y representa a densidade no slide. Cinco pontos de referência são marcados na curva: preto sem detalhes, que representa a densidade mínima no negativo; preto com detalhe; cartão de referência média-cinza; branco com detalhes; e branco sem detalhes. Observe que há espaço entre preto sem detalhes (que representa o preto do dispositivo) e preto com detalhe (sombra preta). Da mesma forma, há espaço entre branco com detalhe (branco difuso) e branco sem detalhes (que representa o dispositivo branco).

![Diagrama que mostra a curva de H e D para filme de slide.](images/gmmp-image079.png)

**Figura 18** : curva de&D para filme de slide

A indústria de vídeo fornece "espaço" e "footroom" em imagens. Na especificação ITU 709, a luminância (chamada Y) é codificada em 8 bits, com um intervalo de 0 a 255. No entanto, a referência preta é codificada em 15 e a branca de referência é codificada como 235. Isso deixa o intervalo de codificação entre 236 e 255 para representar os realces especulares.

O setor de vídeo apresenta um sistema de loops essencialmente fechado. Embora existam muitos fornecedores de equipamentos diferentes, os sistemas de vídeo são baseados nos dispositivos de referência. Há uma codificação padrão para imagens de vídeo. Não é necessário comunicar um limite de gama com imagens de vídeo, pois todas as imagens são codificadas para reprodução no mesmo dispositivo de referência. O filme também é um loop fechado porque não há necessidade de transmitir dados intermediários entre componentes diferentes. Você deseja uma solução que permita imagens de dispositivos com gamas variáveis e que representem cenas previamente renderizados e não renderizados a serem reproduzidos na saída com gamas variáveis.

Um quarto problema que a nova CTE deve resolver é que as cores visualmente cinzas produzidas por um dispositivo, por exemplo, quando vermelho = verde = azul em um monitor, frequentemente não se enquadram no eixo neutro do CAM (quando croma = 0,0). Isso causa grandes dificuldades para o GMAs. Para tornar o GMAs funcionar bem, você precisa ajustar a descrição da gama do dispositivo e dos pontos de entrada para que o eixo neutro do dispositivo fique no eixo neutro do espaço de aparência. Você precisa ajustar os pontos do eixo neutro por um valor semelhante. Caso contrário, não será possível fazer gradações suaves por meio da imagem. No caminho do GMA, você desfaz esse mapeamento em relação ao eixo neutro do dispositivo de saída. Isso é chamado de "chiropractic" a retificação do eixo. Como um chiropractor, você não apenas acerta o esqueleto (eixo neutro), mas ajusta o restante do corpo para se mover junto com o esqueleto. Como um chiropractor, você não ajusta o esqueleto pelo mesmo valor por todo o espaço. Em vez disso, você ajusta diferentes seções de forma diferente.

![Diagrama que mostra a curvatura do eixo neutro do dispositivo em relação ao eixo neutro CIECAM.](images/gmmp-image081.png)

**Figura 19:** Curvatura do eixo neutro do dispositivo em relação ao eixo neutro CIECAM

O que a nova CTE requer é um modelo de um limite de gama que pode ser usado para representar imagens de origem renderizadas e não renderizadas, fornecer informações sobre a aparência de neutros de dispositivo e fornecer informações para imagens de mapeamento de Tom com um grande intervalo de luminância.

![Diagrama que mostra os três shells de gamut.](images/gmmp-image083.png)

**Figura 20** : três shells de gamut

O limite de jogos é composto por três shells que definem três regiões.

Na nova CTE, o shell externo do gamut é formado com um chassi convexa feito de pontos de exemplo na gama de dispositivos. Um chassi é formado por meio de um conjunto de pontos de exemplo e ao redor deles por uma superfície. Um chassi convexa tem a propriedade adicional de ser convexa em todos os lugares. Portanto, esse não é o menor chassi possível que pode ser adequado aos dados. Mas a experimentação mostrou que ajustar os pontos de exemplo muito fortemente causa artefatos não aplainados em imagens, como a falta de sombreamento suave. O chassi convexa parece resolver esses problemas.

No algoritmo, os valores de aparência de cor são obtidos para um conjunto de pontos amostrados do dispositivo. Para monitores e impressoras, os valores de aparência de cor são obtidos pela saída de amostras e, em seguida, medindo-os. Você também pode criar um modelo de dispositivo e, em seguida, executar dados sintéticos por meio do modelo de dispositivo para prever valores medidos. Em seguida, os valores medidos são convertidos de espaço colorimétrico (XYZ) em espaço de aparência (Xyz) e o envolução é envolvido em torno dos pontos.

O ponto chave para esse algoritmo é que o ponto em branco adotado usado na conversão de colorimetric em espaço de aparência não precisa ser o ponto branco da mídia. Em vez disso, você pode selecionar um ponto mais distante dentro do gamut e no eixo neutro (ou próximo). Esse ponto terá um valor J de 100. Exemplos com um valor Y medido maior que o ponto em branco adotado acabarão com um valor J maior que 100.

Se você colocar o ponto em branco difuso da cena como o ponto em branco adotado para a conversão de espaço de cores, os destaques especular na cena serão facilmente detectados como tendo um valor J maior que 100.

Como o modelo de cor CIECAM02 é baseado no sistema visual humano, depois que um branco adotado é selecionado, o nível de luminância do ponto preto (J = 0) é determinado automaticamente pelo modelo. Se a imagem de entrada tiver um amplo intervalo dinâmico, é possível que haja valores que mapeiem para valores J menores que zero.

A Figura 21 a seguir mostra os neutros do dispositivo em execução no centro dos jogos de referência e de negação.

![Diagrama que mostra o eixo neutro do dispositivo adicionado ao limite de jogos.](images/gmmp-image085.png)

**Figura 21:** Eixo neutro do dispositivo adicionado ao limite de jogos

Todos os mapeamentos de jogos envolvem o recorte de um intervalo de entrada para uma gama de saída ou a compactação da gama de entrada para caber na gama de saída. Algoritmos mais complexos são formados pela compactação e recorte em diferentes direções ou pela divisão da gama em regiões diferentes e, em seguida, pela execução de recorte ou compactação em regiões diferentes.

A nova CTE estende esse conceito para dar suporte às regiões de uma possível gama, uma jogos de referência e uma gama de referência, além de permitir que os GMAs mapeiem-os de maneiras diferentes. Além disso, os GMAs têm informações sobre o eixo neutro do dispositivo. A discussão a seguir aborda como lidar com situações em que os jogos de referência e os jogos de referência difíceis foram recolhidos uns nos outros.

![Diagrama que mostra o GM A com dois descritores de jogos não recolhidos.](images/gmmp-image091.png)

**Figura 22:** GMA com dois descritores de jogos não recolhidos

Você poderá ver este exemplo se mapear de um dispositivo de entrada, como uma câmera ou scanner que é caracterizado por um destino reflexivo, para o espaço scRGB. Aqui, as cores mais claras que são mais claras do que o branco de referência são realçadas especular. Na prática, identificar uma câmera com um destino pode não gerar a gama completa de valores possíveis na câmera; no entanto, realças especular e cores muito chromatic encontradas por natureza. (Destinos transmissivos geralmente têm um patch que é a densidade mínima possível na mídia. Com esse destino, realçamentos especular se enquadram no intervalo do destino.) A referência preta para um destino reflexivo seria o início da região de sombra preta. Ou seja, é provável que haja cores nas sombras mais escuras do que o preto no destino. Se a imagem contiver muito conteúdo interessante nessa região, poderá valer a pena preservar essa variação tonal.

![Diagrama que mostra o GM A com uma gama de destino recolhido.](images/gmmp-image095.png)

**Figura 23:** GMA com a gama de destino recolhido

A Figura 23 mostra um possível algoritmo de mapeamento de jogos quando a gama de destino fornece apenas o intervalo entre branco e preto do dispositivo e não há cores possíveis fora desse gamut. Isso provavelmente ocorrerá para dispositivos de saída típicos, como impressoras. As cores possíveis são mapeadas para a borda da gama de destino. Mas não tem uma curva de tom para o dispositivo de saída. O GMA deve selecionar algum ponto neutro de luminância inferior a ser usado como um destino de mapeamento para a referência branca. Um algoritmo sofisticado pode fazer isso histogramando as luzidades na imagem de origem e vendo quantos estão no intervalo esperado, mas mais leve do que o branco de referência. Quanto mais leve for, mais espaço será necessário no dispositivo de destino entre os pontos mapeados para os destaques especular e a referência em branco. Um algoritmo mais simples pode escolher uma distância arbitrária abaixo da escala de luz em branco do dispositivo, como 5%. Uma abordagem semelhante se aplica ao mapeamento do máximo preto e preto-sombra.

Depois de gerar a curva de tom de destino, você pode mapear em um método semelhante ao usado na Figura 23 anterior. Todos os pontos na curva de tom de destino se enquadram na gama de dispositivos e todos os pontos no mapeamento devem estar dentro da gama de dispositivos.

Se você inverter as figuras esquerdas e direitas e as direções das setas na Figura 23, poderá descrever o caso em que a imagem de origem tem apenas um gamut de referência e os três jogos do dispositivo de saída não foram recolhidos uns nos outros. Um exemplo disso pode ser o mapeamento de um monitor para scRGB. Novamente, o GMA deve sintetizar os pontos de controle para os cinco pontos na curva de tom da imagem de origem. Alguns mapeamentos podem colocar todos os pontos da curva de tom dentro da gama de dispositivos scRGB, enquanto outros mapeamentos podem usar mais da gama scRGB mapeando branco difuso para a referência branca e permitindo que o branco especular mapeie para um valor mais claro.

Por fim, você tem o caso em que ambos os dispositivos têm apenas a gama de referência, que é como a maioria dos algoritmos de mapeamento de jogos funciona. Portanto, você pode resolver isso apenas voltando para os algoritmos atuais. Como alternativa, se você tiver uma maneira razoável de determinar os cinco pontos de referência para os dispositivos de origem e de destino, poderá organizar o mapeamento dos pontos de referência.

Os jogos de dispositivo contêm mais de cinco pontos de referência no eixo neutro. Eles representam apenas os limites entre regiões potenciais na imagem. Entre cada um dos pontos de referência, você pode usar qualquer uma das técnicas de mapeamento de gamut existentes. Portanto, você pode cortar o intervalo de cores inesperadas e compactar todas as cores entre o branco e o preto esperados ou pode cortar todas as cores fora do intervalo de referência e compactar dentro desse intervalo. Há muitas possibilidades, que podem ser implementadas em DIFERENTES GMAs. Além disso, os GMAs podem compactar e cortar de maneiras diferentes. Todas essas combinações são abordadas nessa invenção.

Até agora nesta discussão, o gamut foi tratado como se fosse apenas uma função do dispositivo no qual a imagem foi criada, capturada ou exibida. No entanto, não há nenhum motivo pelo qual todas as imagens de um dispositivo devem ter a mesma gama. Os GMAs dependem dos dados no GBD. Se o descritor for alterado entre imagens, não haverá como os GMAs saberem. Em particular, se as imagens não têm realças especulares, os GMAs terão um desempenho melhor se o descritor de gamut não mostrar que há cores mais claras do que branco difuso.

Na nova arquitetura de CTE, é possível usar mais de um GMA. O uso de vários GMAs é inerentemente mal definido. Por exemplo, se um dispositivo de captura associar um GMA à sua "aparência", ele tende a fazer isso com um gamut de destino "direcionado". O mesmo é verdadeiro para dispositivos de saída e jogos de origem "direcionados". A gama sRGB é uma gama implícita comumente direcionada. Portanto, é altamente recomendável que você use um único GMA, se a previsibilidade for uma prioridade. Um único fluxo de trabalho de GMA deve ser o padrão para todos os fluxos de trabalho, especialmente fluxos de trabalho de consumidor e prosumer. Embora o mapeamento de jogos para reprodução preferencial deva ser feito uma vez, há instâncias em que vários processos de mapeamento são incluídos. Primeiro, para a prova, você faz um mapeamento preferencial para a gama do dispositivo de destino final e, em seguida, uma renderização colorimétrica para a gama do dispositivo de prova. Em segundo lugar, alguns tipos de mapeamento são usados para alterar as características da imagem, mas não são incluídos para mapear para uma gama de dispositivos, por exemplo, ajustando a curva de tom ou a chromaticidade. Se vários GMAs são usados, a interface de transformação utiliza uma matriz de mapas de jogos limitados, ou seja, mapas de jogos que foram inicializados com um par de descrições de limite de jogos. Quando há mais de um mapa de jogos, o limite de jogos de entrada para um mapa de jogos bem-sucedido deve ser o mesmo que o limite de gama de saída de seu antecessor.

A função de limite de jogos do dispositivo pega o mecanismo de modelo do dispositivo e os parâmetros analíticos e deriva um limite de jogos do dispositivo de cores descrito como uma lista de vértices ordenada do chassi convexa do gamut do dispositivo. A lista de vértices ordenados é armazenada em CIEJab. A estrutura da lista de vértices ordenados é otimizada para aceleração de hardware pelo DirectX. Essa abordagem tem muitas soluções conhecidas (pesquise "Convex hull DirectX" na Web e você obterá mais de 100 acertos). Também há uma referência de 1983 neste tópico (Computer Graphics Theory and Application, "Shiphulls, b-spline surfaces and cadcam" pp. 34-49), com referências de 1970 a 1982 sobre o tópico.

Duas técnicas diferentes podem ser usadas para calcular os triângulos no shell de jogos. Para outros dispositivos diferentes de dispositivos RGB aditivos, você computa um chassi convexa. Você pode considerar a investigação do suporte de chassi não convexa para outros dispositivos se tiver acesso direto a esses dispositivos para validar a robustez, o desempenho e a fidelidade dos algoritmos. Esse é um processo conhecido que não requer mais descrição. A técnica usada para dispositivos RGB aditivos é descrita da seguinte forma.

GbDs diferentes têm vantagens e desvantagens. A representação de enxadas convexa garante propriedades geométricas interessantes, como fatias de matiz convexa que fornecem um ponto de interseção exclusivo com um raio emanando de um ponto no eixo neutro. A desvantagem da representação convexa de chassi também é convexa. É conhecido que muitos dispositivos, especificamente dispositivos de exibição, têm jogos que estão longe de serem convexas. Se o gamut real se desvia significativamente da suposição de convexidade, a representação convexa de chassi seria imprecisa, possivelmente até a medida em que não representa a realidade.

Depois de adotar um GBD que fornece uma representação razoavelmente precisa da gama real, outros problemas surgem, alguns devido ao próprio conceito de fatia de matiz. Há pelo menos duas situações de vulnerabilidade. Na Figura 24 a seguir, uma gama CRT gera fatias de matiz com "ilhas". Na Figura 25, uma gama de impressoras gera uma fatia de matiz com parte do eixo neutro ausente. As fatias de matiz não são causadas por limites de jogos particularmente interessantes nesses casos. Eles são causados pelo próprio conceito de fatia de matiz, porque (a) ele é levado ao longo do matiz constante e (b) ele leva apenas uma metade do plano que corresponde ao ângulo de matiz.

![Diagrama que mostra uma exibição superior e uma exibição lateral do "curving in" nos matizes azuis.](images/gmmp-image097.jpg)

**Figura 24:** um monitor CRT típico tem um gamut que mostra "curving in" nos matizes azuis. Se as fatias de matiz são feitas dentro desse intervalo de matiz, as ilhas isoladas podem aparecer nas fatias de matiz.

![Diagrama de um gamut com uma "lacuna" em seu eixo neutro.](images/gmmp-image099.jpg)

**Figura 25:** uma impressora pode ter uma gama que tem "lacuna" em seu eixo neutro. Quando uma fatia de matiz é tomada (que é apenas metade do plano), há uma "diferença" na parte do limite que é o eixo neutro. Isso pode ser difícil de resolver de forma algorítmicamente.

Para resolver essas dificuldades, é proposta uma nova estrutura que abandonará o conceito de fatia de matiz usada como ponto de partida. Em vez disso, a estrutura usa o conjunto de "elementos de linha de limite" ou linhas que estão no limite de jogos. Eles não fornecem necessariamente uma visualização geométrica coerente, como fatias de matiz, mas dão suporte a todas as operações comuns de jogos. Além de resolver os problemas mencionados anteriormente, essa abordagem também sugere que a construção de fatias de matiz, mesmo quando possível, é computacionalmente desperdício.

### <a name="triangulation-of-the-gamut-boundary"></a>Imposição do limite de gamut

O ponto de partida é um GBD que consiste em uma triangularção do limite de jogos. Métodos conhecidos de construção de GBDs geralmente fornecem essa triangularção. Para concretar, um método de construção de GBDs para dispositivos aditivos seu espaço de dispositivo é descrito aqui. Esses dispositivos incluem monitores (baseados em CRT e baseados em LCD) e projetores. A geometria simples do cubo permite que você introduza uma rede regular no cubo. As faces de limite do cubo podem ser ofetadas de várias modas, como as mostradas na Figura 26. A arquitetura fornece um modelo de dispositivo para o dispositivo para que os valores colorimétricos dos pontos de rede possam ser obtidos de forma algorítmicamente ou medidas tenham sido feitas diretamente para esses pontos. A arquitetura também fornece CIECAM02, para que você possa supor que os dados inativos já foram mapeados para o espaço CIECAM02 Dem. Em seguida, cada ponto de estilos nas faces de limite do cubo RGB tem um ponto correspondente no espaço Dem. As conexões de pontos que formam o conjunto de triângulos no espaço RGB também induz um conjunto de triângulos no espaço Demão. Esse conjunto de triângulos forma uma ofisseção razoável do limite de jogos se (a) a grade no cubo RGB estiver bem o suficiente e (b) a transformação do espaço do dispositivo para o espaço de cores uniforme estiver topologicamente bem-comportada; ou seja, ele mapeia o limite para o limite e não transforma a gama de dentro para fora para que os pontos interiores se tornem pontos de limite.

![Diagrama que mostra um método simples para fazer a trianglagem do limite de jogos de um dispositivo com R G B como seu espaço de dispositivo.](images/gmmp-image100.png)

**Figura 26:** um método simples para fazer o limite de jogos de um dispositivo com RGB como seu espaço de dispositivo

### <a name="boundary-line-elements"></a>Elementos de linha de limite

Central para essa estrutura é o conceito de elementos de linha de limite; um conjunto de segmentos de linha que (a) estão no limite de jogos e (b) estão em um plano. Nesse caso, o plano é um plano de matiz. Cada segmento de linha é o resultado da interseção do plano com um triângulo de limite de jogos. Embora muitos pesquisadores tenham usado a construção da interseção de um plano com triângulos de limite, eles geralmente analisam a relação entre esses segmentos de linha e tentam construir um objeto geométrico coerente fora dos segmentos de linha. Diferentes algoritmos foram organizados para seguir esses segmentos de linha um após o outro até que uma fatia de matiz inteira seja obtida e muitas tentativas tenham sido feitas para acelerar o processo de pesquisa.

Essa abordagem é diferente. Intersecção do plano com os triângulos para obter os segmentos de linha. Em seguida, considere esses segmentos de linha como *os objetos conceituais* básicos. É necessário analisar a relação entre os segmentos de linha; você não precisa saber como eles estão interconectados entre si. Esse ponto de vista resolve o problema de fatia de matiz com ilhas. As abordagens conhecidas que tentam construir a fatia de matiz pressupom que, se um começar com um segmento de linha e o seguir para o próximo segmento de linha e assim por diante; ele eventualmente leva de volta ao ponto de partida, no qual uma fatia de matiz inteira seria construída. Infelizmente, essa abordagem teria perdido a ilha (e no pior cenário, o continente). Ao não invassar na obtenção de uma imagem geométrica coerente; ou seja, fatia de matiz, você pode lidar com o problema da ilha sem esforço. Outra diferença importante nessa abordagem é que, para acelerar a construção de segmentos de linha, ele usa um "filtro de triângulo". O filtro de triângulo lança determinados triângulos que definitivamente não produzirão segmentos de linha que seriam úteis na operação de jogos atual. Como a interseção de um triângulo com o plano é computacionalmente cara, isso melhora a velocidade. Um efeito colateral é que você não pode construir a fatia de matiz porque alguns segmentos de linha estariam ausentes devido à filtragem de triângulo.

### <a name="gamut-operation-checkgamut"></a>Operação gamut: CheckGamut

O exemplo a seguir explicará como a estrutura funciona e como CheckGamut é executada, ou seja, a operação de verificação se uma cor está em jogo.

A estrutura geral é ilustrada na Figura 27 a seguir. Há vários componentes. Os componentes rotulados em itálico são componentes que podem ser diferentes na implementação, dependendo da operação de jogos em questão. Os outros componentes são invariáveis em todas as operações de jogos. Para começar, a ***Entrada é*** um conjunto de atributos de cor. No caso de CheckGamut, é a cor da consulta. Na Figura 27 e na discussão a seguir, supõe-se que o ângulo de matiz está entre os atributos de cor de entrada ou pode ser obtido deles. Esse é claramente o caso se a entrada for o ponto de cor inteiro, seja em Hue ou JCh, a partir do qual você poderá calcular o ângulo de matiz. Observe que o ângulo de matiz só é necessário porque os planos de matiz estão sendo usados. Dependendo da operação de jogos em questão, talvez não seja necessário usar o plano de matiz. Por exemplo, na construção da rotina CheckGamut, talvez você queira usar planos da constante J. Essa é uma generalidade que não será usada nem discutida ainda mais; mas pode ser útil lembrar dessa flexibilidade da metodologia para dar suporte a outras operações de jogos quando o plano de matiz pode não ser a melhor opção.

![Diagrama que mostra o fluxo para dar suporte a operações de jogos.](images/gmmp-image112.jpg)

**Figura 27:** a estrutura para dar suporte a operações de jogos

O ângulo de matiz, que é obtido diretamente das entradas ou computado das entradas, é usado para inicializar o plano de matiz rotulado Plano de **Matiz** Completo na figura. "Completo" é enfatizado porque esse é o plano completo, não apenas o meio plano que contém o matiz. O plano completo contém o ângulo de matiz de entrada e o ângulo de 180 graus oposto a ele. A principal funcionalidade do plano de matiz é a função Intersect, que é explicada na subseção a seguir, Plano de Matiz Completo: Intersect. Suponha que o GBD já tenha sido construído e que o conjunto de Triângulos de Limite de **Gamut** está disponível. Intersecção dos triângulos que sobreviveram ao * Filtro *_de Triângulo_* _ com o plano de matiz usando Intersect. O _componente Filtro de Triângulo* é rotulado em itálico, o que significa que o componente varia na implementação para diferentes operações de jogos. O *Filtro de Triângulo* para CheckGamut é explicado na seção Operação de Gamut: CheckGamut (continuação). O resultado da interseção de um triângulo com o plano de matiz é vazio ou um Elemento **de** Linha de Limite , ou seja, um par de pontos distintos. Se o resultado não estiver vazio,**_ ele será passado para o * Processador de Elemento de Linha , que novamente faz coisas diferentes dependendo da operação de jogos. O Processador de Elemento de Linha* atualiza a estrutura de dados _interna, ***Dados** Processados_ Internos , cujo conteúdo ou layout também depende da operação de jogos. Em geral, os Dados Processados Internos* contêm a "resposta" para o problema, que é atualizada continuamente com cada novo Elemento de Linha _de Limite encontrado. Quando todos os Elementos de Linha de Limite foram processados, a resposta foi encontrada. Ele permanece para acessá-lo por meio do ***Adaptador de Saída**_. Como a _Internal dados processados* é específica da operação de jogos, o Adaptador de Saída *também* é específico da operação de jogos.

### <a name="full-hue-plane-intersect"></a>Plano de matiz completo: Interseção

A função Intersect calcula a interseção do plano de matiz e um triângulo. Por mais simples que pareça, essa função é importante por dois motivos.

Primeiro, a interseção de cada borda do triângulo com o plano pode gerar três pontos de interseção, uma situação geométrico impossível. O motivo pelo qual isso pode acontecer na computação é que, quando os cálculos são feitos em ponto flutuante, por exemplo, formato IEEE, há incertezas ou "ruído numérico", em cada etapa que afeta a conclusão de se uma borda intersecção do plano. Quando o plano cruza as bordas em uma situação de quase erro, os pontos de interseção estão próximos uns dos outros e a determinação de se um ponto de interseção está dentro da borda é aleatória. Embora o ruído nos valores numéricos dos pontos seja pequeno, a conclusão qualitativa de que há mais de dois pontos de interseção é geométrico impossível e difícil de lidar corretamente no algoritmo.

Em segundo lugar, essa função está no loop crítico para cada borda de cada triângulo filtrado, portanto, é importante otimizar sua eficiência o máximo possível.

Para resolver o primeiro problema De ruído numérico, execute os cálculos em inteiros. Para resolver o segundo problema de otimização de sua eficiência, armazena em cache o atributo mais usado de cada vértice ou o "produto de ponto" associado a cada vértice. A passagem de inteiros é uma maneira típica de garantir a consistência geométrica. A ideia básica é que, se você tiver que quantificar, faça isso no início. Em seguida, cálculos subsequentes podem ser executados em inteiros e, se os inteiros são largos o suficiente para que não haja nenhum risco de estouro, os cálculos podem ser feitos com precisão infinita. A função de quantização a seguir é útil para essa finalidade.

ScaleAndTruncate(x) = Parte inteira de x \* 10000

O fator de dimensionamento 10000 significa que o número de ponto flutuante de entrada tem quatro casas decimais, o que é preciso o suficiente para esse aplicativo. Dependendo do intervalo de valores do espaço de aparência de cor, você deseja escolher um tipo inteiro com bits largos o suficiente para manter os cálculos intermediários. Na maioria dos espaços de aparência de cor, o intervalo de cada coordenada está dentro do intervalo -1.000 a 1.000. A coordenada quantificada tem um valor absoluto máximo possível de 1.000 \* 10.000 = 10.000.000. Como você verá, a quantidade intermediária é um produto de ponto, que é uma soma de dois produtos de coordenadas, portanto, tem um valor absoluto máximo possível de 2 \* (10.000.000) = 2?10 . O número de bits necessários é log (2?10 ) = 47,51. Uma opção conveniente para o tipo inteiro é, portanto, inteiros de 64 bits.

Para garantir que a interseção de um plano com um triângulo sempre dê um conjunto vazio ou um conjunto de dois pontos, você deve considerar o triângulo como um todo, não como bordas individuais do triângulo separadamente. Para entender a situação geométrica, considere as "distâncias assinadas" dos vértices do triângulo do plano de matiz. Não calcule essas distâncias assinadas diretamente; em vez disso, calcule os produtos de ponto dos vetores de posição dos vértices com o vetor normal quantificado para o plano. Mais especificamente, durante a inicialização do plano de matiz, o vetor normal quantificado é calculado da seguinte forma.

NormalVector = (ScaleAndTruncate(-sin(hue)), ScaleAndTruncate(cos(hue)))

Observe que esse vetor é um vetor bidimensional. Você pode usar um vetor bidimensional porque o plano de matiz é vertical, portanto, o terceiro componente do vetor normal é sempre zero. Além disso, uma tabela de pesquisa de produtos de ponto é inicializada para ter uma entrada para cada vértice dos Triângulos de Limite de Gamut e o produto de ponto correspondente definido como um valor inválido.

Durante uma operação de intersecção do plano de matiz com um triângulo, o produto de ponto de cada vértice do triângulo é procurado. Se o valor na tabela de lookup for o valor inválido, o produto de ponto será calculado usando a expressão a seguir.

NormalVector. a \* ScaleAndTruncate (Vertex. a) + NormalVector. b \* ScaleAndTruncate (vértice. b)

Novamente, o componente J do vértice nunca é usado, pois o vetor normal é horizontal. Esse produto de ponto é salvo na tabela de pesquisa para que não precise ser computado novamente se o produto de ponto do vértice for consultado posteriormente.

Caching permite uma rápida determinação de se uma borda cruza o plano, depois que os produtos de ponto são tabulados na tabela de pesquisa, que é criada progressivamente conforme os vértices são processados.

![Diagrama que mostra a interseção do plano de matiz com um triângulo.](images/gmmp-image114.jpg)

**Figura 28** : interseccionando o plano de matiz com um triângulo

Para o triângulo da figura 28 Interseccionar o plano de matiz em um segmento de linha que não é degenerado, os produtos de ponto dos vértices devem estar em um dos padrões a seguir, quando classificados em ordem crescente.

0, 0, +; -, 0, 0; -, 0, +; -,-,+; -,+,+

Um ponto de extremidade do segmento de linha surge quando o plano é interseccionado por uma borda com vértices que têm sinais diferentes no produto do ponto. Se o sinal for zero, o vértice estará diretamente no plano e a interseção da borda com o plano será o próprio vértice. Observe também que os casos 0, 0, 0; -,-, 0; 0, +, + não são relatados. O primeiro caso (0, 0, 0) significa que o triângulo inteiro está no plano. Isso não é relatado porque cada borda do triângulo deve pertencer a um triângulo vizinho que também não se encontra inteiramente no plano. A borda será relatada quando esse triângulo for considerado. Os outros dois casos (-,-, 0 e 0, +, +) correspondem à configuração geométrica que o triângulo toca no plano em um vértice. Esses casos não são relatados porque não fornecem aumento para um segmento de linha que não é degenerado.

O algoritmo anterior determina quando calcular uma interseção entre uma borda do triângulo e o plano de matiz. Depois que uma borda é determinada, a interseção é calculada usando equações paramétricas. Se um dos produtos de ponto for zero, a interseção é o próprio vértice, portanto, nenhum cálculo é necessário. Supondo que os dois produtos de ponto dos vértices da borda sejam diferentes de zero, vertex1 é o vértice com o ponto *negativo* dotProduct1 do produto; e vertex2 é o vértice com o ponto *positivo* dotProduct2 do produto. Essa ordem é importante para garantir que o ponto de interseção calculado não dependa de como a ordenação dos vértices aparece na representação da borda. O conceito geométrico da borda é simétrico em relação aos seus vértices. O aspecto computacional do uso de equações paramétricas da borda apresenta assimetria (escolha de vértice inicial), que pode dar um ponto de interseção um pouco diferente devido ao ruído numérico e à condição das equações lineares a serem resolvidas. Dito isso, o ponto de interseção, a interseção, é fornecido pelo seguinte.

t = dotProduct1/(dotProduct1-dotProduct2)

interseção. J = vertex1. J + t \* (vertex2. J-vertex1. J

interseção. a = vertex1. a + t \* (vertex2. a-vertex1. a)

interseção. b = vertex1. b + t \* (vertex2. b-vertex1. b)

### <a name="gamut-operation-checkgamut-continued"></a>Operação de gama: CheckGamut (continuação)

O algoritmo geométrico básico usado para verificação de gama é contar o número de raios cruzados. Para um determinado ponto de consulta, considere um raio começando com o ponto de consulta e apontando para cima (direção J). Contar o número de vezes que esse raio cruza o limite de gama. Se esse número for par, o ponto de consulta estará fora do gamut. Se esse número for ímpar, o ponto estará dentro. Em princípio, esse algoritmo pode ser implementado em 3-D, geralmente é afetado por dificuldades causadas por situações de degeneração, como o raio (parte) de um triângulo de limite, ou um Degeneracy dimensional inferior, como o raio (parte) de uma borda de um triângulo de limite. Mesmo em 2-D, você precisa lidar com essas situações de degeneração; Mas o problema é mais simples e foi resolvido de maneira satisfatória. Consulte \[ O'Rourke \] .

Para um determinado ponto de entrada jab, determine seu ângulo de matiz h da seguinte maneira.

h = ATAN (b/a),

Inicialize o plano de matiz e determine os elementos da linha de limite correspondentes a este plano de matiz. Como os elementos da linha de limite só são relevantes se eles cruzam o raio de cima, configure um filtro de triângulo para remover triângulos que fornecem elementos de linha que definitivamente não interseccionam o raio de cima. Nesse caso, considere a caixa delimitadora do triângulo. O raio para cima não interseccionará o triângulo se o ponto de consulta estiver fora da conversão de "sombra" pela caixa delimitadora se uma fonte de luz estava diretamente acima. Aumente isso ligeiramente com uma tolerância fixa para permitir ruídos numéricos para que você não jogue inadvertidamente triângulos que possam dar elementos de linha úteis. O resultado é o cilindro retangular semiinfinito mostrado na figura 29. Verificar se o ponto de consulta está dentro ou fora desse cilindro pode ser implementado com eficiência usando desigualdades simples.

![Mostra o filtro de triângulo para CheckGamut.](images/gmmp-image116.jpg)

**Figura 29** : filtro de triângulo para CheckGamut

CheckGamut tem três componentes específicos de operação de gama: *dados processados internos*,*processador de elemento de linha* e adaptador de *saída*. Os *dados processados internos* são uma lista de elementos de linha que foram processados por *processador de elemento de linha*. Nesse caso, o *processador de elemento de linha* simplesmente adiciona um elemento de linha à lista. A estrutura de dados interna para *dados processados internos* pode ser uma lista vinculada ou uma matriz que pode crescer em tamanho.

O *adaptador de saída* é um módulo que acessa a lista de elementos de linha, determina se um elemento de linha cruza o raio superior (contagem 1) ou não (contagem 0). Somar todas essas contagens fornece uma contagem total. O *adaptador de saída* , por fim, gera uma resposta de "Sim" (em gamut) ou "não" (fora do gamut), dependendo se a contagem total é ímpar ou uniforme. A etapa em que você determina se um elemento de linha cruza o raio de cima merece atenção, pois é aí que ocorre o problema do Degeneracy e também o problema de excesso de contagem. Após \[ O'Rourke \] , para um elemento de linha cruzar o raio, o ponto de extremidade direito (o ponto de extremidade com croma maior) deve ser estritamente no lado direito do raio. Isso garante que, se um ponto de extremidade já estiver exatamente no raio, ele será contado apenas uma vez. A mesma regra também resolve a situação de degeneração em que o elemento line está exatamente no raio. Você não incrementa a contagem para este elemento de linha.

A figura 30 mostra os elementos de linha resultantes de uma gama de amostra com o ponto de consulta em várias posições.

![Diagrama que mostra os elementos de linha resultantes de uma gama de amostra com o ponto de consulta em várias posições.](images/gmmp-image118.jpg)

**Figura 30** : como o CheckGamut funciona

### <a name="minimum-color-difference-gamut-mapping"></a>Mapeamento de gama da diferença de cor mínima

O mapeamento de gama da diferença de cor mínima, MinDEMap, tem uma especificação simples: se uma cor estiver em gamut, não faça nada. Se uma cor estiver fora do gamut, projeta-a no ponto "mais próximo" no limite de gamut. A palavra-chave "mais próxima" não é bem definida até que você especifique a equação de diferença de cor a ser usada. Na prática, para tornar a computação mais fácil e rápida, a distância euclidiana do espaço de aparência da cor escolhida, ou uma variante dela, é usada como a métrica de diferença de cor. A vantagem da métrica euclidiana é que ela é compatível com o produto dot do espaço, o que torna possível o uso de algebra linear. Em detalhes, se um "produto de ponto" for definido no espaço, uma distância poderá ser definida como a raiz quadrada do produto de ponto do vetor de diferença com ele mesmo. Um produto de ponto geralmente pode ser definido por uma matriz 3x3 definida positiva A.

u? v = u <sub>T</sub> AV

onde o lado direito é a multiplicação de matriz usual. Se um for a matriz de identidade, o produto Standard dot será recuperado. Na prática, se jab for o espaço de cores, você não deseja misturar os componentes, portanto, uma matriz diagonal diferente da matriz de identidade pode ser usada. Além disso, talvez você queira manter a escala em a e b inalterada para que a medida de matiz seja preservada. Portanto, uma variação útil do produto Standard euclidiana dot é a seguinte.

w <sub>j</sub> (componente j de você) (componente j de v) + (um componente de você) (um componente do v) + (componente b de você) (componente b de v)

onde w <sub>J</sub> é um número positivo. Uma variação adicional é permitir que w <sub>J</sub> varie de acordo com o ponto de consulta de entrada:

w <sub>j \ =</sub> w <sub>j</sub> (queryPoint)

O resultado final é uma medida de distância que é assimétrica em relação aos dois pontos e com pesos relativos diferentes na claridade e croma ou matiz à medida que o ponto de consulta de entrada varia. Isso é de acordo com algumas observações sobre a percepção de cores humanas de que as diferenças de cores não são ponderadas igualmente em todas as dimensões. Foi detectado que as pessoas são menos sensíveis às diferenças na claridade do que são diferenças no matiz e no croma.

A função de peso a seguir é útil.

w <sub>J</sub> = k ₂-k ₁ (C-c m ₐ ₓ) n

em que k ₂ = 1, k ₁ = 0,75/(C m ₐ ₓ) n, C m ₐ ₓ = 100, n = 2 e C é o menor de croma do ponto de consulta e C m ₐ ₓ.

de forma que um peso de 0,25 seja colocado no termo J quando croma for zero e um peso de 1 quando croma for 100. A tendência de colocar menos peso em J quando croma é pequena e mais peso em J quando croma é grande segue o uso recomendado para CMC e CIEDE2000.

![Graph que mostra a função weight no componente J da métrica.](images/gmmp-image119.png)

**Figura 31** : a função Weight no componente J da métrica

Use o espaço jab para o exemplo a seguir. É computacionalmente exigente Pesquisar todos os triângulos de limite para determinar o ponto mais próximo na métrica euclidiana. Veja a seguir uma abordagem simples para tornar esse processo o mais eficiente possível, sem introduzir suposições adicionais que possam acelerar o processo, mas também terminar em apenas uma resposta aproximada. Primeiro, é necessário entender o procedimento geométrico do projeto de um ponto no triângulo determinado. Uma descrição é fornecida aqui.

Uma projeção ortogonal no plano infinito que contém o triângulo é executada pela primeira vez. A distância mais curta do ponto de consulta do plano pode ser determinada em duas etapas.

**(a)** Calcule o vetor normal da unidade para o triângulo.

**(b)** calcular o produto de ponto do vetor normal da unidade e um vetor formado do ponto de consulta e um ponto no triângulo; ou seja, um de seus vértices. Como o vetor normal tem comprimento de unidade, o valor absoluto deste ponto é a distância do ponto de consulta do plano.

O ponto projetado pode não ser a resposta, pois pode estar fora do triângulo. Portanto, você deve executar uma verificação primeiro. O cálculo é equivalente ao cálculo das coordenadas barycentric do ponto projetado em relação ao triângulo. Se o ponto projetado for determinado para estar dentro do triângulo, será a resposta. Caso contrário, o ponto mais próximo é adquirido em uma das bordas do triângulo. Faça uma pesquisa em cada uma das três bordas. A determinação da projeção do ponto de consulta em uma borda é um processo semelhante à projeção no triângulo, mas uma dimensão é menor. Uma projeção ortogonal é calculada pela primeira vez. Se o ponto projetado estiver na borda, será a resposta. Caso contrário, o ponto mais próximo é adquirido em um dos dois pontos de extremidade. Executar uma pesquisa nos dois pontos de extremidade; ou seja, calcule a distância do ponto de consulta de cada um e compare qual deles é menor.

O exame cuidadoso revela que há muita pesquisa repetida quando você passa por todos os triângulos porque uma borda é sempre compartilhada por dois triângulos e um vértice compartilhado por pelo menos três bordas. Além disso, você não está muito interessado em encontrar o ponto mais próximo de um triângulo específico; em vez disso, você está interessado em encontrar o ponto mais próximo de todo o limite da gama. No entanto, um triângulo específico seria aquele em que isso é conseguido. Há duas estratégias que você pode usar para acelerar a pesquisa.

**Estratégia I**. Cada vértice será processado, no máximo, uma vez. Cada borda será processada, no máximo, uma vez.

**Estratégia II**. Em qualquer ponto da pesquisa, você tem um melhor candidato com a melhor distância correspondente. Se você puder determinar, por uma verificação rápida, que um triângulo não é capaz de dar uma distância melhor, não há necessidade de continuar o cálculo ainda mais. Você não precisa do ponto e da distância mais próximos deste triângulo.

![Diagrama que mostra o fluxo do mínimo DE mapeamento.](images/gmmp-image120.png)

**Figura 32** : esquemáticos mínimos de mapeamento

A Figura 32 mostra o fluxo geral de lógica para o mapa de gamut MinDEMap. Para um ponto de consulta, a função CheckGamut é invocada pela primeira vez. Se o ponto estiver em gamut, o mapa será não operacional. Se o ponto estiver fora do gamut, chame ProjectPointToBoundary. Agora, passe para a figura 33. Neste ponto, supõe-se que os valores a seguir foram computados.

**(a)** unidade de vetor normal para cada triângulo de limite de gamut em relação ao produto Standard dot.

**(b)** lista de vértices e lista de borda, além da lista de triângulos.

![Diagrama que mostra a rotina ' ProjectPointToBoundary '.](images/gmmp-image122.jpg)

**Figura 33** : a rotina ProjectPointToBoundary

Tudo isso é uma sobrecarga constante e diminuiria o custo se consultas suficientes a esse limite de gama forem feitas. Normalmente, esse é o caso quando você cria um LUT de transformação de um dispositivo para outro, onde há apenas duas gamas fixas, e o LUT de transformação é executado por pontos na grade de amostra uniforme. Você computa previamente os vetores normais em relação ao produto Standard dot, mesmo que a noção da perpendicularidade se baseie no produto de ponto ponderado, que depende do ponto de consulta, conforme explicado anteriormente. O motivo é que um vetor normal em relação ao produto de ponto ponderado pode ser obtido facilmente do vetor normal em relação ao produto Standard dot. Se n ₀ for um vetor normal em relação ao produto Standard dot, então

n = (componente J-de n ₀/w <sub>J</sub>, a-componente de n ₀, b-Component de n ₀)

é normal para o triângulo em relação ao produto de ponto ponderado. Por causa dessa relação, ainda é benéfico computar n ₀, mesmo que ele deva ser ajustado com base no ponto de consulta.

A rotina ProjectPointToBoundary começa redefinindo o "histórico processado" dos vértices e das bordas. Essas são tabelas de sinalizadores BOOLIANos que controlam se um vértice ou uma borda foi visitada antes. Ele também redefine a variável ShortestDistance para "Infinity", que é o valor codificado máximo no sistema de números de ponto flutuante usado. Em seguida, ele é executado por meio de um loop, pesquisando o ponto mais próximo de cada triângulo usando a chamada ProcessTriangle. ProcessTriangle é a rotina para atualizar a variável ShortestDistance e está claramente no loop crítico. Uma otimização é parar quando o resultado é bom o suficiente. Após cada chamada para ProcessTriangle, a variável ShortestDistance é examinada. Se ele satisfizer um limite predefinido, você poderá parar. O limite predefinido depende do espaço de cores usado e da precisão necessária do sistema de imagem colorida. Para um aplicativo típico, você não deseja fazer trabalho desnecessário se a diferença de cores for menor do que o que pode ser discernido pela visão humana. Para CIECAM02, essa diferença de cor é 1. No entanto, use um valor de limite de 0, 5 na implementação para preservar a precisão dos cálculos, pois isso pode ser apenas uma etapa intermediária em uma cadeia de transformações.

ProcessTriangle implementa a estratégia anterior II. Obter um vetor normal do vetor normal da unidade previamente computada para o triângulo em relação ao produto de ponto padrão, ele computa a distância do ponto de consulta para o plano infinito que contém o triângulo formando o produto de ponto do vetor normal da unidade e o queryVector, o vetor de um dos vértices do triângulo,  vertex1, para o ponto de consulta, queryPoint.

queryVector = queryPoint-vertex1

Distance = \| normalVector \* queryVector \| / \| \| normalVector\|\|

Esse é um cálculo relativamente barato e a distância é necessária para realizar cálculos adicionais. Se essa distância não for menor que a melhor distância atual, ShortestDistance, esse triângulo não produzirá uma distância melhor, pois não dará uma distância melhor do que o plano que a contém. Nesse caso, você retorna o controle para o loop de triângulo. Se a distância for menor do que ShortestDistance, potencialmente, você terá um ponto mais próximo, se esse ponto estiver dentro do triângulo. Você deve executar alguns cálculos "difíceis" (embora nada além de algebra linear) para determinar isso. Se os outros dois vértices do triângulo forem vertex2 e vertex3, formate os vetores de base firstBasisVector e secondBasisVector.

firstBasisVector = vertex2-vertex1

secondBasisVector = vertex3-vertex1

Use o sistema linear a seguir de equações para resolver os desconhecidos e v.

firstBasisVector \* queryVector = (firstBasisVector \* firstBasisVector) u + (firstBasisVector \* secondBasisVector) v

secondBasisVector \* queryVector = (secondBasisVector \* firstBasisVector) u + (secondBasisVector \* secondBasisVector) v

e as condições para o ponto projetado estar dentro do triângulo são:

0 ≤ u ≤ 1, 0 ≤ v ≤ 1 e + v ≤ 1

Após esse cálculo, se for determinado que o ponto projetado está dentro do triângulo, você encontrará um novo ponto mais próximo; a distância que você calculou no início é a nova distância mais curta. Nesse caso, atualize as variáveis ShortestDistance e ClosestPoint. Se o ponto projetado estiver fora do triângulo, você poderá encontrar um ponto mais próximo em uma de suas bordas. Portanto, você pode chamar a rotina ProcessEdge em cada uma das três bordas.

![Diagrama que mostra o fluxo das rotinas ProcessEdge e ProcessVertex.](images/gmmp-image124.jpg)

**Figura 34** : rotinas ProcessEdge e ProcessVertex

A rotina ProcessEdge implementa a estratégia I, que é ilustrada na Figura 34. ProcessEdge começa verificando se a borda foi processada antes. Nesse caso, nenhuma ação adicional é executada. Caso contrário, ele continua a calcular a projeção ortogonal do ponto de consulta na linha infinita que contém a borda. A Algebra linear envolvida no cálculo é semelhante às equações de triângulo anteriores. No entanto, o cálculo é mais simples, não é descrito aqui. Se o ponto projetado estiver dentro da borda, você descobrirá a distância do ponto projetado do ponto de consulta. Se essa distância for menor que ShortestDistance, você encontrará um novo ponto mais próximo. Atualize ShortestDistance e ClosestPoint. Se o ponto projetado estiver fora da borda, chame ProcessVertex nos dois pontos de extremidade. Antes de retornar o controle, atualize o histórico de borda para que essa borda seja marcada como "PROCESSAda".

Por fim, você fornece uma descrição de ProcessVertex. A rotina ProjectVertex também implementa a estratégia I e mantém uma tabela de histórico de vértice. Como ilustrado na Figura 34, ele primeiro verifica se o vértice foi processado antes. Nesse caso, nenhuma ação adicional é executada. Caso contrário, ele prossegue para calcular a distância do vértice do ponto de consulta. Se a distância for menor que ShortestDistance, atualize ShortestDistance e ClosestPoint. No final, ele atualiza o histórico de vértice para que esse vértice seja marcado como "processado".

Quando o loop de controle externo tiver esgotado todos os triângulos ou encerrado antes do limite de diferença de cor ter sido atingido, a variável ClosestPoint será acessada. Esse é o resultado de MinDEMap. O chamador também pode recuperar ShortestDistance se estiver interessado em quão longe a cor mapeada é da cor da consulta.

### <a name="hue-smoothing"></a>Suavização de matiz

![Diagrama que mostra duas exibições principais de suavização de matiz, o original na parte superior e o matiz suaves na parte inferior.](images/gmmp-image125.png)

**Figura 35:** Suavização de matiz

Ocorre um problema com operações restritas por matiz; ou seja, a operação considera apenas variáveis dentro de um plano de matiz. A Figura 35 mostra um exemplo de uma gama exibindo fatias de matiz "descontinuosas" nos matizes azuis. Dentro desse intervalo de matiz, para determinados ângulos de matiz, o limite de jogos é tangente ao plano de matiz. Na verdade, isso causa uma alteração na estrutura topológica das fatias de matiz. No exemplo mostrado, à medida que o plano de matiz é vareado por esse intervalo de matiz, uma "ilha" surge e aparece. Essa alteração na topologia fará com que as operações específicas do matiz sejam descontinuárias. Por exemplo, o ao matiz fixo será alterado de forma repentina à medida que o ângulo de matiz mudar nesse intervalo.

Há um motivo para a ciência de cores ser desejável para preservar o matiz em determinadas operações. Para resolver o problema anterior, os Triângulos de Limite de Gamut originais devem ser "suavizados de matiz". Em termos gerais, uma suavização de matiz de um conjunto de Triângulos de Limite de Gamut é um conjunto de triângulos, de modo que (a) ele forma o limite de um novo "gamut", que pode não corresponder ao gamut do dispositivo real e que contém o gamut definido pelo conjunto original de triângulos; e (b) os triângulos no novo conjunto estão limitados a serem paralelos aos planos de matiz.

Uma maneira prática de obter um conjunto suave de triângulos de matiz é pegar a enxada convexa dos vértices originais. Conforme ilustrado na Figura 35, as fatias de matiz da ensola convexa variam suavemente no intervalo de matiz problemático sem uma alteração repentina na topologia.

### <a name="setting-primaries-and-secondaries-in-the-gamut-boundary-description"></a>Definindo primários e secundários na descrição do limite de jogos

Determinados métodos de mapeamento de gamut, como HueMap, dependem da localização dos primários e secundários do dispositivo. Para dispositivos aditivos, os principais são vermelho, verde e azul (R, G e B); e os secundários são ciano, magenta e amarelo (C, M e Y). Para dispositivos subtrativos, os primários são C, M e Y; e os secundários são R, G e B. O GBD mantém o controle de todos os seis valores, além de branco e preto (W e K), em uma matriz de valores de cores de Clara. Esses valores são definidos na descrição do limite de jogos quando são criados. Para dispositivos de saída, os primários podem ser determinados executando combinações de valores de controle de dispositivo por meio do modelo de dispositivo. Para dispositivos de captura, essa abordagem não é adequada para criar o GBD de referência, pois é quase impossível capturar uma imagem que produz um valor de dispositivo puro totalmente saturado, como (0,0, 0,0, 1,0). Os perfis de dispositivo WCS contêm os índices dos primários no destino de captura. Como esses valores não estão contidos em um perfil ICC, use os valores medidos de um destino típico do scanner após a conversão em Reais, em relação às condições de exibição do ICC.

### <a name="setting-the-neutral-axis-in-the-gamut-boundary-description"></a>Definindo o eixo neutro na descrição do limite de jogos

Os métodos de mapeamento de gamut HueMap e Relative MinCD usam o eixo neutro do dispositivo para desatar. Para os dispositivos de saída de linha de base, o eixo neutro pode ser determinado executando valores neutros do dispositivo (R=G=B ou C=M=Y) por meio do método DeviceToColorimetric e, em seguida, por meio do método ColorimetricToAppearance do objeto CIECAM02. No entanto, os dispositivos de captura nem sempre retornam um valor neutro do dispositivo quando é apresentado um exemplo neutro. Isso é particularmente verdadeiro quando a iluminação do ambiente não é perfeitamente neutra. Os perfis de dispositivo WCS contêm os índices das amostras neutras no destino. Use esses exemplos para definir o eixo neutro. Como essas informações não estão disponíveis para perfis ICC, você deve usar o mesmo método usado para dispositivos de saída; execute exemplos neutros de dispositivo por meio do método DeviceToColorimetric e adoque os valores de entrada e os resultados colorimétricos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conceitos básicos de gerenciamento de cores](basic-color-management-concepts.md)
</dt> <dt>

[Algoritmos e esquemas do sistema de cores do Windows](windows-color-system-schemas-and-algorithms.md)
</dt> </dl>

 

 




