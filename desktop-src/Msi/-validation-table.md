---
description: A \_ tabela de validação é uma tabela do sistema que contém os nomes de coluna e os valores de coluna para todas as tabelas no banco de dados.
ms.assetid: 52b1c537-efb6-4bb8-9e7f-b4848be52a71
title: Tabela de _Validation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 666f00ccccda11706dce6a8d7e04e0efea91b7cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828101"
---
# <a name="_validation-table"></a>\_Tabela de validação

A \_ tabela de validação é uma tabela do sistema que contém os nomes de coluna e os valores de coluna para todas as tabelas no banco de dados. Ele é usado durante o processo de validação do banco de dados para garantir que todas as colunas sejam contadas e tenham os valores corretos. Esta tabela não é enviada com o banco de dados do instalador.

A \_ tabela de validação tem as colunas a seguir.



| Coluna      | Tipo                               | Chave | Nullable |
|-------------|------------------------------------|-----|----------|
| Tabela       | [Identificador](identifier.md)       | S   | N        |
| Coluna      | [Identificador](identifier.md)       | S   | N        |
| Nullable    | [Text](text.md)                   | N   | N        |
| MinValue    | [DoubleInteger](doubleinteger.md) | N   | S        |
| MaxValue    | [DoubleInteger](doubleinteger.md) | N   | S        |
| KeyTable    | [Identificador](identifier.md)       | N   | S        |
| KeyColumn   | [Inteiro](integer.md)             | N   | S        |
| Categoria    | [Text](text.md)                   | N   | S        |
| Definir         | [Text](text.md)                   | N   | S        |
| Descrição | [Text](text.md)                   | N   | S        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="Table"></span><span id="table"></span><span id="TABLE"></span>Tabela
</dt> <dd>

Usado para identificar uma tabela específica. Essa chave e a chave de coluna formam a chave primária da \_ tabela de validação.

</dd> <dt>

<span id="Column"></span><span id="column"></span><span id="COLUMN"></span>Pilha
</dt> <dd>

Usado para identificar uma coluna específica da tabela. Essa chave e a chave de tabela formam a chave primária da \_ tabela de validação.

</dd> <dt>

<span id="Nullable"></span><span id="nullable"></span><span id="NULLABLE"></span>Anula
</dt> <dd>

Identifica se a coluna pode conter um valor nulo.

Essa coluna pode ter um dos valores a seguir.



| String | Significado                                   |
|--------|-------------------------------------------|
| S      | Sim, a coluna pode ter um valor nulo.    |
| N      | Não, a coluna pode não ter um valor nulo. |



 

</dd> <dt>

<span id="MinValue"></span><span id="minvalue"></span><span id="MINVALUE"></span>MinValue
</dt> <dd>

Este campo se aplica a colunas com valor numérico. O campo contém o valor mínimo permitido. Esse pode ser o valor mínimo de um inteiro ou o valor mínimo para uma cadeia de caracteres de data ou versão.

</dd> <dt>

<span id="MaxValue"></span><span id="maxvalue"></span><span id="MAXVALUE"></span>MaxValue
</dt> <dd>

Este campo se aplica a colunas com valor numérico. O campo é o valor máximo permitido. Esse pode ser o valor máximo de um inteiro ou o valor máximo para uma cadeia de caracteres de data ou versão.

</dd> <dt>

<span id="KeyTable"></span><span id="keytable"></span><span id="KEYTABLE"></span>KeyTable
</dt> <dd>

Esse campo se aplica a colunas que são chaves externas. O campo identificado na coluna deve ser vinculado ao número da coluna especificado por KeyColumn na tabela chamada em keyTable. Isso pode ser uma lista de tabelas separadas por ponto e vírgula.

</dd> <dt>

<span id="KeyColumn"></span><span id="keycolumn"></span><span id="KEYCOLUMN"></span>KeyColumn
</dt> <dd>

Esse campo se aplica a colunas de tabela que são chaves externas. O campo identificado na coluna deve ser vinculado ao número da coluna especificado por KeyColumn na tabela chamada em keyTable. O intervalo permitido do campo KeyColumn é 1-32.

</dd> <dt>

<span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Categorias
</dt> <dd>

Esse é o tipo de dados contidos no campo de banco de dado especificado pelas colunas de tabela e coluna da \_ tabela de validação. Se for um tipo com um valor numérico, como [Integer](integer.md), [DoubleInteger](doubleinteger.md) ou [Time/Date](time-date.md), insira NULL nesse campo e especifique o intervalo do valor usando as colunas MinValue e MaxValue. Use a coluna categoria para especificar os tipos de dados não numéricos descritos em [tipos de dados de coluna](column-data-types.md).

</dd> <dt>

<span id="Set"></span><span id="set"></span><span id="SET"></span>Definição
</dt> <dd>

Esta é uma lista de valores permitidos para este campo separados por ponto e vírgula. Esse campo é geralmente usado para enumerações.

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Ndescrição
</dt> <dd>

Uma descrição dos dados que são armazenados na coluna.

</dd> </dl>

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
</dl>

## <a name="remarks"></a>Comentários

O campo Categoria desta tabela se aplica somente a dados de cadeia de caracteres. Se o campo de coluna se referir a uma coluna com dados binários, o tipo de dados Binary deverá ser especificado no campo Categoria. Os tipos de coluna de dados inteiros ignoram o campo de categoria durante a validação.

 

 



