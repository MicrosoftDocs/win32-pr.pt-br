---
description: 'Saiba mais sobre: função JetDeleteTable'
title: Função JetDeleteTable
TOCTitle: JetDeleteTable Function
ms:assetid: e8a4131f-a69b-41f3-94c6-a1607fc23c1f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294128(v=EXCHG.10)
ms:contentKeyID: 32765742
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDeleteTable
- JetDeleteTableA
- JetDeleteTableW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2cdac49d766835a0d26a3b9d474b8759a552ed1d
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984899"
---
# <a name="jetdeletetable-function"></a>Função JetDeleteTable


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetdeletetable-function"></a>Função JetDeleteTable

A função **JetDeleteTable** exclui uma tabela em um banco de dados ESE.

```cpp
    JET_ERR JET_API JetDeleteTable(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          const tchar* szTableName
    );
```

### <a name="parameters"></a>Parâmetros

*sesid*

O contexto da sessão de banco de dados a ser usado para a chamada à API.

*DBID*

O identificador de banco de dados a ser usado para a chamada à API.

*szTableName*

O nome da tabela a ser excluída.

### <a name="return-value"></a>Valor Retornado

Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir. para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de Armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errTableInUse</p> | <p>Foi feita uma tentativa de excluir uma tabela enquanto outra sessão tem uma ID de tabela aberta (<a href="gg269182(v=exchg.10).md">JET_TABLEID</a>) com <a href="gg294118(v=exchg.10).md">JetOpenTable</a> ou <a href="gg269193(v=exchg.10).md">JetDupCursor</a>.</p> | 
| <p>Tabela de JET_errCannotDeletetemporary</p> | <p>Foi feita uma tentativa de excluir uma tabela temporária. Uma tabela temporária é excluída automaticamente quando fechada com <a href="gg294087(v=exchg.10).md">JetCloseTable</a>.</p> | 
| <p>JET_errCannotDeleteTemplateTable</p> | <p>Foi feita uma tentativa de excluir uma tabela de modelo, ou seja, uma tabela da qual o DDL pode ser herdado.</p> | 



#### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>requer o Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Servidor</strong></p> | <p>requer o Windows server 2008, Windows server 2003 ou Windows servidor 2000.</p> | 
| <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | 
| <p><strong>Biblioteca</strong></p> | <p>Use ESENT. lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implementado como <strong>JetDeleteTableW</strong> (Unicode) e <strong>JetDeleteTableA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Consulte Também

[JET_DBID](./jet-dbid.md)  
[JET_SESID](./jet-sesid.md)  
[JetCloseTable](./jetclosetable-function.md)
