---
title: Estratégias de tipo de perfil comuns do sistema de cores do Windows, controle de versão e localização
description: Estratégias de tipo de perfil comuns do sistema de cores do Windows, controle de versão e localização
ms.assetid: 295522c6-7c53-47f6-9b98-aeee2b0e34fc
keywords:
- WCS (sistema de cores do Windows), tipos de perfil comuns
- WCS (sistema de cores do Windows), tipos de perfil comuns
- gerenciamento de cores de imagem, tipos de perfil comuns
- gerenciamento de cores, tipos de perfil comuns
- cores, tipos de perfil comuns
- WCS (sistema de cores do Windows), perfis
- WCS (sistema de cores do Windows), perfis
- gerenciamento de cores de imagem, perfis
- gerenciamento de cores, perfis
- cores, perfis
- WCS (sistema de cores do Windows), controle de versão
- WCS (sistema de cores do Windows), controle de versão
- gerenciamento de cores de imagem, controle de versão
- gerenciamento de cores, controle de versão
- cores, controle de versão
- WCS (sistema de cores do Windows), localização
- WCS (sistema de cores do Windows), localização
- gerenciamento de cores de imagem, localização
- gerenciamento de cores, localização
- cores, localização
- Tipos de perfil comuns do WCS
- consumidores de perfil
- tipos de perfil comuns
- esquemas, tipos de perfil comuns
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4814b652b654b6416b42a7a3484950273a93ea96
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "105798341"
---
# <a name="windows-color-system-common-profile-types-schema-versioning-and-localization-strategies"></a>Estratégias de tipo de perfil comuns do sistema de cores do Windows, controle de versão e localização

