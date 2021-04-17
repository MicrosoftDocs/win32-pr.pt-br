---
description: A \_ tabela Columns é uma tabela de sistema somente leitura que contém o catálogo de colunas. Ele lista as colunas de todas as tabelas. Você pode consultar esta tabela para descobrir se existe uma determinada coluna.
ms.assetid: 1ddde4e2-90a9-4dd8-a4f9-b6802d0b11cf
title: Tabela de _Columns
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d896f330e5fc2e13b5f172581341eb11a09617d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105754655"
---
# <a name="_columns-table"></a>\_Tabela de colunas

A \_ tabela Columns é uma tabela de sistema somente leitura que contém o catálogo de colunas. Ele lista as colunas de todas as tabelas. Você pode consultar esta tabela para descobrir se existe uma determinada coluna.

A \_ tabela Columns tem as colunas a seguir.



| Coluna | Tipo                   | Chave | Nullable |
|--------|------------------------|-----|----------|
| Tabela  | [Text](text.md)       | S   | N        |
| Número | [Inteiro](integer.md) | S   | N        |
| Nome   | [Text](text.md)       | N   | N        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="Table"></span><span id="table"></span><span id="TABLE"></span>Tabela
</dt> <dd>

O nome da tabela que contém a coluna.

</dd> <dt>

<span id="Number"></span><span id="number"></span><span id="NUMBER"></span>Automática
</dt> <dd>

A ordem da coluna na tabela.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Nomes
</dt> <dd>

O nome da coluna.

</dd> </dl>

## <a name="remarks"></a>Comentários

Como a \_ tabela Columns é uma tabela do sistema que não pode ser modificada por meio de consultas SQL, você não pode obter as chaves primárias com a função [**MsiDatabaseGetPrimaryKeys**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegetprimarykeysa) ou a [**Propriedade primarykeys**](database-primarykeys.md).

Somente colunas persistentes são armazenadas na \_ tabela colunas. Para determinar se uma coluna temporária existe, é necessário criar uma exibição usando uma instrução SELECT \* em relação à tabela e, em seguida, fazer um loop por todos os campos em um registro retornado pela função [**MsiViewGetColumnInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgetcolumninfo) com a \_ opção nomes de MSICOLINFO.

 

 



