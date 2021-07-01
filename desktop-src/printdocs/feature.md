---
description: Revise Elementos de recurso, que contêm uma lista de elementos Option e Property que descrevem um atributo de dispositivo, uma configuração de formatação de trabalho ou outra característica relevante.
ms.assetid: 5a6553c2-f322-47e2-bbc8-44f6541f1288
title: Recurso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b28ab7e8cc69ecc9ba3956fbae3c5278baace8cf
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120631"
---
# <a name="feature"></a>Recurso

Este tópico não é atual. Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Um elemento Feature contém uma lista completa dos elementos Option e Property que descrevem totalmente um atributo de dispositivo, a configuração de formatação de trabalho ou outra característica relevante.

## <a name="element-tag"></a>Marca de elemento

<Feature>

## <a name="xml-attributes"></a>Atributos XML

A tabela a seguir lista os atributos XML que podem pertencer a esse elemento.



| Atributo XML   | Detalhes                                                                                              |
|-----------------|------------------------------------------------------------------------------------------------------|
| name<br/> | Contém o nome do Recurso, um Recurso padrão ou um Recurso definido de forma privada. <br/> |



 

Para obter mais informações, consulte a [seção Atributos XML.](xml-attributes.md)

## <a name="element-information"></a>Informações do elemento

A tabela a seguir lista os elementos que podem ser pais desse elemento, os elementos que podem ser filhos desse elemento e quaisquer restrições sobre o próprio elemento.



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
<td>Esse elemento<br/></td>
<td>Nenhum dado de caractere é permitido.<br/> Elementos de opção filho duplicados que são irmãos são permitidos. Atalhos de atributo de nome duplicados permitidos. <br/></td>
</tr>
</tbody>
</table>



 

## <a name="configuration-dependencies"></a>Dependências de configuração

Os elementos de recurso podem não ter nenhuma dependência de configuração.

## <a name="element-usage"></a>Uso do elemento

### <a name="relationship-to-xml-attributes"></a>Relação com atributos XML

Na representação Recurso/Opção, um atributo de dispositivo é representado por um elemento Feature. O atributo de dispositivo é identificado exclusivamente pelo atributo name no elemento Feature do atributo do dispositivo, como no exemplo a seguir. Neste exemplo, o atributo do dispositivo é Resolução.

``` syntax
<Feature name="Resolution" />
```

O Esquema de Impressão define um conjunto de atributos de nome para determinadas instâncias de recurso. Esses atributos de nome servem para identificar um conjunto de instâncias de recurso predefinidos associadas a atributos de dispositivo configuráveis específicos. Esses nomes de instância de recurso devem ser usados sempre que aplicável, pois aumentam a portabilidade do documento PrintCapabilities e os PrintTickets derivados deles. Instâncias de recurso definidas de forma privada poderão ser introduzidas se determinados atributos de dispositivo não corresponderem a nenhuma das instâncias de recurso definidas pelo esquema. Para obter informações sobre a sintaxe para atributos de nome e as convenções que se aplicam a nomes definidos por esquema e definidos de forma privada, consulte [Atributos XML](xml-attributes.md).

### <a name="relationship-to-option-element"></a>Relação com o elemento Option

Cada um dos estados possíveis é representado por um elemento Option. Cada definição option contém um ou mais elementos ScoredProperty, que juntos descrevem ou caracterizam exclusivamente o estado que está sendo representado. A técnica usada para criar definições de opção é descrita em [Definições de opção](option-definitions.md). Todos os elementos Option associados a um elemento Feature específico residem como elementos filho do elemento Feature.

### <a name="subfeatures"></a>Sub-recursos

A Estrutura de Esquema de Impressão também permite que elementos de recurso sejam agrupados de maneira hierárquica. Ou seja, um elemento Feature pode conter um ou mais elementos de recurso filho (sub-recursos). Isso pode ser útil para organizar elementos de recurso relacionados ou para elementos de recurso que controlam aspectos de um recurso de dispositivo. Um exemplo é um dispositivo que dá suporte ao stapling. Esse dispositivo pode oferecer ao usuário uma opção de onde localizar o tronco, como no canto superior esquerdo ou no canto superior direito, ou ao longo da borda superior ou ao longo da borda esquerda. A interface do usuário para esse dispositivo deve ser capaz de apresentar ao usuário as opções de nível mais alto primeiro, que, nesse caso, é se usar o stapling. Somente depois que o usuário decidir usar o stapling, ele deverá ser apresentado a uma segunda camada de opções, localização de grampeador. Uma hierarquia de recursos adiciona a estrutura adicional que possibilita essa interface do usuário. A Estrutura de Esquema de Impressão permite que subfeturas tenham suas próprias subfegmentações filho, permitindo assim um nível ilimitado de aninhamento.

A Estrutura de Esquema de Impressão também permite que os elementos Option apareçam no mesmo nível que subfeatures; ou seja, como irmãos dentro do mesmo elemento pai Feature. Isso permite que o usuário faça a decisão de alto nível (se deve usar o stapling) antes de fazer as seleções de subfeature. Neste exemplo, o elemento raiz Feature, "Grampeador", pode conter dois elementos Option, "On" e "Off", bem como uma subfeature chamada "Location".

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

 

 




