---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 5a6553c2-f322-47e2-bbc8-44f6541f1288
title: Recurso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad89655181563e2da3a8d4841b1d90ecd4e6ac07
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105782760"
---
# <a name="feature"></a>Recurso

Este tópico não é atual. Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Um elemento Feature contém uma lista completa dos elementos Option e Property que descrevem totalmente um atributo de dispositivo, configuração de formatação de trabalho ou outra característica relevante.

## <a name="element-tag"></a>Marca do elemento

<Feature>

## <a name="xml-attributes"></a>Atributos XML

A tabela a seguir lista os atributos XML que podem ser relativos a esse elemento.



| Atributo XML   | Detalhes                                                                                              |
|-----------------|------------------------------------------------------------------------------------------------------|
| name<br/> | Mantém o nome do recurso, um recurso padrão ou um recurso definido de forma privada. <br/> |



 

Para obter mais informações, consulte a seção [atributos XML](xml-attributes.md) .

## <a name="element-information"></a>Informações do elemento

A tabela a seguir lista os elementos que podem ser pais deste elemento, os elementos que podem ser filhos desse elemento e quaisquer restrições no próprio elemento.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Categoria</th>
<th>Detalhes</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Elementos pai<br/></td>
<td>PrintCapabilities <br/> PrintTicket <br/> Recurso<br/></td>
</tr>
<tr class="even">
<td>Elementos filho<br/></td>
<td>Um dos seguintes grupos:<br/>
<ul>
<li><em>Recurso</em> (zero ou mais)<br/></li>
<li><em>Opção</em> (um ou mais)<br/></li>
<li><em>Propriedade</em> (zero ou mais)<br/></li>
</ul>
ou <br/>
<ul>
<li><em>Recurso</em> (um ou mais)<br/></li>
<li><em>Opção</em> (zero ou mais)<br/></li>
<li><em>Propriedade</em> (zero ou mais)<br/></li>
</ul></td>
</tr>
<tr class="odd">
<td>Este elemento<br/></td>
<td>Nenhum dado de caractere é permitido.<br/> Elementos de opção filho duplicados que são irmãos são permitidos. Atalhos de atributo de nome duplicados permitidos. <br/></td>
</tr>
</tbody>
</table>



 

## <a name="configuration-dependencies"></a>Dependências de configuração

Elementos de recurso podem não ter nenhuma dependência de configuração.

## <a name="element-usage"></a>Uso do elemento

### <a name="relationship-to-xml-attributes"></a>Relação com atributos XML

Na representação de recurso/opção, um atributo de dispositivo é representado por um elemento Feature. O atributo de dispositivo é identificado exclusivamente pelo atributo de nome no elemento de recurso do atributo de dispositivo, como no exemplo a seguir. Neste exemplo, o atributo de dispositivo é resolução.

``` syntax
<Feature name="Resolution" />
```

O esquema de impressão define um conjunto de atributos de nome para determinadas instâncias de recursos. Esses atributos de nome servem para identificar um conjunto de instâncias de recursos predefinidas associadas a atributos de dispositivo configuráveis específicos. Esses nomes de instância de recurso devem ser usados sempre que aplicável, pois aumentam a portabilidade do seu documento de PrintCapabilities e os PrintTickets que são derivados deles. As instâncias de recurso definidas de forma privada poderão ser introduzidas se determinados atributos de dispositivo não corresponderem a nenhuma das instâncias de recurso definidas pelo esquema. Para obter informações sobre a sintaxe de atributos de nome e as convenções que se aplicam a nomes definidos pelo esquema e definidos de modo privado, consulte [atributos XML](xml-attributes.md).

### <a name="relationship-to-option-element"></a>Relação com o elemento Option

Cada um dos Estados possíveis é representado por um elemento Option. Cada definição de opção contém um ou mais elementos ScoredProperty, que, juntos, descrevem exclusivamente ou caracterizam o estado que está sendo representado. A técnica usada para criar definições de opção é descrita nas [definições de opção](option-definitions.md). Todos os elementos Option associados a um determinado elemento Feature residem como elementos filho do elemento Feature.

### <a name="subfeatures"></a>Sub-recursos

A estrutura de esquema de impressão também permite que elementos de recurso sejam agrupados de maneira hierárquica. Ou seja, um elemento Feature pode conter um ou mais elementos de recurso filho (sub-recursos). Isso pode ser útil para organizar elementos de recurso relacionados ou para elementos de recurso que controlam aspectos de um recurso de dispositivo. Um exemplo é um dispositivo que dá suporte a grampeamento. Esse dispositivo pode oferecer ao usuário uma opção de onde localizar o grampo, como no canto superior esquerdo ou no canto superior direito, ou na borda superior, ou ao longo da borda esquerda. A interface do usuário (IU) para este dispositivo deve ser capaz de apresentar o usuário com as opções de nível mais alto primeiro, que nesse caso é usar o grampeamento. Somente depois que o usuário decidir usar o grampeamento, ele receberá uma segunda camada de opções, o local de grampeamento. Uma hierarquia de recursos adiciona a estrutura adicional que possibilita essa interface de usuário. A estrutura de esquema de impressão permite que os sub-recursos tenham seus próprios sub-recursos filho, permitindo, assim, um nível ilimitado de aninhamento.

A estrutura de esquema de impressão também permite que elementos de opção apareçam no mesmo nível que os sub-recursos; ou seja, como irmãos dentro do mesmo elemento de recurso pai. Isso permite que o usuário faça a decisão de alto nível (se usar grampeamento) antes de fazer as seleções de subrecurso. Para este exemplo, o elemento de recurso raiz, "grampo", pode conter dois elementos Option, "on" e "off", bem como um subrecurso chamado "StapleLocation".

## <a name="example"></a>Exemplo

``` syntax
<psf:Feature name="psk:JobOutputBin">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option constrained="psk:None">
    <psf:ScoredProperty name="psk:Bin">
      <psf:Value xsi:type="xs:string">SorterBin</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSheetCapacity">
      <psf:Value xsi:type="xs:integer">100</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




