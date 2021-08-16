---
description: A \_ tabela Armazenamentos lista os armazenamentos de dados OLE inseridos. Essa é uma tabela temporária, criada somente quando referenciada por uma instrução SQL.
ms.assetid: b2f2907d-6966-4b63-9589-c1580f8db574
title: _Storages tabela
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee16db075df86e5c5a9c794d3320b49052cf746023bd70e02305d6ce079dbbf9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146069"
---
# <a name="_storages-table"></a>\_Tabela de armazenamentos

A \_ tabela Armazenamentos lista os armazenamentos de dados OLE inseridos. Essa é uma tabela temporária, criada somente quando referenciada por uma instrução SQL.



| Coluna | Tipo                 | Chave | Nullable |
|--------|----------------------|-----|----------|
| Nome   | [Text](text.md)     | Y   | N        |
| Dados   | [Binary](binary.md) | N   | Y        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Nome
</dt> <dd>

Uma chave exclusiva que identifica o armazenamento. O comprimento máximo de Nome é de 31 caracteres.

</dd> <dt>

<span id="Data"></span><span id="data"></span><span id="DATA"></span>Dados
</dt> <dd>

Os dados binários não formatados.

</dd> </dl>

## <a name="remarks"></a>Comentários

Para adicionar um armazenamento OLE a um banco de dados, crie um novo registro na tabela Armazenamentos e insira o nome do armazenamento \_ na coluna Nome. Use [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) para copiar dados para a coluna Dados desse registro. Por fim, use [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) para inserir o registro na \_ tabela Armazenamentos.

Os dados não podem ser \_ lidos da tabela Armazenamentos. No entanto, \_ a tabela Armazenamentos pode ser consultada para verificar a existência de um armazenamento específico. Isso significa que não é possível mover um armazenamento OLE de um banco de dados para outro. Em vez disso, você deve importar o arquivo de armazenamento original para o novo banco de dados. Para excluir um armazenamento OLE, busque o registro que contém os dados binários, de definir a coluna Dados na tabela \_ Armazenamentos como nulo e, em seguida, atualize o registro. Um método alternativo é simplesmente excluir o registro usando [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) ou uma consulta SQL simples.

Para renomear um armazenamento OLE, atualize a coluna Nome do registro.

Se uma espera for colocada nessa tabela usando SQL (ALTER TABLE) <table> HOLD) ou uma coluna é adicionada com HOLD, a tabela deve ser liberada usando FREE. Os armazenamentos não são gravados até que a tabela seja liberada ou comprometida.

 

 



