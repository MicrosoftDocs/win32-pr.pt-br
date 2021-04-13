---
description: 'Saiba mais sobre: função JetRenameTable'
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
ms.openlocfilehash: 624b194a1cad836b8927e6e7e4b8490fcad250b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297402"
---
# <a name="jetrenametable-function"></a>Função JetRenameTable


_**Aplica-se a:** Windows | Windows Server_

## <a name="jetrenametable-function"></a>Função JetRenameTable

A função **JetRenameTable** pode ser usada para alterar o nome de uma tabela existente.

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

A sessão a ser usada para esta chamada.

*DBID*

O banco de dados a ser usado para esta chamada.

*szName*

O nome atual da tabela que será renomeada.

*szNameNew*

O novo nome da tabela que será renomeada.

### <a name="return-value"></a>Valor Retornado

Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir. Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Código de retorno</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess</p></td>
<td><p>A operação foi concluída com sucesso.</p></td>
</tr>
<tr class="even">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados. Esse erro só será retornado pelo Windows XP e por versões posteriores.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidDatabase</p></td>
<td><p>O banco de dados especificado era inválido.</p>
<p>Esse erro só é retornado no Windows 2000 quando uma operação de renomeação de tabela é tentada no banco de dados temporário. JET_errInvalidDatabaseId é retornado para esse caso em versões posteriores.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidDatabaseId</p></td>
<td><p>A ID de banco de dados especificada era inválida.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidName</p></td>
<td><p>Um dos nomes de objeto especificados era inválido. Todos os nomes de objeto devem estar em conformidade com o mesmo conjunto de regras. Essas regras são as seguintes:</p>
<ul>
<li><p>Os nomes de objeto devem ser compostos por caracteres ASCII.</p></li>
<li><p>Os nomes de objeto devem ter pelo menos um caractere de comprimento.</p></li>
<li><p>Os nomes de objeto não podem exceder JET_cbNameMost (64) caracteres de comprimento.</p></li>
<li><p>Os nomes de objeto não podem começar com um espaço.</p></li>
<li><p>Os nomes de objeto não podem conter caracteres de controle ASCII (0x00 a 0x1F).</p></li>
<li><p>Os nomes de objeto não podem conter um ponto de exclamação (!), ponto (.), colchete esquerdo ([) ou colchete direito (]), uma vez validado, somente a parte da cadeia de caracteres até o primeiro espaço (se houver) será usado para o nome do objeto. Isso efetivamente significa que os nomes de objeto também não podem conter um espaço.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Um dos parâmetros fornecidos continha um valor inesperado ou continha um valor que não fazia sentido quando combinado com o valor de outro parâmetro. Isso pode ocorrer para <strong>JetRenameTable</strong> quando:</p>
<ul>
<li><p><em>szName</em> é nulo.</p></li>
<li><p><em>szNameNew</em> é nulo.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errObjectNotFound</p></td>
<td><p>Esta tabela especificada não existe para este banco de dados.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo. Esse erro só será retornado pelo Windows XP e por versões posteriores.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTransReadOnly</p></td>
<td><p>Uma atualização não pode ser feita enquanto estiver dentro do escopo de uma transação somente leitura. Uma transação somente leitura é uma transação que foi iniciada usando uma chamada para <a href="gg269268(v=exchg.10).md">JetBeginTransaction2</a> com JET_bitTransactionReadOnly.</p>
<p>Esse erro só será retornado pelo Windows XP e por versões posteriores.</p></td>
</tr>
</tbody>
</table>


Em caso de sucesso, o nome da tabela especificada no banco de dados especificado é permanentemente alterado para o novo nome.

Se houver falha, nenhuma alteração no estado do banco de dados ocorrerá.

#### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Servidor</strong></p></td>
<td><p>Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Cabeçalho</strong></p></td>
<td><p>Declarado em ESENT. h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Biblioteca</strong></p></td>
<td><p>Use ESENT. lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>DLL</strong></p></td>
<td><p>Requer ESENT.dll.</p></td>
</tr>
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Implementado como <strong>JetRenameTableW</strong> (Unicode) e <strong>JetRenameTableA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Consulte Também

[JET_DBID](./jet-dbid.md)  
[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JetBeginTransaction2](./jetbegintransaction2-function.md)
