---
title: Esquema e algoritmo de perfil do modelo de aparência de cores do WCS
description: Esquema e algoritmo de perfil do modelo de aparência de cores do WCS
ms.assetid: 017588fe-cec9-4178-a912-7950cefc036c
keywords:
- WCS (sistema de cores do Windows), perfil de modelo de aparência de cores (CAMP)
- WCS (sistema de cores do Windows), perfil de modelo de aparência de cores (CAMP)
- gerenciamento de cores de imagem, perfil de modelo de aparência de cores (CAMP)
- gerenciamento de cores, perfil de modelo de aparência de cores (CAMP)
- cores, perfil de modelo de aparência de cor (CAMP)
- WCS (sistema de cores do Windows), perfis
- WCS (sistema de cores do Windows), perfis
- gerenciamento de cores de imagem, perfis
- gerenciamento de cores, perfis
- cores, perfis
- perfil do modelo de aparência de cores (CAMP)
- CAMP (perfil de modelo de aparência de cores)
- esquemas, perfil de modelo de aparência de cores (CAMP)
- algoritmos, perfil de modelo de aparência de cor (CAMP)
- Perfil do modelo de aparência de cores WCS
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a928aebcfe02f1db39de2452a0b49e5c888bccc
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/04/2021
ms.locfileid: "105798335"
---
# <a name="wcs-color-appearance-model-profile-schema-and-algorithm"></a>Esquema e algoritmo de perfil do modelo de aparência de cores do WCS

