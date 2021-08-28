---
description: 'Saiba mais sobre: JET_TABLEID'
title: JET_TABLEID
TOCTitle: JET_TABLEID
ms:assetid: 09705c32-97d8-460c-8b58-921497e29c13
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269182(v=EXCHG.10)
ms:contentKeyID: 32765485
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f3221fcb23e6c512ff7b5a2ade7abad0791b9449
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465433"
---
# <a name="jet_tableid"></a>JET_TABLEID


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jet_tableid"></a>JET_TABLEID

O tipo de dados JET_TABLEID contém um identificador para o cursor de banco de dado a ser usado para uma chamada para a API do JET. Um cursor só pode ser usado com a sessão que foi usada para abrir esse cursor.

```cpp
    typedef JET_API_PTR JET_TABLEID;
```

### <a name="data-types"></a>Tipos de dados

JET_TABLEID

**Nulo** ou [JET_tableidNil](./invalid-handle-constants.md) pode ser usado para indicar um identificador de cursor inválido.

### <a name="remarks"></a>Comentários

Um cursor gerencia o uso de uma tabela para o mecanismo de banco de dados. Um cursor pode executar as seguintes tarefas:

  - Verificar registros

  - Pesquisar por registros

  - Escolha a ordem de classificação efetiva e a visibilidade desses registros

  - Criar, atualizar ou excluir registros

  - Modificar o esquema da tabela

A funcionalidade com suporte do cursor pode mudar à medida que o status ou o tipo da tabela subjacente é alterado. Por exemplo, uma tabela temporária pode não permitir a pesquisa de dados quando ela é aberta com determinadas opções. O cursor sempre está totalmente conectado à tabela subjacente e interage com esses dados diretamente sem qualquer cache. Quase todas as funcionalidades de ISAM principais que são expostas por esse mecanismo de banco de dados funcionam com o cursor.

Um cursor pode ser criado usando [JetOpenTable](./jetopentable-function.md) ou [JetOpenTempTable](./jetopentemptable-function.md). Um cursor pode ser duplicado usando [JetDupCursor](./jetdupcursor-function.md). Um cursor pode ser fechado explicitamente usando [JetCloseTable](./jetclosetable-function.md) ou implicitamente fechado usando [JetEndSession](./jetendsession-function.md) ou [JetTerm](./jetterm-function.md). Um cursor também pode ser fechado implicitamente pelo [JetRollback](./jetrollback-function.md) se ele foi aberto na transação que foi anulada. O número máximo de cursores que podem ser criados a qualquer momento é controlado por [JET_paramMaxCursors](./resource-parameters.md), que pode ser configurado usando [JetSetSystemParameter](./jetsetsystemparameter-function.md).

### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>requer o Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>requer o Windows server 2008, Windows server 2003 ou Windows servidor 2000.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | 



### <a name="see-also"></a>Consulte Também

[JET_paramMaxSessions](./resource-parameters.md)  
[JetCloseTable](./jetclosetable-function.md)  
[JetDupCursor](./jetdupcursor-function.md)  
[JetEndSession](./jetendsession-function.md)  
[JetOpenTable](./jetopentable-function.md)  
[JetOpenTempTable](./jetopentemptable-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[JetTerm](./jetterm-function.md)
