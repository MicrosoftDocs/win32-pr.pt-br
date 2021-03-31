---
description: A \_ tabela de armazenamentos lista armazenamentos de dados OLE inseridos. Essa é uma tabela temporária, criada somente quando referenciada por uma instrução SQL.
ms.assetid: b2f2907d-6966-4b63-9589-c1580f8db574
title: Tabela de _Storages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27995dd61c7d25100fc0e1ae2297695e361f44f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828104"
---
# <a name="_storages-table"></a>\_Tabela de armazenamentos

A \_ tabela de armazenamentos lista armazenamentos de dados OLE inseridos. Essa é uma tabela temporária, criada somente quando referenciada por uma instrução SQL.



| Coluna | Tipo                 | Chave | Nullable |
|--------|----------------------|-----|----------|
| Name   | [Text](text.md)     | S   | N        |
| Dados   | [Binary](binary.md) | N   | S        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Nomes
</dt> <dd>

Uma chave exclusiva que identifica o armazenamento. O comprimento máximo do nome é 31 caracteres.

</dd> <dt>

<span id="Data"></span><span id="data"></span><span id="DATA"></span>Dado
</dt> <dd>

Os dados binários não formatados.

</dd> </dl>

## <a name="remarks"></a>Comentários

Para adicionar um armazenamento OLE a um banco de dados, crie um novo registro na \_ tabela armazenamentos e insira o nome do armazenamento na coluna nome. Use [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) para copiar dados para a coluna de dados deste registro. Por fim, use [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) para inserir o registro na \_ tabela armazenamentos.

Os dados não podem ser lidos da \_ tabela de armazenamentos. No entanto, a \_ tabela de armazenamentos pode ser consultada para verificar a existência de um armazenamento específico. Isso significa que não é possível mover um armazenamento OLE de um banco de dados para outro. Em vez disso, você deve importar o arquivo de armazenamento original para o novo banco de dados. Para excluir um armazenamento OLE, busque o registro que contém os dados binários, defina a coluna de dados na \_ tabela armazenamentos como NULL e, em seguida, atualize o registro. Um método alternativo é simplesmente excluir o registro usando [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) ou uma consulta SQL simples.

Para renomear um armazenamento OLE, atualize a coluna nome do registro.

Se uma espera for colocada nessa tabela usando SQL (ALTER TABLE <table> HOLD) ou uma coluna é adicionada com HOLD, a tabela deve ser liberada usando FREE. Os armazenamentos não são gravados até que a tabela seja liberada ou confirmada.

 

 



