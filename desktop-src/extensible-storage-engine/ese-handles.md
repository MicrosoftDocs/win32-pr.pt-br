---
description: 'Saiba mais sobre: identificadores ESE'
title: Identificadores ESE
TOCTitle: ESE Handles
ms:assetid: 969ae14f-3548-431d-a19d-5df92891441d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269349(v=EXCHG.10)
ms:contentKeyID: 32765636
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: cc91a4586fc1619c55b5f45afbca39ce04c0c6cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171220"
---
# <a name="ese-handles"></a>Identificadores ESE


_**Aplica-se a:** Windows | Windows Server_

## <a name="ese-handles"></a>Identificadores ESE

Os identificadores ESE são usados para criar sessões e acessar bancos de dados. Eles são mantidos em uma hierarquia, o que significa que a saída de um nível é usada para acessar recursos no próximo nível.

O diagrama aqui mostra a hierarquia de identificadores e as funções correspondentes que criam os identificadores. Também indicado junto com as funções são os identificadores que são usados na chamada para criar o novo identificador.

![ESE_Documentation_handles2](images/Gg269349.ESE_Documentation_handles2(EXCHG.10).gif "ESE_Documentation_handles2")

Conforme mostrado no diagrama, a instância é o identificador raiz e o nível no qual o banco de dados é recuperado no caso de um encerramento de processo inesperado ou desligamento do sistema. O identificador de instância, JET_INSTANCE, é criado por [JetCreateInstance](./jetcreateinstance-function.md) e [JetCreateInstance2](./jetcreateinstance2-function.md). O próximo nível, o nível de sessão, é o contexto de transação do mecanismo de banco de dados e o nível no qual todas as operações de banco de dados são executadas. O identificador de sessão, JET_SESID, é criado no contexto da instância na chamada de [JetBeginSession](./jetbeginsession-function.md). A ID de sessão é usada em todas as chamadas subsequentes para acessar tabelas e bancos de dados. Se a instância estiver sendo usada por mais de um thread por vez, cada thread deverá usar seu próprio identificador de sessão. O identificador de banco de dados é criado usando o identificador de sessão e usado principalmente para gerenciar o esquema do banco de dados, mas também pode ser usado para gerenciar tabelas dentro do banco de dados. Os identificadores de banco de dados só podem ser usados na sessão sob a qual eles são criados. O identificador para o banco de dados é criado na chamada para [JetCreateDatabase](./jetcreatedatabase-function.md) ou [JetOpenDatabase](./jetopendatabase-function.md). As tabelas são associadas à ID do banco de dados sob a qual elas são criadas.

O tipo de dados JET_TABLEID contém um identificador para um cursor de banco de dado. Ele é usado para verificar registros, pesquisar registros ou criar atualizações e excluir registros. O identificador de tabela é criado na chamada para [JetOpenTable](./jetopentable-function.md)ou [JetCreateTable](./jetcreatetable-function.md). [JetOpenTempTable](./jetopentemptable-function.md), [JetOpenTempTable2](./jetopentemptable2-function.md)e [JetOpenTempTable3](./jetopentemptable3-function.md) também criam IDs de tabela para tabelas temporárias e [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md) e [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md) retornam IDs de tabela na estrutura de saída. As colunas criadas na tabela têm um identificador de coluna exclusivo ou COLUMN_ID. As IDs de colunas são criadas nas chamadas para [JetAddColumn](./jetaddcolumn-function.md), ou em chamadas para [JetOpenTempTable](./jetopentemptable-function.md), [JetOpenTempTable2](./jetopentemptable2-function.md)ou [JetOpenTempTable3](./jetopentemptable3-function.md) para tabelas temporárias. As IDs de coluna também podem ser recuperadas para uma determinada coluna pelo nome com APIs como [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md).
