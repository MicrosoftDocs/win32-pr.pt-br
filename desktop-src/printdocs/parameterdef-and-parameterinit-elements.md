---
description: Este tópico não é atual. Para obter informações atuais, consulte a Especificação de Esquema de Impressão.
ms.assetid: f1c73aed-fca4-47f6-bb98-bab40a6a9b2e
title: Elementos ParameterDef e ParameterInit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fa945ad7fec484828bd81b2052f9b330d0e1679
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475122"
---
# <a name="parameterdef-and-parameterinit-elements"></a>Elementos ParameterDef e ParameterInit

Este tópico não é atual. Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Um elemento ParameterDef difere de um elemento ParameterInit, já que ele descreve o valor que um elemento ParameterInit pode conter, enquanto um elemento ParameterInit atribui um valor ao parâmetro . Um elemento ParameterDef consiste em um conjunto específico de elementos Property, que são filhos do elemento ParameterDef, que especificam o tipo de dados, os valores máximo, mínimo e padrão para os dados e outras informações. Esses elementos property são discutidos posteriormente neste tópico.

Os elementos ParameterDef só podem aparecer no contexto permitido. Para a versão inicial do Esquema de Impressão, eles podem estar localizados no nível raiz do documento PrintCapabilities. O atributo name do elemento ParameterDef define o nome do parâmetro. Cada elemento ParameterDef no documento PrintCapabilities deve ser atribuído a um atributo de nome exclusivo.

> [!Note]
> para imprimir provedores de documentos de funcionalidades:
> 
> O significado de um nome de parâmetro é universal; ou seja, se um elemento ParameterDef em um documento PrintCapabilities tiver o mesmo atributo de nome (a cadeia de caracteres formada do namespace e o nome descritivo do elemento ParameterDef) como um elemento ParameterDef em outro documento PrintCapabilities, supõe-se que ambos esses elementos representam o mesmo conceito e devem ser interpretados da mesma maneira. Portanto, um elemento ParameterDef definido em um PrintTicket para um documento PrintCapabilities pode ser usado para inicializar o elemento ParameterInit com o mesmo nome definido em um documento PrintCapabilities diferente.

 

## <a name="relationship-to-xml-attributes"></a>Relação com atributos XML

Como é verdadeiro para todos os atributos de nome, o nome do parâmetro está na forma de um QName XML. Um constructo de parâmetro definido pelo esquema tem um nome qualificado pelo namespace público, que forma o atributo name, enquanto o atributo name de um constructo de parâmetro definido de forma privada é qualificado por um namespace privado que é exclusivo para o criador.

## <a name="relationship-between-parameterdef-and-property-element-types"></a>Relação entre ParameterDef e tipos de elemento property

Os elementos ParameterDef definidos nas Palavras-chave de esquema de impressão devem ser totalmente definidos em um documento PrintCapabilities. O documento Palavras-chave de esquema de impressão fornece valores nominais para alguns elementos Property de um elemento ParameterDef (como DefaultValue e outros), mas o autor de um documento PrintCapabilities é responsável por definir os elementos property restantes. Em qualquer caso, todos os elementos Property devem ser explicitamente definidos em um elemento ParameterDef, incluindo aqueles definidos nas Palavras-chave de esquema de impressão.

Determinados elementos property de cada elemento ParameterDef que aparecem nas Palavras-chave de esquema de impressão são designados como *imutáveis.* Isso significa que todas as definições de documento PrintCapabilities dos elementos ParameterDef definidos por Palavras-chave de esquema de impressão devem preservar esses elementos Property sem modificação. Esses elementos property imutáveis permitem que os constructos de parâmetro sejam portáteis e não ambíguos em todos os documentos PrintCapabilities. Um exemplo principal são as unidades usadas em um elemento ParameterDef. Essas unidades devem ser imutáveis para promover uma compreensão consistente de seu significado. Os elementos de propriedade de um ParameterDef designados como não imutáveis podem ser redefinidos em um documento PrintCapabilities.

Um elemento ParameterDef é composto pelos seguintes elementos Property. Todos devem estar presentes, a menos que seja notado de outra forma.




