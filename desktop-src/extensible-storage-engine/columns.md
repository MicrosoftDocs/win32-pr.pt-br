---
description: 'Saiba mais sobre: colunas'
title: Colunas
TOCTitle: Columns
ms:assetid: bc16ca4c-e3c9-43db-ac16-284d7cc0926d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294073(v=EXCHG.10)
ms:contentKeyID: 32765688
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 8cc7e3921c1904cdae3a09432d6a17eae3953251d3bd39c288cb6d6ffe184ffc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118982696"
---
# <a name="columns"></a>Colunas


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="columns"></a>Colunas

Uma tabela pode ser criada com um conjunto inicial de colunas chamando [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md) ou sem um conjunto inicial de colunas chamando [JetCreateTable](./jetcreatetable-function.md). As tabelas no ESE podem conter até 127 colunas de comprimento fixo, 128 colunas de comprimento variável e 64.993 colunas marcadas. As colunas são identificadas por seu nome e ID e podem ser adicionadas dinamicamente à tabela com [JetAddColumn](./jetaddcolumn-function.md). As colunas são criadas com um tipo de dados específico e um conjunto opcional de atributos, como se a coluna tem comprimento fixo ou se pode ser nula ou não.

O tipo de uma coluna determina os dados que podem ser armazenados na coluna e muitas das propriedades da coluna, incluindo sua ordem de indexação. O ESE dá suporte a uma ampla gama de tipos de coluna, variando de tamanho de 1 a 2 GB (2146483647 caracteres ASCII ou 1073741823 caracteres Unicode). Para obter uma lista completa dos tipos de dados de coluna com suporte pelo ESE, consulte o tópico [JET_COLTYP](./jet-coltyp.md) . Os tópicos a seguir discutem alguns dos tipos de colunas com suporte no ESE:

  - [Colunas marcadas, fixas e variáveis](./tagged-fixed-and-variable-columns.md)

  - [Colunas de versão, incremento automático e caução](./version-auto-increment-and-escrow-columns.md)

  - [Colunas de valor longo](./long-value-columns.md)

  - [Colunas esparsas com valores múltiplos](./multi-valued-sparse-columns.md)

  - [Colunas definidas pelo usuário](./user-defined-columns.md)

  - [Usando colunas em uma tabela](./using-columns-in-a-table.md)
