---
description: A tabela Validação é uma tabela do sistema que contém os nomes das colunas e os valores de coluna para todas \_ as tabelas no banco de dados.
ms.assetid: 52b1c537-efb6-4bb8-9e7f-b4848be52a71
title: _Validation tabela
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81a42fbe2a2f8da4abceb04912eee2a12edd708ff88d979fbf45f7de8051dc80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118640441"
---
# <a name="_validation-table"></a>\_Tabela de validação

A tabela Validação é uma tabela do sistema que contém os nomes das colunas e os valores de coluna para todas \_ as tabelas no banco de dados. Ele é usado durante o processo de validação de banco de dados para garantir que todas as colunas sejam contabiladas e tenham os valores corretos. Esta tabela não é enviada com o banco de dados do instalador.

A \_ tabela Validação tem as seguintes colunas.



| Coluna      | Tipo                               | Chave | Nullable |
|-------------|------------------------------------|-----|----------|
| Tabela       | [Identificador](identifier.md)       | Y   | N        |
| Coluna      | [Identificador](identifier.md)       | Y   | N        |
| Nullable    | [Text](text.md)                   | N   | N        |
| Minvalue    | [DoubleInteger](doubleinteger.md) | N   | Y        |
| MaxValue    | [DoubleInteger](doubleinteger.md) | N   | Y        |
| Keytable    | [Identificador](identifier.md)       | N   | Y        |
| KeyColumn   | [Inteiro](integer.md)             | N   | Y        |
| Categoria    | [Text](text.md)                   | N   | Y        |
| Definir         | [Text](text.md)                   | N   | Y        |
| Descrição | [Text](text.md)                   | N   | Y        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="Table"></span><span id="table"></span><span id="TABLE"></span>Tabela
</dt> <dd>

Usado para identificar uma tabela específica. Essa chave e a chave Column formam a chave primária da tabela \_ Validação.

</dd> <dt>

<span id="Column"></span><span id="column"></span><span id="COLUMN"></span>Coluna
</dt> <dd>

Usado para identificar uma coluna específica da tabela. Essa chave e a chave Tabela formam a chave primária da tabela \_ validação.

</dd> <dt>

<span id="Nullable"></span><span id="nullable"></span><span id="NULLABLE"></span>Nullable
</dt> <dd>

Identifica se a coluna pode conter um valor Nulo.

Essa coluna pode ter um dos valores a seguir.



| String | Significado                                   |
|--------|-------------------------------------------|
| Y      | Sim, a coluna pode ter um valor Nulo.    |
| N      | Não, a coluna pode não ter um valor Nulo. |



 

</dd> <dt>

<span id="MinValue"></span><span id="minvalue"></span><span id="MINVALUE"></span>Minvalue
</dt> <dd>

Esse campo se aplica a colunas com valor numérico. O campo contém o valor mínimo permitido. Esse pode ser o valor mínimo para um inteiro ou o valor mínimo para uma cadeia de caracteres de data ou versão.

</dd> <dt>

<span id="MaxValue"></span><span id="maxvalue"></span><span id="MAXVALUE"></span>Maxvalue
</dt> <dd>

Esse campo se aplica a colunas com valor numérico. O campo é o valor máximo permitido. Esse pode ser o valor máximo para um inteiro ou o valor máximo para uma cadeia de caracteres de data ou versão.

</dd> <dt>

<span id="KeyTable"></span><span id="keytable"></span><span id="KEYTABLE"></span>Keytable
</dt> <dd>

Esse campo se aplica a colunas que são chaves externas. O campo identificado em Column deve vincular ao número da coluna especificado por KeyColumn na tabela chamada em KeyTable. Essa pode ser uma lista de tabelas separadas por ponto e vírgula.

</dd> <dt>

<span id="KeyColumn"></span><span id="keycolumn"></span><span id="KEYCOLUMN"></span>Keycolumn
</dt> <dd>

Esse campo se aplica a colunas de tabela que são chaves externas. O campo identificado em Column deve vincular ao número da coluna especificado por KeyColumn na tabela chamada em KeyTable. O intervalo permitido do campo KeyColumn é de 1 a 32.

</dd> <dt>

<span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Categoria
</dt> <dd>

Esse é o tipo de dados contido pelo campo de banco de dados especificado pelas colunas Tabela e Coluna da tabela \_ Validação. Se esse for um tipo com um valor numérico, como [Integer](integer.md), [DoubleInteger](doubleinteger.md) ou [Time/Date](time-date.md), insira null nesse campo e especifique o intervalo do valor usando as colunas MinValue e MaxValue. Use a coluna Categoria para especificar os tipos de dados não numéricos descritos em [Tipos de Dados de Coluna](column-data-types.md).

</dd> <dt>

<span id="Set"></span><span id="set"></span><span id="SET"></span>Definir
</dt> <dd>

Esta é uma lista de valores permitidos para esse campo separado por ponto e vírgula. Esse campo geralmente é usado para enumerações.

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descrição
</dt> <dd>

Uma descrição dos dados armazenados na coluna.

</dd> </dl>

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
</dl>

## <a name="remarks"></a>Comentários

O campo Categoria desta tabela só se aplica a dados de cadeia de caracteres. Se o campo Coluna se referir a uma coluna com dados binários, o tipo de dados binário deverá ser especificado no campo Categoria. Dados inteiros Tipos de coluna ignoram o campo Categoria durante a validação.

 

 



