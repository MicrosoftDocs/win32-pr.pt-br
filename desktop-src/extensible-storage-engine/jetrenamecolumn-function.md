---
description: 'Saiba mais sobre: Função JetRenameColumn'
title: Função JetRenameColumn
TOCTitle: JetRenameColumn Function
ms:assetid: 30967765-355b-417c-b0d6-8b59e677cc98
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269218(v=EXCHG.10)
ms:contentKeyID: 32765521
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRenameColumn
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c60418a0723214b2d2312ebe67a4f47184814e0a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470233"
---
# <a name="jetrenamecolumn-function"></a>Função JetRenameColumn


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetrenamecolumn-function"></a>Função JetRenameColumn

A **função JetRenameColumn** pode ser usada para alterar o nome de uma coluna existente em uma tabela.

**Windows XP:****JetRenameColumn** é introduzido no Windows XP.  

```cpp
    JET_ERR JET_API JetRenameColumn(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_PCSTR szName,
      __in          JET_PCSTR szNameNew,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parâmetros

*sesid*

A sessão a ser usada para essa chamada.

*Tableid*

O cursor a ser usado para essa chamada.

*Szname*

O nome atual da coluna que será renomeada.

*szNameNew*

O novo nome para a coluna que será renomeada.

*grbit*

Esse parâmetro deve ser 0.

### <a name="return-value"></a>Valor Retornado

Essa função retorna o [JET_ERR](./jet-err.md) de dados com um dos códigos de retorno a seguir. Para obter mais informações sobre os possíveis erros de ESE, consulte [Extensible Armazenamento Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Não é possível concluir a operação porque todas as atividades na instância associada à sessão foram encerradas como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errColumnNotFound</p> | <p>Essa coluna especificada não existe para esta tabela.</p> | 
| <p>JET_errInvalidName</p> | <p>Um dos nomes de objeto especificados era inválido. Todos os nomes de objeto devem estar em conformidade com o mesmo conjunto de regras. Essas regras são as seguintes:</p><ul><li><p>Os nomes de objeto devem ser compostos de caracteres ASCII.</p></li><li><p>Os nomes de objeto devem ter pelo menos um caractere de comprimento.</p></li><li><p>Os nomes de objeto não podem exceder JET_cbNameMost (64) caracteres de comprimento.</p></li><li><p>Os nomes de objeto podem não começar com um espaço – os nomes de objeto podem não conter caracteres de controle ASCII (0x00 por meio 0x1F).</p></li><li><p>Os nomes de objeto podem não conter um ponto de exclamação (!), ponto (.), colchete esquerdo ([) ou um caractere de colchete direito (]).</p></li><li><p>Depois de validada, somente a parte da cadeia de caracteres até o primeiro espaço (se algum) será usada para o nome do objeto. Isso significa efetivamente que os nomes de objeto também podem não conter um espaço.</p></li></ul> | 
| <p>JET_errInvalidParameter</p> | <p>Um dos parâmetros fornecidos continha um valor inesperado ou continha um valor que não fazia sentido quando combinado com o valor de outro parâmetro. Isso pode acontecer para <strong>JetRenameColumn</strong> quando:</p><ul><li><p><em>szName</em> é NULL.</p></li><li><p><em>szNameNew</em> é NULL.</p></li></ul> | 
| <p>JET_errInstanceUnavailable</p> | <p>Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados. Esse erro só será retornado por Windows XP e versões posteriores.</p> | 
| <p>JET_errInTransaction</p> | <p>Essa operação só poderá ser executada quando a sessão não estiver dentro de uma transação no momento.</p> | 
| <p>JET_errNotInitialized</p> | <p>Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo. Esse erro só será retornado por Windows XP e versões posteriores.</p> | 
| <p>JET_errTermInProgress</p> | <p>Não é possível concluir a operação porque a instância associada à sessão está sendo desligado.</p> | 
| <p>JET_errTransReadOnly</p> | <p>Uma atualização não pode ser feita enquanto estiver dentro do escopo de uma transação somente leitura. Uma transação somente leitura é uma transação que foi iniciada usando uma chamada para <a href="gg269268(v=exchg.10).md">JetBeginTransaction2</a> com JET_bitTransactionReadOnly. Esse erro só será retornado por Windows XP e versões posteriores.</p> | 



Em caso de êxito, o nome da coluna especificada na tabela associada ao cursor é alterado permanentemente para o novo nome. Todos os índices que referenciam essa coluna também serão atualizados.

Em caso de falha, nenhuma alteração no estado do banco de dados ocorrerá.

#### <a name="remarks"></a>Comentários

A operação de renomear coluna é incomum porque, ao contrário de outras operações de esquema, ela não é executada como uma transação. Quando uma coluna em uma determinada tabela é renomeada em uma sessão, qualquer outra sessão que usa essa tabela verá a alteração imediatamente, mesmo se elas estão em uma transação que impediria que a sessão veja qualquer outra alteração feita pela sessão que está fazendo a operação de renomear.

A ID da coluna de uma coluna não é afetada pela operação de renomear.

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requer Windows Vista ou Windows XP.</p> | | <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008 ou Windows Server 2003.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | | <p><strong>Biblioteca</strong></p> | <p>Use ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Implementado como <strong>JetRenameColumnW</strong> (Unicode) e <strong>JetRenameColumnA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Consulte Também

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetBeginTransaction2](./jetbegintransaction2-function.md)
