---
description: 'Saiba mais sobre: Função JetCloseTable'
title: Função JetCloseTable
TOCTitle: JetCloseTable Function
ms:assetid: c8975145-e48a-4029-9522-1509263019ae
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294087(v=EXCHG.10)
ms:contentKeyID: 32765702
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCloseTable
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 48082b4ecf80b0b9c8da8a70efcb2c0cde1ff90a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482882"
---
# <a name="jetclosetable-function"></a>Função JetCloseTable


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetclosetable-function"></a>Função JetCloseTable

A **função JetCloseTable** fecha uma tabela aberta em um banco de dados. A tabela pode ser uma tabela temporária ou uma tabela normal.

```cpp
JET_ERR JET_API JetCloseTable(
  __in          JET_SESID sesid,
  __in          JET_TABLEID tableid
);
```

### <a name="parameters"></a>Parâmetros

*sesid*

Identifica o contexto de sessão do banco de dados que será usado para a chamada à API.

*Tableid*

Identifica a tabela a ser fechada.

De *definir tableid* como JET_tableidNil para liberar memória.

### <a name="return-value"></a>Valor Retornado

Essa função retorna o [JET_ERR](./jet-err.md) de dados com um dos códigos de retorno a seguir. Para obter mais informações sobre os possíveis erros de ESE, consulte [Extensible Armazenamento Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 



#### <a name="remarks"></a>Comentários

Essa função deve ser chamada em todas as tabelas abertas [com JetOpenTable](./jetopentable-function.md).

A exceção a essa regra ocorre [quando JetOpenTable](./jetopentable-function.md) é chamado em uma transação e a transação é reenvelhada (com [JetRollback](./jetrollback-function.md)). Ao reverter uma transação, a tabela é fechada automaticamente. Nesse caso, é um erro fechar a tabela com **JetCloseTable.**

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requer Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | | <p><strong>Biblioteca</strong></p> | <p>Use ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte Também

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetOpenTable](./jetopentable-function.md)  
[JetRollback](./jetrollback-function.md)
