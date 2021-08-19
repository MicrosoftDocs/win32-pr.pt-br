---
description: a \_ tabela Fluxos lista os fluxos de dados OLE inseridos. essa é uma tabela temporária, criada somente quando referenciada por uma instrução SQL.
ms.assetid: 1e30472d-6ba5-410a-a81b-07ed225dcb69
title: Tabela de _Streams
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23f3796a3abb402027dc9985991a6ba673f5381d8f35657e7d80b0714c40f1e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013334"
---
# <a name="_streams-table"></a>\_Fluxos Tabela

a \_ tabela Fluxos lista os fluxos de dados OLE inseridos. essa é uma tabela temporária, criada somente quando referenciada por uma instrução SQL.



| Coluna | Tipo                 | Chave | Nullable |
|--------|----------------------|-----|----------|
| Nome   | [Text](text.md)     | Y   | N        |
| Dados   | [Binary](binary.md) | N   | Y        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Nomes
</dt> <dd>

Uma chave exclusiva que identifica o fluxo. O comprimento máximo do nome é de 62 caracteres.

</dd> <dt>

<span id="Data"></span><span id="data"></span><span id="DATA"></span>Dado
</dt> <dd>

Os dados binários não formatados.

</dd> </dl>

## <a name="remarks"></a>Comentários

para copiar um fluxo de dados OLE (por exemplo, um objeto do tipo de dados [Binary](binary.md) ) de um arquivo para um banco de dado, crie um registro na \_ tabela Fluxos e insira o nome do fluxo de dados na coluna nome desse registro e copie os dados do arquivo para a coluna de dados usando [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama). Use [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) para inserir o novo registro na tabela.

para ler um fluxo de dados binários inserido em um banco de dado, use uma consulta SQL para localizar e buscar o registro que contém os dados binários. Use [**MsiRecordReadStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordreadstream) para ler os dados binários em um buffer.

Para mover um fluxo de dados binários de um banco para outro, primeiro exporte os dados para um arquivo. use uma consulta SQL para localizar o fluxo de dados no arquivo e use [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) para copiar os dados do arquivo para a coluna de dados da \_ tabela Fluxos do segundo banco de dado. Isso garante que cada banco de dados tenha sua própria cópia dos dados binários. Não é possível mover dados binários de um banco de dado para outro simplesmente buscando um registro com os dados do primeiro banco de dado e inserindo-o no segundo banco de dados.

Para excluir um fluxo de dados, busque o registro e defina a coluna de dados como NULL antes de atualizar o registro. outro método é remover o registro da tabela, excluindo-o usando [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) ou uma consulta simples de SQL. Um fluxo não deve ser buscado em um registro se o fluxo for excluído da tabela.

Para renomear um fluxo de dados OLE, atualize a coluna ' name ' do registro.

se uma espera for colocada nessa tabela usando SQL (ALTER table <table> HOLD) ou uma coluna é adicionada com HOLD, a tabela deve ser liberada usando FREE. Fluxos não são gravados até que a tabela seja liberada ou confirmada.

 

 



