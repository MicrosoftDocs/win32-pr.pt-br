---
description: 'Saiba mais sobre: Função JetRenameTable'
title: Função JetRenameTable
TOCTitle: JetRenameTable Function
ms:assetid: face9341-58e3-450b-980d-08eb1dc3e9d2
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294142(v=EXCHG.10)
ms:contentKeyID: 32765756
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRenameTableW
- JetRenameTableA
- JetRenameTable
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0d91f7af4896e5cb3145321de087a2803aaddd09
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122985739"
---
# <a name="jetrenametable-function"></a>Função JetRenameTable


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetrenametable-function"></a>Função JetRenameTable

A **função JetRenameTable** pode ser usada para alterar o nome de uma tabela existente.

```cpp
    JET_ERR JET_API JetRenameTable(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          const tchar* szName,
      __in          const tchar* szNameNew
    );
```

### <a name="parameters"></a>Parâmetros

*sesid*

A sessão a ser usada para essa chamada.

*Dbid*

O banco de dados a ser usado para essa chamada.

*Szname*

O nome atual da tabela que será renomeada.

*szNameNew*

O novo nome para a tabela que será renomeada.

### <a name="return-value"></a>Valor Retornado

Essa função retorna o [JET_ERR](./jet-err.md) de dados com um dos códigos de retorno a seguir. Para obter mais informações sobre os possíveis erros de ESE, consulte [Extensible Armazenamento Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Não é possível concluir a operação porque todas as atividades na instância associada à sessão foram encerradas como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados. Esse erro só será retornado por Windows XP e versões posteriores.</p> | 
| <p>JET_errInvalidDatabase</p> | <p>O banco de dados especificado era inválido.</p><p>Esse erro só é retornado no Windows 2000 quando uma operação de renomear tabela é tentada no banco de dados temporário. JET_errInvalidDatabaseId é retornado para esse caso em versões posteriores.</p> | 
| <p>JET_errInvalidDatabaseId</p> | <p>A ID do banco de dados especificada era inválida.</p> | 
| <p>JET_errInvalidName</p> | <p>Um dos nomes de objeto especificados era inválido. Todos os nomes de objeto devem estar em conformidade com o mesmo conjunto de regras. Essas regras são as seguintes:</p><ul><li><p>Os nomes de objeto devem ser compostos de caracteres ASCII.</p></li><li><p>Os nomes de objeto devem ter pelo menos um caractere de comprimento.</p></li><li><p>Os nomes de objeto não podem exceder JET_cbNameMost (64) caracteres de comprimento.</p></li><li><p>Os nomes de objeto podem não começar com um espaço.</p></li><li><p>Os nomes de objeto podem não conter caracteres de controle ASCII (0x00 por meio 0x1F).</p></li><li><p>Os nomes de objeto podem não conter um ponto de exclamação (!), ponto (.), colchete esquerdo ([) ou caractere de colchete direito (]) – depois de validados, somente a parte da cadeia de caracteres até o primeiro espaço (se algum) será usada para o nome do objeto. Isso significa efetivamente que os nomes de objeto também podem não conter um espaço.</p></li></ul> | 
| <p>JET_errInvalidParameter</p> | <p>Um dos parâmetros fornecidos continha um valor inesperado ou continha um valor que não fazia sentido quando combinado com o valor de outro parâmetro. Isso pode acontecer para <strong>JetRenameTable</strong> quando:</p><ul><li><p><em>szName</em> é NULL.</p></li><li><p><em>szNameNew</em> é NULL.</p></li></ul> | 
| <p>JET_errNotInitialized</p> | <p>Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</p> | 
| <p>JET_errObjectNotFound</p> | <p>Essa tabela especificada não existe para esse banco de dados.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo. Esse erro só será retornado por Windows XP e versões posteriores.</p> | 
| <p>JET_errTermInProgress</p> | <p>Não é possível concluir a operação porque a instância associada à sessão está sendo desligado.</p> | 
| <p>JET_errTransReadOnly</p> | <p>Uma atualização não pode ser feita enquanto estiver dentro do escopo de uma transação somente leitura. Uma transação somente leitura é uma transação que foi iniciada usando uma chamada para <a href="gg269268(v=exchg.10).md">JetBeginTransaction2</a> com JET_bitTransactionReadOnly.</p><p>Esse erro só será retornado por Windows XP e versões posteriores.</p> | 



Em caso de êxito, o nome da tabela especificada no banco de dados especificado é alterado permanentemente para o novo nome.

Em caso de falha, nenhuma alteração no estado do banco de dados ocorrerá.

#### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requer Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</p> | 
| <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | 
| <p><strong>Biblioteca</strong></p> | <p>Use ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implementado como <strong>JetRenameTableW</strong> (Unicode) e <strong>JetRenameTableA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Consulte Também

[JET_DBID](./jet-dbid.md)  
[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JetBeginTransaction2](./jetbegintransaction2-function.md)
