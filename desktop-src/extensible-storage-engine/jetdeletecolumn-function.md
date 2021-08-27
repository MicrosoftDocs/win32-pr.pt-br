---
description: 'Saiba mais sobre: função JetDeleteColumn'
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
ms.openlocfilehash: fd20ba923157d50b3130250f4784ea9bfb19b9b1
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476442"
---
# <a name="jetdeletecolumn-function"></a>Função JetDeleteColumn


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetdeletecolumn-function"></a>Função JetDeleteColumn

A função **JetDeleteColumn** exclui uma coluna de uma tabela de banco de dados ESE.

```cpp
JET_ERR JET_API JetDeleteColumn(
  __in          JET_SESID sesid,
  __in          JET_TABLEID tableid,
  __in          const tchar* szColumnName
);
```

### <a name="parameters"></a>Parâmetros

*sesid*

O contexto da sessão de banco de dados a ser usado para a chamada à API.

*TableID*

A tabela da qual excluir a coluna.

*szColumnName*

O nome da coluna a ser excluída.

### <a name="return-value"></a>Valor Retornado

Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir. para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de Armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errColumnInUse</p> | <p>A coluna está em uso no momento. Ele pode estar sendo usado por um índice.</p> | 
| <p>JET_errFixedDDL</p> | <p>Foi feita uma tentativa de modificar o DDL fixo.</p> | 
| <p>JET_errFixedInheritedDDL</p> | <p>A coluna chamada em <em>szColumnName</em> existe na tabela de modelo e o DDL de uma tabela de modelo não pode ser modificado.</p> | 
| <p>JET_errInvalidName</p> | <p>Isso pode ser retornado se um nome inadequado para <em>szColumnName</em> foi fornecido.</p> | 
| <p>JET_errPermissionDenied</p> | <p>A tabela não é gravável. Isso poderá ser retornado se o banco de dados tiver sido aberto no modo somente leitura.</p> | 
| <p>JET_errTransReadOnly</p> | <p>A transação é uma transação somente leitura.</p> | 



#### <a name="remarks"></a>Comentários

Chamar **JetDeleteColumn** é idêntico a chamar [JetDeleteColumn2](./jetdeletecolumn2-function.md) com *grbit* definido como zero (0).

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>requer o Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>requer o Windows server 2008, Windows server 2003 ou Windows servidor 2000.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | | <p><strong>Biblioteca</strong></p> | <p>Use ESENT. lib.</p> | | <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Implementado como <strong>JetDeleteColumnW</strong> (Unicode) e <strong>JetDeleteColumnA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Consulte Também

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetDeleteColumn2](./jetdeletecolumn2-function.md)
