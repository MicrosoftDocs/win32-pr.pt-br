---
description: A tabela Colunas é uma tabela do sistema \_ somente leitura que contém o catálogo de colunas. Ele lista as colunas de todas as tabelas. Você pode consultar essa tabela para descobrir se uma determinada coluna existe.
ms.assetid: 1ddde4e2-90a9-4dd8-a4f9-b6802d0b11cf
title: _Columns tabela
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7cbb603c077d7873cdfbea88070e555902883ba579b422627b2581aca04745b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118640471"
---
# <a name="_columns-table"></a>\_Tabela de colunas

A tabela Colunas é uma tabela do sistema \_ somente leitura que contém o catálogo de colunas. Ele lista as colunas de todas as tabelas. Você pode consultar essa tabela para descobrir se uma determinada coluna existe.

A \_ tabela Colunas tem as seguintes colunas.



| Coluna | Tipo                   | Chave | Nullable |
|--------|------------------------|-----|----------|
| Tabela  | [Text](text.md)       | Y   | N        |
| Número | [Inteiro](integer.md) | Y   | N        |
| Nome   | [Text](text.md)       | N   | N        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="Table"></span><span id="table"></span><span id="TABLE"></span>Tabela
</dt> <dd>

O nome da tabela que contém a coluna.

</dd> <dt>

<span id="Number"></span><span id="number"></span><span id="NUMBER"></span>Número
</dt> <dd>

A ordem da coluna dentro da tabela.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Nome
</dt> <dd>

O nome da coluna.

</dd> </dl>

## <a name="remarks"></a>Comentários

Como a tabela Columns é uma tabela do sistema que não pode ser modificada por meio de consultas SQL, você não pode obter as chaves primárias com \_ a [**função MsiDatabaseGetPrimaryKeys**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegetprimarykeysa) ou a propriedade [**PrimaryKeys**](database-primarykeys.md).

Somente colunas persistentes são armazenadas na \_ tabela Colunas. Para determinar se existe uma coluna temporária, seria necessário criar uma exibição usando uma instrução SELECT na tabela e, em seguida, fazer um loop em todos os campos em um registro retornado pela \* [**função MsiViewGetColumnInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgetcolumninfo) com a opção MSICOLINFO \_ NAMES.

 

 



