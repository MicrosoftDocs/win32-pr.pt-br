---
description: Saiba mais sobre o elemento Property em documentos e impressão. Este tópico não é atual. Para obter as informações mais atuais, consulte a Especificação de Esquema de Impressão.
ms.assetid: 14631336-adfc-4edf-81ef-63e426d41c87
title: Propriedade (documentos e impressão)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dedeb635ec0f16fe4caee48d8e5db7fbcc8bfe6651e3bdc4de2166dbbc053286
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119886316"
---
# <a name="property-documents-and-printing"></a>Propriedade (documentos e impressão)

Este tópico não é atual. Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Um elemento Property declara um dispositivo, formatação de trabalho ou outra propriedade relevante cujo nome é dado por seu atributo de nome. Um elemento Value é usado para atribuir um valor à Propriedade.

Uma propriedade pode ser complexa, possivelmente contendo várias subpropriedades. As subpropriedades também são representadas por elementos Property.

## <a name="element-tag"></a>Marca de elemento

<Property>

## <a name="xml-attributes"></a>Atributos XML

A tabela a seguir lista os atributos XML que podem pertencer a esse elemento.



| Atributo XML   | Detalhes                                                                                                                    |
|-----------------|----------------------------------------------------------------------------------------------------------------------------|
| name<br/> | Contém o atributo name da Propriedade, que é uma propriedade padrão ou uma propriedade definida de forma privada. <br/> |



 

Para obter mais informações, consulte a [seção Atributos XML.](xml-attributes.md)

## <a name="element-information"></a>Informações do elemento

A tabela a seguir lista os elementos que podem ser pais desse elemento, os elementos que podem ser filhos desse elemento e quaisquer restrições sobre o próprio elemento.



| Categoria                   | Detalhes                                                                                                                                                                                                                                                                                                                      |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Elementos pai<br/> | PrintCapabilities <br/> Recurso<br/> PrintTicket<br/> Opção<br/> ParameterDef<br/> Propriedade<br/> Scoredproperty<br/>                                                                                                                                                              |
| Elementos filho<br/>  | O sistema não atribui significância à ordenação dos elementos. Se os clientes optarem por atribuir algum significado na ordenação dos elementos, eles poderão fazer isso. <br/> *Propriedade* (um ou mais) *Valor* (zero ou mais)<br/> ou <br/> *Propriedade* (zero ou mais) *Valor* (um ou mais)<br/> |
| Esse elemento<br/>    | Nenhum dado de caractere é permitido.<br/> Elementos de Valor filho duplicados que são irmãos são permitidos.<br/>                                                                                                                                                                                                        |



 

## <a name="configuration-dependencies"></a>Dependências de configuração

Uma Propriedade pode ter dependências de configuração, exceto quando aparece dentro de um elemento ParameterDef.

## <a name="element-usage"></a>Uso do elemento

Além de aparecerem nos elementos Recurso e Opção, os elementos Property podem aparecer no nível raiz das respectivas tecnologias subjacentes. O Esquema de Impressão define um conjunto de elementos Property que podem ser usados para descrever um dispositivo de maneira portátil. No entanto, se essas propriedades não são suficientes para suas necessidades como um provedor PrintCapabilities (normalmente porque o dispositivo com suporte tem novos aspectos não previstos pelo Esquema de Impressão), você pode introduzir seus próprios elementos de Propriedade privada. Você pode aprimorar ou elaborar as informações fornecidas por uma propriedade pública adicionando uma ou mais subpropriedades privadas como conteúdo do elemento da Propriedade pública.

Os elementos de propriedade são definidos usando uma marca de elemento XML, <Property> . Cada Propriedade recebe um nome por meio de seu atributo de nome. O nome deve ser um QName XML e deve estar em conformidade com a Convenção de Namespace. Para obter detalhes, consulte [Atributos XML](xml-attributes.md). O atributo Nome da propriedade e sua localização dentro da hierarquia de elementos property pai (se for uma subpropriedade) identificam exclusivamente a Propriedade no documento PrintCapabilities ou PrintTicket.

Uma Propriedade pode conter um ou mais elementos Value ou um ou mais elementos de Propriedade filho (chamados de subpropriedades) ou uma combinação de ambos. As subpropriedades são úteis quando a propriedade em si é composta por vários componentes. Por exemplo, uma propriedade "ConsumableColor" pode ter componentes "C", "M" e "Y".

## <a name="example"></a>Exemplo

``` syntax
<psf:Property name="psk:DisplayName">
  <psf:Value xsi:type="xs:string">6</psf:Value>
</psf:Property>
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




