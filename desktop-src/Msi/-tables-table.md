---
description: A \_ tabela tabelas é uma tabela de sistema somente leitura que lista todas as tabelas no banco de dados. Consulte esta tabela para descobrir se existe uma tabela.
ms.assetid: d064855b-8c10-476e-9570-cc3ab48ae998
title: Tabela de _Tables
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10c251693d89bb23634b222518e98dba270856e672362bcdc9acddd3c0b86c56
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013314"
---
# <a name="_tables-table"></a>\_Tabela de tabelas

A \_ tabela tabelas é uma tabela de sistema somente leitura que lista todas as tabelas no banco de dados. Consulte esta tabela para descobrir se existe uma tabela.

A \_ tabela tabelas tem a seguinte coluna.



| Coluna | Tipo             | Chave | Nullable |
|--------|------------------|-----|----------|
| Nome   | [Text](text.md) | Y   | N        |



 

## <a name="column"></a>Coluna

<dl> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Nomes
</dt> <dd>

Nome de uma das tabelas.

</dd> </dl>

## <a name="remarks"></a>Comentários

como a \_ tabela tabelas é uma tabela do sistema que não pode ser modificada por meio de consultas SQL, não é possível obter as chaves primárias com a função [**MsiDatabaseGetPrimaryKeys**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegetprimarykeysa) ou a [**propriedade primarykeys**](database-primarykeys.md).

 

 



