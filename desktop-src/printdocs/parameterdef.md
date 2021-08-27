---
description: Saiba mais sobre o elemento ParameterDef, que define as características válidas da entrada de parâmetro. O valor é inserido por meio de um elemento ParameterInit.
ms.assetid: cb00edc9-2c8a-446d-989b-a4429ee8f544
title: ParameterDef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5eddca78b76751c6083d1c5b5bac8c1040155e6
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477842"
---
# <a name="parameterdef"></a>ParameterDef

Este tópico não é atual. Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Um elemento ParameterDef define as características válidas da entrada de parâmetro. O valor é inserido por meio de um elemento ParameterInit.

## <a name="element-tag"></a>Marca do elemento

<ParameterDef>

## <a name="xml-attributes"></a>Atributos XML

A tabela a seguir lista os atributos XML que podem ser relativos a esse elemento.



| Atributo XML   | Detalhes                                                                                                                                                                          |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| name<br/> | Define um nome exclusivo para o parâmetro no contexto do documento atual. Atributos de nome de ParameterDef duplicados renderizam o documento PrintCapabilities inválido.<br/> |



 

Para obter mais informações, consulte a seção [atributos XML](xml-attributes.md) .

## <a name="element-information"></a>Informações do elemento

A tabela a seguir lista os elementos que podem ser pais deste elemento, os elementos que podem ser filhos desse elemento e quaisquer restrições no próprio elemento.




| Categoria | Detalhes | 
|----------|---------|
| Elementos pai<br /> | PrintCapabilities <br /> | 
| Elementos filho<br /> | Propriedade (um ou mais)<br /> Os seguintes elementos de propriedade padrão devem aparecer como o conteúdo de um elemento ParameterDef. <br /><ul><li>Tipo de dados <br /></li><li>DefaultValue <br /></li><li>Obrigatório <br /></li><li>MaxLength ou MaxValue<br /></li><li>MinLength ou MinValue<br /></li><li>Vários <br /></li><li>UnitType <br /></li></ul> | 
| Este elemento<br /> | Nenhum dado de caractere é permitido.<br /> Irmãos filho duplicados não são permitidos.<br /> | 




 

\*Necessário quando DataType é inteiro ou Decimal. Opcional quando DataType é uma cadeia de caracteres.

## <a name="configuration-dependencies"></a>Dependências de configuração

Um ParameterDef e seu conteúdo para qualquer nível de aninhamento podem não ter nenhuma dependência de configuração.

## <a name="example"></a>Exemplo

O exemplo a seguir define todos os elementos de propriedade necessários para esse parâmetro. O exemplo em [ParameterInit](parameterinit.md) demonstra como inicializar esse parâmetro.

``` syntax
<psf:ParameterDef name="psk:PageMediaSizeMediaSizeHeight">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">microns</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Multiple">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">594106</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinValue">
    <psf:Value xsi:type="xs:integer">152400</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">152400</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Optional</psf:Value>
  </psf:Property>
</psf:ParameterDef>
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




