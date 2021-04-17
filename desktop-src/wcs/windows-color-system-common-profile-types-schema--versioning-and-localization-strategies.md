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
# <a name="windows-color-system-common-profile-types-schema-versioning-and-localization-strategies"></a><span data-ttu-id="72448-127">Estratégias de tipo de perfil comuns do sistema de cores do Windows, controle de versão e localização</span><span class="sxs-lookup"><span data-stu-id="72448-127">Windows Color System Common Profile Types schema, Versioning and Localization Strategies</span></span>

-   [<span data-ttu-id="72448-128">Esquema de tipos de perfil comum WCS v1</span><span class="sxs-lookup"><span data-stu-id="72448-128">WCS Common Profile Types Schema V1</span></span>](#wcs-common-profile-types-schema-v1)
-   [<span data-ttu-id="72448-129">Adições do esquema v2 de tipos de perfil comuns do WCS</span><span class="sxs-lookup"><span data-stu-id="72448-129">WCS Common Profile Types Schema V2 Additions</span></span>](#wcs-common-profile-types-schema-v2-additions)
-   [<span data-ttu-id="72448-130">Controle de versão do esquema do perfil WCS</span><span class="sxs-lookup"><span data-stu-id="72448-130">WCS Profile Schema Versioning</span></span>](#wcs-profile-schema-versioning)
-   [<span data-ttu-id="72448-131">Localização do perfil WCS</span><span class="sxs-lookup"><span data-stu-id="72448-131">WCS Profile Localization</span></span>](#wcs-profile-localization)
    -   [<span data-ttu-id="72448-132">Expressando elementos localizáveis</span><span class="sxs-lookup"><span data-stu-id="72448-132">Expressing localizable elements</span></span>](#expressing-localizable-elements)
    -   [<span data-ttu-id="72448-133">Suporte a esquemas</span><span class="sxs-lookup"><span data-stu-id="72448-133">Schema Support</span></span>](#schema-support)
    -   [<span data-ttu-id="72448-134">Selecionando o idioma</span><span class="sxs-lookup"><span data-stu-id="72448-134">Selecting the Language</span></span>](#selecting-the-language)
    -   [<span data-ttu-id="72448-135">Perfis internos</span><span class="sxs-lookup"><span data-stu-id="72448-135">Built-in profiles</span></span>](#built-in-profiles)
-   [<span data-ttu-id="72448-136">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="72448-136">Related topics</span></span>](#related-topics)

## <a name="wcs-common-profile-types-schema-v1"></a><span data-ttu-id="72448-137">Esquema de tipos de perfil comum WCS v1</span><span class="sxs-lookup"><span data-stu-id="72448-137">WCS Common Profile Types Schema V1</span></span>

<span data-ttu-id="72448-138">O seguinte fornece a definição de esquema v 1.0 para os tipos de perfil comuns do WCS.</span><span class="sxs-lookup"><span data-stu-id="72448-138">The following provides the v1.0 schema definition for the WCS Common Profile Types.</span></span>


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



<span data-ttu-id="72448-139">Somente há suporte para codificações UTF-8 ou UTF-16.</span><span class="sxs-lookup"><span data-stu-id="72448-139">Only UTF-8 or UTF-16 encodings are supported.</span></span> <span data-ttu-id="72448-140">Todas as outras codificações de XML são altamente desencorajadas para preservar a interoperabilidade ideal.</span><span class="sxs-lookup"><span data-stu-id="72448-140">All other XML encodings are strongly discouraged in order to preserve optimum interoperability.</span></span>

## <a name="wcs-common-profile-types-schema-v2-additions"></a><span data-ttu-id="72448-141">Adições do esquema v2 de tipos de perfil comuns do WCS</span><span class="sxs-lookup"><span data-stu-id="72448-141">WCS Common Profile Types Schema V2 Additions</span></span>

<span data-ttu-id="72448-142">No Windows 7, o esquema de tipos de perfil comum WCS foi atualizado para incluir tipos para dar suporte ao [esquema de calibração WCS](wcs-calibration-schema.md).</span><span class="sxs-lookup"><span data-stu-id="72448-142">In Windows 7, the WCS Common Profile Types schema has been updated to include types to support the [WCS Calibration schema](wcs-calibration-schema.md).</span></span>


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



## <a name="wcs-profile-schema-versioning"></a><span data-ttu-id="72448-143">Controle de versão do esquema do perfil WCS</span><span class="sxs-lookup"><span data-stu-id="72448-143">WCS Profile Schema Versioning</span></span>

<span data-ttu-id="72448-144">Neste apêndice, o termo "consumidor de perfil" refere-se ao software WCS ou a um componente de software de terceiros que consome os perfis WCS.</span><span class="sxs-lookup"><span data-stu-id="72448-144">In this Appendix, the term "profile consumer" refers to the WCS software, or to a third-party software component that consumes WCS profiles.</span></span>

<span data-ttu-id="72448-145">Versões mais recentes de consumidores de perfil poderão consumir perfis WCS gravados de acordo com versões mais antigas dos esquemas.</span><span class="sxs-lookup"><span data-stu-id="72448-145">Newer versions of profile consumers will be able to consume WCS profiles written according to older versions of the schemas.</span></span> <span data-ttu-id="72448-146">Para aproveitar ao máximo os recursos definidos na versão mais recente dos esquemas, a versão mais recente de um consumidor de perfil geralmente será necessária.</span><span class="sxs-lookup"><span data-stu-id="72448-146">To take full advantage of features defined in the newest version of the schemas, the newest version of a profile consumer will generally be required.</span></span> <span data-ttu-id="72448-147">No entanto, os consumidores de perfil mais antigos podem consumir perfis gravados de acordo com as versões mais recentes dos esquemas.</span><span class="sxs-lookup"><span data-stu-id="72448-147">However, older profile consumers can consume profiles written according to newer versions of the schemas.</span></span> <span data-ttu-id="72448-148">O consumidor do perfil pode ignorar elementos e atributos XML que ele não entende.</span><span class="sxs-lookup"><span data-stu-id="72448-148">The profile consumer can ignore XML elements and attributes that it does not understand.</span></span> <span data-ttu-id="72448-149">Os resultados estarão corretos, mas o desempenho ou a fidelidade pode degradar em comparação com os resultados obtidos com a versão mais recente do consumidor do perfil.</span><span class="sxs-lookup"><span data-stu-id="72448-149">The results will be correct, but performance or fidelity may degraded as compared to the results achieved with the newest version of the profile consumer.</span></span>

<span data-ttu-id="72448-150">Veja a seguir as diretrizes de controle de versão para consumidores de perfil:</span><span class="sxs-lookup"><span data-stu-id="72448-150">The following are versioning guidelines for profile consumers:</span></span>

-   <span data-ttu-id="72448-151">Uma determinada versão de um consumidor de perfil deve reconhecer todos os elementos e atributos de um namespace de versão ou nenhum deles.</span><span class="sxs-lookup"><span data-stu-id="72448-151">A given version of a profile consumer must recognize either all of the elements and attributes from a version namespace, or none of them.</span></span>
-   <span data-ttu-id="72448-152">Se um consumidor de perfil encontrar um elemento ou atributo de um namespace que ele não entende, ele deverá tratá-lo como uma condição de erro, a menos que o perfil contenha orientação explícita sobre o processamento de fallback.</span><span class="sxs-lookup"><span data-stu-id="72448-152">If a profile consumer encounters an element or attribute from a namespace that it does not understand, it must treat this as an error condition, unless the profile contains explicit guidance on fallback processing.</span></span>
-   <span data-ttu-id="72448-153">A [especificação de empacotamento aberto](https://www.microsoft.com/whdc/xps/xpspkg.mspx) define um URI de namespace adicional, o namespace de compatibilidade de marcação, que define elementos e atributos que fornecem essas diretrizes de processamento de fallback.</span><span class="sxs-lookup"><span data-stu-id="72448-153">The [Open Packaging Specification](https://www.microsoft.com/whdc/xps/xpspkg.mspx) defines an additional namespace URI, the markup compatibility namespace, which defines elements and attributes that provide this fallback processing guidance.</span></span>
-   <span data-ttu-id="72448-154">Todas as versões de todos os consumidores de perfil devem reconhecer e respeitar todos os elementos e atributos no namespace de compatibilidade de marcação.</span><span class="sxs-lookup"><span data-stu-id="72448-154">All versions of all profile consumers must recognize and respect all the elements and attributes in the markup compatibility namespace.</span></span>
-   <span data-ttu-id="72448-155">Os consumidores de perfil com base em uma nova versão dos esquemas de perfil devem dar suporte a todos os namespaces de versão definidos anteriormente.</span><span class="sxs-lookup"><span data-stu-id="72448-155">Profile consumers based on a new version of the profile schemas must support all previously defined version namespaces.</span></span>

<span data-ttu-id="72448-156">Na versão v 1.0, o WCS reconhece elementos e atributos dos seguintes namespaces:</span><span class="sxs-lookup"><span data-stu-id="72448-156">In the v1.0 release, WCS recognizes elements and attributes from the following namespaces:</span></span>

-   https://schemas.microsoft.com/windows/2005/02/color/ColorDeviceModel
-   https://schemas.microsoft.com/windows/2005/02/color/GamutMapModel
-   https://schemas.microsoft.com/windows/2005/02/color/ColorAppearanceModel
-   https://schemas.microsoft.com/winfx/2005/06/markup-compatibility

<span data-ttu-id="72448-157">A seguir, é demonstrado um exemplo de compatibilidade de marcação.</span><span class="sxs-lookup"><span data-stu-id="72448-157">The following demonstrates an example of markup compatibility.</span></span>


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



## <a name="wcs-profile-localization"></a><span data-ttu-id="72448-158">Localização do perfil WCS</span><span class="sxs-lookup"><span data-stu-id="72448-158">WCS Profile Localization</span></span>

<span data-ttu-id="72448-159">**Requirements**</span><span class="sxs-lookup"><span data-stu-id="72448-159">**Requirements**</span></span>

<span data-ttu-id="72448-160">Os perfis WCS contêm determinados elementos, como ProfileName e Description, que contêm texto legível por humanos.</span><span class="sxs-lookup"><span data-stu-id="72448-160">WCS profiles contain certain elements such as ProfileName and Description which contain human-readable text.</span></span> <span data-ttu-id="72448-161">Esse texto é localizável.</span><span class="sxs-lookup"><span data-stu-id="72448-161">This text is localizable.</span></span>

<span data-ttu-id="72448-162">Veja a seguir as diretrizes de controle de versão para criadores de perfil:</span><span class="sxs-lookup"><span data-stu-id="72448-162">The following are versioning guidelines for profile creators:</span></span>

-   <span data-ttu-id="72448-163">Para perfis criados por terceiros, como fabricantes de impressoras, o autor do perfil deve incorporar texto descritivo em vários idiomas.</span><span class="sxs-lookup"><span data-stu-id="72448-163">For profiles created by 3rd parties such as printer manufacturers, the profile author should incorporate descriptive text in multiple languages.</span></span>
-   <span data-ttu-id="72448-164">Os seguintes elementos devem ser localizáveis:</span><span class="sxs-lookup"><span data-stu-id="72448-164">The following elements should be localizable:</span></span> 

    | <span data-ttu-id="72448-165">Elemento</span><span class="sxs-lookup"><span data-stu-id="72448-165">Element</span></span>     | <span data-ttu-id="72448-166">CDMP</span><span class="sxs-lookup"><span data-stu-id="72448-166">CDMP</span></span> | <span data-ttu-id="72448-167">GMMP</span><span class="sxs-lookup"><span data-stu-id="72448-167">GMMP</span></span> | <span data-ttu-id="72448-168">CAMP</span><span class="sxs-lookup"><span data-stu-id="72448-168">CAMP</span></span> |
    |-------------|------|------|------|
    | <span data-ttu-id="72448-169">ProfileName</span><span class="sxs-lookup"><span data-stu-id="72448-169">ProfileName</span></span> | <span data-ttu-id="72448-170">x</span><span class="sxs-lookup"><span data-stu-id="72448-170">x</span></span>    | <span data-ttu-id="72448-171">x</span><span class="sxs-lookup"><span data-stu-id="72448-171">x</span></span>    | <span data-ttu-id="72448-172">x</span><span class="sxs-lookup"><span data-stu-id="72448-172">x</span></span>    |
    | <span data-ttu-id="72448-173">Descrição</span><span class="sxs-lookup"><span data-stu-id="72448-173">Description</span></span> | <span data-ttu-id="72448-174">x</span><span class="sxs-lookup"><span data-stu-id="72448-174">x</span></span>    | <span data-ttu-id="72448-175">x</span><span class="sxs-lookup"><span data-stu-id="72448-175">x</span></span>    | <span data-ttu-id="72448-176">x</span><span class="sxs-lookup"><span data-stu-id="72448-176">x</span></span>    |
    | <span data-ttu-id="72448-177">Autor</span><span class="sxs-lookup"><span data-stu-id="72448-177">Author</span></span>      | <span data-ttu-id="72448-178">x</span><span class="sxs-lookup"><span data-stu-id="72448-178">x</span></span>    | <span data-ttu-id="72448-179">x</span><span class="sxs-lookup"><span data-stu-id="72448-179">x</span></span>    | <span data-ttu-id="72448-180">x</span><span class="sxs-lookup"><span data-stu-id="72448-180">x</span></span>    |

    

     

### <a name="expressing-localizable-elements"></a><span data-ttu-id="72448-181">Expressando elementos localizáveis</span><span class="sxs-lookup"><span data-stu-id="72448-181">Expressing localizable elements</span></span>

<span data-ttu-id="72448-182">Em vez de conter texto diretamente, cada elemento localizável contém um ou mais subelemento WCS: Text, cada um deles deve especificar o atributo XML: lang.</span><span class="sxs-lookup"><span data-stu-id="72448-182">Instead of directly containing text, each localizable element contains one or more wcs:Text sub-elements, each of which must specify the xml:lang attribute.</span></span> <span data-ttu-id="72448-183">Conforme descrito na seção de [especificação xml](http://www.w3.org/TR/REC-xml/) 2,12 ("identificação de idioma"), o valor do atributo XML: lang deve ser um identificador de idioma IETF RFC 3066, como "en-US", "en" ou "FR-FR".</span><span class="sxs-lookup"><span data-stu-id="72448-183">As described in the [XML specification](http://www.w3.org/TR/REC-xml/) Section 2.12 ("Language Identification"), the value of the xml:lang attribute must be an IETF RFC 3066 language identifier such as "en-US", "en", or "fr-FR".</span></span> <span data-ttu-id="72448-184">Nos esquemas WCS, o valor do atributo XML: lang não deve ser a cadeia de caracteres vazia "", embora o XML permita isso em geral.</span><span class="sxs-lookup"><span data-stu-id="72448-184">In WCS schemas, the value of the xml:lang attribute must not be the empty string "", even though XML allows this in the general case.</span></span> <span data-ttu-id="72448-185">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="72448-185">For example:</span></span>


```XML
<cdm:ColorDeviceModel ... />
    <cdm:Description>
        <wcs:Text xml:lang="en-US">Hello</wcs:Text>
        <wcs:Text xml:lang="fr-FR">Bonjour</wcs:Text>
    </cdm:Description>
    ...
</cdm:ColorDeviceeModel>
```



<span data-ttu-id="72448-186">Não há dois WCS: elementos de texto podem ter o mesmo atributo XML: lang.</span><span class="sxs-lookup"><span data-stu-id="72448-186">No two wcs:Text elements can have the same xml:lang attribute.</span></span> <span data-ttu-id="72448-187">Cada esquema de perfil WCS deve impor essa restrição separadamente para cada elemento localizável.</span><span class="sxs-lookup"><span data-stu-id="72448-187">Each WCS profile schema must enforce this constraint separately for each localizable element.</span></span> <span data-ttu-id="72448-188">Somente as codificações UTF-8 e UTF-16 são compatíveis.</span><span class="sxs-lookup"><span data-stu-id="72448-188">Only UTF-8 and UTF-16 encodings are supported.</span></span>

### <a name="schema-support"></a><span data-ttu-id="72448-189">Suporte a esquemas</span><span class="sxs-lookup"><span data-stu-id="72448-189">Schema Support</span></span>

<span data-ttu-id="72448-190">O design usa os tipos XSD WCS: LocalizedText e WCS: multilocalizadotype definido no esquema de tipo de perfil comum WCS:</span><span class="sxs-lookup"><span data-stu-id="72448-190">The design makes use of the XSD types wcs:LocalizedText and wcs:MultiLocalizedType defined in the WCS Common Profile Type schema:</span></span>


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



<span data-ttu-id="72448-191">Cada esquema de perfil WCS declara que cada elemento localizável é do tipo multitraduzitype, por exemplo:</span><span class="sxs-lookup"><span data-stu-id="72448-191">Each WCS profile schema declares each localizable element to be of type MultiLocalizedType, for example:</span></span>


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



<span data-ttu-id="72448-192">O esquema CDMP impõe a restrição de que cada WCS: Text Child do elemento CDM: Description deve ter um atributo XML: lang exclusivo.</span><span class="sxs-lookup"><span data-stu-id="72448-192">The CDMP schema enforces the constraint that each wcs:Text child of the cdm:Description element must have a unique xml:lang attribute.</span></span> <span data-ttu-id="72448-193">Ele impõe a mesma restrição para os outros elementos localizáveis.</span><span class="sxs-lookup"><span data-stu-id="72448-193">It enforces the same constraint for the other localizable elements.</span></span> <span data-ttu-id="72448-194">Os esquemas CAMP e GMMP fazem o mesmo.</span><span class="sxs-lookup"><span data-stu-id="72448-194">The CAMP and GMMP schemas do the same.</span></span>

### <a name="selecting-the-language"></a><span data-ttu-id="72448-195">Selecionando o idioma</span><span class="sxs-lookup"><span data-stu-id="72448-195">Selecting the Language</span></span>

<span data-ttu-id="72448-196">Ao decidir qual versão de idioma de um elemento localizável exibir, o código do aplicativo deve selecionar a "versão mais próxima" para a "linguagem atual".</span><span class="sxs-lookup"><span data-stu-id="72448-196">When deciding which language version of a localizable element to display, application code should select the "closest version" to the "current language".</span></span> <span data-ttu-id="72448-197">O que "versão mais próxima" e "idioma atual" realmente significam que depende da plataforma; Veja abaixo.</span><span class="sxs-lookup"><span data-stu-id="72448-197">What "closest version" and "current language" actually mean is platform-dependent; see below.</span></span> <span data-ttu-id="72448-198">Se o perfil não contiver uma versão de idioma que corresponda ao idioma atual, o aplicativo deverá selecionar a primeira versão no perfil (o primeiro elemento de texto filho WCS: Text do elemento localizável).</span><span class="sxs-lookup"><span data-stu-id="72448-198">If the profile does not contain a language version that matches the current language, the application should select the first version in the profile (the first wcs:Text child element of the localizable element).</span></span>

<span data-ttu-id="72448-199">No Windows Vista, a seleção de idioma é feita da seguinte maneira: cada thread tem uma lista associada de "linguagens de interface do usuário preferenciais", que pode ser obtida chamando [**GetThreadPreferredUILanguages**](/windows/win32/api/winnls/nf-winnls-getthreadpreferreduilanguages).</span><span class="sxs-lookup"><span data-stu-id="72448-199">On Windows Vista, the language selection is done as follows: Each thread has an associated list of "preferred UI languages", which can be obtained by calling [**GetThreadPreferredUILanguages**](/windows/win32/api/winnls/nf-winnls-getthreadpreferreduilanguages).</span></span> <span data-ttu-id="72448-200">A lista é retornada em ordem de preferência do usuário.</span><span class="sxs-lookup"><span data-stu-id="72448-200">The list is returned in order of user preference.</span></span> <span data-ttu-id="72448-201">Por exemplo, em um sistema configurado para inglês americano, a lista retornada por **GetThreadPreferredUILanguages** é {"en-US", "en"}.</span><span class="sxs-lookup"><span data-stu-id="72448-201">For instance, on a system set up for US English, the list returned by **GetThreadPreferredUILanguages** is { "en-US", "en" }.</span></span> <span data-ttu-id="72448-202">Isso significa: 1) inglês americano, se presente.</span><span class="sxs-lookup"><span data-stu-id="72448-202">This means: 1) US English if present.</span></span> <span data-ttu-id="72448-203">2) caso contrário, use qualquer variante regional do inglês, como "en-GB" ou simplesmente "en" simples.</span><span class="sxs-lookup"><span data-stu-id="72448-203">2) Otherwise, use any regional variant of English, such as "en-GB" or just plain "en".</span></span>

<span data-ttu-id="72448-204">Para cada idioma nessa lista, em ordem de lista, o código da interface do usuário procura um elemento WCS: Text cujo atributo XML: lang é uma correspondência exata.</span><span class="sxs-lookup"><span data-stu-id="72448-204">For each language in that list, in list order, the UI code looks for a wcs:Text element whose xml:lang attribute is an exact match.</span></span> <span data-ttu-id="72448-205">A primeira versão correspondente é usada.</span><span class="sxs-lookup"><span data-stu-id="72448-205">The first matching version is used.</span></span> <span data-ttu-id="72448-206">Se nenhuma versão corresponder, o primeiro elemento WCS: Text será usado.</span><span class="sxs-lookup"><span data-stu-id="72448-206">If no version matches, the first wcs:Text element is used.</span></span>

### <a name="built-in-profiles"></a><span data-ttu-id="72448-207">Perfis internos</span><span class="sxs-lookup"><span data-stu-id="72448-207">Built-in profiles</span></span>

<span data-ttu-id="72448-208">Os perfis WCS padrão fornecidos com o Windows Vista, como sRGB. CDMP, têm as mesmas propriedades localizáveis que outros perfis.</span><span class="sxs-lookup"><span data-stu-id="72448-208">The standard WCS profiles shipped with Windows Vista, such as sRGB.cdmp, have the same localizable properties as other profiles.</span></span>

<span data-ttu-id="72448-209">A solução padrão do Windows seria colocar as cadeias de caracteres localizadas em uma DLL do MUI e consultá-las da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="72448-209">The standard Windows solution would be to put the localized strings in a MUI DLL, and refer to them like this:</span></span>


```XML
<cdm:Description resourceId="mscms.dll,-101">
    <wcs:Text xml:lang="en-US">Hello, world!</wcs:Text>
<cdm:Description>
```



<span data-ttu-id="72448-210">Em um sistema Windows, o texto de descrição seria extraído da ID de recurso 101 na versão localizada apropriada dos recursos do MUI para mscms.dll.</span><span class="sxs-lookup"><span data-stu-id="72448-210">On a Windows system, the description text would be extracted from resource ID 101 in the appropriate localized version of the MUI resources for mscms.dll.</span></span> <span data-ttu-id="72448-211">Os sistemas não Windows usariam os subelementos WCS: Text, conforme descrito acima.</span><span class="sxs-lookup"><span data-stu-id="72448-211">Non-Windows systems would use the wcs:Text sub-elements as described above.</span></span>

<span data-ttu-id="72448-212">Apresentamos um atributo de ID opcional, globalmente exclusivo, no elemento raiz de cada esquema de perfil do WCS.</span><span class="sxs-lookup"><span data-stu-id="72448-212">We introduce an optional, globally unique ID attribute on the root element of each WCS profile schema.</span></span> <span data-ttu-id="72448-213">O perfil padrão wcsRGB. CDMP pode ser assim:</span><span class="sxs-lookup"><span data-stu-id="72448-213">The standard profile wcsRGB.cdmp might look like this:</span></span>


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



<span data-ttu-id="72448-214">Para os perfis de cores WCS fornecidos com o Windows, a CPL de cor exibe informações descritivas dos recursos, em vez dos elementos WCS: Text nos perfis.</span><span class="sxs-lookup"><span data-stu-id="72448-214">For the WCS color profiles shipped with windows, the Color CPL displays descriptive information from the resources, rather than from the wcs:Text elements in the profiles.</span></span> <span data-ttu-id="72448-215">Isso permite que o Windows exiba informações localizadas para esses perfis em todos os idiomas com suporte, sem exigir que os perfis themlselves contenham informações descritivas em todos os idiomas.</span><span class="sxs-lookup"><span data-stu-id="72448-215">This allows Windows to display localized information for these profiles in all supported languages, without requiring the profiles themlselves to contain descriptive information in all languages.</span></span>

## <a name="related-topics"></a><span data-ttu-id="72448-216">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="72448-216">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="72448-217">Conceitos básicos de gerenciamento de cores</span><span class="sxs-lookup"><span data-stu-id="72448-217">Basic color management concepts</span></span>](basic-color-management-concepts.md)
</dt> <dt>

[<span data-ttu-id="72448-218">Algoritmos e esquemas do sistema de cores do Windows</span><span class="sxs-lookup"><span data-stu-id="72448-218">Windows Color System Schemas and Algorithms</span></span>](windows-color-system-schemas-and-algorithms.md)
</dt> </dl>

 

 