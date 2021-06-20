---
description: Saiba mais sobre o elemento JobPrimaryCoverBackSource, que especifica a origem de uma folha primária de capa de fundo personalizada para o trabalho.
ms.assetid: b5c8e79c-cdae-4c53-b594-915726423b4f
title: JobPrimaryCoverBackSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74ed9bbc1b49e230eabc3fd7f45773a73401e058
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408689"
---
# <a name="jobprimarycoverbacksource"></a>JobPrimaryCoverBackSource

Este tópico não é atual. Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Especifica a origem de uma folha primária de capa de fundo personalizada para o trabalho.

-   [Informações do elemento](#element-information)
-   [Conteúdo da estrutura](#structure-content)

## <a name="element-information"></a>Informações do elemento



| Name | Valor |
|----------------------------|-------------------------------------------|
| Tipo de elemento <br/>   | ParameterDef<br/>                   |
| Prefixo de escopo <br/> | Trabalho<br/>                            |
| Observações <br/>          | Vinculado ao elemento JobCoverBack<br/> |



 

## <a name="structure-content"></a>Conteúdo da estrutura

A estrutura XML desse elemento é:

``` syntax
<psf:ParameterDef name="psk:JobPrimaryCoverBackSource">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:string</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxLength">
    <psf:Value xsi:type="xs:integer ">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinLength">
    <psf:Value xsi:type="xs:integer ">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">characters</psf:Value>
  </psf:Property>
</psf:ParameterDef>      
```

## <a name="structure-properties"></a>Propriedades da estrutura

A tabela a seguir descreve as características das variáveis definidas na estrutura XML.



| Propriedade                | xsi:type           | Valor                      |
|-------------------------|--------------------|----------------------------|
| Tipo de dados<br/>     | string<br/>  | xs:string<br/>       |
| DefaultValue<br/> | string<br/>  | não definido<br/>       |
| MaxLength<br/>    | Número inteiro<br/> | não definido<br/>       |
| MinLength<br/>    | integer<br/> | 1<br/>               |
| Obrigatório<br/>    | string<br/>  | PSK: condicional<br/> |
| UnitType<br/>     | string<br/>  | characters<br/>      |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




