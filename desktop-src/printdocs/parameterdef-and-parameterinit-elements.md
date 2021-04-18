---
description: Este tópico não é atual. Para obter informações atuais, consulte a especificação do esquema de impressão.
ms.assetid: f1c73aed-fca4-47f6-bb98-bab40a6a9b2e
title: Elementos ParameterDef e ParameterInit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64e71ed86d627072ee4b5b0ca0acb4e068ae62b6
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105760517"
---
# <a name="parameterdef-and-parameterinit-elements"></a>Elementos ParameterDef e ParameterInit

Este tópico não é atual. Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Um elemento ParameterDef é diferente de um elemento ParameterInit, pois descreve o valor que um elemento ParameterInit pode conter, enquanto um elemento ParameterInit atribui um valor ao parâmetro. Um elemento ParameterDef consiste em um conjunto específico de elementos Property, que são filhos do elemento ParameterDef, que especificam o tipo de dados, o máximo, o mínimo, os valores padrão para os dados e outras informações. Esses elementos de propriedade são discutidos posteriormente neste tópico.

Elementos ParameterDef podem aparecer apenas em seu contexto permitido. Para a versão inicial do esquema de impressão, eles podem estar localizados no nível raiz do documento PrintCapabilities. O atributo Name do elemento ParameterDef define o nome do parâmetro. Cada elemento ParameterDef no documento PrintCapabilities deve ser atribuído a um atributo de nome exclusivo.

> [!Note]
> para recursos de impressão provedores de documentos:
> 
> O significado de um nome de parâmetro é universal; ou seja, se um elemento ParameterDef em um documento PrintCapabilities tiver o mesmo atributo Name (a cadeia de caracteres formada do namespace e o nome descritivo do elemento ParameterDef) como um elemento ParameterDef em outro documento PrintCapabilities, supõe-se que esses dois elementos representam o mesmo conceito e devem ser interpretados da mesma maneira. Portanto, um elemento ParameterDef definido em um PrintTicket para um documento PrintCapabilities pode ser usado para inicializar o elemento ParameterInit do mesmo nome definido em um documento de PrintCapabilities diferente.

 

## <a name="relationship-to-xml-attributes"></a>Relação com atributos XML

Assim como acontece com todos os atributos Name, o nome do parâmetro está na forma de um QName XML. Uma construção de parâmetro definida pelo esquema tem um nome que é qualificado pelo namespace público, formando o atributo Name, enquanto o atributo Name de uma construção de parâmetro definida de forma privada é qualificado por um namespace privado exclusivo para o criador.

## <a name="relationship-between-parameterdef-and-property-element-types"></a>Relação entre ParameterDef e tipos de elemento de propriedade

Os elementos ParameterDef definidos nas palavras-chave do esquema de impressão devem ser totalmente definidos em um documento PrintCapabilities. O documento imprimir palavras-chave do esquema fornece valores nominais para alguns elementos de propriedade de um elemento ParameterDef (como DefaultValue e outros), mas o autor de um documento PrintCapabilities é responsável por definir os elementos de propriedade restantes. Em qualquer caso, todos os elementos de propriedade devem ser explicitamente definidos em um elemento ParameterDef, incluindo aqueles que são definidos nas palavras-chave do esquema de impressão.

Determinados elementos de propriedade de cada elemento ParameterDef que aparece nas palavras-chave do esquema de impressão são designados como *imutáveis*. Isso significa que todas as definições de documentos de PrintCapabilities das palavras-chave do esquema de impressão – elementos ParameterDef definidos devem preservar esses elementos de propriedade sem modificação. Esses elementos de propriedade imutáveis permitem que os constructos de parâmetro sejam portáteis e não ambíguos em todos os documentos de PrintCapabilities. Um exemplo primo é as unidades usadas em um elemento ParameterDef. Essas unidades devem ser imutáveis para promover uma compreensão consistente de seu significado. Os elementos de propriedade de um ParameterDef designados como não imutáveis podem ser redefinidos em um documento de PrintCapabilities.

