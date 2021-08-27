---
description: 'Saiba mais sobre: função JetDeleteColumn2'
title: Função JetDeleteColumn2
TOCTitle: JetDeleteColumn2 Function
ms:assetid: 840b5acd-8bbf-4524-9741-5d74e3427329
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269320(v=EXCHG.10)
ms:contentKeyID: 32765610
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDeleteColumn2
- JetDeleteColumn2A
- JetDeleteColumn2W
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 87e9506048094b77674e85f76f6c1718def44cae
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467163"
---
# <a name="jetdeletecolumn2-function"></a>Função JetDeleteColumn2


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetdeletecolumn2-function"></a>Função JetDeleteColumn2

A função **JetDeleteColumn2** exclui uma coluna de uma tabela de banco de dados ESE e permite que uma opção *grbit* seja definida.

**Windows xp: o JetDeleteColumn2** é introduzido no Windows XP.

```cpp
    JET_ERR JET_API JetDeleteColumn2(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          const tchar* szColumnName,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parâmetros

*sesid*

O contexto da sessão de banco de dados a ser usado para a chamada à API.

*TableID*

A tabela que contém a coluna a ser excluída.

*szColumnName*

O nome da coluna a ser excluída.

*grbit*

Um grupo de bits que especifica zero ou mais das opções a seguir.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitDeleteColumnIgnoreTemplateColumns</p> | <p>A configuração JET_bitDeleteColumIgnoreTemplateColumns fará com que a API Tente apenas excluir colunas na tabela derivada. Se existir uma coluna com esse nome na tabela base, ela será ignorada.</p> | 



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

Chamar [JetDeleteColumn](./jetdeletecolumn-function.md) é idêntico a chamar **JetDeleteColumn2** com *grbit* definido como zero (0).

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>requer o Windows Vista ou Windows XP.</p> | | <p><strong>Servidor</strong></p> | <p>requer o Windows server 2008 ou Windows server 2003.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | | <p><strong>Biblioteca</strong></p> | <p>Use ESENT. lib.</p> | | <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Implementado como <strong>JetDeleteColumn2W</strong> (Unicode) e <strong>JetDeleteColumn2A</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Consulte Também

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetDeleteColumn](./jetdeletecolumn-function.md)
