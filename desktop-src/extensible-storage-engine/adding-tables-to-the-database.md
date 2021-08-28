---
description: 'Saiba mais sobre: adicionando tabelas ao banco de dados'
title: Adicionando tabelas ao banco de dados
TOCTitle: Adding Tables to the Database
ms:assetid: 176d4fea-c856-441b-bd58-165b37c35095
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269195(v=EXCHG.10)
ms:contentKeyID: 32765498
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 47cb3b87b96e8cb51f651bf7c069088df9d13f7502e24ed61d9d5c355bc6d827
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117903532"
---
# <a name="adding-tables-to-the-database"></a>Adicionando tabelas ao banco de dados


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="adding-tables-to-the-database"></a>Adicionando tabelas ao banco de dados

As tabelas são uma coleção heterogênea de registros que agrupam de forma física e lógica os dados no banco de dado. As tabelas são identificadas exclusivamente por seu nome. A ID da tabela ([JET_TABLEID](./jet-tableid.md)) é um identificador para um cursor que é usado para atualizar e navegar em tabelas. Você pode abrir vários [JET_TABLEID](./jet-tableid.md) na mesma tabela.

Uma tabela existente é aberta na chamada para [JetOpenTable](./jetopentable-function.md), e uma nova tabela é criada sem linhas ou colunas com [JetCreateTable](./jetcreatetable-function.md). Para criar atomicamente uma tabela com um conjunto inicial de colunas e índices, chame [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md) ou [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md). O tamanho inicial da tabela é fornecido no parâmetro *lPages* em [JetCreateTable](./jetcreatetable-function.md) ou no membro **ulPages** da estrutura [JET_TABLECREATE](./jet-tablecreate-structure.md) na chamada para [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md). As tabelas crescem automaticamente quando os dados são adicionados à tabela. O crescimento é proporcional ao tamanho inicial da tabela. As colunas podem ser adicionadas à tabela a qualquer momento com [JetAddColumn](./jetaddcolumn-function.md). Quando o aplicativo não precisar mais acessar a tabela, o cursor poderá ser fechado com [JetCloseTable](./jetclosetable-function.md). A tabela pode ser excluída por meio de uma chamada para [JetDeleteTable](./jetdeletetable-function.md).

As operações de tabela devem ser executadas dentro do contexto de uma transação.

## <a name="see-also"></a>Consulte Também

[Transações](./transactions.md)
