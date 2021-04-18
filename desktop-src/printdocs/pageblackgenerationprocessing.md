---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 4edd1fdf-9601-440d-b967-82ffa6dceeb1
title: PageBlackGenerationProcessing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6019cd2e4d73e1869f0a71795923509566afebd0
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "105756501"
---
# <a name="pageblackgenerationprocessing"></a>PageBlackGenerationProcessing

Este tópico não é atual. Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Especifica o comportamento de geração de preto para separações CMYK.

-   [Informações do elemento](#element-information)
-   [Conteúdo estrutural](#structural-content)
-   [Conteúdo de linguagem XML (XML)](#extensible-markup-language-xml-content)

## <a name="element-information"></a>Informações do elemento



| Nome                       |                    |
|----------------------------|--------------------|
| Tipo de elemento <br/>   | Recurso<br/> |
| Prefixo de escopo <br/> | ?<br/>    |
| Observações <br/>          | Nenhum <br/>   |



 

## <a name="structural-content"></a>Conteúdo estrutural

A estrutura XML desse elemento é:

``` syntax
<psf:Feature name="psk:PageBlackGenerationProcessing">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
  </psf:Option>
</psf:Feature>
```

## <a name="structure-variables"></a>Variáveis de estrutura

A tabela a seguir descreve as características das variáveis definidas na estrutura XML.



| Nome                               | Tipo de dados         | Unidade                  | Valores com suporte                                                                                                                                                                      | Resumo                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| \_OptionName\_<br/>          | string<br/> | characters<br/> | Nome totalmente qualificado válido, conforme definido pelos [namespaces em XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/). Se nenhum namespace for especificado, o namespace padrão será assumido.<br/> | O nome da opção.<br/>                                           |
| \_IdentityOptionValue\_<br/> | string<br/> | N/D<br/>        | True, False.<br/>                                                                                                                                                               | Define uma opção que, quando selecionada, desabilita esse recurso.<br/> |



 

## <a name="extensible-markup-language-xml-content"></a>Conteúdo de linguagem XML (XML)

As palavras-chave do esquema de impressão pública são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace. O conteúdo do linguagem XML público (XML) para essa palavra-chave é definido abaixo:

``` syntax
<psf:Feature name="psk:PageBlackGenerationProcessing">
  <psf:Option name="psk:Automatic" />
  <psf:Option name="psk:Custom">
    <!-- The max allowable sum of the four ink coverages anywhere in an image. -->
    <psf:ScoredProperty name="psk:TotalInkCoverageLimit">
      <psf:ParameterRef name="psk:PageBlackGenerationProcessingTotalInkCoverageLimit" />
    </psf:ScoredProperty>
    <!-- The maximum allowed K channel value. -->
    <psf:ScoredProperty name="psk:BlackInkLimit">
      <psf:ParameterRef name="psk:PageBlackGenerationProcessingBlackInkLimit" />
    </psf:ScoredProperty>
    <!-- The percentage of gray component replacement to perform. -->
    <psf:ScoredProperty name="psk:GrayComponentReplacementLevel">
      <psf:ParameterRef name="psk:PageBlackGenerationProcessingGrayComponentReplacementLevel" />
    </psf:ScoredProperty>
    <!-- The point in the highlight to shadow range where GCR should start (100% = darkest shadow). -->
    <psf:ScoredProperty name="psk:GrayComponentReplacementStart">
      <psf:ParameterRef name="psk:PageBlackGenerationProcessingGrayComponentReplacementStart" />
    </psf:ScoredProperty>
    <!-- The extented beyond neutrals (into chromatic colors) that GCR applies.  0% = Undercolor component replacement, 100% = Gray component replacement.  -->
    <psf:ScoredProperty name="psk:GrayComponentReplacementExtent">
      <psf:ParameterRef name="psk:PageBlackGenerationProcessingGrayComponentReplacementExtent" />
    </psf:ScoredProperty>
    <!-- The shadow level below which UCA will be applied.  -->
    <psf:ScoredProperty name="psk:UnderColorAdditionStart">
      <psf:ParameterRef name="psk:PageBlackGenerationProcessingUnderColorAdditionStart" />
    </psf:ScoredProperty>
    <!-- The amount chromatic ink (in gray component ratios) to add to areas where GCR/UCR has generated "BlackInkLimit" (or UCAStart, if specified) in the dark neutrals and near-neutral areas.  -->
    <psf:ScoredProperty name="psk:UnderColorAdditionLevel">
      <psf:ParameterRef name="psk:PageBlackGenerationProcessingUnderColorAdditionLevel" />
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature> 
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