Um elemento ParameterDef é composto pelos elementos de propriedade a seguir. Todos devem estar presentes, salvo indicação em contrário.



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Nome da Propriedade</th>
<th>Valores</th>
<th>Descrição</th>
<th>Imutável?</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Tipo de dados <br/></td>
<td>Número inteiro <br/> decimal<br/> string<br/> Sem valor padrão.<br/></td>
<td>Especifica se o valor do parâmetro é um número inteiro, ou de ponto flutuante, ou uma cadeia de texto. O valor de um parâmetro é expresso no mesmo formato que o tipo de dados XSD básico correspondente; ou seja, como um inteiro, um decimal ou uma cadeia de caracteres. <br/></td>
<td>Yes<br/></td>
</tr>
<tr class="even">
<td>DefaultValue <br/></td>
<td>O tipo especificado pela propriedade DataType.<br/> Sem valor padrão.<br/></td>
<td>Especifica o valor com o qual inicializar um controle de interface do usuário.<br/>
<ul>
<li>ou <br/></li>
</ul>
Especifica o valor a ser usado se o elemento de parâmetro relevante estiver ausente do PrintTicket.<br/></td>
<td>No<br/></td>
</tr>
<tr class="odd">
<td>Obrigatório <br/></td>
<td>Incondicional: o elemento ParameterInit sempre deve ser fornecido. <br/> Conditional: o elemento ParameterInit será necessário somente se o parâmetro for referenciado dentro de um elemento Option em um PrintTicket.<br/> DefaultValue: condicional.<br/></td>
<td>Indica quando um elemento ParameterInit deve aparecer explicitamente. Se for condicional, o ParameterInit deverá ser inicializado se o PrintTicket contiver uma opção que referencie o parâmetro.<br/> Usado por clientes de interface de usuário e PrintCapabilities ou provedores PrintTicket. Observe que em qualquer restrição, a propriedade obrigatória do elemento ParameterDef deve ser definida como incondicional. O ParameterDef deve ter um valor definido, caso contrário, o valor dependente ou a restrição não pode ser avaliado.<br/></td>
<td>No<br/></td>
</tr>
<tr class="even">
<td>MaxLength <br/></td>
<td>inteiro se a propriedade DataType especificar a cadeia de caracteres.<br/> DefaultValue: nenhum valor máximo é imposto.<br/></td>
<td>Para parâmetros com valor de cadeia de caracteres, especifica a cadeia de caracteres mais longa permitida. Interface do usuário e PrintCapabilities ou provedores de PrintTicket usam essa propriedade para validar o elemento ParameterDef.<br/></td>
<td>No<br/></td>
</tr>
<tr class="odd">
<td>MaxValue <br/></td>
<td>inteiro se a propriedade DataType especificar Integer.<br/> decimal se a propriedade DataType especificar decimal.<br/> DefaultValue: nenhum valor máximo é imposto.<br/></td>
<td>Para elementos ParameterDef com valor inteiro ou Decimal, define o maior valor permitido.<br/></td>
<td>No<br/></td>
</tr>
<tr class="even">
<td>MinLength <br/></td>
<td>inteiro se a propriedade DataType especificar a cadeia de caracteres. <br/> DefaultValue: nenhum valor mínimo é imposto.<br/></td>
<td>Para valores de cadeia de caracteres, define a cadeia de caracteres mais curta permitida. Interface do usuário e PrintCapabilities ou provedores de PrintTicket usam essa propriedade para validar o elemento ParameterDef.<br/></td>
<td>No<br/></td>
</tr>
<tr class="odd">
<td>MinValue <br/></td>
<td>inteiro se a propriedade DataType especificar Integer.<br/> decimal se a propriedade DataType especificar decimal.<br/> DefaultValue: nenhum valor mínimo é imposto.<br/></td>
<td>Para parâmetros com valor inteiro ou Decimal, define o menor valor permitido. <br/></td>
<td>Não<br/></td>
</tr>
<tr class="even">
<td>Vários <br/></td>
<td>inteiro se a propriedade DataType especificar Integer.<br/> decimal se a propriedade DataType especificar decimal.<br/> Valor de DefaultValue: 1<br/></td>
<td>Para parâmetros com valor inteiro ou Decimal, o valor do parâmetro deve ser um múltiplo desse número. Para obter mais informações, consulte <a href="#notes-on-multiple">observações sobre vários</a> seguindo esta tabela.<br/></td>
<td>No<br/></td>
</tr>
<tr class="odd">
<td>UnitType <br/></td>
<td>valor da cadeia de caracteres que indica as unidades usadas para o parâmetro.<br/> Sem valor padrão.<br/></td>
<td>Indica as unidades nas quais o parâmetro é expresso. Por exemplo, ângulos em décimos de graus, comprimentos em mícrons e assim por diante.<br/></td>
<td>Yes<br/></td>
</tr>
</tbody>
</table>



 

## <a name="notes-on-multiple"></a>Observações sobre vários

Para elementos ParameterInit com valores inteiros ou decimais, o valor de ParameterInit deve ser um múltiplo desse número. Por exemplo, elementos ParameterInit com valor decimal podem ser limitados a décimos definindo essa propriedade como 0,1. Os elementos da interface do usuário usam essa propriedade quando constroem caixas de diálogo e controles de interface do usuário. Além disso, o código de validação PrintTicket pode usar essa propriedade para arredondar o valor de um ParameterInit para o valor mais próximo indicado por Multiple. Observação: os drivers de dispositivo e os provedores de PrintCapabilities não devem supor que os valores de ParameterInit sejam múltiplos desse valor de propriedade. Cada provedor deve ser capaz de arredondar valores arbitrários para o valor utilizável mais próximo devido à possibilidade de que provedores diferentes possam especificar valores diferentes e conflitantes para essa propriedade.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




