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
# <a name="wcs-color-appearance-model-profile-schema-and-algorithm"></a><span data-ttu-id="13583-118">Esquema e algoritmo de perfil do modelo de aparência de cores do WCS</span><span class="sxs-lookup"><span data-stu-id="13583-118">WCS Color Appearance Model Profile Schema and Algorithm</span></span>

[<span data-ttu-id="13583-119">Visão geral</span><span class="sxs-lookup"><span data-stu-id="13583-119">Overview</span></span>](#overview)

[<span data-ttu-id="13583-120">Arquitetura do perfil do modelo de aparência de cores (CAMP)</span><span class="sxs-lookup"><span data-stu-id="13583-120">Color Appearance Model Profile (CAMP) Architecture</span></span>](#color-appearance-model-profile-architecture)

[<span data-ttu-id="13583-121">O esquema CAMP</span><span class="sxs-lookup"><span data-stu-id="13583-121">The CAMP Schema</span></span>](#the-camp-schema)

[<span data-ttu-id="13583-122">Os elementos do esquema CAMP</span><span class="sxs-lookup"><span data-stu-id="13583-122">The CAMP Schema Elements</span></span>](#the-camp-schema-elements)

[<span data-ttu-id="13583-123">O algoritmo CAMP</span><span class="sxs-lookup"><span data-stu-id="13583-123">The CAMP Algorithm</span></span>](#the-camp-algorithm)

### <a name="overview"></a><span data-ttu-id="13583-124">Visão geral</span><span class="sxs-lookup"><span data-stu-id="13583-124">Overview</span></span>

<span data-ttu-id="13583-125">Esse esquema é usado para especificar o conteúdo de um perfil de modelo de aparência de cor (CAMP).</span><span class="sxs-lookup"><span data-stu-id="13583-125">This schema is used to specify the content of a color appearance model profile (CAMP).</span></span> <span data-ttu-id="13583-126">Os algoritmos de linha de base associados são descritos nas seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="13583-126">The associated baseline algorithms are described in the following sections.</span></span>

<span data-ttu-id="13583-127">O CAMP é composto de marcas XML que fornecem valores paramétricos para as variáveis de modelo de aparência de linha de base CIECAM02.</span><span class="sxs-lookup"><span data-stu-id="13583-127">The CAMP is composed of XML tags that provide parametric values to the CIECAM02 baseline color appearance model variables.</span></span> <span data-ttu-id="13583-128">Detalhes sobre os intervalos de parâmetros são fornecidos na especificação do modelo de aparência de cor de linha de base e na recomendação de CIECAM02.</span><span class="sxs-lookup"><span data-stu-id="13583-128">Details on the ranges for parameters are provided in the baseline color appearance model specification and CIECAM02 recommendation.</span></span>

### <a name="color-appearance-model-profile-architecture"></a><span data-ttu-id="13583-129">Arquitetura do perfil do modelo de aparência de cores</span><span class="sxs-lookup"><span data-stu-id="13583-129">Color Appearance Model Profile Architecture</span></span>

![Diagrama que mostra a arquitetura do perfil CAMP composta de marcas X M L.](images/camp-image002new.png)

### <a name="the-camp-schema"></a><span data-ttu-id="13583-131">O esquema CAMP</span><span class="sxs-lookup"><span data-stu-id="13583-131">The CAMP Schema</span></span>


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



## <a name="the-camp-schema-elements"></a><span data-ttu-id="13583-132">Os elementos do esquema CAMP</span><span class="sxs-lookup"><span data-stu-id="13583-132">The CAMP Schema Elements</span></span>

## <a name="colorappearancemodel"></a><span data-ttu-id="13583-133">ColorAppearanceModel</span><span class="sxs-lookup"><span data-stu-id="13583-133">ColorAppearanceModel</span></span>

<span data-ttu-id="13583-134">Esse elemento é uma sequência de:</span><span class="sxs-lookup"><span data-stu-id="13583-134">This element is a sequence of:</span></span>

1.  <span data-ttu-id="13583-135">Cadeia de caracteres ProfileName,</span><span class="sxs-lookup"><span data-stu-id="13583-135">ProfileName string,</span></span>
2.  <span data-ttu-id="13583-136">Cadeia de caracteres de descrição opcional,</span><span class="sxs-lookup"><span data-stu-id="13583-136">optional Description string,</span></span>
3.  <span data-ttu-id="13583-137">Cadeia de caracteres de autor opcional,</span><span class="sxs-lookup"><span data-stu-id="13583-137">optional Author string,</span></span>
4.  <span data-ttu-id="13583-138">Elemento ViewingConditions.</span><span class="sxs-lookup"><span data-stu-id="13583-138">ViewingConditions element.</span></span>

<span data-ttu-id="13583-139">**Condições de validação:** Cada subelemento é validado por seu próprio tipo.</span><span class="sxs-lookup"><span data-stu-id="13583-139">**Validation conditions:** Each sub-element is validated by its own type.</span></span> <span data-ttu-id="13583-140">Os comprimentos da cadeia de caracteres são limitados a 10.000 caracteres.</span><span class="sxs-lookup"><span data-stu-id="13583-140">String lengths are limited to 10,000 characters.</span></span>

## <a name="namespace"></a><span data-ttu-id="13583-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="13583-141">Namespace</span></span>

<span data-ttu-id="13583-142">xmlns: cam = " http://schemas.microsoft.com/windows/2005/02/color/ColorAppearanceModel "</span><span class="sxs-lookup"><span data-stu-id="13583-142">xmlns:cam="http://schemas.microsoft.com/windows/2005/02/color/ColorAppearanceModel"</span></span>

<span data-ttu-id="13583-143">targetNamespace = " http://schemas.microsoft.com/windows/2005/02/color/ColorAppearanceModel "</span><span class="sxs-lookup"><span data-stu-id="13583-143">targetNamespace="http://schemas.microsoft.com/windows/2005/02/color/ColorAppearanceModel"</span></span>

## <a name="version"></a><span data-ttu-id="13583-144">Versão</span><span class="sxs-lookup"><span data-stu-id="13583-144">Version</span></span>

<span data-ttu-id="13583-145">Versão &gt; 0,1 ou &lt; = "1,0" com a primeira versão do Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="13583-145">Version &gt;0.1 or &lt;= "1.0" with the first release of Windows Vista.</span></span>

<span data-ttu-id="13583-146">**Condições de validação:** Qualquer valor &lt; de versão = 2,0 também é válido para dar suporte a alterações não significativas no formato.</span><span class="sxs-lookup"><span data-stu-id="13583-146">**Validation conditions:** Any version value &lt;=2.0 is also valid to support non-breaking changes to the format.</span></span>

## <a name="documentation"></a><span data-ttu-id="13583-147">Documentação</span><span class="sxs-lookup"><span data-stu-id="13583-147">Documentation</span></span>

<span data-ttu-id="13583-148">Esquema de perfil do modelo de aparência de cores.</span><span class="sxs-lookup"><span data-stu-id="13583-148">Color Appearance Model Profile Schema.</span></span>

<span data-ttu-id="13583-149">Copyright (C) Microsoft.</span><span class="sxs-lookup"><span data-stu-id="13583-149">Copyright (C) Microsoft.</span></span> <span data-ttu-id="13583-150">Todos os direitos reservados.</span><span class="sxs-lookup"><span data-stu-id="13583-150">All rights reserved.</span></span>

<span data-ttu-id="13583-151">**Condições de validação:** Cada subelemento é validado por seu próprio tipo.</span><span class="sxs-lookup"><span data-stu-id="13583-151">**Validation conditions:** Each sub-element is validated by its own type.</span></span>

## <a name="surroundtype"></a><span data-ttu-id="13583-152">Surroundtype</span><span class="sxs-lookup"><span data-stu-id="13583-152">SurroundType</span></span>

<span data-ttu-id="13583-153">Esse elemento é uma enumeração de parâmetros de CIECAM02 "média", "Dim" ou "Dark" ou os parâmetros quantitativos reais da recomendação de CIECAM02 c, impacto do surround.</span><span class="sxs-lookup"><span data-stu-id="13583-153">This element is a either an enumeration of "Average," "Dim," or "Dark" CIECAM02 parameters or the actual quantitative parameters from the CIECAM02 recommendation c, impact of the surround.</span></span>

<span data-ttu-id="13583-154">**Condições de validação:** O parâmetro c pode variar de 0,525 a 0,69.</span><span class="sxs-lookup"><span data-stu-id="13583-154">**Validation conditions:** The c parameter can range from 0.525 to 0.69.</span></span>

## <a name="viewingconditions"></a><span data-ttu-id="13583-155">ViewingConditions</span><span class="sxs-lookup"><span data-stu-id="13583-155">ViewingConditions</span></span>

<span data-ttu-id="13583-156">Esse elemento consiste nos seguintes subelementos:</span><span class="sxs-lookup"><span data-stu-id="13583-156">This element consists of the following sub-elements:</span></span>



| <span data-ttu-id="13583-157">Elemento</span><span class="sxs-lookup"><span data-stu-id="13583-157">Element</span></span>                    | <span data-ttu-id="13583-158">Type</span><span class="sxs-lookup"><span data-stu-id="13583-158">Type</span></span>           |
|----------------------------|----------------|
| <span data-ttu-id="13583-159">WhitePoint</span><span class="sxs-lookup"><span data-stu-id="13583-159">WhitePoint</span></span>                 | <span data-ttu-id="13583-160">WhitePointType</span><span class="sxs-lookup"><span data-stu-id="13583-160">WhitePointType</span></span> |
| <span data-ttu-id="13583-161">Tela de fundo</span><span class="sxs-lookup"><span data-stu-id="13583-161">Background</span></span>                 | <span data-ttu-id="13583-162">CIEXYZ</span><span class="sxs-lookup"><span data-stu-id="13583-162">CIEXYZ</span></span>         |
| <span data-ttu-id="13583-163">Ao</span><span class="sxs-lookup"><span data-stu-id="13583-163">Surround</span></span>                   | <span data-ttu-id="13583-164">Surroundtype</span><span class="sxs-lookup"><span data-stu-id="13583-164">SurroundType</span></span>   |
| <span data-ttu-id="13583-165">LuminanceOfAdaptingField</span><span class="sxs-lookup"><span data-stu-id="13583-165">LuminanceOfAdaptingField</span></span>   | <span data-ttu-id="13583-166">FLOAT</span><span class="sxs-lookup"><span data-stu-id="13583-166">float</span></span>          |
| <span data-ttu-id="13583-167">DegreeOfAdaptation</span><span class="sxs-lookup"><span data-stu-id="13583-167">DegreeOfAdaptation</span></span>         | <span data-ttu-id="13583-168">FLOAT</span><span class="sxs-lookup"><span data-stu-id="13583-168">float</span></span>          |
| <span data-ttu-id="13583-169">NormalizeToMediaWhitePoint</span><span class="sxs-lookup"><span data-stu-id="13583-169">NormalizeToMediaWhitePoint</span></span> | <span data-ttu-id="13583-170">Boolean</span><span class="sxs-lookup"><span data-stu-id="13583-170">Boolean</span></span>        |



 

<span data-ttu-id="13583-171">**Condições de validação:** Os subelementos CIEXYZ são validados pelo NonNegativeXYZType.</span><span class="sxs-lookup"><span data-stu-id="13583-171">**Validation conditions:** CIEXYZ sub-elements are validated by NonNegativeXYZType.</span></span> <span data-ttu-id="13583-172">O LuminanceOfAdaptingField é um máximo de 10, 000cd/m ^ 2.</span><span class="sxs-lookup"><span data-stu-id="13583-172">The LuminanceOfAdaptingField is a maximum of 10,000cd/m^2.</span></span> <span data-ttu-id="13583-173">O DegreeOfAdaptation pode variar de 0,0 a 1,0.</span><span class="sxs-lookup"><span data-stu-id="13583-173">The DegreeOfAdaptation can range from 0.0 to 1.0.</span></span> <span data-ttu-id="13583-174">O valor de NormalizeToMediaWhitePoint pode ser "true" ou "false".</span><span class="sxs-lookup"><span data-stu-id="13583-174">The NormalizeToMediaWhitePoint value can be either "true" or "false."</span></span> <span data-ttu-id="13583-175">Se o subelemento NormalizeToMediaWhitePoint estiver ausente, ele será efetivamente padronizado como "true".</span><span class="sxs-lookup"><span data-stu-id="13583-175">If the NormalizeToMediaWhitePoint sub-element is absent, it effectively defaults to "true."</span></span> <span data-ttu-id="13583-176">Consulte a seção de algoritmo CAMP a seguir.</span><span class="sxs-lookup"><span data-stu-id="13583-176">See the following CAMP algorithm section.</span></span>

## <a name="whitepointtype"></a><span data-ttu-id="13583-177">WhitePointType</span><span class="sxs-lookup"><span data-stu-id="13583-177">WhitePointType</span></span>

<span data-ttu-id="13583-178">Esse elemento é uma enumeração do valor de fonte de luz de CIE ("D50", "D65", "" A "ou" F2 ") ou um subelemento CIEXYZ.</span><span class="sxs-lookup"><span data-stu-id="13583-178">This element is a either an enumeration of CIE light source value ("D50," "D65," "A," or "F2") or a CIEXYZ sub-element.</span></span>

<span data-ttu-id="13583-179">**Condições de validação:** Cada subelemento é validado por seu próprio tipo.</span><span class="sxs-lookup"><span data-stu-id="13583-179">**Validation conditions:** Each sub-element is validated by its own type.</span></span>

## <a name="ciexyztype"></a><span data-ttu-id="13583-180">CIEXYZType</span><span class="sxs-lookup"><span data-stu-id="13583-180">CIEXYZType</span></span>

<span data-ttu-id="13583-181">O elemento CIEXYZType é composto de três elementos de ponto flutuante de IEEE de precisão única do NonNegativeFloatType, denominados "X", "Y" e "Z".</span><span class="sxs-lookup"><span data-stu-id="13583-181">The CIEXYZType element is composed of three NonNegativeFloatType single-precision IEEE floating-point elements, named "X," "Y," and "Z."</span></span> <span data-ttu-id="13583-182">Essas medidas podem ser absolutas (não relativas) CIEXYZ 1931 valores de reflexão ou valores absolutos (não relativos) CIEXYZ 1931 diretos (transmissal) em candelas por unidades de metro quadrado.</span><span class="sxs-lookup"><span data-stu-id="13583-182">These measurements can be either absolute (not relative) CIEXYZ 1931 reflective values or absolute (not relative) CIEXYZ 1931 direct (transmissive) values in candelas per meter squared units.</span></span>

<span data-ttu-id="13583-183">**Condições de validação:** Isso significa que apenas valores reais são válidos e valores de medida CIEXYZ negativos são inválidos.</span><span class="sxs-lookup"><span data-stu-id="13583-183">**Validation conditions:** This means that only real-world values are valid, and negative CIEXYZ measurement values are invalid.</span></span> <span data-ttu-id="13583-184">Como esses são valores absolutos, os valores podem variar bem além de 1,0 f.</span><span class="sxs-lookup"><span data-stu-id="13583-184">Since these are absolute values, values can range well beyond 1.0f.</span></span> <span data-ttu-id="13583-185">Um limite razoável para qualquer valor X, Y ou Z será definido arbitrariamente como 10000.0 f.</span><span class="sxs-lookup"><span data-stu-id="13583-185">A reasonable limit for any X, Y, or Z value will be arbitrarily set to 10000.0f.</span></span>

 

### <a name="the-camp-algorithm"></a><span data-ttu-id="13583-186">O algoritmo CAMP</span><span class="sxs-lookup"><span data-stu-id="13583-186">The CAMP Algorithm</span></span>

<span data-ttu-id="13583-187">O CAM (modelo de aparência de cores) é baseado nas equações de modelo de aparência de cor de CIE CIECAM02.</span><span class="sxs-lookup"><span data-stu-id="13583-187">The color appearance model (CAM) is based on the CIE CIECAM02 color appearance model equations.</span></span>

<span data-ttu-id="13583-188">Essa classe implementa a modelagem de aparência de cor.</span><span class="sxs-lookup"><span data-stu-id="13583-188">This class implements the color appearance modeling.</span></span> <span data-ttu-id="13583-189">Observe que a CAM WCS *não* é substituível, por exemplo, usando um plug-in.</span><span class="sxs-lookup"><span data-stu-id="13583-189">Note that the WCS CAM is *not* replaceable, for example, using a plug-in.</span></span> <span data-ttu-id="13583-190">É uma meta de design ter apenas um modelo de aparência de cor.</span><span class="sxs-lookup"><span data-stu-id="13583-190">It is a design goal to have only one color appearance model.</span></span> <span data-ttu-id="13583-191">O CAM é baseado em recomendações de CIECAM02.</span><span class="sxs-lookup"><span data-stu-id="13583-191">The CAM is based on CIECAM02 recommendations.</span></span>

<span data-ttu-id="13583-192">CIECAM02 pode ser usado de duas maneiras.</span><span class="sxs-lookup"><span data-stu-id="13583-192">CIECAM02 can be used in two ways.</span></span> <span data-ttu-id="13583-193">Na direção de colorimétrico a aparência, ele fornece um mapeamento do espaço da CIE XYZ para o espaço de aparência da cor.</span><span class="sxs-lookup"><span data-stu-id="13583-193">In the colorimetric-to-appearance direction, it provides a mapping from CIE XYZ space to color appearance space.</span></span> <span data-ttu-id="13583-194">Na direção de aparência para colorimétrico, ele mapeia do espaço de aparência de cor para o espaço XYZ.</span><span class="sxs-lookup"><span data-stu-id="13583-194">In the appearance-to-colorimetric direction, it maps from color appearance space back to XYZ space.</span></span> <span data-ttu-id="13583-195">A aparência da cor correlaciona a claridade, J, croma, C e matiz, h.</span><span class="sxs-lookup"><span data-stu-id="13583-195">The color appearance correlates lightness, J, chroma, C, and hue, h.</span></span> <span data-ttu-id="13583-196">Esses três valores formam um sistema de coordenadas cilíndrico.</span><span class="sxs-lookup"><span data-stu-id="13583-196">These three values form a cylindrical coordinate system.</span></span> <span data-ttu-id="13583-197">Frequentemente, se torna mais conveniente trabalhar em um sistema de coordenadas retangular, portanto, Compute a = C cos h e b = C Sin h, para dar CIECAM02 jab.</span><span class="sxs-lookup"><span data-stu-id="13583-197">Frequently, it turns out to be more convenient to work in a rectangular coordinate system, so compute a = C cos h and b = C sin h, to give CIECAM02 Jab.</span></span>

<span data-ttu-id="13583-198">Você pode usar valores de luminosidade de CAM maiores que 100.</span><span class="sxs-lookup"><span data-stu-id="13583-198">You can use CAM lightness values greater than 100.</span></span> <span data-ttu-id="13583-199">O Comitê de CIE que formulau o CIECAM02 não resolveu o comportamento do eixo de claridade para valores de entrada com uma luminância maior do que o ponto branco adotado; ou seja, para valores Y de entrada maiores que o valor Y do ponto branco adotado.</span><span class="sxs-lookup"><span data-stu-id="13583-199">The CIE committee that formulated CIECAM02 did not address the behavior of the lightness axis for input values with a luminance greater than the adopted white point; that is, for input Y values greater than the adopted white point Y value.</span></span> <span data-ttu-id="13583-200">A experimentação mostrou que as equações de luminância em CIECAM02 se comportam razoavelmente para tais valores.</span><span class="sxs-lookup"><span data-stu-id="13583-200">Experimentation has shown that the luminance equations in CIECAM02 behave reasonably for such values.</span></span> <span data-ttu-id="13583-201">A claridade aumenta exponencialmente e segue o mesmo expoente (aproximadamente 1/3).</span><span class="sxs-lookup"><span data-stu-id="13583-201">The lightness increases exponentially and follows the same exponent (roughly 1/3).</span></span>

<span data-ttu-id="13583-202">Às vezes, os usuários desejam alterar a forma como o grau de adaptação (D) é calculado.</span><span class="sxs-lookup"><span data-stu-id="13583-202">Users sometimes want to change the way that the degree of adaptation (D) is calculated.</span></span> <span data-ttu-id="13583-203">O design WCS permite que os usuários controlem esse cálculo alterando o valor degreeOfadaptation nos parâmetros de condições de exibição.</span><span class="sxs-lookup"><span data-stu-id="13583-203">The WCS design enables users to control this calculation by changing the degreeOfadaptation value in the viewing conditions parameters.</span></span>

<span data-ttu-id="13583-204">Para fornecer uma correspondência mais consistente às expectativas sutratadas por ICC dos usuários, o degreeOfAdaptation no acampamentos padrão é 1,0.</span><span class="sxs-lookup"><span data-stu-id="13583-204">To provide a more consistent match to users' ICC-influenced expectations, the degreeOfAdaptation in the default CAMPS is 1.0.</span></span> <span data-ttu-id="13583-205">Isso produz resultados melhores em todos os casos diferentes de MinCD Absolute, em que é aconselhável permitir que o WCS Compute o degreeOfAdaptation (via degreeOfAdaptation =-1).</span><span class="sxs-lookup"><span data-stu-id="13583-205">This produces better results in all cases other than MinCD Absolute, where one might want to let WCS compute the degreeOfAdaptation (via degreeOfAdaptation = -1).</span></span>

<span data-ttu-id="13583-206">Em vez de usar um valor surround de "Average", "Dim" e "Dark", um valor de surround contínuo, calculado a partir do valor c, é fornecido.</span><span class="sxs-lookup"><span data-stu-id="13583-206">Instead of using a surround value of "Average," "Dim," and "Dark," a continuous surround value, computed from the value c, is provided.</span></span> <span data-ttu-id="13583-207">O valor de c deve ser um float entre 0,525 e 0,69.</span><span class="sxs-lookup"><span data-stu-id="13583-207">The value of c must be a float between 0.525 and 0.69.</span></span>

<span data-ttu-id="13583-208">De *c*, *NC* e *F* podem ser computados, usando a interpolação linear piecewise entre os valores já fornecidos para "média", "Dim" e "Dark".</span><span class="sxs-lookup"><span data-stu-id="13583-208">From *c*, *Nc* and *F* can be computed, using piecewise linear interpolation between the values already provided for "Average," "Dim," and "Dark."</span></span> <span data-ttu-id="13583-209">Isso modela o que é mostrado na Figura 1 do CIE 159:2004, a especificação CIECAM02.</span><span class="sxs-lookup"><span data-stu-id="13583-209">This models what is shown in Figure 1 of CIE 159:2004, the CIECAM02 specification.</span></span>



| <span data-ttu-id="13583-210">degreeOfAdaption</span><span class="sxs-lookup"><span data-stu-id="13583-210">degreeOfAdaption</span></span>                     | <span data-ttu-id="13583-211">Comportamento</span><span class="sxs-lookup"><span data-stu-id="13583-211">Behavior</span></span>                                                                       |
|--------------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="13583-212">-1,0</span><span class="sxs-lookup"><span data-stu-id="13583-212">-1.0</span></span>                                 | ![Mostra uma fórmula para o comportamento padrão C I E C A M 02.](images/camp-image006.png)<span data-ttu-id="13583-214">Esse é o comportamento padrão de CIECAM02.</span><span class="sxs-lookup"><span data-stu-id="13583-214">This is the default CIECAM02 behavior.</span></span><br/> |
| <span data-ttu-id="13583-215">0,0 &lt; = degreeOfAdaption &lt; = 1,0</span><span class="sxs-lookup"><span data-stu-id="13583-215">0.0 &lt;= degreeOfAdaption &lt;= 1.0</span></span> | <span data-ttu-id="13583-216">*D* = degreeOfAdaptation (o valor fornecido pelo usuário)</span><span class="sxs-lookup"><span data-stu-id="13583-216">*D* = degreeOfAdaptation (the value supplied by the user)</span></span>                      |



 

<span data-ttu-id="13583-217">Uma determinada quantidade de verificação de erros também foi adicionada à implementação.</span><span class="sxs-lookup"><span data-stu-id="13583-217">A certain amount of error checking has also been added to the implementation.</span></span> <span data-ttu-id="13583-218">Os números de equações a seguir são aqueles usados na definição de CIE 159:2004 de CIECAM02.</span><span class="sxs-lookup"><span data-stu-id="13583-218">The following equation numbers are those used in the CIE 159:2004 definition of CIECAM02.</span></span>

<span data-ttu-id="13583-219">**ColorimetricToAppearanceColors**</span><span class="sxs-lookup"><span data-stu-id="13583-219">**ColorimetricToAppearanceColors**</span></span>

<span data-ttu-id="13583-220">Os valores de entrada são verificados para racionalidade: se X ou Z &lt; 0,0, ou se Y &lt; -1,0, o HRESULT é E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="13583-220">The input values are checked for reasonableness: If X or Z &lt; 0.0, or if Y &lt; -1.0, then the HRESULT is E\_INVALIDARG.</span></span> <span data-ttu-id="13583-221">Se-1,0 &lt; = Y &lt; 0,0, J, C e h estão todos definidos como 0,0.</span><span class="sxs-lookup"><span data-stu-id="13583-221">If -1.0 &lt;= Y &lt; 0.0, then J, C, and h are all set to 0.0.</span></span>

<span data-ttu-id="13583-222">Há certas condições internas que podem produzir resultados de erro.</span><span class="sxs-lookup"><span data-stu-id="13583-222">There are certain internal conditions that can produce error results.</span></span> <span data-ttu-id="13583-223">Em vez de produzir esses resultados, os resultados internos são recortados para produzir valores em intervalo.</span><span class="sxs-lookup"><span data-stu-id="13583-223">Instead of producing such results, the internal results are clipped to produce in-range values.</span></span> <span data-ttu-id="13583-224">Isso acontece para especificações de cores que seriam escuras e impossíveis de desvio: na equação 7,23, se for &lt; 0, a = 0.</span><span class="sxs-lookup"><span data-stu-id="13583-224">This happens for specifications of colors that would be dark and impossibly chromatic: In equation 7.23, if A &lt; 0, A = 0.</span></span> <span data-ttu-id="13583-225">Na equação 7,26, se t &lt; 0, t = 0.</span><span class="sxs-lookup"><span data-stu-id="13583-225">In equation 7.26, if t &lt; 0, t = 0.</span></span>

<span data-ttu-id="13583-226">**AppearanceToColorimetricColors**</span><span class="sxs-lookup"><span data-stu-id="13583-226">**AppearanceToColorimetricColors**</span></span>

<span data-ttu-id="13583-227">Os valores de entrada são verificados para racionalidade.</span><span class="sxs-lookup"><span data-stu-id="13583-227">The input values are checked for reasonableness.</span></span> <span data-ttu-id="13583-228">Se C &lt; 0, c &gt; 300 ou J &gt; 500, o HRESULT será E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="13583-228">If C &lt; 0 , C &gt; 300, or J &gt; 500, then the HRESULT is E\_INVALIDARG.</span></span>

<span data-ttu-id="13583-229">*R '<sub>a;</sub>*, *G '<sub>a;</sub>* e *B '<sub>a;</sub>*, (equações 8,19-8,21) são recortados para o intervalo de 399,9.</span><span class="sxs-lookup"><span data-stu-id="13583-229">*R'<sub>a;</sub>*, *G'<sub>a;</sub>*, and *B'<sub>a;</sub>*, (equations 8.19 - 8.21) are clipped to the range   399.9 .</span></span>

<span data-ttu-id="13583-230">Para todos os perfis de modelo de aparência de cor (acampamentos), o mecanismo WCS examinará o ponto branco adotado.</span><span class="sxs-lookup"><span data-stu-id="13583-230">For all Color Appearance Model Profiles (CAMPs), the WCS engine will examine the adopted white point.</span></span> <span data-ttu-id="13583-231">Se Y não for 100,0, o ponto branco adotado será dimensionado para que Y seja igual a 100,0.</span><span class="sxs-lookup"><span data-stu-id="13583-231">If Y is not 100.0, then the adopted white point will be scaled so that Y does equal 100.0.</span></span> <span data-ttu-id="13583-232">O mesmo dimensionamento será aplicado ao valor em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="13583-232">The same scaling will be applied to the background value.</span></span> <span data-ttu-id="13583-233">O fator de dimensionamento é 100.0/adoptedWhitePoint. Y.</span><span class="sxs-lookup"><span data-stu-id="13583-233">The scaling factor is 100.0/adoptedWhitePoint.Y.</span></span> <span data-ttu-id="13583-234">O mesmo fator de dimensionamento é aplicado a cada X, Y e Z. Se o campo NormalizeToMediaWhitePoint for definido como "true" ou se estiver ausente do CAMP, o mecanismo também dimensionará todas as entradas de cores de dispositivo para DeviceToColorimetric, de modo que o valor Y do ponto branco de mídia do dispositivo seja igual a 100,0.</span><span class="sxs-lookup"><span data-stu-id="13583-234">The same scaling factor is applied to each of X, Y, and Z. If the NormalizeToMediaWhitePoint field is set to "True," or if it is absent from the CAMP, the engine also scales all device colors input to DeviceToColorimetric so that the Y value of the device media white point equals 100.0.</span></span> <span data-ttu-id="13583-235">As cores do dispositivo provenientes de ColorimetricToDevice serão dimensionadas pelo inverso multiplicativa do fator de dimensionamento.</span><span class="sxs-lookup"><span data-stu-id="13583-235">Device colors coming from ColorimetricToDevice will be scaled by the multiplicative inverse of that scaling factor.</span></span> <span data-ttu-id="13583-236">Se o sinalizador NormalizeToMediaWhitePoint for definido como "false", os dados colorimétrico não serão dimensionados.</span><span class="sxs-lookup"><span data-stu-id="13583-236">If the NormalizeToMediaWhitePoint flag is set to "False," then the colorimetric data is not scaled.</span></span>

<span data-ttu-id="13583-237">Para algumas tarefas, faz sentido dimensionar os valores colorimétrico provenientes de DeviceToColorimetric.</span><span class="sxs-lookup"><span data-stu-id="13583-237">For some tasks, it makes sense to scale the colorimetric values coming from DeviceToColorimetric.</span></span> <span data-ttu-id="13583-238">As equações de luminosidade hiperbólica no CAM são realmente projetadas para uma luminância de ponto branco de 100,0.</span><span class="sxs-lookup"><span data-stu-id="13583-238">The hyperbolic lightness equations in the CAM are really designed for a white point luminance of 100.0.</span></span> <span data-ttu-id="13583-239">O único lugar em que uma diferença na luminância absoluta (ou illuminance) entra em jogo está na luminância do campo de adaptação.</span><span class="sxs-lookup"><span data-stu-id="13583-239">The only place where a difference in the absolute luminance (or illuminance) comes into play is in the luminance of the adapting field.</span></span> <span data-ttu-id="13583-240">Portanto, o CAM deve ser inicializado com um ponto branco Y de 100,0.</span><span class="sxs-lookup"><span data-stu-id="13583-240">So the CAM must be initialized with a white point Y of 100.0.</span></span> <span data-ttu-id="13583-241">Mas se o ponto branco médio do modelo do dispositivo estiver sendo usado como o ponto branco adotado, todas as cores provenientes do dispositivo deverão ser dimensionadas de forma adequada ou o dispositivo branco não virá com um valor J de 100,0.</span><span class="sxs-lookup"><span data-stu-id="13583-241">But if the device model's medium white point is being used as the adopted white point, then all colors coming from the device must be scaled accordingly, or device white will not come out with a J value of 100.0.</span></span> <span data-ttu-id="13583-242">Portanto, os valores Y precisam ser dimensionados nas medidas.</span><span class="sxs-lookup"><span data-stu-id="13583-242">So the Y values have to be scaled in the measurements.</span></span> <span data-ttu-id="13583-243">Os valores de medida podem ser dimensionados antes da inicialização do modelo do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="13583-243">The measurement values could be scaled before initializing the device model.</span></span> <span data-ttu-id="13583-244">Em seguida, os resultados já estarão no intervalo adequado.</span><span class="sxs-lookup"><span data-stu-id="13583-244">Then results would already be in the proper range.</span></span> <span data-ttu-id="13583-245">Mas isso tornaria o teste do modelo do dispositivo mais difícil, pois os valores que chegam seriam necessários para o dimensionamento.</span><span class="sxs-lookup"><span data-stu-id="13583-245">But that would make testing the device model more difficult, because the values coming out would require scaling.</span></span> <span data-ttu-id="13583-246">Para as tarefas nas quais o ponto branco médio do dispositivo é percebido como um verdadeiro branco, a normalização pelo ponto branco de mídia do dispositivo é desejável.</span><span class="sxs-lookup"><span data-stu-id="13583-246">For tasks in which the device medium white point is perceived to be a true white, normalizing by the device media white point is desirable.</span></span>

<span data-ttu-id="13583-247">O CAM é inicializado diretamente do CAMP.</span><span class="sxs-lookup"><span data-stu-id="13583-247">The CAM is initialized directly from the CAMP.</span></span> <span data-ttu-id="13583-248">Isso permite aos desenvolvedores alguma flexibilidade na inicialização do CAM, com base na tarefa que desejam executar.</span><span class="sxs-lookup"><span data-stu-id="13583-248">This allows developers some flexibility in initializing the CAM, based upon the task they want to perform.</span></span> <span data-ttu-id="13583-249">Em algumas tarefas, os observadores ignorarão qualquer croma nos pontos brancos de mídia, pois eles "sabem" de forma cognitiva que a mídia de origem e de destino são "brancas".</span><span class="sxs-lookup"><span data-stu-id="13583-249">In some tasks, observers will ignore any chroma in the media white points, because they cognitively "know" that the source and destination media are "white."</span></span> <span data-ttu-id="13583-250">Nesses casos, os desenvolvedores desejarão inicializar o câmeras direto e inverso com seus respectivos pontos brancos de mídia.</span><span class="sxs-lookup"><span data-stu-id="13583-250">In such cases, developers will want to initialize the forward and inverse CAMs with their respective media white points.</span></span> <span data-ttu-id="13583-251">Em alguns casos, os observadores podem estar comparando a cor dos planos de fundo de mídia.</span><span class="sxs-lookup"><span data-stu-id="13583-251">In some cases, observers may be comparing the color of the media backgrounds.</span></span> <span data-ttu-id="13583-252">Nesses casos, é aconselhável usar um CAM para ambos os dispositivos, e pode ser desejável não dimensionar os valores colorimétrico de cada dispositivo pelo ponto branco médio desse dispositivo.</span><span class="sxs-lookup"><span data-stu-id="13583-252">In these cases, it is advisable to use one CAM for both devices, and it may be desirable not to scale each device's colorimetric values by that device's medium white point.</span></span> <span data-ttu-id="13583-253">Em seguida, os diferentes valores de triestímulo da mídia levarão a valores de aparência diferentes em CIECAM02.</span><span class="sxs-lookup"><span data-stu-id="13583-253">Then the different tristimulus values of the media will lead to different appearance values in CIECAM02.</span></span>

## <a name="related-topics"></a><span data-ttu-id="13583-254">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="13583-254">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="13583-255">Conceitos básicos de gerenciamento de cores</span><span class="sxs-lookup"><span data-stu-id="13583-255">Basic color management concepts</span></span>](basic-color-management-concepts.md)
</dt> <dt>

[<span data-ttu-id="13583-256">Algoritmos e esquemas do sistema de cores do Windows</span><span class="sxs-lookup"><span data-stu-id="13583-256">Windows Color System Schemas and Algorithms</span></span>](windows-color-system-schemas-and-algorithms.md)
</dt> </dl>

 

 





