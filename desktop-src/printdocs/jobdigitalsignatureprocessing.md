---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 0592f7a4-cace-41b0-91e3-2811f72aeb3e
title: JobDigitalSignatureProcessing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aad9dbe0ba82d219a28602178efa2e102ccf167b
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998283"
---
# <a name="jobdigitalsignatureprocessing"></a>JobDigitalSignatureProcessing

Este tópico não é atual. Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Descreve a configuração do processamento de assinatura digital para todo o trabalho. Aplicável somente ao conteúdo que contém assinaturas digitais.

-   [Informações do elemento](#element-information)
-   [Conteúdo estrutural](#structural-content)

## <a name="element-information"></a>Informações do elemento



| Nome | Valor |
|----------------------------|--------------------|
| Tipo de elemento <br/>   | Recurso<br/> |
| Prefixo de escopo <br/> | Trabalho<br/>     |
| Observações <br/>          | Nenhum<br/>    |



 

## <a name="structural-content"></a>Conteúdo estrutural

A estrutura XML desse elemento é:

``` syntax
<psf:Feature name="psk:JobDigitalSignatureProcessing">
  <psf:Property name="SelectionType">
    <psf:Value xsi:type="xs:string">PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
  </psf:Feature>
```

## <a name="structure-variables"></a>Variáveis de estrutura

A tabela a seguir descreve as características das variáveis definidas na estrutura XML.



| Nome                               | Tipo de dados         | Unidade                   | Valores com suporte                                                                                                                                                                      | Resumo                                                                      |
|------------------------------------|-------------------|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| \_OptionName\_<br/>          | string<br/> | characters <br/> | Nome totalmente qualificado válido, conforme definido pelos [namespaces em XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/). Se nenhum namespace for especificado, o namespace padrão será assumido.<br/> | O nome da opção<br/>                                            |
| \_IdentityOptionValue\_<br/> | string<br/> | N/D<br/>         | Verdadeiro, Falso<br/>                                                                                                                                                                | Define uma opção que, quando selecionada, desabilita esse recurso.<br/> |



 

## <a name="extensible-markup-language-xml-content"></a>Conteúdo de linguagem XML (XML)

As palavras-chave do esquema de impressão pública são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace. O conteúdo do linguagem XML público (XML) para essa palavra-chave é definido abaixo:

``` syntax
<psf:Feature name="psk:JobDigitalSignatureProcessing">
  <psf:Property name="SelectionType">
    <psf:Value xsi:type="xs:string">PickOne</psf:Value>
  </psf:Property>
  <!-- Print the job regardless of the validity of the digital signatures. Digital signatures MAY be ignored.  -->
  <psf:Option name="psk:PrintInvalidSignatures" />
  <!-- Print the job regardless of the validity of the digital signatures.  In the event an invalid signature is encountered, an error page should print at the end of the job.  Digital signatures MUST not be ignored. -->
  <psf:Option name="psk:PrintInvalidSignaturesWithErrorReport" />
  <!-- Print the job only if all digital signatures are valid.  Digital signatures MUST not be ignored. -->
  <psf:Option name="psk:PrintOnlyValidSignatures" />
</psf:Feature>
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