[Visão geral](#overview)

[Arquitetura do perfil do modelo de aparência de cores (CAMP)](#color-appearance-model-profile-architecture)

[O esquema CAMP](#the-camp-schema)

[Os elementos do esquema CAMP](#the-camp-schema-elements)

[O algoritmo CAMP](#the-camp-algorithm)

### <a name="overview"></a>Visão geral

Esse esquema é usado para especificar o conteúdo de um perfil de modelo de aparência de cor (CAMP). Os algoritmos de linha de base associados são descritos nas seções a seguir.

O CAMP é composto de marcas XML que fornecem valores paramétricos para as variáveis de modelo de aparência de linha de base CIECAM02. Detalhes sobre os intervalos de parâmetros são fornecidos na especificação do modelo de aparência de cor de linha de base e na recomendação de CIECAM02.

### <a name="color-appearance-model-profile-architecture"></a>Arquitetura do perfil do modelo de aparência de cores

![Diagrama que mostra a arquitetura do perfil CAMP composta de marcas X M L.](images/camp-image002new.png)

### <a name="the-camp-schema"></a>O esquema CAMP


```C++
<?xml version="1.0" encoding="UTF-8"?>
<xs:schema
  xmlns:cam="http://schemas.microsoft.com/windows/2005/02/color/ColorAppearanceModel"
  xmlns:wcs="http://schemas.microsoft.com/windows/2005/02/color/WcsCommonProfileTypes"
  targetNamespace="http://schemas.microsoft.com/windows/2005/02/color/ColorAppearanceModel"
  xmlns:xs="http://www.w3.org/2001/XMLSchema"
  elementFormDefault="qualified"
  attributeFormDefault="unqualified"
  blockDefault="#all"
  version="1.0">

  <xs:annotation>
    <xs:documentation>
      Color Appearance Model profile schema.
      Copyright (C) Microsoft. All rights reserved.
    </xs:documentation>
  </xs:annotation>

  <xs:import namespace="http://schemas.microsoft.com/windows/2005/02/color/WcsCommonProfileTypes" />

  <xs:annotation>
    <xs:documentation>
      ColorAppearanceModel element contains viewing conditions
      parameters based on CIECAM02.
    </xs:documentation>
  </xs:annotation>
  <xs:element name="ColorAppearanceModel">
    <xs:complexType>
      <xs:sequence>
        <xs:element name="ProfileName" type="wcs:MultiLocalizedTextType"/>
        <xs:element name="Description" type="wcs:MultiLocalizedTextType" minOccurs="0"/>
        <xs:element name="Author" type="wcs:MultiLocalizedTextType" minOccurs="0"/>
        <xs:element name="ViewingConditions">
          <xs:complexType>
            <xs:sequence>
              <xs:choice>
                <xs:element name="WhitePoint" type="wcs:NonNegativeCIEXYZType"/>
                <xs:element name="WhitePointName">
                  <xs:simpleType>
                    <xs:restriction base="xs:string">
                      <xs:enumeration value="D50"/>
                      <xs:enumeration value="D65"/>
                      <xs:enumeration value="A"/>
                      <xs:enumeration value="F2"/>
                    </xs:restriction>
                  </xs:simpleType>
                </xs:element>
              </xs:choice>
              <xs:element name="Background" type="wcs:NonNegativeCIEXYZType"/>
              <xs:choice>
                <xs:element name="ImpactOfSurround" type="xs:float"/>
                <xs:element name="Surround">
                  <xs:simpleType>
                    <xs:restriction base="xs:string">
                      <xs:enumeration value="Average"/>
                      <xs:enumeration value="Dim"/>
                      <xs:enumeration value="Dark"/>
                    </xs:restriction>
                  </xs:simpleType>
                </xs:element>
              </xs:choice>
              <xs:element name="LuminanceOfAdaptingField" type="xs:float"/>
              <xs:element name="DegreeOfAdaptation" type="xs:float"/>
            </xs:sequence>
          </xs:complexType>
        </xs:element>
        <xs:element name="NormalizeToMediaWhitePoint" minOccurs="0">
          <xs:simpleType>
            <xs:restriction base="xs:string">
              <xs:enumeration value="True"/>
              <xs:enumeration value="False"/>
            </xs:restriction>
          </xs:simpleType>
        </xs:element>
      </xs:sequence>
      <xs:attribute name="ID" type="xs:string" use="optional" />
    </xs:complexType>
  </xs:element>
</xs:schema>
```



## <a name="the-camp-schema-elements"></a>Os elementos do esquema CAMP

## <a name="colorappearancemodel"></a>ColorAppearanceModel

Esse elemento é uma sequência de:

1.  Cadeia de caracteres ProfileName,
2.  Cadeia de caracteres de descrição opcional,
3.  Cadeia de caracteres de autor opcional,
4.  Elemento ViewingConditions.

**Condições de validação:** Cada subelemento é validado por seu próprio tipo. Os comprimentos da cadeia de caracteres são limitados a 10.000 caracteres.

## <a name="namespace"></a>Namespace

xmlns: cam = " http://schemas.microsoft.com/windows/2005/02/color/ColorAppearanceModel "

targetNamespace = " http://schemas.microsoft.com/windows/2005/02/color/ColorAppearanceModel "

## <a name="version"></a>Versão

Versão &gt; 0,1 ou &lt; = "1,0" com a primeira versão do Windows Vista.

**Condições de validação:** Qualquer valor &lt; de versão = 2,0 também é válido para dar suporte a alterações não significativas no formato.

## <a name="documentation"></a>Documentação

Esquema de perfil do modelo de aparência de cores.

Copyright (C) Microsoft. Todos os direitos reservados.

**Condições de validação:** Cada subelemento é validado por seu próprio tipo.

## <a name="surroundtype"></a>Surroundtype

Esse elemento é uma enumeração de parâmetros de CIECAM02 "média", "Dim" ou "Dark" ou os parâmetros quantitativos reais da recomendação de CIECAM02 c, impacto do surround.

**Condições de validação:** O parâmetro c pode variar de 0,525 a 0,69.

## <a name="viewingconditions"></a>ViewingConditions

Esse elemento consiste nos seguintes subelementos:



| Elemento                    | Type           |
|----------------------------|----------------|
| WhitePoint                 | WhitePointType |
| Tela de fundo                 | CIEXYZ         |
| Ao                   | Surroundtype   |
| LuminanceOfAdaptingField   | FLOAT          |
| DegreeOfAdaptation         | FLOAT          |
| NormalizeToMediaWhitePoint | Boolean        |



 

**Condições de validação:** Os subelementos CIEXYZ são validados pelo NonNegativeXYZType. O LuminanceOfAdaptingField é um máximo de 10, 000cd/m ^ 2. O DegreeOfAdaptation pode variar de 0,0 a 1,0. O valor de NormalizeToMediaWhitePoint pode ser "true" ou "false". Se o subelemento NormalizeToMediaWhitePoint estiver ausente, ele será efetivamente padronizado como "true". Consulte a seção de algoritmo CAMP a seguir.

## <a name="whitepointtype"></a>WhitePointType

Esse elemento é uma enumeração do valor de fonte de luz de CIE ("D50", "D65", "" A "ou" F2 ") ou um subelemento CIEXYZ.

**Condições de validação:** Cada subelemento é validado por seu próprio tipo.

## <a name="ciexyztype"></a>CIEXYZType

O elemento CIEXYZType é composto de três elementos de ponto flutuante de IEEE de precisão única do NonNegativeFloatType, denominados "X", "Y" e "Z". Essas medidas podem ser absolutas (não relativas) CIEXYZ 1931 valores de reflexão ou valores absolutos (não relativos) CIEXYZ 1931 diretos (transmissal) em candelas por unidades de metro quadrado.

**Condições de validação:** Isso significa que apenas valores reais são válidos e valores de medida CIEXYZ negativos são inválidos. Como esses são valores absolutos, os valores podem variar bem além de 1,0 f. Um limite razoável para qualquer valor X, Y ou Z será definido arbitrariamente como 10000.0 f.

 

### <a name="the-camp-algorithm"></a>O algoritmo CAMP

O CAM (modelo de aparência de cores) é baseado nas equações de modelo de aparência de cor de CIE CIECAM02.

Essa classe implementa a modelagem de aparência de cor. Observe que a CAM WCS *não* é substituível, por exemplo, usando um plug-in. É uma meta de design ter apenas um modelo de aparência de cor. O CAM é baseado em recomendações de CIECAM02.

CIECAM02 pode ser usado de duas maneiras. Na direção de colorimétrico a aparência, ele fornece um mapeamento do espaço da CIE XYZ para o espaço de aparência da cor. Na direção de aparência para colorimétrico, ele mapeia do espaço de aparência de cor para o espaço XYZ. A aparência da cor correlaciona a claridade, J, croma, C e matiz, h. Esses três valores formam um sistema de coordenadas cilíndrico. Frequentemente, se torna mais conveniente trabalhar em um sistema de coordenadas retangular, portanto, Compute a = C cos h e b = C Sin h, para dar CIECAM02 jab.

Você pode usar valores de luminosidade de CAM maiores que 100. O Comitê de CIE que formulau o CIECAM02 não resolveu o comportamento do eixo de claridade para valores de entrada com uma luminância maior do que o ponto branco adotado; ou seja, para valores Y de entrada maiores que o valor Y do ponto branco adotado. A experimentação mostrou que as equações de luminância em CIECAM02 se comportam razoavelmente para tais valores. A claridade aumenta exponencialmente e segue o mesmo expoente (aproximadamente 1/3).

Às vezes, os usuários desejam alterar a forma como o grau de adaptação (D) é calculado. O design WCS permite que os usuários controlem esse cálculo alterando o valor degreeOfadaptation nos parâmetros de condições de exibição.

Para fornecer uma correspondência mais consistente às expectativas sutratadas por ICC dos usuários, o degreeOfAdaptation no acampamentos padrão é 1,0. Isso produz resultados melhores em todos os casos diferentes de MinCD Absolute, em que é aconselhável permitir que o WCS Compute o degreeOfAdaptation (via degreeOfAdaptation =-1).

Em vez de usar um valor surround de "Average", "Dim" e "Dark", um valor de surround contínuo, calculado a partir do valor c, é fornecido. O valor de c deve ser um float entre 0,525 e 0,69.

De *c*, *NC* e *F* podem ser computados, usando a interpolação linear piecewise entre os valores já fornecidos para "média", "Dim" e "Dark". Isso modela o que é mostrado na Figura 1 do CIE 159:2004, a especificação CIECAM02.



| degreeOfAdaption                     | Comportamento                                                                       |
|--------------------------------------|--------------------------------------------------------------------------------|
| -1,0                                 | ![Mostra uma fórmula para o comportamento padrão C I E C A M 02.](images/camp-image006.png)Esse é o comportamento padrão de CIECAM02.<br/> |
| 0,0 &lt; = degreeOfAdaption &lt; = 1,0 | *D* = degreeOfAdaptation (o valor fornecido pelo usuário)                      |



 

Uma determinada quantidade de verificação de erros também foi adicionada à implementação. Os números de equações a seguir são aqueles usados na definição de CIE 159:2004 de CIECAM02.

**ColorimetricToAppearanceColors**

Os valores de entrada são verificados para racionalidade: se X ou Z &lt; 0,0, ou se Y &lt; -1,0, o HRESULT é E \_ INVALIDARG. Se-1,0 &lt; = Y &lt; 0,0, J, C e h estão todos definidos como 0,0.

Há certas condições internas que podem produzir resultados de erro. Em vez de produzir esses resultados, os resultados internos são recortados para produzir valores em intervalo. Isso acontece para especificações de cores que seriam escuras e impossíveis de desvio: na equação 7,23, se for &lt; 0, a = 0. Na equação 7,26, se t &lt; 0, t = 0.

**AppearanceToColorimetricColors**

Os valores de entrada são verificados para racionalidade. Se C &lt; 0, c &gt; 300 ou J &gt; 500, o HRESULT será E \_ INVALIDARG.

*R '<sub>a;</sub>*, *G '<sub>a;</sub>* e *B '<sub>a;</sub>*, (equações 8,19-8,21) são recortados para o intervalo de 399,9.

Para todos os perfis de modelo de aparência de cor (acampamentos), o mecanismo WCS examinará o ponto branco adotado. Se Y não for 100,0, o ponto branco adotado será dimensionado para que Y seja igual a 100,0. O mesmo dimensionamento será aplicado ao valor em segundo plano. O fator de dimensionamento é 100.0/adoptedWhitePoint. Y. O mesmo fator de dimensionamento é aplicado a cada X, Y e Z. Se o campo NormalizeToMediaWhitePoint for definido como "true" ou se estiver ausente do CAMP, o mecanismo também dimensionará todas as entradas de cores de dispositivo para DeviceToColorimetric, de modo que o valor Y do ponto branco de mídia do dispositivo seja igual a 100,0. As cores do dispositivo provenientes de ColorimetricToDevice serão dimensionadas pelo inverso multiplicativa do fator de dimensionamento. Se o sinalizador NormalizeToMediaWhitePoint for definido como "false", os dados colorimétrico não serão dimensionados.

Para algumas tarefas, faz sentido dimensionar os valores colorimétrico provenientes de DeviceToColorimetric. As equações de luminosidade hiperbólica no CAM são realmente projetadas para uma luminância de ponto branco de 100,0. O único lugar em que uma diferença na luminância absoluta (ou illuminance) entra em jogo está na luminância do campo de adaptação. Portanto, o CAM deve ser inicializado com um ponto branco Y de 100,0. Mas se o ponto branco médio do modelo do dispositivo estiver sendo usado como o ponto branco adotado, todas as cores provenientes do dispositivo deverão ser dimensionadas de forma adequada ou o dispositivo branco não virá com um valor J de 100,0. Portanto, os valores Y precisam ser dimensionados nas medidas. Os valores de medida podem ser dimensionados antes da inicialização do modelo do dispositivo. Em seguida, os resultados já estarão no intervalo adequado. Mas isso tornaria o teste do modelo do dispositivo mais difícil, pois os valores que chegam seriam necessários para o dimensionamento. Para as tarefas nas quais o ponto branco médio do dispositivo é percebido como um verdadeiro branco, a normalização pelo ponto branco de mídia do dispositivo é desejável.

O CAM é inicializado diretamente do CAMP. Isso permite aos desenvolvedores alguma flexibilidade na inicialização do CAM, com base na tarefa que desejam executar. Em algumas tarefas, os observadores ignorarão qualquer croma nos pontos brancos de mídia, pois eles "sabem" de forma cognitiva que a mídia de origem e de destino são "brancas". Nesses casos, os desenvolvedores desejarão inicializar o câmeras direto e inverso com seus respectivos pontos brancos de mídia. Em alguns casos, os observadores podem estar comparando a cor dos planos de fundo de mídia. Nesses casos, é aconselhável usar um CAM para ambos os dispositivos, e pode ser desejável não dimensionar os valores colorimétrico de cada dispositivo pelo ponto branco médio desse dispositivo. Em seguida, os diferentes valores de triestímulo da mídia levarão a valores de aparência diferentes em CIECAM02.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conceitos básicos de gerenciamento de cores](basic-color-management-concepts.md)
</dt> <dt>

[Algoritmos e esquemas do sistema de cores do Windows](windows-color-system-schemas-and-algorithms.md)
</dt> </dl>

 

 





