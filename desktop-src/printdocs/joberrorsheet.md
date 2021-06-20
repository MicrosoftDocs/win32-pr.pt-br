---
description: Saiba mais sobre o elemento JobErrorSheet, que descreve a saída da planilha de erros. Todo o trabalho terá uma única folha de erros.
ms.assetid: ad30df59-0051-4471-8c0e-3207bcc7bfbe
title: JobErrorSheet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dcee6c50d482793eeef96e29ad98385da11a4e6
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408899"
---
# <a name="joberrorsheet"></a>JobErrorSheet

Este tópico não é atual. Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Descreve a saída da planilha de erros. Todo o trabalho terá uma única folha de erros. A folha de erros deve ser saída no PageMediaSize padrão e usando o PageMediaType padrão. A folha de erros deve ser isolada do restante do trabalho. Isso significa que qualquer opção de conclusão ou processamento (como JobDuplex, JobStaple ou JobBinding) não deve incluir a folha de erros. A folha de erros deve ocorrer como a planilha final do trabalho.

-   [Informações do elemento](#element-information)
-   [Conteúdo estrutural](#structural-content)
-   [linguagem XML conteúdo (XML)](#extensible-markup-language-xml-content)

## <a name="element-information"></a>Informações do elemento



| Name | Valor |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tipo de elemento <br/>   | Recurso<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Prefixo de definição de scoping <br/> | Trabalho<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Observações <br/>          | Os consumidores compatíveis com XPS DEVEM impor que uma referência de URI a um recurso, como uma imagem ou perfil de cor em um documento Recursos de Impressão ou PrintTicket, DEVE se referir a um nome de parte (um URI relativo para a raiz do pacote) dentro do mesmo pacote do Documento XPS que contém o PrintTicket resultante. Um consumidor XPS compatível NÃO DEVE usar um URI que não está em conformidade com a sintaxe de nome da parte. Essas configurações são específicas do XPS. <br/> URIs que são referenciados em um documento Funcionalidades de Impressão ou PrintTicket NÃO DEVEM ser resolvidos como URLs. Isso não é seguro, pois eles podem não ser resolvidos conforme o esperado e podem criar riscos de segurança prejudiciais para o driver e o sistema operacional.<br/> |



 

## <a name="structural-content"></a>Conteúdo estrutural

A estrutura XML desse elemento é:

``` syntax
<psf:Feature name="psk:JobErrorSheet">
  <!--Describes when an error sheet should be output. -->
  <psf:Feature name="psk:ErrorSheetWhen">
    <psf:Property name="psf:SelectionType">
      <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
    </psf:Property>
    <psf:Option name="psk:_ErrorSheetWhenOptionName_">
      <psf:Property name="psf:IdentityOption">
        <psf:Value xsi:type="xs:string">_ErrorSheetWhenIdentityOptionValue_</psf:Value>
      </psf:Property>
    </psf:Option>
  </psf:Feature>
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <!-- Specifies the XPS part name for the error sheet. -->
    <psf:ScoredProperty name="psk:ErrorSheetSource">
      <psf:ParameterRef name="psk:JobErrorSheetSource" />
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>      
```

## <a name="structure-variables"></a>Variáveis de estrutura

A tabela a seguir descreve as características das variáveis definidas na estrutura XML.



| Nome                                             | Tipo de dados         | Unidade                  | Valores com suporte                                                                                                                                                                      | Resumo                                                                      |
|--------------------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| \_ErrorSheetWhenOptionName\_<br/>          | string<br/> | characters<br/> | Nome totalmente qualificado válido, conforme definido [por Namespaces em XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/) Se nenhum namespace for especificado, o namespace padrão será assumido.<br/> | O nome da opção.<br/>                                           |
| \_ErrorSheetWhenIdentityOptionValue\_<br/> | string<br/> | n/d<br/>        | True, False.<br/>                                                                                                                                                               | Define os critérios de seleção da interface do usuário.<br/>               |
| \_Optionname\_<br/>                        | string<br/> | n/d<br/>        | Nome totalmente qualificado válido, conforme definido por https://www.w3.org/TR/1999/REC-xml-names-19990114/\#dt-qname . Se nenhum namespace for especificado, o namespace padrão será assumido.<br/>          | O nome da opção.<br/>                                           |
| \_IdentityOptionValue\_<br/>               | string<br/> | n/d<br/>        | True, False.<br/>                                                                                                                                                               | Define uma Opção que, quando selecionada, desabilitará esse recurso.<br/> |



 

## <a name="extensible-markup-language-xml-content"></a>linguagem XML conteúdo (XML)

As palavras-chave public Print Schema são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace . O conteúdo linguagem XML XML (public linguagem XML) para essa palavra-chave é definido abaixo:

``` syntax
<psf:Feature name="psk:JobErrorSheet">
  <psf:Feature name="psk:ErrorSheetWhen">
    <psf:Property name="psf:SelectionType">
      <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
    </psf:Property>
    <!-- Specifies an error sheet will be output for every job. -->
    <psf:Option name="psk:Always" />
    <!-- Specifies an error sheet will be output only on error. -->
    <psf:Option name="psk:OnError" />
  </psf:Feature>
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies a custom error sheet should be output. If a JobErrorSheetSource 
     ParameterInit element is not specified, this Option should be ignored. -->
  <psf:Option name="psk:Custom">
    <psf:ScoredProperty name="psk:ErrorSheetSource">
      <psf:ParameterRef name="psk:JobErrorSheetSource" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies no error sheet should be output. -->
  <psf:Option name="psk:None" />
  <!-- Specifies the standard (device defined) error sheet should be output. -->
  <psf:Option name="psk:Standard" />
</psf:Feature>    
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




