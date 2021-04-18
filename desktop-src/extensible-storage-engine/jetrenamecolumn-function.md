---
description: 'Saiba mais sobre: função JetRenameColumn'
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
ms.openlocfilehash: 9ab2dee1895e4148bb2ea0600464d7e9c4a6a358
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105784514"
---
# <a name="jetrenamecolumn-function"></a>Função JetRenameColumn


_**Aplica-se a:** Windows | Windows Server_

## <a name="jetrenamecolumn-function"></a>Função JetRenameColumn

A função **JetRenameColumn** pode ser usada para alterar o nome de uma coluna existente em uma tabela.

**Windows XP:** o **JetRenameColumn** é introduzido no Windows XP.  

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

A sessão a ser usada para esta chamada.

*TableID*

O cursor a ser usado para esta chamada.

*szName*

O nome atual da coluna que será renomeada.

*szNameNew*

O novo nome da coluna que será renomeada.

*grbit*

Esse parâmetro deve ser 0.

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
<td><p>JET_errColumnNotFound</p></td>
<td><p>Esta coluna especificada não existe para esta tabela.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidName</p></td>
<td><p>Um dos nomes de objeto especificados era inválido. Todos os nomes de objeto devem estar em conformidade com o mesmo conjunto de regras. Essas regras são as seguintes:</p>
<ul>
<li><p>Os nomes de objeto devem ser compostos por caracteres ASCII.</p></li>
<li><p>Os nomes de objeto devem ter pelo menos um caractere de comprimento.</p></li>
<li><p>Os nomes de objeto não podem exceder JET_cbNameMost (64) caracteres de comprimento.</p></li>
<li><p>Os nomes de objeto não podem começar com um espaço-os nomes de objeto não podem conter caracteres de controle ASCII (0x00 a 0x1F).</p></li>
<li><p>Os nomes de objeto não podem conter um ponto de exclamação (!), período (.), colchete à esquerda ([) ou caractere de colchete direito (]).</p></li>
<li><p>Depois de validado, somente a parte da cadeia de caracteres até o primeiro espaço (se houver) será usada para o nome do objeto. Isso efetivamente significa que os nomes de objeto também não podem conter um espaço.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Um dos parâmetros fornecidos continha um valor inesperado ou continha um valor que não fazia sentido quando combinado com o valor de outro parâmetro. Isso pode ocorrer para <strong>JetRenameColumn</strong> quando:</p>
<ul>
<li><p><em>szName</em> é nulo.</p></li>
<li><p><em>szNameNew</em> é nulo.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados. Esse erro só será retornado pelo Windows XP e por versões posteriores.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInTransaction</p></td>
<td><p>Esta operação só pode ser executada quando a sessão não está dentro de uma transação no momento.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo. Esse erro só será retornado pelo Windows XP e por versões posteriores.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTransReadOnly</p></td>
<td><p>Uma atualização não pode ser feita enquanto estiver dentro do escopo de uma transação somente leitura. Uma transação somente leitura é uma transação que foi iniciada usando uma chamada para <a href="gg269268(v=exchg.10).md">JetBeginTransaction2</a> com JET_bitTransactionReadOnly. Esse erro só será retornado pelo Windows XP e por versões posteriores.</p></td>
</tr>
</tbody>
</table>


Em caso de sucesso, o nome da coluna especificada na tabela associada ao cursor é permanentemente alterado para o novo nome. Todos os índices que fazem referência a essa coluna também serão atualizados.

Se houver falha, nenhuma alteração no estado do banco de dados ocorrerá.

#### <a name="remarks"></a>Comentários

A operação de renomeação de coluna é incomum porque, ao contrário de outras operações de esquema, ela não é executada como uma transação. Quando uma coluna em uma determinada tabela é renomeada em uma sessão, qualquer outra sessão que usa essa tabela verá a alteração imediatamente, mesmo se elas estiverem em uma transação que impediria que essa sessão verificasse qualquer outra alteração feita pela sessão fazendo a operação de renomeação.

A ID de coluna de uma coluna não é afetada pela operação de renomeação.

#### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requer o Windows Vista ou o Windows XP.</p></td>
</tr>
<tr class="even">
<td><p><strong>Servidor</strong></p></td>
<td><p>Requer o Windows Server 2008 ou o Windows Server 2003.</p></td>
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
<td><p>Implementado como <strong>JetRenameColumnW</strong> (Unicode) e <strong>JetRenameColumnA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Consulte Também

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetBeginTransaction2](./jetbegintransaction2-function.md)
