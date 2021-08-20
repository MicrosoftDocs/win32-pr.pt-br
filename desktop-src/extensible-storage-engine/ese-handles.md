---
description: 'Saiba mais sobre: Alças de ESE'
title: Alças de ESE
TOCTitle: ESE Handles
ms:assetid: 969ae14f-3548-431d-a19d-5df92891441d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269349(v=EXCHG.10)
ms:contentKeyID: 32765636
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 5177de8b7fbc07d592bb599941a1fd02810bbbf81e16b65cd15c6ebdfd75d3d1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119786287"
---
# <a name="ese-handles"></a>Alças de ESE


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="ese-handles"></a>Alças de ESE

Os alças ESE são usados para criar sessões e acessar bancos de dados. Eles são mantidos em uma hierarquia, o que significa que a saída de um nível é usada para acessar recursos no próximo nível.

O diagrama aqui mostra a hierarquia de alças e as funções correspondentes que criam os alças. Também indicados junto com as funções são os alças usados na chamada para criar o novo handle.

![ESE_Documentation_handles2](images/Gg269349.ESE_Documentation_handles2(EXCHG.10).gif "ESE_Documentation_handles2")

Conforme mostrado no diagrama, a instância é o handle raiz e o nível no qual o banco de dados é recuperado no caso de um encerramento inesperado de processo ou desligamento do sistema. O handle de instância, JET_INSTANCE, é criado por [JetCreateInstance](./jetcreateinstance-function.md) e [JetCreateInstance2.](./jetcreateinstance2-function.md) O próximo nível, o nível de sessão, é o contexto de transação do mecanismo de banco de dados e o nível no qual todas as operações de banco de dados são executadas. O handle de sessão, JET_SESID, é criado no contexto da instância na chamada para [JetBeginSession](./jetbeginsession-function.md). A ID da sessão é usada em todas as chamadas subsequentes para acessar tabelas e bancos de dados. Se a instância estiver sendo usada por mais de um thread por vez, cada thread deverá usar seu próprio alça de sessão. O handle de banco de dados é criado usando o alça de sessão e usado principalmente para gerenciar o esquema do banco de dados, mas também pode ser usado para gerenciar tabelas dentro do banco de dados. Os alças de banco de dados só podem ser usados na sessão na qual são criados. O handle para o banco de dados é criado na chamada para [JetCreateDatabase](./jetcreatedatabase-function.md) ou [JetOpenDatabase](./jetopendatabase-function.md). As tabelas são associadas à ID do banco de dados na qual são criadas.

O JET_TABLEID de dados contém um identificador para um cursor de banco de dados. Ele é usado para verificar registros, pesquisar registros ou criar registros de atualização e exclusão. O alça de tabela é criado na chamada para [JetOpenTable](./jetopentable-function.md)ou [JetCreateTable](./jetcreatetable-function.md). [JetOpenTempTable](./jetopentemptable-function.md), [JetOpenTempTable2](./jetopentemptable2-function.md)e [JetOpenTempTable3](./jetopentemptable3-function.md) também criam IDs de tabela para tabelas temporárias e [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md) e [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md) retornam IDs de tabela na estrutura out. As colunas criadas dentro da tabela têm um identificador de coluna exclusivo ou COLUMN_ID. As IDs de colunas são criadas nas chamadas para [JetAddColumn](./jetaddcolumn-function.md)ou em chamadas para [JetOpenTempTable,](./jetopentemptable-function.md) [JetOpenTempTable2](./jetopentemptable2-function.md)ou [JetOpenTempTable3](./jetopentemptable3-function.md) para tabelas temporárias. IDs de coluna também podem ser recuperadas para uma determinada coluna por nome com APIs como [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md).
