---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 752cccf7-1f95-4597-b0e2-a96fd22ffeef
title: DocumentCollate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 959613299c53996ce7d66171d2da1518f28b9298
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993993"
---
# <a name="documentcollate"></a>DocumentCollate

Este tópico não é atual. Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Descreve as características de agrupamento da saída. Todas as páginas em cada documento individual são agrupadas. DocumentCollate e JobCollateAlldocuments são mutuamente exclusivos. O comportamento e a implementação de se ambas ou apenas uma dessas palavras-chave são implementadas são deixados para o driver.

A seguir estão as regras que devem ser seguidas para implementação de agrupamento

## <a name="element-definition-and-rules"></a>Definição de elemento e regras

Você deve primeiro seguir as regras para JobCollateAllDocument e, em seguida, aplicar regras para DocumentCollate para que os cenários funcionem. Observe que, em uma configuração de conversão de PrintTicket para DEVMODE, em que JobCollateAllDocuments não é suportado pelo driver, cabe ao driver escolher o comportamento apropriado a ser adotado (JobCollateAllDocuments = ON ou OFF). Além disso, a escolha pode ser alterada dependendo de outras configurações do PrintTicket.

### <a name="jobcollatealldocuments"></a>JobCollateAllDocuments

EM: imprimir (DocumentCopiesAllPages) cópias de cada documento, repetir JobCopiesAllDocuments vezes.

OFF: para cada documento, Print (JobCopiesAllDocuments x DocumentCopiesAllPages) copia juntos.

### <a name="documentcollate"></a>DocumentCollate

EM: para todas as cópias (JobCopiesAllDocuments x DocumentCopiesAllPages) de um documento impresso de forma contígua, você agrupa as planilhas nesse documento.

DESATIVADO: para todas as cópias (JobCopiesAllDocuments x DocumentCopiesAllPages) são impressas de forma contígua, imprima todas as cópias (JobCopiesAllDocuments x DocumentCopiesAllPages) de cada folha juntas.

-   [Informações do elemento](#element-information)

-   [Conteúdo estrutural](#structural-content)

-   [Conteúdo XML](#extensible-markup-language-xml-content)

## <a name="element-information"></a>Informações do elemento



| Nome | Valor |
|----------------------------|---------------------|
| Tipo de elemento <br/>   | Recurso<br/>  |
| Prefixo de escopo <br/> | Documento<br/> |
| Observações <br/>          | Nenhum<br/>     |



 

## <a name="structural-content"></a>Conteúdo estrutural

A estrutura XML desse elemento é:

``` syntax
<psf:Feature name="psk:DocumentCollate">
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
<psf:Feature name="psk:DocumentCollate">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies collating.  -->
  <psf:Option name="psk:Collated" />
  <!-- Specifies no collating. -->
  <psf:Option name="psk:Uncollated" />
</psf:Feature>
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




