---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 14631336-adfc-4edf-81ef-63e426d41c87
title: Propriedade (documentos e impressão)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9fb4a057b2cf7795262b595c59f9da0343fdf12
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104298022"
---
# <a name="property-documents-and-printing"></a>Propriedade (documentos e impressão)

Este tópico não é atual. Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Um elemento de propriedade declara um dispositivo, formatação de trabalho ou outra propriedade relevante cujo nome é fornecido por seu atributo de nome. Um elemento Value é usado para atribuir um valor à propriedade.

Uma propriedade pode ser complexa, possivelmente contendo várias subpropriedades. As subpropriedades também são representadas por elementos de propriedade.

## <a name="element-tag"></a>Marca do elemento

<Property>

## <a name="xml-attributes"></a>Atributos XML

A tabela a seguir lista os atributos XML que podem ser relativos a esse elemento.



| Atributo XML   | Detalhes                                                                                                                    |
|-----------------|----------------------------------------------------------------------------------------------------------------------------|
| name<br/> | Mantém o atributo Name da propriedade, que é uma propriedade padrão ou uma propriedade definida de forma privada. <br/> |



 

Para obter mais informações, consulte a seção [atributos XML](xml-attributes.md) .

## <a name="element-information"></a>Informações do elemento

A tabela a seguir lista os elementos que podem ser pais deste elemento, os elementos que podem ser filhos desse elemento e quaisquer restrições no próprio elemento.



| Category                   | Detalhes                                                                                                                                                                                                                                                                                                                      |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Elementos pai<br/> | PrintCapabilities <br/> Recurso<br/> PrintTicket<br/> Opção<br/> ParameterDef<br/> Propriedade<br/> ScoredProperty<br/>                                                                                                                                                              |
| Elementos filho<br/>  | O sistema não atribui nenhum significado à ordenação dos elementos. Se os clientes optarem por ascribe algum significado na ordenação dos elementos, eles estarão livres para fazer isso. <br/> *Valor* da *Propriedade* (um ou mais) (zero ou mais)<br/> ou <br/> *Valor* da *Propriedade* (zero ou mais) (um ou mais)<br/> |
| Este elemento<br/>    | Nenhum dado de caractere é permitido.<br/> Elementos de valor filho duplicados que são irmãos são permitidos.<br/>                                                                                                                                                                                                        |



 

## <a name="configuration-dependencies"></a>Dependências de configuração

Uma propriedade pode ter dependências de configuração, exceto quando aparece dentro de um elemento ParameterDef.

## <a name="element-usage"></a>Uso do elemento

Além de aparecer nos elementos de recurso e opção, os elementos de propriedade podem aparecer no nível raiz das respectivas tecnologias subjacentes. O esquema de impressão define um conjunto de elementos de propriedade que pode ser usado para descrever um dispositivo de maneira portátil. No entanto, se essas propriedades não forem suficientes para suas necessidades como um provedor de PrintCapabilities (normalmente, como o dispositivo com suporte tem aspectos de romance não previstos pelo esquema de impressão), você poderá introduzir seus próprios elementos de propriedade privada. Você pode aprimorar ou elaborar as informações fornecidas por uma propriedade pública adicionando uma ou mais subpropriedades privadas como o conteúdo do elemento da propriedade pública.

Elementos de propriedade são definidos usando uma marca de elemento XML, <Property> . Cada propriedade recebe um nome por meio de seu atributo de nome. O nome deve ser um QName de XML e deve estar de acordo com a Convenção de namespace. Para obter detalhes, consulte [atributos XML](xml-attributes.md). O atributo de nome de propriedade e seu local dentro da hierarquia de elementos de propriedade pai (se for um subpropriedade) identificam exclusivamente a propriedade dentro do documento de PrintCapabilities ou PrintTicket.

Uma propriedade pode conter um ou mais elementos de valor, ou um ou mais elementos de propriedade filho (chamados de subpropriedades) ou uma combinação de ambos. As subpropriedades são úteis quando a própria propriedade é composta por vários componentes. Por exemplo, uma propriedade "ConsumableColor" pode ter os componentes "C", "M" e "Y".

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

 

 