| Nome da Propriedade | Valores | Descrição | Imutável? | 
|---------------|--------|-------------|------------|
| Tipo de dados <br /> | Número inteiro <br /> decimal<br /> string<br /> Sem valor padrão.<br /> | Especifica se o valor do parâmetro é um inteiro ou um número de ponto flutuante ou uma cadeia de caracteres de texto. O valor de um parâmetro é expresso no mesmo formato que o tipo de dados básico XSD correspondente; ou seja, como um inteiro, decimal ou cadeia de caracteres. <br /> | Sim<br /> | 
| DefaultValue <br /> | O tipo especificado pela propriedade DataType.<br /> Sem valor padrão.<br /> | Especifica o valor com o qual inicializar um controle de interface do usuário.<br /><ul><li>ou <br /></li></ul>Especifica o valor a ser usado se o elemento de parâmetro relevante estiver ausente do PrintTicket.<br /> | Não<br /> | 
| Obrigatório <br /> | Incondicional: o elemento ParameterInit sempre deve ser fornecido. <br /> Condicional: o elemento ParameterInit só será necessário se o parâmetro for referenciado dentro de um elemento Option em um PrintTicket.<br /> DefaultValue: condicional.<br /> | Indica quando um elemento ParameterInit deve aparecer explicitamente. Se Condicional, ParameterInit deverá ser inicializado se PrintTicket contiver uma Opção que referencia o parâmetro .<br /> Usado por clientes de interface do usuário e provedores PrintCapabilities ou PrintTicket. Observe que, em qualquer restrição, a Propriedade Obrigatória do elemento ParameterDef deve ser definida como Incondicional. O ParameterDef deve ter um Valor definido, caso contrário, não foi possível avaliar o Valor ou a restrição dependente.<br /> | Não<br /> | 
| MaxLength <br /> | integer se a propriedade DataType especificar cadeia de caracteres.<br /> DefaultValue: nenhum valor máximo é imposto.<br /> | Para parâmetros com valor de cadeia de caracteres, especifica a cadeia de caracteres mais longa permitida. Os provedores UI e PrintCapabilities ou PrintTicket usam essa propriedade para validar o elemento ParameterDef.<br /> | Não<br /> | 
| MaxValue <br /> | integer se a propriedade DataType especificar inteiro.<br /> decimal se a propriedade DataType especificar decimal.<br /> DefaultValue: nenhum valor máximo é imposto.<br /> | Para elementos ParameterDef com valor inteiro ou decimal, define o maior valor permitido.<br /> | Não<br /> | 
| Minlength <br /> | integer se a propriedade DataType especificar cadeia de caracteres. <br /> DefaultValue: nenhum valor mínimo é imposto.<br /> | Para valores de cadeia de caracteres, define a cadeia de caracteres mais curta permitida. Os provedores UI e PrintCapabilities ou PrintTicket usam essa propriedade para validar o elemento ParameterDef.<br /> | Não<br /> | 
| Minvalue <br /> | integer se a propriedade DataType especificar inteiro.<br /> decimal se a propriedade DataType especificar decimal.<br /> DefaultValue: nenhum valor mínimo é imposto.<br /> | Para parâmetros com valor inteiro ou decimal, define o menor valor permitido. <br /> | Não<br /> | 
| Vários <br /> | integer se a propriedade DataType especificar inteiro.<br /> decimal se a propriedade DataType especificar decimal.<br /> DefaultValue: 1<br /> | Para parâmetros com valor inteiro ou decimal, o valor do parâmetro deve ser um múltiplo desse número. Para obter mais informações, consulte <a href="#notes-on-multiple">Observações sobre vários</a> seguindo esta tabela.<br /> | Não<br /> | 
| Unittype <br /> | valor da cadeia de caracteres que indica as unidades usadas para o parâmetro .<br /> Sem valor padrão.<br /> | Indica as unidades nas quais o parâmetro é expresso. Por exemplo, ângulos em décimos de graus, comprimentos em mícronos e assim por diante.<br /> | Sim<br /> | 




 

## <a name="notes-on-multiple"></a>Observações sobre vários

Para elementos ParameterInit com valores inteiros ou decimais, o valor de ParameterInit deve ser um múltiplo desse número. Por exemplo, os elementos ParameterInit com valor decimal podem ser limitados a décimos definindo essa propriedade como 0,1. Os elementos da interface do usuário usam essa propriedade quando constroem caixas de diálogo e controles de interface do usuário. Além disso, o código de validação PrintTicket pode usar essa propriedade para arredondar o valor de um ParameterInit para o valor mais próximo indicado por Multiple. Observação: os drivers de dispositivo e os provedores de PrintCapabilities não devem supor que os valores de ParameterInit sejam múltiplos desse valor de propriedade. Cada provedor deve ser capaz de arredondar valores arbitrários para o valor utilizável mais próximo devido à possibilidade de que provedores diferentes possam especificar valores diferentes e conflitantes para essa propriedade.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




