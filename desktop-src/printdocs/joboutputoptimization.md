---
description: Saiba mais sobre o JobOutputOptimization, que descreve o processamento do trabalho, destinado a otimizar a saída para cenários de uso específicos, conforme indicado pela opção especificada.
ms.assetid: 40925dfe-494c-49b5-ae57-de369723ba76
title: JobOutputOptimization
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 756321c586933367215b556eec4c24cef5e2969bf16aeb4f7b089c92cb481f7a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119099654"
---
# <a name="joboutputoptimization"></a>JobOutputOptimization

Este tópico não é atual. Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Descreve o processamento do trabalho, destinado a otimizar a saída para cenários de uso específicos, conforme indicado pela opção especificada.

-   [Informações do elemento](#element-information)
-   [Conteúdo estrutural](#structural-content)
-   [linguagem XML conteúdo (XML)](#extensible-markup-language-xml-content)

## <a name="element-information"></a>Informações do elemento



| Nome | Valor |
|----------------------------|--------------------|
| Tipo de elemento <br/>   | Recurso<br/> |
| Prefixo de definição de scoping <br/> | Trabalho<br/>     |
| Observações <br/>          | Nenhum<br/>    |



 

## <a name="structural-content"></a>Conteúdo estrutural

A estrutura XML desse elemento é:

``` syntax
<psf:Feature name="psk:JobOutputOptimization">
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
| \_Optionname\_<br/>          | string<br/> | characters<br/> | Nome totalmente qualificado válido, conforme definido [por Namespaces em XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/) Se nenhum namespace for especificado, o namespace padrão será assumido.<br/> | O nome da opção.<br/>                                           |
| \_IdentityOptionValue\_<br/> | string<br/> | n/d<br/>        | True, False.<br/>                                                                                                                                                               | Define uma Opção que, quando selecionada, desabilitará esse recurso.<br/> |



 

## <a name="extensible-markup-language-xml-content"></a>linguagem XML conteúdo (XML)

As palavras-chave public Print Schema são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace . O conteúdo linguagem XML xml público para essa palavra-chave está definido abaixo:

``` syntax
<psf:Feature name="psk:JobOutputOptimization">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies the job processing be optimized for archive output. -->
  <psf:Option name="psk:ArchiveFormat" />
  <!-- Specifies the job processing be optimized for portability (cross-device) of output. -->
  <psf:Option name="psk:OptimizeForPortability" />
  <!-- Specifies the job processing be optimized for quality of output. -->
  <psf:Option name="psk:OptimizeForQuality" />
  <!-- Specifies the job processing be optimized for speed of output. -->
  <psf:Option name="psk:OptimizeForSpeed" />
  <!-- Specifies the job processing should not be optimized for a particular scenario. -->
  <psf:Option name="psk:None" />
</psf:Feature>
    
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




