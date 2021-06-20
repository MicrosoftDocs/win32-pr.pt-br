---
description: Saiba mais sobre o elemento JobAccountingSheet, que descreve a planilha de contabilidade a ser saída para o trabalho.
ms.assetid: fd16bd46-32e3-4896-ac5c-03c1bf6ad515
title: JobAccountingSheet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 499d78db7a967e256ee79cd6e0c35d2f7d59dff4
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409090"
---
# <a name="jobaccountingsheet"></a>JobAccountingSheet

Este tópico não é atual. Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Descreve a planilha de contabilidade a ser saída para o trabalho. A planilha de contabilidade deve ser saída no PageMediaSize padrão e usando o PageMediaType padrão. A planilha de contabilidade deve ser isolada do restante do trabalho. Isso significa que todas as opções de conclusão ou processamento (como JobDuplex, JobStaple ou JobBinding) não devem incluir a planilha de contabilidade. A planilha de contabilidade pode ocorrer como a primeira ou a última página do trabalho a critério do implementador.

-   [Informações do elemento](#element-information)
-   [Conteúdo estrutural](#structural-content)
-   [linguagem XML conteúdo (XML)](#extensible-markup-language-xml-content)

## <a name="element-information"></a>Informações do elemento



| Name | Valor |
|----------------------------|--------------------|
| Tipo de elemento <br/>   | Recurso<br/> |
| Prefixo de definição de scoping <br/> | Trabalho<br/>     |
| Observações <br/>          | Nenhum<br/>    |



 

## <a name="structural-content"></a>Conteúdo estrutural

A estrutura XML desse elemento é:

``` syntax
<psf:Feature name="psk:JobAccountingSheet">
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

As palavras-chave public Print Schema são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace . O conteúdo linguagem XML XML (public linguagem XML) para essa palavra-chave é definido abaixo:

``` syntax
<psf:Feature name="psk:JobAccountingSheet">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies no accounting sheet will be output. -->
  <psf:Option name="psk:None" />
  <!-- Specifies the standard (device defined) accounting sheet should be output. -->
  <psf:Option name="psk:Standard" />
</psf:Feature>
        
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




