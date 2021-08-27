---
description: 'Saiba mais sobre: Função JetDeleteIndex'
title: Função JetDeleteIndex
TOCTitle: JetDeleteIndex Function
ms:assetid: c540503b-d5a6-47f2-9113-9650891c4b6d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294081(v=EXCHG.10)
ms:contentKeyID: 32765696
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDeleteIndexW
- JetDeleteIndexA
- JetDeleteIndex
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4170bd4def6ad60953189923252e2d775765b03d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478012"
---
# <a name="jetdeleteindex-function"></a>Função JetDeleteIndex


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetdeleteindex-function"></a>Função JetDeleteIndex

A **função JetDeleteIndex** exclui um índice de uma tabela.

```cpp
    JET_ERR JET_API JetDeleteIndex(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_PCSTR szIndexName
    );
```

### <a name="parameters"></a>Parâmetros

*sesid*

O contexto de sessão do banco de dados a ser usado para a chamada à API.

*Tableid*

A tabela que contém a coluna que deve ser excluída.

*szIndexName*

O nome do índice a ser excluído.

### <a name="return-value"></a>Valor Retornado

Essa função retorna o [JET_ERR](./jet-err.md) de dados com um dos códigos de retorno a seguir. Para obter mais informações sobre os possíveis erros de ESE, consulte [Extensible Armazenamento Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errFixedDDL</p> | <p>Foi feita uma tentativa de excluir um índice de uma tabela fixa (por exemplo, uma criada com JET_bitTableCreateFixedDDL).</p> | 
| <p>JET_errFixedInheritedDDL</p> | <p>Foi feita uma tentativa de excluir um índice de uma tabela de modelo. Uma tabela de modelo tem DDL fixa.</p> | 
| <p>JET_errIndexNotFound</p> | <p>O índice chamado em <em>szIndexName</em> não foi encontrado.</p> | 
| <p>JET_errPermissionDenied</p> | <p>A tabela não pode ser atualizada porque foi aberta somente leitura.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>Vários threads tentaram usar a mesma sessão de banco de dados.</p> | 
| <p>JET_errTransReadOnly</p> | <p>A transação foi aberta como uma transação somente leitura.</p> | 



#### <a name="remarks"></a>Comentários

Quando bem-sucedido, o índice é excluído e, portanto, não pode ser usado posteriormente. Não deve haver nenhuma transação ativa usando o índice.

Em caso de êxito, a moeda é definida antes do primeiro registro.

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requer Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | | <p><strong>Biblioteca</strong></p> | <p>Use ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Implementado como <strong>JetDeleteIndexW</strong> (Unicode) e <strong>JetDeleteIndexA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Consulte Também

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetCreateIndex](./jetcreateindex-function.md)  
[JetCreateIndex2](./jetcreateindex2-function.md)
