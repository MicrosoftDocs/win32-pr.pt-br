---
description: A \_ tabela tabelas é uma tabela de sistema somente leitura que lista todas as tabelas no banco de dados. Consulte esta tabela para descobrir se existe uma tabela.
ms.assetid: d064855b-8c10-476e-9570-cc3ab48ae998
title: Tabela de _Tables
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2dc3ebafd969a07676f64f674f76c3e16ebe059
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828102"
---
# <a name="_tables-table"></a>\_Tabela de tabelas

A \_ tabela tabelas é uma tabela de sistema somente leitura que lista todas as tabelas no banco de dados. Consulte esta tabela para descobrir se existe uma tabela.

A \_ tabela tabelas tem a seguinte coluna.



| Coluna | Tipo             | Chave | Nullable |
|--------|------------------|-----|----------|
| Nome   | [Text](text.md) | S   | N        |



 

## <a name="column"></a>Coluna

<dl> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Nomes
</dt> <dd>

Nome de uma das tabelas.

</dd> </dl>

## <a name="remarks"></a>Comentários

Como a \_ tabela tabelas é uma tabela do sistema que não pode ser modificada por meio de consultas SQL, você não pode obter as chaves primárias com a função [**MsiDatabaseGetPrimaryKeys**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegetprimarykeysa) ou a [**Propriedade primarykeys**](database-primarykeys.md).

 

 



