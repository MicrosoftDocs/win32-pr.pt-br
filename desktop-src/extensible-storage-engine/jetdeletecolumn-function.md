---
description: 'Saiba mais sobre: Função JetDeleteColumn'
title: Função JetDeleteColumn
TOCTitle: JetDeleteColumn Function
ms:assetid: b2f4be8c-7ea9-4f66-925b-4e9c14d9d475
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294062(v=EXCHG.10)
ms:contentKeyID: 32765677
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDeleteColumnA
- JetDeleteColumnW
- JetDeleteColumn
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7c7c73c5a6fd3249a8779526f6655992ad545372
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122985909"
---
# <a name="jetdeletecolumn-function"></a>Função JetDeleteColumn


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetdeletecolumn-function"></a>Função JetDeleteColumn

A **função JetDeleteColumn** exclui uma coluna de uma tabela de banco de dados ESE.

```cpp
JET_ERR JET_API JetDeleteColumn(
  __in          JET_SESID sesid,
  __in          JET_TABLEID tableid,
  __in          const tchar* szColumnName
);
```

### <a name="parameters"></a>Parâmetros

*sesid*

O contexto de sessão do banco de dados a ser usado para a chamada à API.

*Tableid*

A tabela da qual excluir a coluna.

*szColumnName*

O nome da coluna a ser excluída.

### <a name="return-value"></a>Valor Retornado

Essa função retorna o [JET_ERR](./jet-err.md) de dados com um dos códigos de retorno a seguir. Para obter mais informações sobre os possíveis erros de ESE, consulte [Extensible Armazenamento Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errColumnInUse</p> | <p>A coluna está em uso no momento. Ele pode ser usado atualmente por um índice.</p> | 
| <p>JET_errFixedDDL</p> | <p>Foi feita uma tentativa de modificar a DDL fixa.</p> | 
| <p>JET_errFixedInheritedDDL</p> | <p>A coluna nomeada <em>em szColumnName</em> existe na tabela de modelo e a DDL de uma tabela de modelo não pode ser modificada.</p> | 
| <p>JET_errInvalidName</p> | <p>Isso poderá ser retornado se um nome ruim para <em>szColumnName</em> tiver sido dado.</p> | 
| <p>JET_errPermissionDenied</p> | <p>A tabela não pode ser escrita. Isso poderá ser retornado se o banco de dados tiver sido aberto no modo somente leitura.</p> | 
| <p>JET_errTransReadOnly</p> | <p>A transação é uma transação somente leitura.</p> | 



#### <a name="remarks"></a>Comentários

Chamar **JetDeleteColumn** é idêntico a chamar [JetDeleteColumn2](./jetdeletecolumn2-function.md) com *grbit* definido como zero (0).

#### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requer Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</p> | 
| <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | 
| <p><strong>Biblioteca</strong></p> | <p>Use ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implementado como <strong>JetDeleteColumnW</strong> (Unicode) e <strong>JetDeleteColumnA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Consulte Também

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetDeleteColumn2](./jetdeletecolumn2-function.md)