-   [Esquema de tipos de perfil comum WCS v1](#wcs-common-profile-types-schema-v1)
-   [Adições do esquema v2 de tipos de perfil comuns do WCS](#wcs-common-profile-types-schema-v2-additions)
-   [Controle de versão do esquema do perfil WCS](#wcs-profile-schema-versioning)
-   [Localização do perfil WCS](#wcs-profile-localization)
    -   [Expressando elementos localizáveis](#expressing-localizable-elements)
    -   [Suporte a esquemas](#schema-support)
    -   [Selecionando o idioma](#selecting-the-language)
    -   [Perfis internos](#built-in-profiles)
-   [Tópicos relacionados](#related-topics)

## <a name="wcs-common-profile-types-schema-v1"></a>Esquema de tipos de perfil comum WCS v1

O seguinte fornece a definição de esquema v 1.0 para os tipos de perfil comuns do WCS.


```XML
<?xml version="1.0" encoding="UTF-8"?>
<xs:schema
  xmlns:xs="http://www.w3.org/2001/XMLSchema"
  xmlns:wcs="http://schemas.microsoft.com/windows/2005/02/color/WcsCommonProfileTypes"
  targetNamespace="http://schemas.microsoft.com/windows/2005/02/color/WcsCommonProfileTypes"
  elementFormDefault="qualified"
  attributeFormDefault="unqualified"
  blockDefault="#all"
  version="1.0">

  <xs:import namespace="http://www.w3.org/XML/1998/namespace" />

  <xs:annotation>
    <xs:documentation xml:lang="en">
      Common types used in WCS profile schemas.
      Copyright (C) Microsoft. All rights reserved.
    </xs:documentation>
  </xs:annotation>

  <xs:simpleType name="NonNegativeFloatType">
    <xs:restriction base="xs:float">
      <xs:minInclusive value="0"/>
    </xs:restriction>
  </xs:simpleType>

  <xs:complexType name="NonNegativeCIEXYZType">
    <xs:attribute name="X" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="Y" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="Z" type="wcs:NonNegativeFloatType" use="required"/>
  </xs:complexType>

  <xs:simpleType name="GUIDType">
    <xs:restriction base="xs:string">
      <xs:pattern value="\{[a-fA-F0-9]{8}-[a-fA-F0-9]{4}-[a-fA-F0-9]{4}-[a-fA-F0-9]{4}-[a-fA-F0-9]{12}\}"/>
    </xs:restriction>
  </xs:simpleType>

  <xs:complexType name="LocalizedTextType">
    <xs:simpleContent>
      <xs:extension base="xs:string">
        <xs:attribute ref="xml:lang" use="required"/>
      </xs:extension>
    </xs:simpleContent>
  </xs:complexType>

  <xs:complexType name="MultiLocalizedTextType">
    <xs:sequence>
      <xs:element name="Text" type="wcs:LocalizedTextType" minOccurs="1" />
    </xs:sequence>
  </xs:complexType>

</xs:schema>

```



Somente há suporte para codificações UTF-8 ou UTF-16. Todas as outras codificações de XML são altamente desencorajadas para preservar a interoperabilidade ideal.

## <a name="wcs-common-profile-types-schema-v2-additions"></a>Adições do esquema v2 de tipos de perfil comuns do WCS

No Windows 7, o esquema de tipos de perfil comum WCS foi atualizado para incluir tipos para dar suporte ao [esquema de calibração WCS](wcs-calibration-schema.md).


```XML
  <xs:complexType name="ParameterizedCurvesType">
    <xs:sequence>
      <xs:element name="RedTRC" type="wcs:ParameterizedCurveType"/>
      <xs:element name="GreenTRC" type="wcs:ParameterizedCurveType"/>
      <xs:element name="BlueTRC" type="wcs:ParameterizedCurveType"/>
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="ParameterizedCurveType">
    <xs:attribute name="Gamma" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="Offset1" type="xs:float" use="optional"/>
    <xs:attribute name="Gain" type="wcs:NonNegativeFloatType" use="optional"/>
    <xs:attribute name="Offset2" type="xs:float " use="optional"/>
    <xs:attribute name="TransitionPoint" type="wcs:NonNegativeFloatType" use="optional"/>
    <xs:attribute name="Offset3" type="xs:float" use="optional"/>
  </xs:complexType>

  <xs:simpleType name="FloatList">
    <xs:list itemType="xs:float"/>
  </xs:simpleType>

  <xs:complexType name="OneDimensionLutType">
    <xs:sequence>
      <xs:element name="Input" type="wcs:FloatList"/>
      <xs:element name="Output" type="wcs:FloatList"/>
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="HDRToneResponseCurvesType">
    <xs:sequence>
      <xs:element name="RedTRC" type="wcs:OneDimensionLutType"/>
      <xs:element name="GreenTRC" type="wcs:OneDimensionLutType"/>
      <xs:element name="BlueTRC" type="wcs:OneDimensionLutType"/>
    </xs:sequence>
    <xs:attribute name="TRCLength" use="required">
      <xs:simpleType>
        <xs:restriction base="xs:int">
          <xs:minInclusive value="2" />
        </xs:restriction>
      </xs:simpleType>
    </xs:attribute>
  </xs:complexType>
```



## <a name="wcs-profile-schema-versioning"></a>Controle de versão do esquema do perfil WCS

Neste apêndice, o termo "consumidor de perfil" refere-se ao software WCS ou a um componente de software de terceiros que consome os perfis WCS.

Versões mais recentes de consumidores de perfil poderão consumir perfis WCS gravados de acordo com versões mais antigas dos esquemas. Para aproveitar ao máximo os recursos definidos na versão mais recente dos esquemas, a versão mais recente de um consumidor de perfil geralmente será necessária. No entanto, os consumidores de perfil mais antigos podem consumir perfis gravados de acordo com as versões mais recentes dos esquemas. O consumidor do perfil pode ignorar elementos e atributos XML que ele não entende. Os resultados estarão corretos, mas o desempenho ou a fidelidade pode degradar em comparação com os resultados obtidos com a versão mais recente do consumidor do perfil.

Veja a seguir as diretrizes de controle de versão para consumidores de perfil:

-   Uma determinada versão de um consumidor de perfil deve reconhecer todos os elementos e atributos de um namespace de versão ou nenhum deles.
-   Se um consumidor de perfil encontrar um elemento ou atributo de um namespace que ele não entende, ele deverá tratá-lo como uma condição de erro, a menos que o perfil contenha orientação explícita sobre o processamento de fallback.
-   A [especificação de empacotamento aberto](https://www.microsoft.com/whdc/xps/xpspkg.mspx) define um URI de namespace adicional, o namespace de compatibilidade de marcação, que define elementos e atributos que fornecem essas diretrizes de processamento de fallback.
-   Todas as versões de todos os consumidores de perfil devem reconhecer e respeitar todos os elementos e atributos no namespace de compatibilidade de marcação.
-   Os consumidores de perfil com base em uma nova versão dos esquemas de perfil devem dar suporte a todos os namespaces de versão definidos anteriormente.

Na versão v 1.0, o WCS reconhece elementos e atributos dos seguintes namespaces:

-   https://schemas.microsoft.com/windows/2005/02/color/ColorDeviceModel
-   https://schemas.microsoft.com/windows/2005/02/color/GamutMapModel
-   https://schemas.microsoft.com/windows/2005/02/color/ColorAppearanceModel
-   https://schemas.microsoft.com/winfx/2005/06/markup-compatibility

A seguir, é demonstrado um exemplo de compatibilidade de marcação.


```XML
<?xml version="1.0" encoding="utf-8" ?>
<ColorAppearanceModel
  xmlns=http://schemas.microsoft.com/windows/2005/02/color/ColorAppearanceModel
  xmlns:cam2=http://schemas.microsoft.com/windows/2007/08/color/ColorAppearanceModel
  xmlns:mc=http://schemas.microsoft.com/winfx/2005/02/markup-compatibility
  xs:schemaLocation="http://schemas.microsoft.com/windows/2005/02/color/ColorAppearanceModel ColorAppearanceModel.xsd"
  xmlns:xs='http://www.w3.org/2001/XMLSchema-instance'
  mc:Ignorable="cam2">

  <ProfileName>Default profile for ICC viewing conditions</ProfileName>
  <mc:AlternateContent>
    <mc:Choice Requires="cam2">
      <cam2:AudioDescription source="ProfileExplanation.wav"/>
    </mc:Choice>
    <mc:Fallback>
      <Description>Appropriate for a print in a D50 viewing booth</Description>
        </mc:Fallback>
  </mc:AlternateContent>
  <Author>Microsoft</Author>

  <ViewingConditions>
    <WhitePointName>D50</WhitePointName>
    <Background X="19.3" Y="20.0" Z="16.5" />
    <Surround>Average</Surround>
    <LuminanceOfAdaptingField>31.8</LuminanceOfAdaptingField>
    <DegreeOfAdaptation>-1</DegreeOfAdaptation>
    <cam2:Humidity>30%</cam2:Humidity>
  </ViewingConditions>

</ColorAppearanceModel>
```



## <a name="wcs-profile-localization"></a>Localização do perfil WCS

**Requirements**

Os perfis WCS contêm determinados elementos, como ProfileName e Description, que contêm texto legível por humanos. Esse texto é localizável.

Veja a seguir as diretrizes de controle de versão para criadores de perfil:

-   Para perfis criados por terceiros, como fabricantes de impressoras, o autor do perfil deve incorporar texto descritivo em vários idiomas.
-   Os seguintes elementos devem ser localizáveis: 

    | Elemento     | CDMP | GMMP | CAMP |
    |-------------|------|------|------|
    | ProfileName | x    | x    | x    |
    | Descrição | x    | x    | x    |
    | Autor      | x    | x    | x    |

    

     

### <a name="expressing-localizable-elements"></a>Expressando elementos localizáveis

Em vez de conter texto diretamente, cada elemento localizável contém um ou mais subelemento WCS: Text, cada um deles deve especificar o atributo XML: lang. Conforme descrito na seção de [especificação xml](http://www.w3.org/TR/REC-xml/) 2,12 ("identificação de idioma"), o valor do atributo XML: lang deve ser um identificador de idioma IETF RFC 3066, como "en-US", "en" ou "FR-FR". Nos esquemas WCS, o valor do atributo XML: lang não deve ser a cadeia de caracteres vazia "", embora o XML permita isso em geral. Por exemplo:


```XML
<cdm:ColorDeviceModel ... />
    <cdm:Description>
        <wcs:Text xml:lang="en-US">Hello</wcs:Text>
        <wcs:Text xml:lang="fr-FR">Bonjour</wcs:Text>
    </cdm:Description>
    ...
</cdm:ColorDeviceeModel>
```



Não há dois WCS: elementos de texto podem ter o mesmo atributo XML: lang. Cada esquema de perfil WCS deve impor essa restrição separadamente para cada elemento localizável. Somente as codificações UTF-8 e UTF-16 são compatíveis.

### <a name="schema-support"></a>Suporte a esquemas

O design usa os tipos XSD WCS: LocalizedText e WCS: multilocalizadotype definido no esquema de tipo de perfil comum WCS:


```XML
    <xs:complexType name="LocalizedText">
        <xs:simpleContent>
            <xs:extension base="xs:string">
                <xs:attribute name="xml:lang" type="xs:string" use="required"/>
            <xs:extension/>
        <xs:simpleContent/>
    </xs:complexType/>

    <xs:complexType name="MultiLocalizedType">
        <xs:element name="Text" type="cam:LocalizedText" minOccurs="1"/>
    </xs:complexType>
```



Cada esquema de perfil WCS declara que cada elemento localizável é do tipo multitraduzitype, por exemplo:


```XML
<xs:schema 
    xmlns:xs="http://www.w3.org/2001/XMLSchema"
    xmlns:cdm="http://schemas.microsoft.com/windows/2005/02/color/ColorDeviceModel"
    xmlns:wcs="http://schemas.microsoft.com/windows/2005/02/color/WcsCommonProfileTypes"
    targetNamespace=
        "http://schemas.microsoft.com/windows/2005/02/color/ColorDeviceModel"
    version="1.0">
    <xs:import namespace=
        "http://schemas.microsoft.com/windows/2005/02/color/WcsCommonProfileTypes"/>

    <xs:element name="cdm:Description" type="wcs:MultiLocalizableType" minOccurs="0"/>

    <xs:unique name="uniqueDescriptionLanguage">
      <xs:selector xpath="cdm:ColorDeviceModel/cdm:Description/wcs:Text"/>
      <xs:field xpath="@xml:lang"/>
    </unique>

    ...
</xs:schema>
```



O esquema CDMP impõe a restrição de que cada WCS: Text Child do elemento CDM: Description deve ter um atributo XML: lang exclusivo. Ele impõe a mesma restrição para os outros elementos localizáveis. Os esquemas CAMP e GMMP fazem o mesmo.

### <a name="selecting-the-language"></a>Selecionando o idioma

Ao decidir qual versão de idioma de um elemento localizável exibir, o código do aplicativo deve selecionar a "versão mais próxima" para a "linguagem atual". O que "versão mais próxima" e "idioma atual" realmente significam que depende da plataforma; Veja abaixo. Se o perfil não contiver uma versão de idioma que corresponda ao idioma atual, o aplicativo deverá selecionar a primeira versão no perfil (o primeiro elemento de texto filho WCS: Text do elemento localizável).

No Windows Vista, a seleção de idioma é feita da seguinte maneira: cada thread tem uma lista associada de "linguagens de interface do usuário preferenciais", que pode ser obtida chamando [**GetThreadPreferredUILanguages**](/windows/win32/api/winnls/nf-winnls-getthreadpreferreduilanguages). A lista é retornada em ordem de preferência do usuário. Por exemplo, em um sistema configurado para inglês americano, a lista retornada por **GetThreadPreferredUILanguages** é {"en-US", "en"}. Isso significa: 1) inglês americano, se presente. 2) caso contrário, use qualquer variante regional do inglês, como "en-GB" ou simplesmente "en" simples.

Para cada idioma nessa lista, em ordem de lista, o código da interface do usuário procura um elemento WCS: Text cujo atributo XML: lang é uma correspondência exata. A primeira versão correspondente é usada. Se nenhuma versão corresponder, o primeiro elemento WCS: Text será usado.

### <a name="built-in-profiles"></a>Perfis internos

Os perfis WCS padrão fornecidos com o Windows Vista, como sRGB. CDMP, têm as mesmas propriedades localizáveis que outros perfis.

A solução padrão do Windows seria colocar as cadeias de caracteres localizadas em uma DLL do MUI e consultá-las da seguinte maneira:


```XML
<cdm:Description resourceId="mscms.dll,-101">
    <wcs:Text xml:lang="en-US">Hello, world!</wcs:Text>
<cdm:Description>
```



Em um sistema Windows, o texto de descrição seria extraído da ID de recurso 101 na versão localizada apropriada dos recursos do MUI para mscms.dll. Os sistemas não Windows usariam os subelementos WCS: Text, conforme descrito acima.

Apresentamos um atributo de ID opcional, globalmente exclusivo, no elemento raiz de cada esquema de perfil do WCS. O perfil padrão wcsRGB. CDMP pode ser assim:


```XML
<cdm:ColorDeviceModel
    ID=http://schemas.microsoft.com/2005/02/color/profiles/wcsRGB.cdmp
    ... >
    <cdm:Description>
        <wcs:Text xml:lang="en-US">Hello.</wcs:Text>
        <wcs:Text xml:lang="fr-FR">Bonjour.</wcs:Text>
    </cdm:Description>
    ...
</cdm:ColorDeviceModel>
```



Para os perfis de cores WCS fornecidos com o Windows, a CPL de cor exibe informações descritivas dos recursos, em vez dos elementos WCS: Text nos perfis. Isso permite que o Windows exiba informações localizadas para esses perfis em todos os idiomas com suporte, sem exigir que os perfis themlselves contenham informações descritivas em todos os idiomas.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conceitos básicos de gerenciamento de cores](basic-color-management-concepts.md)
</dt> <dt>

[Algoritmos e esquemas do sistema de cores do Windows](windows-color-system-schemas-and-algorithms.md)
</dt> </dl>

 

 